pipeline{
    agent any
    tools{
        maven 'maven3'
        jdk 'OracleJdk8'
    }
    enironment{
        NEXUS_USER='admin'
        NEXUS_PASSWORD='nexus'
        SNAP_REPO='slayeli_snapshot_repo'
        RELEASE_REPO='slayeli_releases_repo'
        CENTRAL_REPO ='slayeli_central_repo'
        NEXUS_GROUP_REPO='slayeli_group_repo'
        NEXUS_IP ='192.168.11.13'
        NEXUS_PORT ='8081'
        NEXUS_LOGIN = 'nexus_credentials'
    }
    stages{
        stage('checkout')
        {
            steps{
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}