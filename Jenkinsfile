properties([pipelineTriggers([githubPush()])])
node('linux') {
    stage('Unit Tests') {
        git 'https://github.com/estenrye/java-project.git'
        sh 'ant -f test.xml -v'
        junit 'reports/result.xml'
    }
    stage('Build') {
        sh 'ant -f build.xml -v'
    }
    stage('Deploy') {
        sh 'ls /workspace/java-pipeline/dist'
        sh 'aws s3 cp /workspace/java-pipeline/dist/rectangle-*.jar s3://jenkins-stack-s3bucket-6hp6znouxyxn'
    }
    stage('Report') {
        sh 'aws cloudformation describe-stack-resources --region us-east-1 --stack-name jenkins'
        cleanWs()
    }
}