pipeline{
    agent any
    
    stages{
        stage("Git Checkout"){
            steps{
               git credentialsId: 'muraliweb', url: 'https://github.com/muralibadagala/muraliweb.git'
            }
        }
        stage("Maven Build"){
            steps{
                sh "mvn clean install"
                sh "mv target/*.war target/myweb.war"
            }
        }      
    }
}
