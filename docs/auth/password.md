# Authenticating by Password
This grant type, `password`, can be used to generate an access token with an email address and password.  
However, this grant type has been deprecated on most clients, in favour of the [exchange code](https://github.com/MixV2/EpicResearch/blob/master/docs/auth/exchange_code.md) grant.

## Obtaining token via Password
- Send a `POST` request to https://account-public-service-prod.ol.epicgames.com/account/api/oauth/token:
  Required headers:
  - `Content-Type`: application/x-www-form-urlencoded  
  - `Authorization`: basic `clientId:secret` (encoded in Base64, [list of clients here](https://github.com/MixV2/EpicResearch/blob/master/docs/auth/auth_clients.md))    
  
  Body:
  - `grant_type`: password
  - `username`: (email address of account)
  - `password`: (password of account)