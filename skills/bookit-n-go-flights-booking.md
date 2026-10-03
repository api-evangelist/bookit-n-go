---
name: bookit-n-go-flights-booking
description: Search for flight offers, rank them for the traveler, and create a booking for the selected offer.
api: openapi/bookit-n-go-openapi.yaml
operations:
- publicSearchFlights
- publicRankFlights
- publicCreateFlightBooking
- publicGetFlightBooking
generated: '2026-10-02'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/bookit-n-go-openapi.yaml ; every operationId checked against the contract
---

# bookit-n-go-flights-booking

Search for flight offers, rank them for the traveler, and create a booking for the selected offer.

## Steps

1. 1. `publicSearchFlights` – provide the search request body as defined in the contract (e.g., origin, destination, dates, passengers).
2. 2. `publicRankFlights` – send the list of offers returned from the search in the request body to obtain a deterministic ranking.
3. 3. `publicCreateFlightBooking` – submit a booking request body that includes the chosen `offerId` and passenger details.
4. 4. `publicGetFlightBooking` – retrieve the newly created booking using the `bookingId` returned from the create step.

## Rules

- Auth: Include the `SandboxApiKey` in the HTTP header as required by the provider.
- Idempotency: The `publicCreateFlightBooking` operation should be called once per unique booking request to avoid duplicate bookings.
