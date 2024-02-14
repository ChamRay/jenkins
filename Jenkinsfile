//写流水线的脚本


pipeline {
    //  全部的CICD流程都在这里定义

    // 在集群模式下任何一个节点可用就可以执行
    agent any
    // 定义一些环境信息
    environment {
        hello = "123456"
        world = "1234555"
    }
    // 定义流水线的加工流程
    stages {
        // 流水线的所有流程
        stage('Build') {
            // 定义流程中的步骤
            steps {
                // sh 'mvn clean package'
                echo "编译打包代码"
                echo "$hello"
            }
        }

        stage('Test') {
            steps {
                // sh 'mvn test'
                echo "执行测试流程"
                echo  "${world}"
            }
        }

        stage('Deploy') {
            steps {
                // sh 'mvn deploy'
                echo "部署到服务器"
                echo "printenv"
            }
        }
    }

}