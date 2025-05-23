

::ApiCard{object='Base.Dict' category='Type'}
#docstring



```julia
Dict([itr])
```


`Dict{K,V}()` constructs a hash table with keys of type `K` and values of type `V`. Keys are compared with `isequal` and hashed with `hash`.

Given a single iterable argument, constructs a [`Dict`](/API/cookies#Base.Dict) whose key-value pairs are taken from 2-tuples `(key,value)` generated by the argument.

**Examples**

```julia
julia> Dict([("A", 1), ("B", 2)])
Dict{String, Int64} with 2 entries:
  "B" => 2
  "A" => 1
```


Alternatively, a sequence of pair arguments may be passed.

```julia
julia> Dict("A"=>1, "B"=>2)
Dict{String, Int64} with 2 entries:
  "B" => 2
  "A" => 1
```



[source](https://github.com/JuliaLang/julia/blob/6f3fdf7b36250fb95f512a2b927ad2518c07d2b5/base/dict.jl#L31-L56)

::
::ApiCard{object='Genie.Cookies.get' category='Function'}
#docstring



```julia
get(payload::Union{HTTP.Response,HTTP.Request}, key::Union{String,Symbol}, default::T; encrypted::Bool = true)::T where T
```


Attempts to get the Cookie value stored at `key` within `payload`. If the `key` is not set, the `default` value is returned.

**Arguments**
- `payload::Union{HTTP.Response,HTTP.Request}`: the request or response object containing the Cookie headers
  
- `key::Union{String,Symbol}`: the name of the cookie value
  
- `default::T`: default value to be returned if no cookie value is set at `key`
  
- `encrypted::Bool`: if `true` the value stored on the cookie is automatically decrypted
  


[source](https://github.com/GenieFramework/Genie.jl/blob/v5.30.6/src/Cookies.jl#L10-L21)



```julia
get(res::HTTP.Response, key::Union{String,Symbol}) :: Union{Nothing,String}
```


Retrieves a value stored on the cookie as `key` from the `Respose` object.

**Arguments**
- `payload::Union{HTTP.Response,HTTP.Request}`: the request or response object containing the Cookie headers
  
- `key::Union{String,Symbol}`: the name of the cookie value
  
- `encrypted::Bool`: if `true` the value stored on the cookie is automatically decrypted
  


[source](https://github.com/GenieFramework/Genie.jl/blob/v5.30.6/src/Cookies.jl#L28-L37)



```julia
get(req::Request, key::Union{String,Symbol}) :: Union{Nothing,String}
```


Retrieves a value stored on the cookie as `key` from the `Request` object.

**Arguments**
- `req::HTTP.Request`: the request or response object containing the Cookie headers
  
- `key::Union{String,Symbol}`: the name of the cookie value
  
- `encrypted::Bool`: if `true` the value stored on the cookie is automatically decrypted
  


[source](https://github.com/GenieFramework/Genie.jl/blob/v5.30.6/src/Cookies.jl#L45-L54)

::
::ApiCard{object='Genie.Cookies.getcookies' category='Function'}
#docstring



```julia
getcookies(req::HTTP.Request) :: Vector{HTTP.Cookies.Cookie}
```


Extracts cookies from within `req`


[source](https://github.com/GenieFramework/Genie.jl/blob/v5.30.6/src/Cookies.jl#L160-L164)



```julia
getcookies(req::HTTP.Request) :: Vector{HTTP.Cookies.Cookie}
```


Extracts cookies from within `req`, filtering them by `matching` name.


[source](https://github.com/GenieFramework/Genie.jl/blob/v5.30.6/src/Cookies.jl#L170-L174)

::
::ApiCard{object='Genie.Cookies.set!' category='Function'}
#docstring



```julia
set!(res::HTTP.Response, key::Union{String,Symbol}, value::Any, attributes::Dict; encrypted::Bool = true) :: HTTP.Response
```


Sets `value` under the `key` label on the `Cookie`.

**Arguments**
- `res::HTTP.Response`: the HTTP.Response object
  
- `key::Union{String,Symbol}`: the key for storing the cookie value
  
- `value::Any`: the cookie value
  
- `attributes::Dict`: additional cookie attributes, such as `path`, `httponly`, `maxage`
  
- `encrypted::Bool`: if `true` the value is stored encoded
  


[source](https://github.com/GenieFramework/Genie.jl/blob/v5.30.6/src/Cookies.jl#L62-L73)

::
::ApiCard{object='Genie.Cookies.nullablevalue' category='Function'}
#docstring



```julia
nullablevalue(payload::Union{HTTP.Response,HTTP.Request}, key::Union{String,Symbol}; encrypted::Bool = true)
```


Attempts to retrieve a cookie value stored at `key` in the `payload object` and returns a `Union{Nothing,String}`

**Arguments**
- `payload::Union{HTTP.Response,HTTP.Request}`: the request or response object containing the Cookie headers
  
- `key::Union{String,Symbol}`: the name of the cookie value
  
- `encrypted::Bool`: if `true` the value stored on the cookie is automatically decrypted
  


[source](https://github.com/GenieFramework/Genie.jl/blob/v5.30.6/src/Cookies.jl#L135-L144)

::
