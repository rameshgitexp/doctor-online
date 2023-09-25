pipeline{
    agent any
    parameters {
      choice choices: ['dev', 'test', 'prod'], description: 'Choose the environment to deploy', name: 'envName'
    }
    stages{
        stage("Maven Build"){
            steps{
               sh "mvn clean package" 
            }
        }
        stage("Deploy To Dev"){
            when {
                params.envName == "dev"
            }
            steps{
                echo params.envName
                echo "Deploy to dev"
            }
        }
        stage("Deploy To Test"){
            steps{
                echo "Deploy to test"
            }
        }
        stage("Deploy To Prod"){
            steps{
                echo "Deploy to prod"
            }
        }
    }
}
