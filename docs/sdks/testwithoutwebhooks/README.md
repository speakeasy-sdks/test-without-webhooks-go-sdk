# TestWithoutWebhooks SDK

## Overview

### Available Operations

* [PostSendPet](#postsendpet)

## PostSendPet

### Example Usage

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
    res, err := s.TestWithoutWebhooks.PostSendPet(ctx, shared.Pet1{
        ID: 847252,
        Name: "Sabrina Oberbrunner",
        Tag: testwithoutwebhooks.String("magnam"),
    })
    if err != nil {
        log.Fatal(err)
    }

    if res.StatusCode == http.StatusOK {
        // handle response
    }
}
```

### Parameters

| Parameter                                             | Type                                                  | Required                                              | Description                                           |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `ctx`                                                 | [context.Context](https://pkg.go.dev/context#Context) | :heavy_check_mark:                                    | The context to use for the request.                   |
| `request`                                             | [shared.Pet1](../../models/shared/pet1.md)            | :heavy_check_mark:                                    | The request object to use for the request.            |


### Response

**[*operations.PostSendPetResponse](../../models/operations/postsendpetresponse.md), error**
