pipeline {
	agent any

	stages {
		stage('build') {
			steps {
				sh 'ant -f build.xml -v'
			}
		}
	}

	post {
		always {
			archiveArtifacts 'dist/*.jar', fingerprint:true
		}
	}
}

