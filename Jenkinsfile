properties([pipelineTriggers([githubPush()])])
node('linux') {
    stage('Unit Tests') {
        steps {
            echo 'Hello Unit Tests'
        }
    },
    stage('Build') {
        steps {
            echo 'Hello Build'
        }
    },
    stage('Deploy') {
        steps {
            echo 'Hello Deploy'
        }
    },
    stage('Report') {
        steps {
            echo 'Hello Report!'
        }
    }
}
}