pipeline{
    
    agent any

    tools{

        maven 'Maven'
    }
    stages{
        stage("Build"){
            steps{
                
                sh "mvn clean"
                sh "mvn package"
            }
        }

        stage("Test"){
            steps{
                
                sh "mvn test"
            }
        }
        stage("run"){
            steps{
                echo "========executing A========"
            }
        }
        stage("Deploy"){
            steps{
                echo "Deploy"
            }
        }
    }
    post{
        always{
            echo "========always========"
        }
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "Ein Fehler ist aufgetreten"
        }
    }
}