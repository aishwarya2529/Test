node {
    stage ('SCM Checkout') {
    git 'https://github.com/aishwarya2529/Test'
    }
    stage ('Compile-Package'){
    def mvnHome = 'tool name: '', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
}
