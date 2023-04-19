pipeline {

    agent any

	stages {
		stage("Checkout") {
			steps {
				checkout scm
			}
		}

		stage("Build") {
        	steps {
                sh 'chmod +x gradlew'
                sh './gradlew clean build -Dorg.gradle.java.home=/usr/lib/jvm/openjdk-17 -b build.gradle'
        	}
        }
	}
}