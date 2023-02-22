pipeline{
    agent any
    stages{
        stage('Code Fetch From Github'){
            steps{
                git branch: "Main", url:"https://github.com/Fahim-Faysal/jenkins-practice.git"
            }
        }
        stage('Install the Dependencies'){
            stages{
                sh "npm install"
            }
        }
        stages("Docker Build"){
            stages{
               sh "docker-compose down"
               sh "docker-compose up -d --force-recreate --no-deps --build web"
            }
        }
        
    }
}
