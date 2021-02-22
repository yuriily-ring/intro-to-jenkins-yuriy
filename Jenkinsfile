pipeline {
    agent { docker { image 'maven:3.3.3' } }
    stages {
            stage('Initialize')
    {
        def dockerHome = tool 'MyDocker'
        def mavenHome  = tool 'MyMaven'
        env.PATH = "${dockerHome}/bin:${mavenHome}/bin:${env.PATH}"
    }
        stage('build') {
            steps {
                sh 'mvn --version'
            }
        }
    }
}
