---
# generated by https://github.com/fbreckle/terraform-plugin-docs
page_title: "netbox_group Resource - terraform-provider-netbox"
subcategory: "Authentication"
description: |-
  This resource is used to manage groups.
---

# netbox_group (Resource)

This resource is used to manage groups.

## Example Usage

```terraform
resource "netbox_group" "test" {
  name = "test-group"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `name` (String)

### Optional

- `description` (String) Defaults to `""`.

### Read-Only

- `id` (String) The ID of this resource.


