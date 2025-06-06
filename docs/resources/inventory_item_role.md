---
# generated by https://github.com/fbreckle/terraform-plugin-docs
page_title: "netbox_inventory_item_role Resource - terraform-provider-netbox"
subcategory: "Data Center Inventory Management (DCIM)"
description: |-
  From the official documentation https://docs.netbox.dev/en/stable/models/dcim/inventoryitemrole/:
  Inventory items can be organized by functional roles, which are fully customizable by the user. For example, you might create roles for power supplies, fans, interface optics, etc.
---

# netbox_inventory_item_role (Resource)

From the [official documentation](https://docs.netbox.dev/en/stable/models/dcim/inventoryitemrole/):

> Inventory items can be organized by functional roles, which are fully customizable by the user. For example, you might create roles for power supplies, fans, interface optics, etc.

## Example Usage

```terraform
# Note that some terraform code is not included in the example for brevity

resource "netbox_device" "test" {
  name           = "%[1]s"
  device_type_id = netbox_device_type.test.id
  tenant_id      = netbox_tenant.test.id
  role_id        = netbox_device_role.test.id
  site_id        = netbox_site.test.id
}

resource "netbox_inventory_item_role" "test" {
  name      = "Role 1"
  slug      = "role-1-slug"
  color_hex = "123456"
}

resource "netbox_inventory_item" "parent" {
  device_id = netbox_device.test.id
  name      = "Inventory Item 1"
  role_id   = netbox_inventory_item_role.test.id
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `color_hex` (String)
- `name` (String)
- `slug` (String)

### Optional

- `custom_fields` (Map of String)
- `description` (String)
- `tags` (Set of String)

### Read-Only

- `id` (String) The ID of this resource.
- `tags_all` (Set of String)


