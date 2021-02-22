pipeline{
	agent any
	stages{
		stage ('Build Application'){
			steps{
				bat 'mvn clean install'
			}
		}
		
		stage ('MUnit Testing Application'){
			steps{
				bat 'mvn test'
			}
		}
		
		stage ('Deploy Application to Mulesoft CloudHub'){
			steps{
				bat 'mvn package deploy -DmuleDeploy'
			}
		}
		
		stage ('Perform Regression Testing'){
			steps{
				bat 'C:\\Users\\premc\\AppData\\Roaming\\npm\\newman run D:\\TrainingWorkspace\\Newman\\WorldTimezone.postman_collection.json --disable-unicode'
			}
		}
	}
}