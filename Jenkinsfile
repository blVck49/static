pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
      steps {
        withAWS(region: 'us-west-2', credentials: 'aws-static', roleAccount: '5115-1688-6450', principalArn: ': arn:aws:iam::511516886450:user/jenkins')
        s3Upload(bucket: 'jenkinsat-bucket', pathStyleAccessEnabled: true, payloadSigningEnabled: true, file: 'index.html')
      }
    }

  }
}