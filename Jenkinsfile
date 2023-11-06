pipeline {

    agent any

    environment { 
        CC = 'clang'
    }

    stages {
        stage('Checkout') {
            steps {
                echo 'Begin checkout...'
                // 在此处添加构建任务的命令或脚本
                git clone https://github.com/arthas3014/yht-test2.git /tmp
            }
        }
        stage('Build') {
            // environment { 
            //     AN_ACCESS_KEY = 'abc' 
            // }
            steps {
                echo 'Begin Build...'
                // 在此处添加构建任务的命令或脚本
                cd /tmp/yht-test2
                mvn package
            }
        }

        stage('Deploy') {
            steps {
                echo 'Begin Deploy...'
                // 在此处添加构建任务的命令或脚本
                java -jar '/tmp/yht-test2/target/my-project-1.0.0.jar'
            }
        }
    }



    post { 
        always { 
            echo 'I will always say Hello again!'
        }
    }
}




// pipeline {
//     agent any
    
//     stages {
//         stage('Build') {
//             steps {
//                 echo 'Building...'
//                 // 在此处添加构建任务的命令或脚本
//             }
//         }
        
//         stage('Test') {
//             steps {
//                 echo 'Testing...'
//                 // 在此处添加运行测试的命令或脚本
//             }
//         }
        
//         stage('Deploy') {
//             steps {
//                 echo 'Deploying...'
//                 // 在此处添加部署到目标环境的命令或脚本
//             }
//         }
//     }
// }

// pipeline {
//     agent any
//     stages {
//         stage('build') {
//             steps {
//                 echo 'hello word'
//             }
//         }
//     }
// }


// pipeline {
//     agent any
    
//     tools {
//         // 配置 JDK 工具
//         jdk 'JDK17'
//         // 配置 Maven 工具
//         maven 'Maven'
//     }
    
//     stages {
//         stage('Build') {
//             steps {
//                 // 使用 Maven 构建项目
//                 sh 'mvn clean package'
//             }
//         }
        
//         stage('Test') {
//             steps {
//                 // 使用 Maven 运行测试
//                 sh 'mvn test'
//             }
//         }
        
//         stage('Deploy') {
//             steps {
//                 // 部署到服务器的步骤
//                 // ...
//             }
//         }
//     }
// }
