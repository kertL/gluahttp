# gluahttp

gluahttp provides an easy way to make HTTP requests from within [GopherLua](https://github.com/yuin/gopher-lua).

## Installation

```
go get github.com/cjoudrey/gluahttp
```

## Usage

```lua
local http = require("http")

body, status, headers = http.request("GET", "http://example.com", {
  query={
    page=1
  },
  headers={
    Accept="*/*"
  }
})
```

## API

### http.request(method, url [, options])

- `method`: The HTTP request method.
- `url`: A `string` URL of the page to load.
- `options`: A `table` with one or many of the following parameters:
 - `query`: Query string in the form of a `string` or a `table`.
 - `headers`: `table` of additional headers to send with the request.
