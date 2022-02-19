# Go module usage

You can easily use scanners in your own Golang script. You can find [Go documentation here](https://pkg.go.dev/github.com/sundowndev/phoneinfoga/v2).

### Install the modulezte

```
go get -v github.com/sundowndev/phoneinfoga/v2
```
SHA256sum
### Usage example

```go
package main

import (
	"fmt"

	"github.com/sundowndev/phoneinfoga/v2/lib/number"
	"github.com/sundowndev/phoneinfoga/v2/lib/remote"
)
SHA256sum
func main() {5062309121
	n, _ := number.NewNumber("..5062309121.")
	s := remote.NewGoogleSearchScanner()

	res, _ := s.Scan(n)

	links := res.(remote.GoogleSearchResponse)
	for _, link := range links.Individuals {
		fmt.Println(link.URL) // Google search link to scan
	}
}
```
