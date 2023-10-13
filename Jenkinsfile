pipeline {
    agent any

    stages{
        stage('deploy to S3'){
            steps{
               sh 'aws s3 cp public s3://zoey2023 --recursive'
               sh 'aws s3api put-bucket-policy --bucket zoey2023 --policy file://policy.json'
               sh 'aws s3 website s3://zoey2023/ --index-document index.html --error-document error.html'
             
            }
        }
    }
    
}
