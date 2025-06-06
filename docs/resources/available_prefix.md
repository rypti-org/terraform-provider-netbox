---
# generated by https://github.com/fbreckle/terraform-plugin-docs
page_title: "netbox_available_prefix Resource - terraform-provider-netbox"
subcategory: "IP Address Management (IPAM)"
description: |-
  
---

# netbox_available_prefix (Resource)



## Example Usage

```terraform
data "netbox_prefix" "test" {
  cidr = "10.0.0.0/24"
}

resource "netbox_available_prefix" "test" {
  parent_prefix_id = data.netbox_prefix.test.id
  prefix_length    = 25
  status           = "active"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `parent_prefix_id` (Number)
- `prefix_length` (Number)
- `status` (String) Valid values are `active`, `container`, `reserved` and `deprecated`.

### Optional

- `description` (String)
- `is_pool` (Boolean)
- `mark_utilized` (Boolean)
- `role_id` (Number)
- `site_id` (Number)
- `tags` (Set of String)
- `tenant_id` (Number)
- `vlan_id` (Number)
- `vrf_id` (Number)

### Read-Only

- `id` (String) The ID of this resource.
- `prefix` (String)
- `tags_all` (Set of String)


