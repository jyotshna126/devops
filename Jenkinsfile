pipeline{
agent any
stages{
stage("Clone repository"){
steps{
git url:'https://github.com/jyotshna126/devops.git',branch:'master'
}
}
stage("Build docker images"){
steps{
bat 'docker build -t registration:v1 .'
}
}
stage("run docker image"){
steps{
bat 'docker rm -f registration-container || exit 0'
bat 'docker run -d -p 5000:5000 --name registration:container registration:v1'
}
}
}
}


