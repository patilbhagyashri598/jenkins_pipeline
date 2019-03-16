pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'Localmaven') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'Localmaven') {
                    sh 'mvn test'
                }
            }
        }

        stage ('Packaging Stage') {

            steps {
                withMaven(maven : 'Localmaven') {
                    sh 'mvn package'
                }
            }
        }

        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'Localmaven') {
                    sh 'mvn install'
                }
            }
        }
    }
}
