GUARD_FILE=`ls *.guard`
TEST_FILE=`ls *_tests.yaml`

test:
	cfn-guard test --rules-file ${GUARD_FILE} --test-data ${TEST_FILE}

test_verbose:
	cfn-guard test --rules-file ${GUARD_FILE} --test-data ${TEST_FILE} --verbose

test_clause:
	cfn-guard test --rules-file ${GUARD_FILE} --test-data ${TEST_FILE} --show-clause-failures
