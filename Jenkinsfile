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
                sh 'sudo usermod -aG docker jenkins'
                sh 'sudo chown jenkins:jenkins /var/run/docker.sock'
                sh 'sh docker.sh'
            }
        }
    }

}
