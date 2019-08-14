pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
      steps {
        withAWS(credentials:'aws-static',region:'ap-southeast-1') {
            s3Upload(file:'index.html', bucket:'udacity-jenkinspipeline-project', path:'index.html')
        }
      }
    }
  }
}
