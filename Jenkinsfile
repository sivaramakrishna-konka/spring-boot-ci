pipeline{
    agent{
        label 'siva'
    }
    environment {
        JAVA_HOME = "/usr/lib/jvm/java-1.8.0-amazon-corretto.x86_64"
        PATH = "${JAVA_HOME}/bin:${env.PATH}"
    }
    stages{
        stage('Build'){
            steps{
               sh 'mvn clean package'
            }
        }
    }
}