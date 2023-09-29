pipeline {
    agent any
    parameters {
        string(name:'TOPIC_NAME', defaultValue:'Devops', description:'Topics to learn')
        string(name:'TARGET', defaultValue:'Dream Job', description:'Target goal')
    }
    stages {
        stage('Clone the repo') {
            steps {
                checkout scm
                sh 'ls *'
            }
        }
        stage('Change permission & run the script file') {
            steps {
                sh 'chmod +x sayhello.sh'
                sh 'sayhello.sh ${TOPIC_NAME} ${TARGET}'
            }
        }
    }
}
