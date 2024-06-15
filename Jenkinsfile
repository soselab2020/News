pipeline {
    agent any
    
    stages {
        stage('Performance Testing') {
            steps {
                script { 
                    bat 'IF EXIST news.CSV (DEL news.CSV)'
                    bat 'jmeter -n -t news.jmx -l news.CSV'                
					bat 'xcopy news.CSV d:\\temp'
                }    
            }
        }
    }
}
