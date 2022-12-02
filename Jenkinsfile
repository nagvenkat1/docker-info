pipeline {
    agent  { label 'DOCKER' } 
    stages {
        stage('vcs') {
            steps {
                git url: "https://github.com/nagvenkat1/docker-info.git",
                    branch: "main"
            }
        }
        stage('docker') {
            steps {
                sh 'sh docker.sh'
            }
        }
    }

}
