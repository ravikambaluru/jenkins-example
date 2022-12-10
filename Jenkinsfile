pipeline{
    agent none
    tools{
       nodejs "node"
    }
    stages{
        stage("Build"){
            steps{
                echo "Build stage started ........."
                sh "npm i"
                echo "Node modules installation completed ........."
            }
        }
        stage("Test"){
            steps{
                echo "Dummy testing section completed ........."
            }
        }
        stage("Deploy"){
            steps{
                echo "Deploy stage started ........."
                sh "pm2 start --name 'server' bin/www"
                echo "pm2 process started ........."
                sh "pm2 logs 0"
            }
        }
    }
    post{
        success{
            echo "Pipeline executed sucessfully"
        }
        failure{
            echo "Pipeline executed sucessfully"
        }
    }
}