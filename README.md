# mulesoft-exchange-upload
GitHub Action to deploy Assets to MuleSoft Anypoint Exchange.  

This action's goal is to deploy RAML assets to Anypoint Exchange.  

## Input Parameters
- Anypoint Username
- Anypoint Password
- Anypoint Organization Id / Business Group Id

## Structure of the repository
- exchange.json
  - File from where the configuration of the asset is read
  - This file is generated automatically by Anypoint Studio. Do not change it unless you know what you're doing.
- RAML definition files

## LIMITATIONS
- Users with `MFA` are not supported
- Authentication with `client_id` & `client_secret` is on the roadmap, but not yet supported

# TODO / Roadmap
- [ ] Supporting more authentication types
- [ ] Supporting more asset types
- [ ] Supporting more actions
# Credits
- Based on:
  - Anypoint CLI 4.x
  - CLI for Exchange Assets - [exchange:asset:upload](https://docs.mulesoft.com/anypoint-cli/4.x/exchange-assets#exchange-asset-upload)
