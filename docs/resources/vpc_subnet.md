---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "t1_vpc_subnet Resource - terraform-provider-t1"
subcategory: ""
description: |-
  Manages a subnet resource within T1.Cloud VPC.
---

# t1_vpc_subnet (Resource)

Manages a subnet resource within T1.Cloud VPC.

## Example Usage

```terraform
resource "t1_vpc_network" "foo" {
  name        = "My network"
  description = "description for my network"
}

resource "t1_vpc_subnet" "subnet1" {
  name        = "foo-subnet"
  description = "description for my subnet"
  region      = "ru-central1"
  cidr        = "10.128.0.1/24"
  network_id  = t1_vpc_network.foo.id
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `cidr` (String) The subnet size is determined by the classless addressing method: the maximum CIDR size is /16, the minimum is /28. IPv4 CIDR must match one of private IPs [10.0-255.x.x/prefix, 172.16.x.x/prefix, 192.168.x.x/prefix], where prefix is value from /16 to /28.
- `name` (String) Name of the subnet provided by the client.
- `network_id` (String) ID of the network this subnet belongs to.

### Optional

- `description` (String) An optional description of the subnet.
- `region` (String) Region where this subnet will be created.

### Read-Only

- `id` (String) The ID of created subnet.