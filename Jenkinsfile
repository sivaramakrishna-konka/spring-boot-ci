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
        stage('Jacaco Reports'){
            steps{
               sh 'mvn jacoco:report'
            }
        }
        stage('SCA:Owasp Dependency Check'){
            steps{
                sh 'mvn org.owasp:dependency-check-maven:check'
            }
        }
    }
}