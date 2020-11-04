pipeline{
    agent{
        label "prod-server"
    }
    stages{
        stage("A"){
            steps{
                echo "========executing Aw========"
                git branch: 'develop', url: 'https://github.com/IonMind/Devops-Project.git'
            }
            post{
                always{
                    echo "========always========"
                }
                success{
                    echo "========A executed successfully========"
                }
                failure{
                    echo "========A execution failed========"
                }
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
            echo "========pipeline execution failed========"
        }
    }
}