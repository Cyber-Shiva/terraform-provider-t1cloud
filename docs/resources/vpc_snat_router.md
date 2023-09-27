---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "t1_vpc_snat_router Resource - terraform-provider-t1"
subcategory: ""
description: |-
  Manages a SNAT router resource within T1.Cloud VPC.
---

# t1_vpc_snat_router (Resource)

Manages a SNAT router resource within T1.Cloud VPC.

## Example Usage

```terraform
resource "t1_vpc_network" "network1" {
  name = "network1"
}

resource "t1_vpc_network" "network2" {
  name = "network2"
}

resource "t1_vpc_snat_router" "foo" {
  region = "ru-central1"
  network_ids = [
    t1_vpc_network.network1.id,
    t1_vpc_network.network2.id,
  ]
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `network_ids` (List of String) IDs of networks that will have access to the Internet. Servers located in the subnets of the specified networks will have access to the Internet.
- `region` (String) Region where this router will be placed.

### Optional

- `name` (String) A name for the SNAT router. Changing this will replace resource.

### Read-Only

- `id` (String) The order ID of this resource
- `public_ip` (String) The public address is automatically assigned to the created router.