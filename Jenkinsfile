pipeline {
    agent any
    // parameters {
    //     string(name:'TOPIC_NAME', defaultValue:'Devops', description:'Topics to learn')
    //     string(name:'TARGET', defaultValue:'Dream Job', description:'Target goal')
    // }
    parameters {
        string(name: 'DEPLOY_ENV', defaultValue: 'staging', description: '')
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    stages {
        stage('Clone the repo') {
            steps {
                checkout scm
                sh 'ls *'
            }
        }
        stage('Example') {
            steps {
                echo "Hello ${params.PERSON}"

                echo "Biography: ${params.BIOGRAPHY}"

                echo "Toggle: ${params.TOGGLE}"

                echo "Choice: ${params.CHOICE}"

                echo "Password: ${params.PASSWORD}"
            }
        }
        stage('Change permission & run the script file') {
            steps {
                sh 'chmod +x sayhello.sh'
                sh './sayhello.sh test name'
            }
        }
    }
}
