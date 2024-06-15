pipeline {
    agent any
    
    stages {
        stage('Performance Testing') {
            steps {
                script { 
                    bat 'IF EXIST news.jmx (DEL news.jmx)'
                    bat 'jmeter -n -t news.jmx -l news.CSV'                
					bat 'xcopy news.CSV d:\temp'
                }    
            }
        }
    }
}
