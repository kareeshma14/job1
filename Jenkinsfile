pipeline {
  agent any
  stages {
    stage ('Build&Test') {
      steps {
      	sh 'mvn clean package'
      }
  	}
  	stage ('Image') {
  	  steps {
			sh 'docker build -t kareeshma14/java .'
	  }
  	}
  	stage ('Login') {
      steps {
  	    sh 'docker login -u kareeshma14 -p Chockiee@03'
  	  }
  	}
  	stage ('Push') {
  	  steps {
		sh 'docker push kareeshma14/java'
	}
  	}
  }
}