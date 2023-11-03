pipeline {

    agent any

    environment { 
        CC = 'clang'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                // 在此处添加构建任务的命令或脚本
            }
        }
        stage('test') {
            environment { 
                AN_ACCESS_KEY = 'abc' 
            }
            steps {
                sh 'printenv'
                // 在此处添加构建任务的命令或脚本
            }
        }
    }

    post { 
        always { 
            echo 'I will always say Hello again!'
        }
    }
}





