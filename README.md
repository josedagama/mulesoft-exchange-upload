# Mulesoft Exchange Upload
GitHub Action to deploy Assets to MuleSoft Anypoint Exchange.  

This action's goal is to deploy RAML assets to Anypoint Exchange.  

# Usage
Here's an example on how to use this action:

```yaml
jobs:
  deploy-to-exchange:
    runs-on: ubuntu-latest
    steps:
    - name: Deploy to Exchange
      uses: josedagama/mulesoft-exchange-upload@1.0.0
      with:
        anypoint-organization-id: ${{ secrets.anypoint_platform_organization_id }}
        anypoint-username: ${{ secrets.anypoint_platform_username }}
        anypoint-password: ${{ secrets.anypoint_platform_password }}
```

## Input Parameters
- **anypoint-organization-id**
  - Anypoint Organization Id / Business Group Id
- **anypoint-username**
  - Anypoint Username
- **anypoint-password**
  - Anypoint Password
  - 
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
