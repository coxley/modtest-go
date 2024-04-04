# Summary

I needed somewhere to test and verify what the tags / lifecycle look like when
having a sub-module in repo-module that version independently.

```go
package main

import (
	"fmt"

	"github.com/coxley/modtest-go"
	sub1 "github.com/coxley/modtest-go/sub"
	sub2 "github.com/coxley/modtest-go/sub/v2"
)

func main() {
	fmt.Println("modtest-go:", modtest.Version)
	fmt.Println("modtest-go/sub1:", sub1.Version)
	fmt.Println("modtest-go/sub2:", sub2.Version)
}

// modtest-go: 1
// modtest-go/sub1: 1
// modtest-go/sub2: 2
```
