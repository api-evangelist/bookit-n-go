---
name: bookit-n-go-hotel-booking
description: Search for hotels, rank the offers, create a booking, and retrieve the booking details.
api: openapi/bookit-n-go-openapi.yaml
operations:
- publicSearchHotels
- publicRankHotels
- publicCreateHotelBooking
- publicGetHotelBooking
generated: '2026-10-02'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/bookit-n-go-openapi.yaml ; every operationId checked against the contract
---

# bookit-n-go-hotel-booking

Search for hotels, rank the offers, create a booking, and retrieve the booking details.

## Steps

1. 1. `publicSearchHotels`
2. 2. `publicRankHotels`
3. 3. `publicCreateHotelBooking`
4. 4. `publicGetHotelBooking`

## Rules

- Include the SandboxApiKey in the HTTP Authorization header.
