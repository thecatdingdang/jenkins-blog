pipeline {
    agent any
    // 避免 npm install 报权限问题
    environment {
        PATH="/bin:/sbin:/usr/bin:/usr/sbin:/usr/local/bin"
    }
    stages {
        stage('build') {
            steps {
                sh 'node -v'
                sh 'npm -v'
                dir ("/Users/r/my-blog") {
                   sh 'git pull'
                   sh 'npm install'
                   sh 'hexo g'
                }
            }
        }
    }
}
