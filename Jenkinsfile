pipeline {
    agent {
        label 'docker-agent'
    }
    parameters {
        string(name: 'SCRIPT_NAME', defaultValue: 'run.sh', description: 'script')
    }
    stages {
        stage('Clone Repo') {
            steps {
                git 'https://github.com/rivo22/lab3-scripts.git'
            }
        }
        stage('Run Script') {
            steps {
                sh "chmod +x ${params.SCRIPT_NAME}"
                sh "./${params.SCRIPT_NAME}"
            }
        }
    }
}
