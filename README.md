# datacatalogtordf-service
This service takes a datacatalog json-object as input and return the object as an rdf-serialization according to DCAT-AP-NO v2

The service uses the library developed by us: http://github.com/Informasjonsforvaltning/datacatalogtordf and exposes a simple endpoint.

In general it would be easier for a python-based client to use the library locally by installing from https://pypi.org/project/datacatalogtordf/


## Usage
Example using curl:
```
% echo "{{"indentifier": ""http://example.com/datasets/1}, "name": {"en": "A dataset}}" > dataset.json
% curl -i -H "Content-Type: application/json" -d @dataset.json -X POST "http://localhost:8201/dataset"
```
