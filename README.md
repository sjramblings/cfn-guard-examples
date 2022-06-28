# cfn-guard-examples

Contains examples for using cfn-guard with AWS Config

## Usage

Within each directory within resource-types run ```make test```

```bash
$ cd resource-types/AWS::ACM::Certificate 
$
$ AWS::ACM::Certificate % make test

cfn-guard test --rules-file `ls *.guard` --test-data `ls *_tests.yaml`

Test Case #1
Name: "NoMatchedResource"
  No Test expectation was set for Rule check_approved_domain_name
  PASS Rules:
    check_resource_type_and_status: Expected = FAIL, Evaluated = FAIL

Test Case #2
Name: "ApprovedDomainName"
  PASS Rules:
    check_resource_type_and_status: Expected = PASS, Evaluated = PASS
    check_approved_domain_name: Expected = PASS, Evaluated = PASS

Test Case #3
Name: "UnApprovedDomainName"
  PASS Rules:
    check_resource_type_and_status: Expected = PASS, Evaluated = PASS
    check_approved_domain_name: Expected = FAIL, Evaluated = FAIL
```

## References

- https://github.com/aws-cloudformation/cloudformation-guard