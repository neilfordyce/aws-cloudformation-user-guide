# AWS::WAFv2::WebACL RegexMatchStatement<a name="aws-properties-wafv2-webacl-regexmatchstatement"></a>

A rule statement used to search web request components for a match against a single regular expression\. 

## Syntax<a name="aws-properties-wafv2-webacl-regexmatchstatement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-webacl-regexmatchstatement-syntax.json"></a>

```
{
  "[FieldToMatch](#cfn-wafv2-webacl-regexmatchstatement-fieldtomatch)" : FieldToMatch,
  "[RegexString](#cfn-wafv2-webacl-regexmatchstatement-regexstring)" : String,
  "[TextTransformations](#cfn-wafv2-webacl-regexmatchstatement-texttransformations)" : [ TextTransformation, ... ]
}
```

### YAML<a name="aws-properties-wafv2-webacl-regexmatchstatement-syntax.yaml"></a>

```
  [FieldToMatch](#cfn-wafv2-webacl-regexmatchstatement-fieldtomatch): 
    FieldToMatch
  [RegexString](#cfn-wafv2-webacl-regexmatchstatement-regexstring): 
    String
  [TextTransformations](#cfn-wafv2-webacl-regexmatchstatement-texttransformations): 
    - TextTransformation
```

## Properties<a name="aws-properties-wafv2-webacl-regexmatchstatement-properties"></a>

`FieldToMatch`  <a name="cfn-wafv2-webacl-regexmatchstatement-fieldtomatch"></a>
The part of the web request that you want AWS WAF to inspect\.   
*Required*: Yes  
*Type*: [FieldToMatch](aws-properties-wafv2-webacl-fieldtomatch.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RegexString`  <a name="cfn-wafv2-webacl-regexmatchstatement-regexstring"></a>
The string representing the regular expression\.  
*Required*: Yes  
*Type*: String  
*Minimum*: `1`  
*Maximum*: `512`  
*Pattern*: `.*`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`TextTransformations`  <a name="cfn-wafv2-webacl-regexmatchstatement-texttransformations"></a>
Text transformations eliminate some of the unusual formatting that attackers use in web requests in an effort to bypass detection\. Text transformations are used in rule match statements, to transform the `FieldToMatch` request component before inspecting it, and they're used in rate\-based rule statements, to transform request components before using them as custom aggregation keys\. If you specify one or more transformations to apply, AWS WAF performs all transformations on the specified content, starting from the lowest priority setting, and then uses the component contents\.   
*Required*: Yes  
*Type*: List of [TextTransformation](aws-properties-wafv2-webacl-texttransformation.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)