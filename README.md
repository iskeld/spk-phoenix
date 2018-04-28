# Code samples from dev@LDZ speech

Immutability

```
list = [1, 2, 3]
list ++ [4, 5, 6]
```

if expression

```
drink = if age >= 18 do
  "gin"
else
  "milk"
end
```

Lambdas

```
numbers = [5, 18, 10, 50]
square = fn(x) -> x * x end
Enum.map(numbers, square)
```

Pattern matching

```
a = 5
5 = a
6 = a
[x, y] = [1, 2]
```

Plug sample:

```
mix new plug_test --sup

{:cowboy, "~> 1.1.2"},
{:plug, "~> 1.5"}

Plug.Adapters.Cowboy.child_spec(scheme: :http, plug: PlugTest.Router, options: [port: 4001])

defmodule PlugTest.Handler do
  use Plug.Builder

  plug Plug.Logger
  plug :hello

  def hello(conn, _opts) do
    send_resp(conn, 200, "Meow!")
  end
end
```

New phoenix app
```
mix phx.new devldz --no-ecto
```
