pipeline {
  agent any
  stages {
    stage('Lint HTML') {
      steps {
        sh 'tidy -q -e *.html'
      }
    }
    stage('Upload to AWS') {
      steps {
        withAWS(credentials:'aws-static',region:'ap-southeast-1') {
            s3Upload(file:'index.html', bucket:'udacity-jenkinspipeline-project', path:'index.html')
        }
      }
    }
  }
}
