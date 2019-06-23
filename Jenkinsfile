pipeline {
    agent { dockerfile true }
    stages {
        stage("Build") {
            steps {
                sh "bundle install"
            }
        }
        stage("Tests") {
            steps {
                sh "bundler exec cucumber -p ci -t@minha_busca"
            }
        }
    }
}