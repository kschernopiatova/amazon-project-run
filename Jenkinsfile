pipeline {
    agent any
    stages {
        stage("Pull Latest Image"){
        	steps{
        		sh "docker pull kchernopiatova/amazon-project"
        	}
        }
        stage("Start Grid"){
        	steps{
        		sh "docker-compose up -d hub chrome firefox chrome-recording"
        	}
        }
        stage("Run Test"){
        	steps{
        		sh "docker-compose up my_project"
        	}
        }
		stage("Stop Grid"){
        	steps{
        		sh "docker-compose down"
        	}
        }
    }
}