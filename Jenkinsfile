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
                        script {
        					component.each{ entry ->
        						stage ("${entry.key} Build"){
        							if(entry.value){
        								var = entry.key
        								sh "docker-compose build ${var.toLowerCase()}"
        							}
        						}
        			        }
        		        }
        	        }
        }
	}
}