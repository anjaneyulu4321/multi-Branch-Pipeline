node()
{
    stage('continous Download') 
    {
        git 'https://github.com/intelliqittrainings/maven.git'
    }
    stage('continous BuilD') 
    {
        sh 'mvn package'
    }
    stage('Continous Deploy')
    {
        deploy adapters: [tomcat9(credentialsId: '4376a190-1bc7-4695-9de4-be7a3e8633f0', path: '', url: 'http://172.31.18.27:8080')], contextPath: 'test', war: '**/*.war'
    }       
}
