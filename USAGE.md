<!-- Start SDK Example Usage -->


```go
package main

import(
	"context"
	"log"
	"github.com/speakeasy-sdks/test-without-webhooks-go-sdk"
	"github.com/speakeasy-sdks/test-without-webhooks-go-sdk/pkg/models/shared"
)

func main() {
    s := testwithoutwebhooks.New()

    ctx := context.Background()
    res, err := s.PostSendPet(ctx, shared.Pet1{
        ID: 548814,
        Name: "Kelvin Sporer",
        Tag: testwithoutwebhooks.String("corrupti"),
    })
    if err != nil {
        log.Fatal(err)
    }

    if res.StatusCode == http.StatusOK {
        // handle response
    }
}
```
<!-- End SDK Example Usage -->