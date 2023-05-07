node {
 stage('Checkout') {
 checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/saipolana/resume_deployment_in-_tomcat.git']])
}
}
stage('Deploy approval'){
 input "Do you want to proceed for production deployment?"
}
node{
 stage('Deploy') {
deploy adapters: [tomcat9(credentialsId: 'b9e12e24-4afb-4b83-a22a-3097e12a0290', path: '', url: 'http://localhost:9090/')], contextPath: 'sai_polana_resume4', war: 'myresume.war'}
}
