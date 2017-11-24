properties([pipelineTriggers([githubPush()])])
node('linux') {
    stage('Unit Tests') {
        echo 'Hello Unit Tests!'
        git 'https://github.com/estenrye/java-project.git'
    }
    stage('Build') {
        echo 'Hello Build!'
    }
    stage('Deploy') {
        echo 'Hello Deploy!'
    }
    stage('Report') {
        echo 'Hello Report!'
    }
}