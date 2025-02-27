---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "cockroach_log_export_config Resource - terraform-provider-cockroach"
subcategory: ""
description: |-
  Log Export configuration for a cluster.
---

# cockroach_log_export_config (Resource)

Log Export configuration for a cluster.



<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `auth_principal` (String) Either the AWS Role ARN that identifies a role that the cluster account can assume to write to CloudWatch or the GCP Project ID that the cluster service account has permissions to write to for cloud logging.
- `id` (String) Cluster ID.
- `log_name` (String) An identifier for the logs in the customer's log sink.
- `type` (String) The cloud selection being exported to along with the cloud logging platform. Possible values are:
  * AWS_CLOUDWATCH
  * GCP_CLOUD_LOGGING

### Optional

- `groups` (Attributes List) (see [below for nested schema](#nestedatt--groups))
- `redact` (Boolean) Controls whether logs are redacted before forwarding to customer sinks.
- `region` (String) Controls whether all logs are sent to a specific region in the customer sink.

### Read-Only

- `created_at` (String) Indicates when log export was initially configured.
- `status` (String) Encodes the possible states that a log export configuration can be in as it is created, deployed, and disabled.
- `updated_at` (String) Indicates when the log export configuration was last updated.
- `user_message` (String) Elaborates on the log export status and hints at how to fix issues that may have occurred during asynchronous operations.

<a id="nestedatt--groups"></a>
### Nested Schema for `groups`

Required:

- `channels` (List of String) A list of CockroachDB log channels to include in this group.
- `log_name` (String) The name of the group, reflected in the log sink.

Optional:

- `min_level` (String) The minimum log level to filter to this log group.
- `redact` (Boolean) Governs whether this log group should aggregate redacted logs if unset.


