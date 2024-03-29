# TestWithoutWebhooks SDK


## Overview

### Available Operations

* [PostSendPet](#postsendpet)

## PostSendPet

### Example Usage

```go
package main

import(
	testwithoutwebhooksgosdk "github.com/speakeasy-sdks/test-without-webhooks-go-sdk"
	"context"
	"github.com/speakeasy-sdks/test-without-webhooks-go-sdk/pkg/models/shared"
	"log"
)

func main() {
    s := testwithoutwebhooksgosdk.New()

    ctx := context.Background()
    res, err := s.PostSendPet(ctx, &shared.Pet1{
        ID: 794362,
        Name: "<value>",
    })
    if err != nil {
        log.Fatal(err)
    }
    if res != nil {
        // handle response
    }
}
```

### Parameters

| Parameter                                             | Type                                                  | Required                                              | Description                                           |
| ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| `ctx`                                                 | [context.Context](https://pkg.go.dev/context#Context) | :heavy_check_mark:                                    | The context to use for the request.                   |
| `request`                                             | [shared.Pet1](../../pkg/models/shared/pet1.md)        | :heavy_check_mark:                                    | The request object to use for the request.            |


### Response

**[*operations.PostSendPetResponse](../../pkg/models/operations/postsendpetresponse.md), error**
| Error Object       | Status Code        | Content Type       |
| ------------------ | ------------------ | ------------------ |
| sdkerrors.SDKError | 4xx-5xx            | */*                |
