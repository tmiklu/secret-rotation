pipeline {
  agent any

  parameters {
    string(
      description: '''Sample TASK_JSON Body:
        [{"OP": "getAccount", "ACCOUNT_ID": "123"},
        {"OP": "getAccount", "ACCOUNT_ID": "456"},
        {"OP": "getAccount", "ACCOUNT_ID": "789"}]
      ''',
      name: 'TASK_JSON'
    )
  }

  stages {
    stage ('JSON Validation') {
      steps {
        echo "${params.TASK_JSON}"
        sh 'echo \'${params.TASK_JSON}\' | jq .'
      }
    }
  }
}
