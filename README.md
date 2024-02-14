# [Backstage](https://backstage.io)

This is your newly scaffolded Backstage App, Good Luck!

To start the app, run:

```sh
yarn install
yarn dev
```

# Apicurio

```
docker run -it -p 8080:8080 apicurio/apicurio-registry-mem:latest-release

curl --request POST \
  --url http://localhost:8080/apis/registry/v2/groups/my-group/artifacts \
  --header 'Content-type: application/json' \
  --header 'X-Registry-ArtifactId: datalake-ref' \
  --data '{
  "openapi": "3.0.0",
  "info": {
    "version": "1.0.0",
    "title": "Datalake API",
    "license": {
      "name": "MIT"
    }
  },
  "paths": {
    "/truncate": {
      "delete": {
        "summary": "Empty the lake",
        "responses": {
          "200": {
            "description": "All gone!"
          }
        }
      }
    }
  }
}'
```