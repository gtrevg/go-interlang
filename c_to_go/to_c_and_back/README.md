# Calling from Go to C and back

To run this example run `go build` then `./to_c_and_back`.

The example shows how to use the `//export` cgo comment to call Go functions
from C. Cgo will generate a `_cgo_export.h` with definitions for the exported Go
functions, which can then be included in a C file in the same folder as the Go
project.

Note: When using //export, the "C" preamble can only have, declarations 
(no definitions), because it gets copied twice. (See 
[cgo docs](https://golang.org/cmd/cgo/)).
