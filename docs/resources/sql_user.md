---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "cockroach_sql_user Resource - terraform-provider-cockroach"
subcategory: ""
description: |-
  CockroachDB SQL user.
---

# cockroach_sql_user (Resource)

CockroachDB SQL user.



<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `cluster_id` (String)
- `name` (String) SQL user name.

### Optional

- `password` (String, Sensitive) If provided, this field sets the password of the SQL user when created. If omitted, a random password is generated, but not saved to Terraform state. The password must be changed via the CockroachDB cloud console.

### Read-Only

- `id` (String) A unique identifier with format `<cluster ID>:<SQL user name>`.


