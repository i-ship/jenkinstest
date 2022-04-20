pipeline{
    parameters {
        gitParameter(
            name: "BRANCH",
            type: "PT_TAG", // tags
            sortMode: "DESCENDING_SMART",
            defaultValue: "v1.0.1"
        )
    }
    agent{
        label "master"
    }
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
