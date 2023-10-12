---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "t1_vpc_security_group Data Source - terraform-provider-t1"
subcategory: ""
description: |-
  Get a T1.Cloud VPC Security Group data source, that can be used by other resources.
---

# t1_vpc_security_group (Data Source)

Get a T1.Cloud VPC Security Group data source, that can be used by other resources.

## Example Usage

```terraform
data "t1_vpc_security_group" "name" {
  name = "default"
}

data "t1_vpc_security_group" "name" {
  id = "4a26a434-bb63-48eb-a08d-5010e89fe2c5"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Optional

- `id` (String) Security Group ID.
- `name` (String) Name of the security group.

### Read-Only

- `description` (String) Description of the security group.