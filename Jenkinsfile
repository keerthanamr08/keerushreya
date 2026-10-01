pipeline{
agent any
environment{
  DOCKER_IMAGE="keerthanamr08/keerthana-image"
}
stages{
stage('Clone Repository'){
steps{
git 'https://github.com/keerthanamr08/keerushreya.git'
}
}
stage('Build Docker Image'){
steps{
script{
dpcker.build("${DOCKER_IMAGE}:v1")
}
}
}
stage('Login to Docker Hub'){
steps{
withCredentails
