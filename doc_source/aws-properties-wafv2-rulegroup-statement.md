# AWS::WAFv2::RuleGroup Statement<a name="aws-properties-wafv2-rulegroup-statement"></a>

The processing guidance for a rule, used by AWS WAF to determine whether a web request matches the rule\. 

## Syntax<a name="aws-properties-wafv2-rulegroup-statement-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-wafv2-rulegroup-statement-syntax.json"></a>

```
{
  "[AndStatement](#cfn-wafv2-rulegroup-statement-andstatement)" : AndStatement,
  "[ByteMatchStatement](#cfn-wafv2-rulegroup-statement-bytematchstatement)" : ByteMatchStatement,
  "[GeoMatchStatement](#cfn-wafv2-rulegroup-statement-geomatchstatement)" : GeoMatchStatement,
  "[IPSetReferenceStatement](#cfn-wafv2-rulegroup-statement-ipsetreferencestatement)" : IPSetReferenceStatement,
  "[LabelMatchStatement](#cfn-wafv2-rulegroup-statement-labelmatchstatement)" : LabelMatchStatement,
  "[NotStatement](#cfn-wafv2-rulegroup-statement-notstatement)" : NotStatement,
  "[OrStatement](#cfn-wafv2-rulegroup-statement-orstatement)" : OrStatement,
  "[RateBasedStatement](#cfn-wafv2-rulegroup-statement-ratebasedstatement)" : RateBasedStatement,
  "[RegexMatchStatement](#cfn-wafv2-rulegroup-statement-regexmatchstatement)" : RegexMatchStatement,
  "[RegexPatternSetReferenceStatement](#cfn-wafv2-rulegroup-statement-regexpatternsetreferencestatement)" : RegexPatternSetReferenceStatement,
  "[SizeConstraintStatement](#cfn-wafv2-rulegroup-statement-sizeconstraintstatement)" : SizeConstraintStatement,
  "[SqliMatchStatement](#cfn-wafv2-rulegroup-statement-sqlimatchstatement)" : SqliMatchStatement,
  "[XssMatchStatement](#cfn-wafv2-rulegroup-statement-xssmatchstatement)" : XssMatchStatement
}
```

### YAML<a name="aws-properties-wafv2-rulegroup-statement-syntax.yaml"></a>

```
  [AndStatement](#cfn-wafv2-rulegroup-statement-andstatement): 
    AndStatement
  [ByteMatchStatement](#cfn-wafv2-rulegroup-statement-bytematchstatement): 
    ByteMatchStatement
  [GeoMatchStatement](#cfn-wafv2-rulegroup-statement-geomatchstatement): 
    GeoMatchStatement
  [IPSetReferenceStatement](#cfn-wafv2-rulegroup-statement-ipsetreferencestatement): 
    IPSetReferenceStatement
  [LabelMatchStatement](#cfn-wafv2-rulegroup-statement-labelmatchstatement): 
    LabelMatchStatement
  [NotStatement](#cfn-wafv2-rulegroup-statement-notstatement): 
    NotStatement
  [OrStatement](#cfn-wafv2-rulegroup-statement-orstatement): 
    OrStatement
  [RateBasedStatement](#cfn-wafv2-rulegroup-statement-ratebasedstatement): 
    RateBasedStatement
  [RegexMatchStatement](#cfn-wafv2-rulegroup-statement-regexmatchstatement): 
    RegexMatchStatement
  [RegexPatternSetReferenceStatement](#cfn-wafv2-rulegroup-statement-regexpatternsetreferencestatement): 
    RegexPatternSetReferenceStatement
  [SizeConstraintStatement](#cfn-wafv2-rulegroup-statement-sizeconstraintstatement): 
    SizeConstraintStatement
  [SqliMatchStatement](#cfn-wafv2-rulegroup-statement-sqlimatchstatement): 
    SqliMatchStatement
  [XssMatchStatement](#cfn-wafv2-rulegroup-statement-xssmatchstatement): 
    XssMatchStatement
```

## Properties<a name="aws-properties-wafv2-rulegroup-statement-properties"></a>

`AndStatement`  <a name="cfn-wafv2-rulegroup-statement-andstatement"></a>
A logical rule statement used to combine other rule statements with AND logic\. You provide more than one `Statement` within the `AndStatement`\.   
*Required*: No  
*Type*: [AndStatement](aws-properties-wafv2-rulegroup-andstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`ByteMatchStatement`  <a name="cfn-wafv2-rulegroup-statement-bytematchstatement"></a>
A rule statement that defines a string match search for AWS WAF to apply to web requests\. The byte match statement provides the bytes to search for, the location in requests that you want AWS WAF to search, and other settings\. The bytes to search for are typically a string that corresponds with ASCII characters\. In the AWS WAF console and the developer guide, this is called a string match statement\.  
*Required*: No  
*Type*: [ByteMatchStatement](aws-properties-wafv2-rulegroup-bytematchstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`GeoMatchStatement`  <a name="cfn-wafv2-rulegroup-statement-geomatchstatement"></a>
A rule statement that labels web requests by country and region and that matches against web requests based on country code\. A geo match rule labels every request that it inspects regardless of whether it finds a match\.  
+ To manage requests only by country, you can use this statement by itself and specify the countries that you want to match against in the `CountryCodes` array\. 
+ Otherwise, configure your geo match rule with Count action so that it only labels requests\. Then, add one or more label match rules to run after the geo match rule and configure them to match against the geographic labels and handle the requests as needed\. 
 AWS WAF labels requests using the alpha\-2 country and region codes from the International Organization for Standardization \(ISO\) 3166 standard\. AWS WAF determines the codes using either the IP address in the web request origin or, if you specify it, the address in the geo match `ForwardedIPConfig`\.   
If you use the web request origin, the label formats are `awswaf:clientip:geo:region:<ISO country code>-<ISO region code>` and `awswaf:clientip:geo:country:<ISO country code>`\.  
If you use a forwarded IP address, the label formats are `awswaf:forwardedip:geo:region:<ISO country code>-<ISO region code>` and `awswaf:forwardedip:geo:country:<ISO country code>`\.  
For additional details, see [Geographic match rule statement](https://docs.aws.amazon.com/waf/latest/developerguide/waf-rule-statement-type-geo-match.html) in the [AWS WAF Developer Guide](https://docs.aws.amazon.com/waf/latest/developerguide/waf-chapter.html)\.   
*Required*: No  
*Type*: [GeoMatchStatement](aws-properties-wafv2-rulegroup-geomatchstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`IPSetReferenceStatement`  <a name="cfn-wafv2-rulegroup-statement-ipsetreferencestatement"></a>
A rule statement used to detect web requests coming from particular IP addresses or address ranges\. To use this, create an [AWS::WAFv2::IPSet](aws-resource-wafv2-ipset.md) that specifies the addresses you want to detect, then use the ARN of that set in this statement\.   
Each IP set rule statement references an IP set\. You create and maintain the set independent of your rules\. This allows you to use the single set in multiple rules\. When you update the referenced set, AWS WAF automatically updates all rules that reference it\.  
*Required*: No  
*Type*: [IPSetReferenceStatement](aws-properties-wafv2-rulegroup-ipsetreferencestatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`LabelMatchStatement`  <a name="cfn-wafv2-rulegroup-statement-labelmatchstatement"></a>
A rule statement to match against labels that have been added to the web request by rules that have already run in the web ACL\.   
The label match statement provides the label or namespace string to search for\. The label string can represent a part or all of the fully qualified label name that had been added to the web request\. Fully qualified labels have a prefix, optional namespaces, and label name\. The prefix identifies the rule group or web ACL context of the rule that added the label\. If you do not provide the fully qualified name in your label match string, AWS WAF performs the search for labels that were added in the same context as the label match statement\.   
*Required*: No  
*Type*: [LabelMatchStatement](aws-properties-wafv2-rulegroup-labelmatchstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`NotStatement`  <a name="cfn-wafv2-rulegroup-statement-notstatement"></a>
A logical rule statement used to negate the results of another rule statement\. You provide one `Statement` within the `NotStatement`\.  
*Required*: No  
*Type*: [NotStatement](aws-properties-wafv2-rulegroup-notstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`OrStatement`  <a name="cfn-wafv2-rulegroup-statement-orstatement"></a>
A logical rule statement used to combine other rule statements with OR logic\. You provide more than one `Statement` within the `OrStatement`\.   
*Required*: No  
*Type*: [OrStatement](aws-properties-wafv2-rulegroup-orstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RateBasedStatement`  <a name="cfn-wafv2-rulegroup-statement-ratebasedstatement"></a>
A rate\-based rule counts incoming requests and rate limits requests when they are coming at too fast a rate\. The rule categorizes requests according to your aggregation criteria, collects them into aggregation instances, and counts and rate limits the requests for each instance\.   
You can specify individual aggregation keys, like IP address or HTTP method\. You can also specify aggregation key combinations, like IP address and HTTP method, or HTTP method, query argument, and cookie\.   
Each unique set of values for the aggregation keys that you specify is a separate aggregation instance, with the value from each key contributing to the aggregation instance definition\.   
For example, assume the rule evaluates web requests with the following IP address and HTTP method values:   
+ IP address 10\.1\.1\.1, HTTP method POST
+ IP address 10\.1\.1\.1, HTTP method GET
+ IP address 127\.0\.0\.0, HTTP method POST
+ IP address 10\.1\.1\.1, HTTP method GET
The rule would create different aggregation instances according to your aggregation criteria, for example:   
+ If the aggregation criteria is just the IP address, then each individual address is an aggregation instance, and AWS WAF counts requests separately for each\. The aggregation instances and request counts for our example would be the following: 
  + IP address 10\.1\.1\.1: count 3
  + IP address 127\.0\.0\.0: count 1
+ If the aggregation criteria is HTTP method, then each individual HTTP method is an aggregation instance\. The aggregation instances and request counts for our example would be the following: 
  + HTTP method POST: count 2
  + HTTP method GET: count 2
+ If the aggregation criteria is IP address and HTTP method, then each IP address and each HTTP method would contribute to the combined aggregation instance\. The aggregation instances and request counts for our example would be the following: 
  + IP address 10\.1\.1\.1, HTTP method POST: count 1
  + IP address 10\.1\.1\.1, HTTP method GET: count 2
  + IP address 127\.0\.0\.0, HTTP method POST: count 1
For any n\-tuple of aggregation keys, each unique combination of values for the keys defines a separate aggregation instance, which AWS WAF counts and rate\-limits individually\.   
You can optionally nest another statement inside the rate\-based statement, to narrow the scope of the rule so that it only counts and rate limits requests that match the nested statement\. You can use this nested scope\-down statement in conjunction with your aggregation key specifications or you can just count and rate limit all requests that match the scope\-down statement, without additional aggregation\. When you choose to just manage all requests that match a scope\-down statement, the aggregation instance is singular for the rule\.   
You cannot nest a `RateBasedStatement` inside another statement, for example inside a `NotStatement` or `OrStatement`\. You can define a `RateBasedStatement` inside a web ACL and inside a rule group\.   
For additional information about the options, see [Rate limiting web requests using rate\-based rules](https://docs.aws.amazon.com/waf/latest/developerguide/waf-rate-based-rules.html) in the * AWS WAF Developer Guide*\.   
If you only aggregate on the individual IP address or forwarded IP address, you can retrieve the list of IP addresses that AWS WAF is currently rate limiting for a rule through the API call `GetRateBasedStatementManagedKeys`\. This option is not available for other aggregation configurations\.  
 AWS WAF tracks and manages web requests separately for each instance of a rate\-based rule that you use\. For example, if you provide the same rate\-based rule settings in two web ACLs, each of the two rule statements represents a separate instance of the rate\-based rule and gets its own tracking and management by AWS WAF\. If you define a rate\-based rule inside a rule group, and then use that rule group in multiple places, each use creates a separate instance of the rate\-based rule that gets its own tracking and management by AWS WAF\.   
*Required*: No  
*Type*: [RateBasedStatement](aws-properties-wafv2-rulegroup-ratebasedstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RegexMatchStatement`  <a name="cfn-wafv2-rulegroup-statement-regexmatchstatement"></a>
A rule statement used to search web request components for a match against a single regular expression\.   
*Required*: No  
*Type*: [RegexMatchStatement](aws-properties-wafv2-rulegroup-regexmatchstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`RegexPatternSetReferenceStatement`  <a name="cfn-wafv2-rulegroup-statement-regexpatternsetreferencestatement"></a>
A rule statement used to search web request components for matches with regular expressions\. To use this, create a [AWS::WAFv2::RegexPatternSet](aws-resource-wafv2-regexpatternset.md) that specifies the expressions that you want to detect, then use the ARN of that set in this statement\. A web request matches the pattern set rule statement if the request component matches any of the patterns in the set\.   
Each regex pattern set rule statement references a regex pattern set\. You create and maintain the set independent of your rules\. This allows you to use the single set in multiple rules\. When you update the referenced set, AWS WAF automatically updates all rules that reference it\.  
*Required*: No  
*Type*: [RegexPatternSetReferenceStatement](aws-properties-wafv2-rulegroup-regexpatternsetreferencestatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SizeConstraintStatement`  <a name="cfn-wafv2-rulegroup-statement-sizeconstraintstatement"></a>
A rule statement that compares a number of bytes against the size of a request component, using a comparison operator, such as greater than \(>\) or less than \(<\)\. For example, you can use a size constraint statement to look for query strings that are longer than 100 bytes\.   
If you configure AWS WAF to inspect the request body, AWS WAF inspects only the number of bytes of the body up to the limit for the web ACL\. By default, for regional web ACLs, this limit is 8 KB \(8,192 kilobytes\) and for CloudFront web ACLs, this limit is 16 KB \(16,384 kilobytes\)\. For CloudFront web ACLs, you can increase the limit in the web ACL `AssociationConfig`, for additional fees\. If you know that the request body for your web requests should never exceed the inspection limit, you could use a size constraint statement to block requests that have a larger request body size\.  
If you choose URI for the value of Part of the request to filter on, the slash \(/\) in the URI counts as one character\. For example, the URI `/logo.jpg` is nine characters long\.  
*Required*: No  
*Type*: [SizeConstraintStatement](aws-properties-wafv2-rulegroup-sizeconstraintstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`SqliMatchStatement`  <a name="cfn-wafv2-rulegroup-statement-sqlimatchstatement"></a>
A rule statement that inspects for malicious SQL code\. Attackers insert malicious SQL code into web requests to do things like modify your database or extract data from it\.   
*Required*: No  
*Type*: [SqliMatchStatement](aws-properties-wafv2-rulegroup-sqlimatchstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)

`XssMatchStatement`  <a name="cfn-wafv2-rulegroup-statement-xssmatchstatement"></a>
A rule statement that inspects for cross\-site scripting \(XSS\) attacks\. In XSS attacks, the attacker uses vulnerabilities in a benign website as a vehicle to inject malicious client\-site scripts into other legitimate web browsers\.   
*Required*: No  
*Type*: [XssMatchStatement](aws-properties-wafv2-rulegroup-xssmatchstatement.md)  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)