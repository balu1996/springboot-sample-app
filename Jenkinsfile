pipeline {
    agent any

   // tools {
        // Install the Maven version configured as "M3" and add it to the path.
      //  maven "M3"
    //}

    stages {  

          stage('Checkout SCM') {
            steps {
			script{ 
			    sh 'pwd'
                dir('gitclone'){
			      git branch: '*/master', credentialsId: 'balu', url: 'https://github.com/balu1996/springboot-sample-app.git'  
                }
			    }
				}
				}

          stage('Build') {
            steps {
			 script {
                sh "mvn -Dmaven.test.failure.ignore=true clean package"  
                }
				}
				}
	}
	}
