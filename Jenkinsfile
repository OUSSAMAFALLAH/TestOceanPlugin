pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build Complete'
        retry(count: 4) {
          sh '''sssh
'''
        }

      }
    }

    stage('Test Stage') {
      parallel {
        stage('Test 2') {
          steps {
            echo 'Running Test 2'
          }
        }

        stage('Test 1') {
          steps {
            echo 'Runnnnning Test 1'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        input(message: 'Are you sure to Deploy', ok: 'Yes ,Im sure')
        echo 'Deploy Complete'
      }
    }

    stage('Notify for Deploy') {
      steps {
        echo 'New Completed succesuflly'
      }
    }

  }
}