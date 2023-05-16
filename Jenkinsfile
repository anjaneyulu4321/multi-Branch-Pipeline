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
    deploy adapters: [tomcat9(credentialsId: 'e070de16-f8b9-4545-bfbc-bbfed919de03', path: '', url: 'http://172.31.18.27:8080')], contextPath: 'testsapp', war: '**/*.war'
    }       
}
