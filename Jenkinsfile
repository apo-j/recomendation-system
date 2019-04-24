pipeline {

    agent any

    options {
        buildDiscarder(logRotator(numToKeepStr: '50'))
        //disableConcurrentBuilds()
        skipDefaultCheckout()
        skipStagesAfterUnstable()
    }

    stages{
        stage('Checkout repo') {
            steps {
                checkout([
                    $class: 'GitSCM',
                    branches: [[name: '*/master']],
                    doGenerateSubmoduleConfigurations: false,
                    submoduleCfg: [],
                    userRemoteConfigs: [[url: 'https://github.com/apo-j/recomendation-system.git']]
                ])

            }
        }
    }
}
