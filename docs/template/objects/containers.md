# Docker containers

Don't use the constructor directly. Instead use 
```python
from python_on_whales import docker

my_container = docker.container.inspect("my-container-name")

# for example:
if my_container.state.running:
    my_container.kill()

```
For type hints, use this

```python
from python_on_whales import Container

def print_dodo(container: Container):
    print(container.execute(["echo", "dodo"]))
```

## Attributes

It attributes are the same that you get with the command line:
`docker container inspect ...`

If you want to know the exact structure, you can go to the 
[`docker container inspect` reference page](https://docs.docker.com/engine/api/v1.40/#operation/ContainerInspect)
and click on "200 no error".
An example is worth many lines of descriptions.


```
In [1]: from python_on_whales import docker

In [2]: container = docker.run("ubuntu", ["sleep", "infinity"], detach=True)

In [4]: def super_print(obj):
   ...:     print(f"type={type(obj)}, value={obj}")
   ...:

@INSERT_GENERATED_CODE@
```

## Methods

{{autogenerated}}