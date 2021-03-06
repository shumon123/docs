---
title: Package @pulumi/aws-infra
---


Node.js:

```javascript
var awsInfra = require("@pulumi/aws-infra");
```

ES6 modules:

```typescript
import * as awsInfra from "@pulumi/aws-infra";
```

<h2 class="pdoc-module-header">Index</h2>

* <a href="#Cluster">class Cluster</a>
* <a href="#Network">class Network</a>
* <a href="#checkCompat">function checkCompat</a>
* <a href="#combineArrays">function combineArrays</a>
* <a href="#getAvailabilityZone">function getAvailabilityZone</a>
* <a href="#getAvailabilityZones">function getAvailabilityZones</a>
* <a href="#ifUndefined">function ifUndefined</a>
* <a href="#sha1hash">function sha1hash</a>
* <a href="#ClusterArgs">interface ClusterArgs</a>
* <a href="#ClusterNetworkArgs">interface ClusterNetworkArgs</a>
* <a href="#NetworkArgs">interface NetworkArgs</a>
* <a href="#NetworkVpcArgs">interface NetworkVpcArgs</a>
* <a href="#Compatible">type Compatible</a>
* <a href="#Mutable">type Mutable</a>
* <a href="#Overwrite">type Overwrite</a>

<a href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/aws.ts">aws.ts</a> <a href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/cluster.ts">cluster.ts</a> <a href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/network.ts">network.ts</a> <a href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/utils.ts">utils.ts</a> 


<h2 class="pdoc-module-header" id="Cluster">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/cluster.ts#L107">class Cluster</a>
</h2>

A Cluster is a general purpose ECS cluster configured to run in a provided
Network.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/cluster.ts#L128">constructor</a>
</h3>

```typescript
new Cluster(name: string, args: ClusterArgs, opts?: pulumi.ResourceOptions)
```

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L13">method getProvider</a>
</h3>

```typescript
getProvider(moduleMember: string): ProviderResource | undefined
```

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L12">method isInstance</a>
</h3>

```typescript
static isInstance(obj: any): boolean
```

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L135">method registerOutputs</a>
</h3>

```typescript
protected registerOutputs(outputs: Inputs | Promise<Inputs> | Output<Inputs> | undefined): void
```

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/cluster.ts#L124">property autoScalingGroupStack</a>
</h3>

```typescript
public autoScalingGroupStack?: pulumi.Resource;
```


The auto-scaling group that ECS Service's should add to their
`dependsOn`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/cluster.ts#L115">property ecsClusterARN</a>
</h3>

```typescript
public ecsClusterARN: pulumi.Output<string>;
```


The ECS Cluster ARN.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/cluster.ts#L128">property efsMountPath</a>
</h3>

```typescript
public efsMountPath?: undefined | string;
```


The EFS host mount path if EFS is enabled on this Cluster.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/cluster.ts#L111">property network</a>
</h3>

```typescript
public network: ClusterNetworkArgs;
```


The network in which to create this cluster.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/cluster.ts#L119">property securityGroupId</a>
</h3>

```typescript
public securityGroupId?: pulumi.Output<string>;
```


The ECS Cluster's Security Group ID.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L11">property urn</a>
</h3>

```typescript
urn: Output<URN>;
```


urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.

<h2 class="pdoc-module-header" id="Network">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/network.ts#L92">class Network</a>
</h2>

Network encapsulates the configuration of an Amazon VPC.  Both [VPC with Public
Subnet](https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Scenario1.html) and [VPC with Public and Private
Subnets (NAT)](https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Scenario2.html) configurations are
supported.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/network.ts#L161">constructor</a>
</h3>

```typescript
new Network(name: string, args?: NetworkArgs, opts?: pulumi.ResourceOptions)
```

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/network.ts#L146">method fromVpc</a>
</h3>

```typescript
public static fromVpc(name: string, vpcArgs: NetworkVpcArgs, opts?: pulumi.ResourceOptions): Network
```


Creates a new network using the configuration values of an existing VPC.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/network.ts#L120">method getDefault</a>
</h3>

```typescript
public static getDefault(opts?: pulumi.ResourceOptions): Network
```


Gets the default VPC for the AWS account as a Network.  This first time this is called,
the default network will be lazily created, using whatever options are provided in opts.
All subsequent calls will return that same network even if different opts are provided.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L13">method getProvider</a>
</h3>

```typescript
getProvider(moduleMember: string): ProviderResource | undefined
```

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L12">method isInstance</a>
</h3>

```typescript
static isInstance(obj: any): boolean
```

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L135">method registerOutputs</a>
</h3>

```typescript
protected registerOutputs(outputs: Inputs | Promise<Inputs> | Output<Inputs> | undefined): void
```

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/network.ts#L113">property publicSubnetIds</a>
</h3>

```typescript
public publicSubnetIds: pulumi.Output<string>[];
```


The public subnets for the VPC.  In case [usePrivateSubnets] == false, these are the same as [subnets].

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/network.ts#L104">property securityGroupIds</a>
</h3>

```typescript
public securityGroupIds: pulumi.Output<string>[];
```


The security group IDs for the network.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/network.ts#L109">property subnetIds</a>
</h3>

```typescript
public subnetIds: pulumi.Output<string>[];
```


The subnets in which compute should run.  These are the private subnets if [usePrivateSubnets] == true, else
these are the public subnets.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/node_modules/@pulumi/pulumi/resource.d.ts#L11">property urn</a>
</h3>

```typescript
urn: Output<URN>;
```


urn is the stable logical URN used to distinctly address a resource, both before and after
deployments.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/network.ts#L100">property usePrivateSubnets</a>
</h3>

```typescript
public usePrivateSubnets: boolean;
```


Whether the network includes private subnets.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/network.ts#L96">property vpcId</a>
</h3>

```typescript
public vpcId: pulumi.Output<string>;
```


The VPC id of the network.

<h2 class="pdoc-module-header" id="checkCompat">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/utils.ts#L65">function checkCompat</a>
</h2>

```typescript
checkCompat<T,U>(): Compatible<T, U>
```

<h2 class="pdoc-module-header" id="combineArrays">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/utils.ts#L42">function combineArrays</a>
</h2>

```typescript
combineArrays<T>(e1: pulumi.Input<T[] | undefined>, e2: pulumi.Input<T[] | undefined>): pulumi.Output<T[]>
```

<h2 class="pdoc-module-header" id="getAvailabilityZone">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/aws.ts#L23">function getAvailabilityZone</a>
</h2>

```typescript
getAvailabilityZone(index: number): Promise<string>
```

<h2 class="pdoc-module-header" id="getAvailabilityZones">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/aws.ts#L28">function getAvailabilityZones</a>
</h2>

```typescript
getAvailabilityZones(): Promise<string[]>
```

<h2 class="pdoc-module-header" id="ifUndefined">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/utils.ts#L56">function ifUndefined</a>
</h2>

```typescript
ifUndefined<T>(input: pulumi.Input<T> | undefined, value: pulumi.Input<T>): Output<Unwrap<T>>
```

<h2 class="pdoc-module-header" id="sha1hash">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/utils.ts#L33">function sha1hash</a>
</h2>

```typescript
sha1hash(s: string): string
```

<h2 class="pdoc-module-header" id="ClusterArgs">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/cluster.ts#L39">interface ClusterArgs</a>
</h2>

Arguments bag for creating infrastrcture for a new Cluster.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/cluster.ts#L47">property addEFS</a>
</h3>

```typescript
addEFS: boolean;
```


Whether to create an EFS File System to manage volumes across the cluster.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/cluster.ts#L100">property ecsOptimizedAMIName</a>
</h3>

```typescript
ecsOptimizedAMIName?: undefined | string;
```


The name of the ECS-optimzed AMI to use for the Container Instances in this cluster, e.g.
"amzn-ami-2017.09.l-amazon-ecs-optimized". Defaults to using the latest recommended ECS Optimized AMI, which may
change over time and cause recreation of EC2 instances when new versions are release. To control when these
changes are adopted, set this parameter explicitly to the version you would like to use.

See http://docs.aws.amazon.com/AmazonECS/latest/developerguide/ecs-optimized_AMI.html for valid values.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/cluster.ts#L70">property instanceDockerImageVolumeSize</a>
</h3>

```typescript
instanceDockerImageVolumeSize?: undefined | number;
```


The size (in GiB) of the EBS volume to attach to each instance to use for Docker image and metadata storage.

The default is 50 GiB.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/cluster.ts#L58">property instanceRolePolicyARNs</a>
</h3>

```typescript
instanceRolePolicyARNs?: string[];
```


The policy to apply to the cluster instance role.

The default is `["arn:aws:iam::aws:policy/service-role/AmazonEC2ContainerServiceforEC2Role",
"arn:aws:iam::aws:policy/AmazonEC2ReadOnlyAccess"]`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/cluster.ts#L64">property instanceRootVolumeSize</a>
</h3>

```typescript
instanceRootVolumeSize?: undefined | number;
```


The size (in GiB) of the EBS volume to attach to each instance as the root volume.

The default is 8 GiB.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/cluster.ts#L76">property instanceSwapVolumeSize</a>
</h3>

```typescript
instanceSwapVolumeSize?: undefined | number;
```


The size (in GiB) of the EBS volume to attach to each instance for swap space.

The default is 5 GiB.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/cluster.ts#L51">property instanceType</a>
</h3>

```typescript
instanceType?: undefined | string;
```


The EC2 instance type to use for the Cluster.  Defaults to `t2.micro`.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/cluster.ts#L85">property maxSize</a>
</h3>

```typescript
maxSize?: undefined | number;
```


The maximum size of the cluster. Setting to 0 will prevent an EC2 AutoScalingGroup from being created. Defaults
to 100.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/cluster.ts#L80">property minSize</a>
</h3>

```typescript
minSize?: undefined | number;
```


The minimum size of the cluster. Defaults to 2.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/cluster.ts#L43">property network</a>
</h3>

```typescript
network: ClusterNetworkArgs;
```


The network in which to create this cluster.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/cluster.ts#L91">property publicKey</a>
</h3>

```typescript
publicKey?: undefined | string;
```


Public key material for SSH access. See allowed formats at:
https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html
If not provided, no SSH access is enabled on VMs.

<h2 class="pdoc-module-header" id="ClusterNetworkArgs">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/cluster.ts#L25">interface ClusterNetworkArgs</a>
</h2>
<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/cluster.ts#L33">property subnetIds</a>
</h3>

```typescript
subnetIds: pulumi.Input<string>[];
```


The network subnets for the clusters

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/cluster.ts#L29">property vpcId</a>
</h3>

```typescript
vpcId: pulumi.Input<string>;
```


The VPC id of the network for the cluster

<h2 class="pdoc-module-header" id="NetworkArgs">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/network.ts#L28">interface NetworkArgs</a>
</h2>

Optional arguments that can be provided when creating a network.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/network.ts#L39">property cidrBlock</a>
</h3>

```typescript
cidrBlock?: pulumi.Input<string>;
```


The CIDR block for the VPC.  Defaults to "10.10.0.0/16" if unspecified.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/network.ts#L44">property enableDnsHostnames</a>
</h3>

```typescript
enableDnsHostnames?: pulumi.Input<boolean>;
```


Whether or not to have DNS hostnames in the VPC. Defaults to 'true' if unspecified.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/network.ts#L49">property enableDnsSupport</a>
</h3>

```typescript
enableDnsSupport?: pulumi.Input<boolean>;
```


Whether or not to have DNS support in the VPC.  Defaults to 'true' if unspecified.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/network.ts#L54">property instanceTenancy</a>
</h3>

```typescript
instanceTenancy?: pulumi.Input<default | dedicated>;
```


A tenancy option for instances launched into the VPC.  Defaults to 'default' if unspecified.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/network.ts#L33">property numberOfAvailabilityZones</a>
</h3>

```typescript
numberOfAvailabilityZones?: undefined | number;
```


The maximum number of availability zones to use in the current region.  Defaults to '2' if
unspecified.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/network.ts#L34">property usePrivateSubnets</a>
</h3>

```typescript
usePrivateSubnets?: undefined | false | true;
```

<h2 class="pdoc-module-header" id="NetworkVpcArgs">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/network.ts#L60">interface NetworkVpcArgs</a>
</h2>

Arguments necessary when creating a network using Network.fromVpc.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/network.ts#L80">property publicSubnetIds</a>
</h3>

```typescript
publicSubnetIds: pulumi.Input<string>[];
```


The public subnets for the VPC.  In case [usePrivateSubnets] == false, these are the same as [subnets].

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/network.ts#L76">property securityGroupIds</a>
</h3>

```typescript
securityGroupIds: pulumi.Input<string>[];
```


The security group IDs for the network.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/network.ts#L68">property subnetIds</a>
</h3>

```typescript
subnetIds: pulumi.Input<string>[];
```


The network subnets for the clusters

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/network.ts#L72">property usePrivateSubnets</a>
</h3>

```typescript
usePrivateSubnets: boolean;
```


Whether the network includes private subnets.

<h3 class="pdoc-member-header">
<a class="pdoc-child-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/network.ts#L64">property vpcId</a>
</h3>

```typescript
vpcId: pulumi.Input<string>;
```


The VPC id of the network for the cluster

<h2 class="pdoc-module-header" id="Compatible">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/utils.ts#L62">type Compatible</a>
</h2>

```typescript
type Compatible = Compatible<T, U>;
```

<h2 class="pdoc-module-header" id="Mutable">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/utils.ts#L27">type Mutable</a>
</h2>

```typescript
type Mutable = { ... };
```

<h2 class="pdoc-module-header" id="Overwrite">
<a class="pdoc-member-name" href="https://github.com/pulumi/pulumi-aws-infra/blob/master/nodejs/utils.ts#L24">type Overwrite</a>
</h2>

```typescript
type Overwrite = Pick<T, Diff<keyof T, keyof U>> & U;
```

