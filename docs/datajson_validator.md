# Data.json Validator

The following documents the simplicity and ease of the `datajson_validator` plugin.

## Plugin Features

- Make `/dcat-us/validator` route available to users
  - Provides a web form with single-option for url input
  - Downloads data.json from url provided and validates against DCAT-US 
metadata schema

## Validation Motivation

The DCAT-US Metadata Schema can be found [here](https://resources.data.gov/resources/dcat-us/).

The validation code is based on the [`jsonschema`](https://github.com/python-jsonschema/jsonschema)
package and defines schema rules in [`ckanext/datajson/pod_schema`](https://github.com/GSA/ckanext-datajson/tree/main/ckanext/datajson/pod_schema).
`jsonschema` provides a [few different types](https://github.com/python-jsonschema/jsonschema/blob/8fd12e29d8ad6e44ab48e0cd54c87ffe015b6c2a/jsonschema/__init__.py#L24-L29) of validators.
This extension is built on the [`Draft4Validator`]([https://github.com/python-jsonschema/jsonschema/blob/8fd12e29d8ad6e44ab48e0cd54c87ffe015b6c2a/jsonschema/validators.py#L453).

Currently, the validator only validates against the `federal-v1.1` schema.
