#!groovy

// https://github.com/feedhenry/fh-pipeline-library
@Library('fh-pipeline-library') _

stage('Trust') {
    enforceTrustedApproval('aerogear')
}

node ("ocp-slave") { 
    stage('Cleanup') {
        deleteDir()
    }
    stage('Cloning the repo') {
        checkout scm
    }

    stage('Run APB test') {
        def test_output = sh (
            script: 'apb test --registry-route docker-registry.default.svc:5000',
            returnStdout: true
        ).trim()
        
        if (test_output.contains("Pod phase Failed")) {
            error("APB test failed.")
        }
    }
}