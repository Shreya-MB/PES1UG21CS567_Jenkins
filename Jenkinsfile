pipeline {
2
agent any
3
stages {
4
11
5
6
11
7
11
8
//
9
11
10
}
11
12
13
14
stage('Clone repository') {
steps {
}
checkout([$class: 'GitSCM',
branches: [[name: '*/main']],
userRemoteConfigs: [[url: 'https://github.com/Jatinsharma159/Jenkins.git']]])
stage('Build') {
steps {
build 'PES2UG19CS159-1'
sh 'g++ main.cpp -o output'
15
}
16
}
17
stage('Test') {
18
steps {
19
sh./output'
20
}
21
}
22
stage('Deploy') {
23
24
steps {
echo 'deploy'
25
}
26
}
27
}
28
post{
29
failure{
30
error 'Pipeline failed'
31
}
32
}
33 }
