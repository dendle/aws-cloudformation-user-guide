# AWS::LakeFormation::Resource<a name="aws-resource-lakeformation-resource"></a>

The `AWS::LakeFormation::Resource` represents the data \( buckets and folders\) that is being registered with AWS Lake Formation\. During a stack operation, AWS CloudFormation calls the AWS Lake Formation [https://docs.aws.amazon.com/lake-formation/latest/dg/aws-lake-formation-api-credential-vending.html#aws-lake-formation-api-credential-vending-RegisterResource](https://docs.aws.amazon.com/lake-formation/latest/dg/aws-lake-formation-api-credential-vending.html#aws-lake-formation-api-credential-vending-RegisterResource) API operation to register the resource\. To remove a `Resource` type, AWS CloudFormation calls the AWS Lake Formation [https://docs.aws.amazon.com/lake-formation/latest/dg/aws-lake-formation-api-credential-vending.html#aws-lake-formation-api-credential-vending-DeregisterResource](https://docs.aws.amazon.com/lake-formation/latest/dg/aws-lake-formation-api-credential-vending.html#aws-lake-formation-api-credential-vending-DeregisterResource) API operation\.

**Note**  
`AWS::LakeFormation::Resource` is a legacy resource that doesn't support the `UPDATE` operation\. Changes to the resource will require an explicit deletion and recreation to apply new properties\. 

## Syntax<a name="aws-resource-lakeformation-resource-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-resource-lakeformation-resource-syntax.json"></a>

```
{
  "Type" : "AWS::LakeFormation::Resource",
  "Properties" : {
      "[ResourceArn](#cfn-lakeformation-resource-resourcearn)" : String,
      "[RoleArn](#cfn-lakeformation-resource-rolearn)" : String,
      "[UseServiceLinkedRole](#cfn-lakeformation-resource-useservicelinkedrole)" : Boolean
    }
}
```

### YAML<a name="aws-resource-lakeformation-resource-syntax.yaml"></a>

```
Type: AWS::LakeFormation::Resource
Properties: 
  [ResourceArn](#cfn-lakeformation-resource-resourcearn): String
  [RoleArn](#cfn-lakeformation-resource-rolearn): String
  [UseServiceLinkedRole](#cfn-lakeformation-resource-useservicelinkedrole): Boolean
```

## Properties<a name="aws-resource-lakeformation-resource-properties"></a>

`ResourceArn`  <a name="cfn-lakeformation-resource-resourcearn"></a>
The Amazon Resource Name \(ARN\) of the resource\.  
*Required*: Yes  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RoleArn`  <a name="cfn-lakeformation-resource-rolearn"></a>
The IAM role that registered a resource\.  
*Required*: No  
*Type*: String  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`UseServiceLinkedRole`  <a name="cfn-lakeformation-resource-useservicelinkedrole"></a>
Designates a trusted caller, an IAM principal, by registering this caller with the Data Catalog\.  
*Required*: Yes  
*Type*: Boolean  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)