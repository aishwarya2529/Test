node {
    stage ('SCM Checkout') {
    git 'https://github.com/aishwarya2529/Test'
    }
    stage ('Compile-Package'){
    def mvnHome = tool name: 'Maven', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
    stage ('Email Notification'){
        mail bcc: '', body: '''Hi, welcome to Jenkins email alerts!
        Thanks''', cc: 'javalove007@gmail.com', from: '', replyTo: '', subject: 'Jenkins Mail', to: 'aishwaryaa415@gmail.com'
    }
    stage ('Slack Notification'){
        slackSend baseUrl: 'https://hooks.slack.com/services/', 
            channel: '#jenkins-pipeline-demo', 
            color: 'good', 
            message: 'Welcome to jenkins, Slack!', 
            tokenCredentialId: 'slack-demo'
    }
}
