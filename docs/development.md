# Change a template

Work flows from a feature branch to `staging` to `main`. Pull requests go into
`staging` and are merged with a merge commit.

1. Import the template into a test Zabbix 6.0 and make the change there.
2. Export it again from Zabbix, rather than editing the YAML by hand, so the
   UUIDs stay consistent.
3. Replace the template's `.yaml` file and update its README if macros,
   discovery rules or triggers changed.
4. Open the pull request.

The template directory names carry spaces and the Zabbix version. They stay as
they are, because renaming them would break existing links.

## Check

The `Validate` workflow parses every YAML file and requires a `zabbix_export`
root in each template.
