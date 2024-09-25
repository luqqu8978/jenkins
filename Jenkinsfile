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
