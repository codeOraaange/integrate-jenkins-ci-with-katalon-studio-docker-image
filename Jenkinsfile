pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                dir('/integrate-jenkins-ci-with-katalon-studio-docker-image') {
                    bat 'docker run -t --rm -v "%cd%":/tmp/project katalonstudio/katalon katalonc.sh -projectPath=/tmp/project -browserType="Chrome" -retry=0 -statusDelay=15 -testSuitePath="Test Suites/TS_RegressionTest" -apiKey=3b3a9a71-d3d2-4e76-bf37-8e57f12b6987'
                }    
            }
        }
    }
}
