pipeline{
agent any
stages{
stage("Build docker image"){
steps{
bat 'docker build -t registration:v1 .'
}
}
stage("push to docker hub"){
steps{
bat 'docker tag registration:v1 jyotshna2884/registration:v1'
bat 'docker push jyotshna2884/registration:v1'
}
}
stage("deploy to kubernetes"){
steps{
bat 'kubectl apply -f F:\devops\deployment.yaml'
bat 'kubectl apply -f F:\devops\service.yaml'
}
}
}
}




