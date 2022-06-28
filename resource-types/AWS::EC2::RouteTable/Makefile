GUARD_FILE=`ls *.guard`
TEST_FILE=`ls *_tests.yaml`

test:
	cfn-guard test --rules-file ${GUARD_FILE} --test-data ${TEST_FILE}

testverbose:
	cfn-guard test --rules-file ${GUARD_FILE} --test-data ${TEST_FILE} --verbose
