pipeline{
    agent any
    environment {
        name = "Deepak"
    }

    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        booleanParam(name: 'ismale', defaultValue: true, description: 'Toggle this value')
        }
    
    
    stages{
        stage("A"){
            steps{
                
                echo "${PERSON}}"
            }
        }
        stage("B"){
            environment{
            names = "Sharma"
         }
            input {
                message "Should we continue?"
                ok "Yes, we should."
                submitter "alice,bob"
            }
            steps{
                echo "========executing B========"
                
            }
        }
        stage("c"){
            steps{
                sh "pwd"
                sh "date"
            }
        }
    }

}
