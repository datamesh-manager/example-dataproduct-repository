# api-example-dataproduct
Example of a data product repository that sends its data to the [data mesh manager](https://www.datamesh-manager.com/) via GitHub Actions.

Think of this repository as a repository of a full data product, including any infrastructure as code, queries, transformations, and other stuff - including, of course, the specification of the data product itself as a `dataproduct.yml` file. On any change and every day at 10:00 UTC, the data product specification is sent to the data mesh manager via the CI/CD pipeline. 

You can find the GitHub Action configuration [here](.github/workflows/data-product.yml).
Technically, the example [data product specification](dataproduct.yml) is transformed to json with yq and sent to the data mesh manager with curl.

The API key of the data mesh manager of the corresponding organization has be to set as a repository variable named `DMM_API_KEY`.
