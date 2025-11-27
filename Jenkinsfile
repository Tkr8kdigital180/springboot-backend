pipeline{
    
    agent any

    tools{

        maven 'Maven'
    }
    stages{
        stage("Build"){
            steps{
                
                sh "mvn clean package"
            }
        }

        stage("Test"){
            steps{
                
                sh "mvn test"
            }
        }
        stage("run"){
            steps{
                 sh"java -jar target/springboot-backend-0.0.1-SNAPSHOT.jar"
            }
        }
        stage("Deploy"){
            steps{
                echo "Deploy"
            }
        }
    }
    post{
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "Ein Fehler ist aufgetreten"
        }
    }
}