properties([pipelineTriggers([githubPush()])])
node('linux') {
    stage('Unit Tests') {
        git 'https://github.com/estenrye/java-project.git'
        sh 'ant -f test.xml -v'
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