pipeline{
    agent any
    stages{
        stage('Code Fetch From Github'){
            steps{
                git branch: "main", url:"https://github.com/Fahim-Faysal/jenkins-practice.git"
            }
        }
        stage('Install the Dependencies'){
            steps{
                sh "npm install"
            }
        }
        stage("Docker Build"){
            steps{
               sh "docker-compose down"
               sh "docker-compose up -d --force-recreate --no-deps --build web"
            }
        }
        
    }
}
