pipeline{
    agent any
    stages{
        stage('Clone repo')
        {
            steps{
                git branch:'main',url:'https://github.com/luqqu8978/jenkins.git'
            }
        }
        
    
        stage('Install dependencies'){
            steps{
                sh 'npm i'
            }
        }
        stage('Testing my application')
        {
            steps{
                sh 'npm test'
            }
        }

        stage('zip the project'){
            input{
                message 'do you really want to deploy?'
                ok "click on ok"
                submitter 'Asif'
            }
            steps{
                sh 'zip -r JenkinsTest.zip ../JenkinsTest/'
                sh 'cp JenkinsTest.zip /home/asifshahapurkar/Videos/JenkinTest/jenkins'
            }
        }

        stage('Start the application'){
            input{
                message 'do you really want to start?'
                ok "click on ok"
                submitter 'Asif'
            }
            steps{
                sh 'npm start'
            }
        }

        
    }
}
