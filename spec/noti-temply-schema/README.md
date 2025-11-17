# noti-temply-schema

This repository stores JSON schemas for notification templates.

## Overview

This repository manages schema files from the [noti-temply](https://github.com/mieeru/noti-temply) repository. When a tag is created in `noti-temply`, it automatically deploys to this repository and saves `schema.json` files for each template.

## Structure

```
{tag-name}/
  └── templates/
      └── {template-name}/
          └── schema.json
```

### Example

```
ORM-1234/
  └── templates/
      ├── arrangement_mailer:receive_message/
      │   └── schema.json
      ├── order_mailer:order_request/
      │   └── schema.json
      └── ...
```

## Deployment Process

1. Create and merge a PR with a branch named `noti-temply/{alpha}-{number}` in the `noti-temply` repository.
2. A tag with format `{alpha}-{number}` is created automatically.
3. The `tag-deploy-to-schema` workflow runs automatically when the tag is created.
4. A folder with the same name as the tag is created in this repository, and only `schema.json` files are copied.

> **Note**: For trigger-related information, please refer to the [noti-temply](https://github.com/mieeru/noti-temply) repository.

## Tag Format

- **Format**: `{alpha}-{number}`
- **Examples**: 
  - `ORM-1234`
  - `ABC-456`
  - `OR-789`

## Related Links

### Template Repository
- GitHub: https://github.com/mieeru/noti-temply

### Admin
- GitHub: https://github.com/mieeru/noti-temply-admin
- Web: https://noti-temply.rentals.sh
