---
name: bookit-n-go-book-trip
description: Create a new trip, add a booking item, preview cancellation, and cancel the item if needed.
api: openapi/bookit-n-go-openapi.yaml
operations:
- publicCreateTrip
- publicAddTripItem
- publicCreateCancellationPreview
- publicCancelTripItem
generated: '2026-10-02'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/bookit-n-go-openapi.yaml ; every operationId checked against the contract
---

# bookit-n-go-book-trip

Create a new trip, add a booking item, preview cancellation, and cancel the item if needed.

## Steps

1. 1. Call `publicCreateTrip` with the required trip body fields.
2. 2. Call `publicAddTripItem` with `tripId` path parameter and the item details in the request body.
3. 3. Call `publicCreateCancellationPreview` with `tripId` and `itemId` path parameters to get a cancellation preview.
4. 4. Call `publicCancelTripItem` with `tripId` and `itemId` path parameters to cancel the item.

## Rules

- Auth: Include the `SandboxApiKey` API key in the request header as required by the sandbox authentication scheme.
- Idempotency: No explicit idempotency key is defined for these operations; repeat calls may create duplicate resources.
- Errors: The API returns standard HTTP error codes (e.g., 400 for bad request, 401 for unauthorized, 404 for not found).
