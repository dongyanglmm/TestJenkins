node{
    stage('get clone'){
        //check CODE
       git credentialsId: '79f543f3ecd1bfc3609563f8c928420432592988', url: 'https://github.com/dongyanglmm/TestJenkins.git'
    }

    //����mvn����
    def mvnHome = tool 'M3'
    env.PATH = "${mvnHome}/bin:${env.PATH}"

    stage('mvn test'){
        //mvn ����
        sh "mvn test"
    }

    stage('mvn build'){
        //mvn����
        sh "mvn clean install -Dmaven.test.skip=true"
    }

    stage('deploy'){
        //ִ�в���ű�
        echo "deploy ......" 
    }
}