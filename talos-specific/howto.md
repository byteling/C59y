## Getting schematics id

# POST the yaml to the image factory

$ curl -X POST --data-binary @bare-metal.yaml https://factory.talos.dev/schematics
{"id":"b8e8fbbe1b520989e6c52c8dc8303070cb42095997e76e812fa8892393e1d176"}

# Update to a new talos version

talosctl upgrade --image factory.talos.dev/metal-installer/b8e8fbbe1b520989e6c52c8dc8303070cb42095997e76e812fa8892393e1d176:<new_version>

# Update to a different schematic

For example changed system extension (v1.11.0 is latest as of writing)

talosctl upgrade --image factory.talos.dev/metal-installer/<new_schematic_id>:v1.11.0 --nodes <ip,ip,ip>
