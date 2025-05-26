pipeline{
    agent any
    environment{
       def XYZ='Hello ITI'
        
    }
    stages{
        stage("build Docker image"){
            steps{
                sh ''' echo "${XYZ}" '''
                sh "docker build -t mariam191/python_app:v${BUILD_NUMBER} ."
            }
        }
        stage("Push Docker image"){
            steps{
                sh "docker push mariam191/python_app:v${BUILD_NUMBER}"
            }
        }
    }
}
