pipeline {
agent any
stages {
stage ("gitcheckout")
{
step{checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Ram230197/github.git']]])
}
}
stage ("build using maven")
{
step{sh 'mvn clean install'
}
}
}
}
