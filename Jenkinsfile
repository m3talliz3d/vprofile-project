pipeline {
    agent any
    tools {
        maven "MAVEN3"
        jdk "OracleJDK8"
    }

    environment {
        NEXUS-USER = 'admin' 
        NEXUS_PASS = 'admin123'
        RELEASE_REPO = 'vprofile-release'
        SNAP_REPO = 'vprofile-snapshot'
        CENTRAL_REPO = 'vpro-maven-central'
        NEXUS_GRP_REPO = '10.10.10.102'
        NEXUSIP = '8081'
        NEXUSPORT = 'vpro-maven-group'
        NEXUS_LOGIN = 'nexuslogin'
    }
    
    stages {
        stage('Build') {
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}