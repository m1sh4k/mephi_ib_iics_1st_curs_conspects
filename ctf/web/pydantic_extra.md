```python
@app.post("/auth/login", response_model=Token)
async def login(login_request: LoginRequest):
    
    req = {k: v for k, v in login_request} # какашка! прыгаем по родительским классам видим перегруз в __iter  в BaseModel в pydantic 
    user = authenticate_user(req["username"], req["password"])
    if not user:
        raise HTTPException(
            status_code=status.HTTP_401_UNAUTHORIZED,
            detail="Incorrect username or password",
            headers={"WWW-Authenticate": "Bearer"},
        )
    req.pop("password")

    access_token_expires = timedelta(minutes=ACCESS_TOKEN_EXPIRE_MINUTES)
    access_token = create_access_token(
        data=req, expires_delta=access_token_expires
    )
    return {"access_token": access_token, "token_type": "bearer"}
```
#### schemas.py
```python
class BaseModel(BaseModel): # BaseModel from pydantic!
    model_config = {'extra': 'allow'} # вот эту хуйню и эксплуатируем!

class LoginRequest(BaseModel):
    username: str = Field(..., min_length=4, max_length=50)
    password: str = Field(..., min_length=6)
```
#### main.py
```python
from auth.auth import (
    authenticate_user, create_access_token, get_current_user,
    require_satellite_access, ACCESS_TOKEN_EXPIRE_MINUTES
)
```
#### pydantic/deprecated/copy_internals.py
```python
def _iter(
    self: BaseModel,
    to_dict: bool = False,
    by_alias: bool = False,
    include: AbstractSetIntStr | MappingIntStrAny | None = None,
    exclude: AbstractSetIntStr | MappingIntStrAny | None = None,
    exclude_unset: bool = False,
    exclude_defaults: bool = False,
    exclude_none: bool = False,
) -> TupleGenerator:
...
...
if self.__pydantic_extra__ is None:
        items = self.__dict__.items()
    else:
        items = list(self.__dict__.items()) + list(self.__pydantic_extra__.items()) # просто конкатенирует extra вместе с обычным, при запуске for k, v из extra просто перезапишет то что было
```