pipeline {
  agent any

  parameters {
    string(
      name: 'TASK_JSON',
      description: '''
      Sample TASK_JSON Body:\n
        [
          {"OP": "getAccount", "ACCOUNT_ID": "123"},
          {"OP": "getAccount", "ACCOUNT_ID": "456"},
          {"OP": "getAccount", "ACCOUNT_ID": "789"},
          {"OP": "getAccount", "ACCOUNT_ID": "331"}
        ]
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
