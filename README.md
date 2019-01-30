Assimp-Golang
======

Go port of the Open Asset Import Library, a modified version of the one here: https://github.com/krux02/assimp

To use this port, you must have Assimp installed and in your path. You must also have a working CGO setup, which requires MinGW or similar for Windows.

Usage:

```go
package main

import (
	assimp "github.com/rishabh-bector/assimp-golang"
)

func main {
	scene := assimp.ImportFile("random.fbx", uint(assimp.Process_Triangulate|assimp.Process_FlipUVs))
  
  rootNode := scene.RootNode()
  // etc etc
}
```

See the implementation of glutils here: https://github.com/raedatoui/glutils/blob/master/model.go for a more full example.
