pipeline{
    agent any
    stages{
        stage("A"){
            steps{
                echo "========executing A========"
                sh 'sleep 5'
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
                        sh 'sleep 5'
                    }
                }
                stage("B2"){
                    steps{
                        echo "========executing B2========"
                        sh 'sleep 5'
                    }
                }
            }
        }
        stage("C"){
            steps{
                echo "========executing C========"
                sh 'sleep 5'
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