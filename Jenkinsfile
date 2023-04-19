pipeline {

    environment {
        imagename = "jenkins/hello-world"
        registry = "url"
        registryCredential = "credential"
        dockerImage = ''
    }
    agent any

	stages {
		stage("Checkout") {
			steps {
				checkout scm
			}
		}

		stage("Build jar") {
        	steps {
                sh 'chmod +x gradlew'
                sh './gradlew clean build -Dorg.gradle.java.home=/usr/lib/jvm/java-17-openjdk-amd64 -b build.gradle'
        	}
        }

        stage("Build image") {
             steps {
                 script {
                     dockerImage = docker.build( imagename, "-f Dockerfile ." )
                 }
             }
        }

	}
}