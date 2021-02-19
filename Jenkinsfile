awsCredentials = [
    default : "aws-credentials"
]

pipeline{
        agent any
        stages{
            stage('Cone Repo'){
                steps{
                    withAWS(credentials: awsCredentials, region: 'ap-southeast-1') {
                    sh "export AWS_DEFAULT_REGION=ap-southeast-1"
                    sh "aws cloudformation create-stack --stack-name myteststack --template-body file://S3Bucket.json --region 'ap-southeast-1'"
                    }
                }
            }
        }
}

