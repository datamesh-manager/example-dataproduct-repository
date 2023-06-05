# api-example-dataproduct
Example of a data product sending its data to the data mesh manager via GitHub Actions.

You can find the GitHub Action configuration [here](.github/workflows/data-product.yml).
The example [data product configuration](dataproduct.yml) is transformed to json with yq and sent to the data mesh manager with curl.

The API key of the data mesh manager of the corresponding organization has be to set as a repository variable named `DMM_API_KEY`.
