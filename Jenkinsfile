pipeline {
  agent any

  parameters {
    string(
      name: 'TASK_JSON',
      description: '''Sample TASK_JSON Body:
        [{"OP": "getAccount", "ACCOUNT_ID": "123"},
        {"OP": "getAccount", "ACCOUNT_ID": "456"},
        {"OP": "getAccount", "ACCOUNT_ID": "789"}]
      '''
    )
  }

  stages {
    stage ('JSON Validation') {
      steps {
        sh 'python3 main.py ${params.TASK_JSON}'
      }
    }
  }
}
