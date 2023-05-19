pipeline {
agent any
tools {
maven 'Maven'
}
stages {
stage('Initialize') {
steps {
sh '''
echo "PATH = ${PATH}"
echo "JAVA_HOME" = ${JAVA_HOME}
echo "MAVEN_HOME = ${MAVEN_HOME}"
'''
}
}
stage('Build') {
steps {
echo 'BUILD'
sh 'mvn clean install'
}
}
stage('Test') {
steps {
sh 'mvn test'
}
}
stage('Package') {
steps {
sh 'mvn clean package'
}
}
stage('Deploy') {
steps {
echo 'DEPLOY'
}
}
}
}