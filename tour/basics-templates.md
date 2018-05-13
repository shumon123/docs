---
title: Templates
---

Creating projects, programs, and stacks isn't hard, but it's a common activity, and involves many steps.

[`pulumi new`](/reference/cli/pulumi_new.html) uses templates to speed up the process:

```bash
$ pulumi new hello-aws-javascript
This command will walk you through creating a new Pulumi project.
Enter a value or leave blank to accept the default, and press <ENTER>.
Press ^C at any time to quit.

project name: (ahoy-pulumi)
project description: Ahoy, Pulumi!
stack name: (ahoy-pulumi-dev)
aws:region: (us-east-1)

New project is configured and ready to deploy with 'pulumi update'.
```

This single command created a project, program, stack, and even configured it!

Templates are available for different languages, target clouds, and scenarios.  Run `pulumi new` without an
argument to see a list.

All of our templates are defined at [pulumi/templates](https://github.com/pulumi/templates).  If you don't find what
you're looking for, [let us know](mailto:support@pulumi.com).  PRs welcome!

***

This concludes the Tour of Pulumi basics.  Next up, let's see how to deploy our program's stacks.

<div class="tour-nav">
    <a class="tour-button enabled" href="basics-configuration.html" title="Configuration">◀</a>
    <span class="tour-index"><strong>9</strong>/9</span>
    <a class="tour-button enabled" href="deployments.html" title="Deployments">▶</a>
</div>