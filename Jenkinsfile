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
        
    stage('Build') {
        sh "'${mvnHome}/bin/mvn' -P ${activeProfile} -Dmaven.test.skip=true clean install"
    }
    stage('Archive') {
        archive '**/target/*.jar'
    }
    stage('Deploy') {
        echo "Deploy is not yet implemented"
    }
        
}
}
