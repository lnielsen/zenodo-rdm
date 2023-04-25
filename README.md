<div align="center">
  <img width="500" src="https://about.zenodo.org/static/img/logos/zenodo-black-border.svg">
</div>

## Deployment instructions

Need to set up the following config variables:

``` python
# Invenio-App-RDM
RDM_RECORDS_USER_FIXTURE_PASSWORDS = {
    'admin@inveniosoftware.org': '123456'
}

# Invenio-Records-Resources
SITE_UI_URL = "https://127.0.0.1:5000"
SITE_API_URL = "https://127.0.0.1:5000/api"

# Invenio-RDM-Records
RDM_RECORDS_DOI_DATACITE_USERNAME = ""
RDM_RECORDS_DOI_DATACITE_PASSWORD = ""
RDM_RECORDS_DOI_DATACITE_PREFIX = ""

# Invenio-OAuthclient
# secrets will be injected on deployment
CERN_APP_CREDENTIALS = {
    "consumer_key": "CHANGE ME",
    "consumer_secret": "CHANGE ME",
}
ORCID_APP_CREDENTIALS = {
    "consumer_key": "CHANGE ME",
    "consumer_secret": "CHANGE ME",
}
```

## Development quick start

```
pip install invenio-cli
invenio-cli check-requirements --development
invenio-cli install
invenio-cli services setup
invenio-cli run
```

See the [InvenioRDM Documentation](https://inveniordm.docs.cern.ch/install/)
for further installation options.
