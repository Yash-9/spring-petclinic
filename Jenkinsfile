pipeline{
     agent{
     label 'master'
     }
	 tools{
     maven 'mymaven'
     jdk 'myjava'
     }
	 stages{
	   stage('checkout the code'){
	       steps{
		     git branch: 'master' , url: 'https://github.com/Yash-9/spring-petclinic.git'
		   }
	   
	   }
	    stage('Code Compile'){
	        steps{
			 sh"""
			 mvn compile
			 """
			}
	   }
	   stage('JUNIT Test'){
	        steps{
			 sh"""
			 mvn test
			 """
			}
	   }
	     stage('Packaging'){
	        steps{
			 sh"""
			 mvn package
			 """
			}
	   }  
	   
	 }

} 
