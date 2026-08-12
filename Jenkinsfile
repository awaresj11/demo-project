pipeline{
    agent any
    
    stages{
        stage("Code Clone"){
            steps{
                echo "Code Clone Stage"
                git url: "https://github.com/Un/node-todo-cicd.git", branch: "master"
            }
        }
        stage("Code Build"){
            steps{
                echo "Code Build Stage"
                sh "docker build -t node-app ."
            }
        }
        stage("Code Testing"){
            steps{
                echo "Testing done..!"
                
            }
        }
       
        stage("Deploy"){
            steps{
                sh "docker compose down && docker compose up -d --build"
            }
        }
    }
}
