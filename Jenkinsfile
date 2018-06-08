node {
    stage('Clone Repository') {
        checkout scm
    }

    stage('SonarCube') {
         def scannerHome = tool 'sonarqubeScanner';
         withSonarQubeEnv('sonarqubeServer') {
         sh "${scannerHome}/bin/sonar-scanner -Dsonar.sources=./routes -Dsonar.projectKey=PareKey -Dsonar.host.url=http://10.48.253.181:9000 -Dsonar.login=23307d76147a27fd6e8a282c281fe2802d7171f0"
    }   
    }

}

