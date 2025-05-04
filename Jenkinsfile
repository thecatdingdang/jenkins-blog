pipeline {
    agent any
    // 避免 npm install 报权限问题
    environment {
        PATH="/Users/r/.pyenv/shims:/Users/r/.gvm/bin:/opt/homebrew/opt/openjdk/bin:/opt/homebrew/bin:/opt/homebrew/sbin:/usr/local/bin:/System/Cryptexes/App/usr/bin:/usr/bin:/bin:/usr/sbin:/sbin:/var/run/com.apple.security.cryptexd/codex.system/bootstrap/usr/local/bin:/var/run/com.apple.security.cryptexd/codex.system/bootstrap/usr/bin:/var/run/com.apple.security.cryptexd/codex.system/bootstrap/usr/appleinternal/bin"
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
