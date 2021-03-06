# Project Settings

Lets you change the settings of a commercetools project.

!!! note
    The project itself needs to be set up already. Before you can apply
    changes, you need to import the project:

    ```$ terraform import commercetools_project.project my-project-key```

Also, the project can not be destroyed with terraform.

## Example Usage

```hcl
resource "commercetools_project_settings" "project" {
  name = "My project"
  countries = ["NL", "DE", "US", "CA"]
  currencies = ["EUR", "USD", "CAD"]
  languages = ["nl", "de", "en", "fr-CA"]
  messages = {
    enabled = true
  }
}
```

## Argument Reference

The following arguments are supported:

* `name` -  The name of the project
* `countries` - A two-digit country code as per ISO 3166-1 alpha-2
* `currencies` - A three-digit currency code as per ISO 4217
* `languages` - An IETF language tag
* `messages.enabled` - When true the creation of messages is enabled
