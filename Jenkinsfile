pipeline {
    agent {
        label 'Node-1'
    }

    tools {
        jdk 'jdk8'
    }

    triggers {
        githubPush()
    }

    stages {
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
    }
}
