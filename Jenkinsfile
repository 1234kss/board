pipeline 
{
    agent any
    tools {
        maven 'M3' 
    }
    stages {
    	stage('parameter check')
    	{
    		steps
    		{
    			 echo "Current workspace : ${workspace}"
    			 sh 'mvn -version'
    		}
    	}
    	stage('clone project')
    	{
    	     steps {
    	        git branch: 'master',
                credentialsId: '1234kss_git_board1',
                url: 'https://github.com/1234kss/board.git'

    	     }
    	}
        
}
}
