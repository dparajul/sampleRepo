node {
    stage ('SCM Checkout') {
        git 'https://github.com/dparajul/addressbook'
    }
    
    stage ('MVN Package') {
        def mvnHome = tool name: 'maven-3.5.4', type: 'maven'
        def mvnCMD = "${mvnHome}/bin/mvn"
        sh "${mvnCMD} clean package"
    }
}
