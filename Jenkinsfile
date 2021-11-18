pipeline {
agent any
stages {
stage ("gitcheckout")
{
steps{checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Ram230197/github.git']]])
}
}
stage ("build using maven")
{
steps{sh 'mvn clean install'
}
}
}
}
