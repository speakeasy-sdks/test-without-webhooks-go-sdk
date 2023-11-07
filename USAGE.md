<!-- Start SDK Example Usage -->


```go
package main

import (
	"context"
	testwithoutwebhooksgosdk "github.com/speakeasy-sdks/test-without-webhooks-go-sdk"
	"github.com/speakeasy-sdks/test-without-webhooks-go-sdk/pkg/models/shared"
	"log"
)

func main() {
	s := testwithoutwebhooksgosdk.New()

	ctx := context.Background()
	res, err := s.PostSendPet(ctx, &shared.Pet1{
		ID:   794362,
		Name: "string",
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