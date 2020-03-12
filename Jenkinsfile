pipeline {
	agent any
	environment { EXECUTE = true 
		    }
		stages {
			stage('First') {
				steps {
					sh 'echo "Step One"'
				      }
			               }
			stage('Second') {
				when { 
					expression {EXECUTE} 
				     }
				steps {
					sh 'echo "Updating Second Stage"'
                                      }
                                        }
                        stage('Third') {
				when {
					expression {EXECUTE == false}
				     }
                                steps {
                                        sh 'echo "Step Three"'
                                      }
                                       }
                       }
         }
