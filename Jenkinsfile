pipeline {
    agent any

    stages {
        stage('BUILD') {
            steps {
                echo 'BUILD STAGE SUCCESSFULL'
            }
        }
    
   
        stage('TEST') {
            steps {
                echo 'TEST IS SUCCESSFULL'
            }
        }
    
        stage('DEPLOY') {
            steps {
                echo 'DEPLOY IS SUCCESSFULL'
            }
        }
        
        
    }
    post{
            always{
                build job: 'test', parameters: [string(name: 'Username', value: 'postactionUser')]
            }
            failure{
                build job: 'test', parameters: [string(name: 'Username', value: 'failactionUser')]
            }
            
        }
}
