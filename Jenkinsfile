// Powered by Infostretch 

timestamps {

node () {

	stage ('App-IO - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'git-login-VLC', url: 'https://github.com/ValentinLeblanc/FormationTP1.git']]]) 
	}
	stage ('App-IO - Build') {
 			// Maven build step
	withMaven(maven: 'maven') { 
 			if(isUnix()) {
 				sh "mvn clean package " 
			} else { 
 				bat "mvn clean package " 
			} 
 		} 
	}
}
}