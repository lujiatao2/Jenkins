pipeline {
    agent any
    stages {
        stage('构建') {
            steps {
                sh 'echo "进行构建！"'
            }
        }
        stage('单元测试') {
            when {
                branch 'dev'
            }
            steps {
                sh 'echo "进行单元测试！"'
            }
        }
        stage('集成和系统测试') {
            when {
                branch 'test'
            }
            steps {
                sh 'echo "进行集成和系统测试！"'
            }
        }
        stage('验收测试') {
            when {
                branch 'master'
            }
            steps {
                sh 'echo "进行验收测试！"'
            }
        }
    }
}
