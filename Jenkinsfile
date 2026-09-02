pipeline {
 agent any
 stages {
 stage('Build Docker Image') {
 steps {
 dir('Jenkins') {
 bat 'docker build -t flaskapp .'
 }
 }
 }
 stage('Run Dev Container') {
 steps {
 dir('Jenkins') {
 bat 'docker run -d --name dev-container -p 5000:5000 flaskapp'
 }
 }
 }
 stage('Run Test Container') {
 steps {
 dir('Jenkins') {
 bat 'docker run -d --name test-container -p 5001:5000 flaskapp'
 }
 }
 }
 }
}
