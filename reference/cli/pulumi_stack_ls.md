## pulumi stack ls

List all known stacks

### Synopsis


List all known stacks

```
pulumi stack ls [flags]
```

### Options

```
  -a, --all    List all stacks instead of just stacks for the current project
  -h, --help   help for ls
```

### Options inherited from parent commands

```
  -C, --cwd string                   Run pulumi as if it had been started in another directory
      --disable-integrity-checking   Disable integrity checking of checkpoint files
  -e, --emoji                        Enable emojis in the output (default true)
      --logflow                      Flow log settings to child processes (like plugins)
      --logtostderr                  Log to stderr instead of to files
  -i, --show-ids                     Display each resource's provider-assigned unique ID
  -u, --show-urns                    Display each resource's Pulumi-assigned globally unique URN
      --tracing string               Emit tracing to a Zipkin-compatible tracing endpoint
  -v, --verbose int                  Enable verbose logging (e.g., v=3); anything >3 is very verbose
```

### SEE ALSO
* [pulumi stack](pulumi_stack.md)	 - Manage stacks

###### Auto generated by spf13/cobra on 28-Apr-2018