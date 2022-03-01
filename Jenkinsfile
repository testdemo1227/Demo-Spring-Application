node{
    
    stage('Check Maven version'){
        bat 'mvn -v'
    }
    stage('Git Cloning'){
        git credentialsId: 'bbaecc57-f68c-41d7-b0a4-e9a7696d514a', url: 'https://github.com/testdemo1227/Demo-Spring-Application.git'
    }
    stage('building stage'){
        bat 'mvn clean test'
    }
    stage('cucumber report generate'){
        cucumber failedFeaturesNumber: -1, failedScenariosNumber: -1, failedstepsNumber: -1, fileIncludePattern:'**/*.json', pendingStepsNumber: -1, skippedStepsNumber: -1, sortingMethod:'ALPHABETICAL', undefinedStepsNumber: -1
    }
}
