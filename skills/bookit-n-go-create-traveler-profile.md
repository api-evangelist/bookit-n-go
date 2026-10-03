---
name: bookit-n-go-create-traveler-profile
description: Create a new traveler profile and configure its preferences, constraints, and consent.
api: openapi/bookit-n-go-openapi.yaml
operations:
- publicCreateTravelerProfile
- publicReplaceTravelerPreferences
- publicReplaceTravelerConstraints
- publicGrantTravelerConsent
generated: '2026-10-02'
method: generated
generator: extract-docs-artifacts.py skills (local)
source: openapi/bookit-n-go-openapi.yaml ; every operationId checked against the contract
---

# bookit-n-go-create-traveler-profile

Create a new traveler profile and configure its preferences, constraints, and consent.

## Steps

1. 1. Call `publicCreateTravelerProfile` with the required request body fields for the traveler profile.
2. 2. Call `publicReplaceTravelerPreferences` with `profileId` from step 1 and the preferences payload.
3. 3. Call `publicReplaceTravelerConstraints` with `profileId` from step 1 and the constraints payload.
4. 4. Call `publicGrantTravelerConsent` with `profileId` from step 1 and the consent details.

## Rules

- Auth: Include the `SandboxApiKey` header as required by the API.
- Idempotency: Use the same request body for replace operations to achieve idempotent updates.
