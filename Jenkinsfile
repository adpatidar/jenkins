pipeline {
    agent { label 'tests' }
    stages {
        stage('Code pull') {
            steps {
                git branch: 'main', url: 'https://github.com/adpatidar/jenkins'
            }
        }
        stage('build & run') {
            steps {
                sh 'sudo docker-compose down'
                sh'sudo docker-compose build --force-rm --no-cache && sudo docker-compose up -d'
            }    
        }
    }
}
