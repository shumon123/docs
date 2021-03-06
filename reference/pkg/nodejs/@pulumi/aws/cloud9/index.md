---
title: Module cloud9
---

<a href="../index.html">@pulumi/aws</a> &gt; cloud9

<h2 class="pdoc-module-header">Index</h2>

* <a href="#EnvironmentEC2">class EnvironmentEC2</a>
* <a href="#EnvironmentEC2Args">interface EnvironmentEC2Args</a>
* <a href="#EnvironmentEC2State">interface EnvironmentEC2State</a>

<a href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloud9/environmentEC2.ts">cloud9/environmentEC2.ts</a> 


<h2 class="pdoc-module-header" id="EnvironmentEC2">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloud9/environmentEC2.ts#L10">class EnvironmentEC2</a>
</h2>

Provides a Cloud9 EC2 Development Environment.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloud9/environmentEC2.ts#L54">constructor</a>
</h3>

```typescript
new EnvironmentEC2(name: string, args: EnvironmentEC2Args, opts?: pulumi.CustomResourceOptions)
```


Create a EnvironmentEC2 resource with the given unique name, arguments, and options.

* `name` The _unique_ name of the resource.
* `args` The arguments to use to populate this resource&#39;s properties.
* `opts` A bag of options that control this resource&#39;s behavior.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloud9/environmentEC2.ts#L19">method get</a>
</h3>

```typescript
public static get(name: string, id: pulumi.Input<pulumi.ID>, state?: EnvironmentEC2State): EnvironmentEC2
```


Get an existing EnvironmentEC2 resource's state with the given name, ID, and optional extra
properties used to qualify the lookup.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L13">method getProvider</a>
</h3>

```typescript
getProvider(moduleMember: string): ProviderResource | undefined
```

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L85">method isInstance</a>
</h3>

```typescript
static isInstance(obj: any): boolean
```


Returns true if the given object is an instance of CustomResource.  This is designed to work even when
multiple copies of the Pulumi SDK have been loaded into the same process.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloud9/environmentEC2.ts#L26">property arn</a>
</h3>

```typescript
public arn: pulumi.Output<string>;
```


The ARN of the environment.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloud9/environmentEC2.ts#L30">property automaticStopTimeMinutes</a>
</h3>

```typescript
public automaticStopTimeMinutes: pulumi.Output<number | undefined>;
```


The number of minutes until the running instance is shut down after the environment has last been used.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloud9/environmentEC2.ts#L34">property description</a>
</h3>

```typescript
public description: pulumi.Output<string | undefined>;
```


The description of the environment.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L80">property id</a>
</h3>

```typescript
id: Output<ID>;
```


id is the provider-assigned unique ID for this managed resource.  It is set during
deployments and may be missing (undefined) during planning phases.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloud9/environmentEC2.ts#L38">property instanceType</a>
</h3>

```typescript
public instanceType: pulumi.Output<string>;
```


The type of instance to connect to the environment, e.g. `t2.micro`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloud9/environmentEC2.ts#L42">property name</a>
</h3>

```typescript
public name: pulumi.Output<string>;
```


The name of the environment.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloud9/environmentEC2.ts#L46">property ownerArn</a>
</h3>

```typescript
public ownerArn: pulumi.Output<string>;
```


The ARN of the environment owner. This can be ARN of any AWS IAM principal. Defaults to the environment's creator.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloud9/environmentEC2.ts#L50">property subnetId</a>
</h3>

```typescript
public subnetId: pulumi.Output<string | undefined>;
```


The ID of the subnet in Amazon VPC that AWS Cloud9 will use to communicate with the Amazon EC2 instance.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloud9/environmentEC2.ts#L54">property type</a>
</h3>

```typescript
public type: pulumi.Output<string>;
```


The type of the environment (e.g. `ssh` or `ec2`)

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L11">property urn</a>
</h3>

```typescript
urn: Output<URN>;
```


urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.

<h2 class="pdoc-module-header" id="EnvironmentEC2Args">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloud9/environmentEC2.ts#L135">interface EnvironmentEC2Args</a>
</h2>

The set of arguments for constructing a EnvironmentEC2 resource.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloud9/environmentEC2.ts#L139">property automaticStopTimeMinutes</a>
</h3>

```typescript
automaticStopTimeMinutes?: pulumi.Input<number>;
```


The number of minutes until the running instance is shut down after the environment has last been used.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloud9/environmentEC2.ts#L143">property description</a>
</h3>

```typescript
description?: pulumi.Input<string>;
```


The description of the environment.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloud9/environmentEC2.ts#L147">property instanceType</a>
</h3>

```typescript
instanceType: pulumi.Input<string>;
```


The type of instance to connect to the environment, e.g. `t2.micro`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloud9/environmentEC2.ts#L151">property name</a>
</h3>

```typescript
name?: pulumi.Input<string>;
```


The name of the environment.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloud9/environmentEC2.ts#L155">property ownerArn</a>
</h3>

```typescript
ownerArn?: pulumi.Input<string>;
```


The ARN of the environment owner. This can be ARN of any AWS IAM principal. Defaults to the environment's creator.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloud9/environmentEC2.ts#L159">property subnetId</a>
</h3>

```typescript
subnetId?: pulumi.Input<string>;
```


The ID of the subnet in Amazon VPC that AWS Cloud9 will use to communicate with the Amazon EC2 instance.

<h2 class="pdoc-module-header" id="EnvironmentEC2State">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloud9/environmentEC2.ts#L97">interface EnvironmentEC2State</a>
</h2>

Input properties used for looking up and filtering EnvironmentEC2 resources.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloud9/environmentEC2.ts#L101">property arn</a>
</h3>

```typescript
arn?: pulumi.Input<string>;
```


The ARN of the environment.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloud9/environmentEC2.ts#L105">property automaticStopTimeMinutes</a>
</h3>

```typescript
automaticStopTimeMinutes?: pulumi.Input<number>;
```


The number of minutes until the running instance is shut down after the environment has last been used.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloud9/environmentEC2.ts#L109">property description</a>
</h3>

```typescript
description?: pulumi.Input<string>;
```


The description of the environment.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloud9/environmentEC2.ts#L113">property instanceType</a>
</h3>

```typescript
instanceType?: pulumi.Input<string>;
```


The type of instance to connect to the environment, e.g. `t2.micro`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloud9/environmentEC2.ts#L117">property name</a>
</h3>

```typescript
name?: pulumi.Input<string>;
```


The name of the environment.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloud9/environmentEC2.ts#L121">property ownerArn</a>
</h3>

```typescript
ownerArn?: pulumi.Input<string>;
```


The ARN of the environment owner. This can be ARN of any AWS IAM principal. Defaults to the environment's creator.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloud9/environmentEC2.ts#L125">property subnetId</a>
</h3>

```typescript
subnetId?: pulumi.Input<string>;
```


The ID of the subnet in Amazon VPC that AWS Cloud9 will use to communicate with the Amazon EC2 instance.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws/blob/master/sdk/nodejs/cloud9/environmentEC2.ts#L129">property type</a>
</h3>

```typescript
type?: pulumi.Input<string>;
```


The type of the environment (e.g. `ssh` or `ec2`)

