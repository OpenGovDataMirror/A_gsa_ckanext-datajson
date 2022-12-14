# Data.json Harvesting

The following documents tips and cool tricks for enabling the `datajson_harvest`
plugin.

## Harvesting

To use the data.json harvester, you'll also need to set up the CKAN harvester
extension. See the CKAN harvester README at https://github.com/okfn/ckanext-harvest
for how to do that. You'll set some configuration variables and then initialize the
CKAN harvester plugin using:

	ckan -c /path/to/ckan.ini harvester initdb

Now you can set up a new DataJson harvester by visiting:

	http://yourdomain.com/harvest

And when configuring the data source, just choose "/data.json" as the source type.

