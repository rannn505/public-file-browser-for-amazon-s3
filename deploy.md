## Changes:

### Copilot:
#### Working Set:
- README.md
- template.yaml
- index.html
- main.js
- app.py
#### Prompt:
- remove the logging feature entirely, s3 bucket access logs, cloudfront access logs, and all access logs definition, and any related reference like the actual logging bucket itself - i dont need this feature at all
- remove the versioning feature entirely - s3 bucket versioning definition for all buckets, and any related reference like the `s3:GetObjectVersion` permissions on the bucket policies - i dont need this feature at all
- remove all `SiteName` references then change relevant code accordingly. I pre assigned the name in the relevant code.
- remove all `VisibleStorageClasses` and `StorageClass`, row_class references including in the table view itself, start with the cloud formation template, then the website html and js, then the seed app.py
- remove all `FilesOpenTabMode` references then change relevant code accordingly. treat the rest of the code as it was "In New Tab".

### Manual:
- replace "Powered by ..." at website/index.html to useful Configu links
- replace website/icon/ to Configu icons - https://cthedot.de/icongen/
- update index.html to suite Configu style guide

## Development:

- install https://www.npmjs.com/package/local-web-server globally with pnpm/npm then run snippet from readme

## Deployment

- export envs
```shell
export AWS_REGION=us-east-1
export AWS_PROFILE=configu
```
- follow readme deploy
- create dns record and attach it to the cloudfront