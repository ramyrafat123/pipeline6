pipeline{
    agent any

    stages{
        stage('Compile Stage'){
            steps {
                withMaven(maven : 'maven-3'){
                    def mvnHome = tool name: 'maven-3' , type:'maven'
                    def mvnCMD ="${mvnHome}/bin/mvn"
                    sh "${mvnCMD} clean compile"
                }

            }
        }
        stage('Testing Stage'){
            steps{
                withMaven(maven : 'maven-3'){
                    def mvnHome = tool name: 'maven-3' , type:'maven'
                    def mvnCMD ="${mvnHome}/bin/mvn"
                    sh "${mvnCMD} test"
                }
            }
        }
        stage('Deploy Stage'){
            steps{
                withMaven(maven : 'maven-3'){
                    def mvnHome = tool name: 'maven-3' , type:'maven'
                    def mvnCMD ="${mvnHome}/bin/mvn"
                    sh "${mvnCMD} deploy"
                }
            }
        }
    }
}

# my name is ramy