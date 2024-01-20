pipeline {
    agent any
    stages {
        stage('git repo & clean') {
            steps {
             //  bat "rmdir  /s /q TicketBookingServiceJunitTesting"
                git "https://github.com/pagarwal1212/TicketBookingServiceJunitTesting.git"
               // sh "mvn clean -f TicketBookingService"
            }
        }
        stage('install') {
            steps {
                sh "sudo apt install maven -y -f TicketBookingService"
            }
        }
        stage('test') {
            steps {
                sh "mvn test -f TicketBookingService"
            }
        }
        stage('package') {
            steps {
                sh "mvn package -f TicketBookingService"
            }
        }
    }
}
