pipeline{
    agent any
    stages{
        stage("A"){
            steps{
                echo "========executing A========"
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
        stage("B - Parallel"){
            parallel{
                stage("B1"){
                    steps{
                        echo "========executing B1========"
                    }
                }
                stage("B2"){
                    steps{
                        echo "========executing B2========"
                    }
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