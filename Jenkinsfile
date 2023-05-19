pipeline {
agent any
stages {
stage('Build') {
steps {
echo 'BUILD'
bat 'mvn clean install -DskipTests=true'
}
}
stage('Test') {
steps {
bat 'mvn test'
}
}
stage('Package') {
steps {
bat 'mvn clean package -DskipTests=true'
}
}
stage('Deploy') {
steps {
echo 'DEPLOY'
}
}
}
}