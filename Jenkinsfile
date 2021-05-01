pipeline {	 
	agent any	 
    	stages {     	 
    	stage("Compile") {          	 
            	steps {               	 
                	sh "mvn compile"          	 
            	}     	 
        	}     	 
    	stage("Unit test") {          	 
        	steps {               	 
                	sh "mvn test"          	 
            	}     	 
        	}	 
    	stage("Deploy to Tomcat") {          	 
        	steps {               	 
                	deploy adapters: [tomcat8(credentialsId: '53c4e603-9b58-4b58-8c11-c1b21d86e77e', path: '', url: 'http://localhost:8888/')], contextPath: 'devops', war: '**/*.war'
            	}     	 
        	}	 
    	}
}