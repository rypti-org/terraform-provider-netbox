---
# generated by https://github.com/fbreckle/terraform-plugin-docs
page_title: "netbox_vlans Data Source - terraform-provider-netbox"
subcategory: "IP Address Management (IPAM)"
description: |-
  
---

# netbox_vlans (Data Source)





<!-- schema generated by tfplugindocs -->
## Schema

### Optional

- `filter` (Block Set) (see [below for nested schema](#nestedblock--filter))
- `limit` (Number) Defaults to `0`.

### Read-Only

- `id` (String) The ID of this resource.
- `vlans` (List of Object) (see [below for nested schema](#nestedatt--vlans))

<a id="nestedblock--filter"></a>
### Nested Schema for `filter`

Required:

- `name` (String)
- `value` (String)


<a id="nestedatt--vlans"></a>
### Nested Schema for `vlans`

Read-Only:

- `description` (String)
- `group_id` (Number)
- `id` (Number)
- `name` (String)
- `role` (Number)
- `site` (Number)
- `status` (String)
- `tag_ids` (List of Number)
- `tenant` (Number)
- `vid` (Number)


