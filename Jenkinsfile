pipeline {

agent {
		label {
		
				label 'slave-1'
				customWorkspace '/data/pipeline'
				
		}

}

stages {
			stage ('create-file-1'){
			
			steps {
						sh "rm -rf *"
						sh "touch file1"
			}
			
			}
			
			stage ('create-file-2'){
			
			steps {
					dir ('/data/wsp2'){
						sh "rm -rf *"
						sh "touch file2"
			}
			
			}
			}
			
			
			
			




}

}
