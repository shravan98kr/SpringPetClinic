pipeline
{
    agent
    {
        label 'master'
    }
    tools{maven 'M3'}
    stages
    {
        stage('Checkout')
        {
            steps{
            git branch: 'main', url: 'https://github.com/shravan98kr/SpringPetClinic.git'
            }
        }
        stage('Build'){
            steps{
                sh 'mvn compile'
            }
        }
        stage('test')
        {
            steps{
            sh 'mvn test'
        
            }
            }
        
        stage('Pacakage')
        {
            steps{
            sh 'mvn package'
            }
            
        }
        stage('Deploy')
        {
         steps{
             sh 'java -jar /var/lib/jenkins/workspace/PetClinicDeclarativePipeline/target/*.jar'
         }   
        }
    }
}
