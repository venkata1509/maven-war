// Powered by Infostretch 

timestamps {

node () {

	stage ('Maven-freestyle - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '900caf5f-a681-49c4-ad6b-a026f64612bf', url: 'https://github.com/ganesh8338/maven-war.git']]]) 
	}
	stage ('Maven-freestyle - Build') {
 			// Maven build step
	withMaven(maven: 'Maven') { 
 			if(isUnix()) {
 				sh "mvn install tomcat7:deploy " 
			} else { 
 				bat "mvn install tomcat7:deploy " 
			} 
 		} 
	}
}
}