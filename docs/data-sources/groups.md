---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "googleworkspace_groups Data Source - terraform-provider-googleworkspace"
subcategory: ""
description: |-
  Groups data source in the Terraform Googleworkspace provider. Groups resides under the https://www.googleapis.com/auth/admin.directory.group client scope.
---

# googleworkspace_groups (Data Source)

Groups data source in the Terraform Googleworkspace provider. Groups resides under the `https://www.googleapis.com/auth/admin.directory.group` client scope.

## Example Usage

```terraform
data "googleworkspace_groups" "my-domain-groups" {
}

output "num_groups" {
  value = length(data.googleworkspace_groups.my-domain-groups.groups)
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Read-Only

- **groups** (List of Object) A list of Group resources. (see [below for nested schema](#nestedatt--groups))
- **id** (String) The ID of this resource.

<a id="nestedatt--groups"></a>
### Nested Schema for `groups`

Read-Only:

- **admin_created** (Boolean) Value is true if this group was created by an administrator rather than a user.
- **aliases** (List of String) asps.list of group's email addresses.
- **description** (String) An extended description to help users determine the purpose of a group.For example, you can include information about who should join the group,the types of messages to send to the group, links to FAQs about the group, or related groups.
- **direct_members_count** (Number) The number of users that are direct members of the group.If a group is a member (child) of this group (the parent),members of the child group are not counted in the directMembersCount property of the parent group.
- **etag** (String) ETag of the resource.
- **name** (String) The group's display name.
- **non_editable_aliases** (List of String) asps.list of the group's non-editable alias email addresses that are outside of the account's primary domain or subdomains. These are functioning email addresses used by the group.


