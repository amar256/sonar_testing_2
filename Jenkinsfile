node{
    def mvnHome
	def workspace
	           stage('Preparation') {
       git 'https://github.com/amar5607/sonar_testing_2.git'
	         mvnHome = tool 'maven_new'
			 scannerhome = tool 'sonar_qube'
	                                 }
           stage('SonarQube Analysis'){
		   sh """echo ${workspace}"""
                                    withSonarQubeEnv('sonar_qube') { 
                                     sh """
				     ${scannerhome}/bin/sonar-scanner \
				     -Dsonar.projectKey=jenkins \
				     -Dsonar.sources=. \
				     """
                                    }
									}
}
