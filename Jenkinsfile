node{
    stage('get clone'){
        //check CODE
       git credentialsId: '79f543f3ecd1bfc3609563f8c928420432592988', url: 'https://github.com/dongyanglmm/TestJenkins.git'
    }

    //定义mvn环境
    def mvnHome = tool 'M3'
    env.PATH = "${mvnHome}/bin:${env.PATH}"

    stage('mvn test'){
        //mvn 测试
        sh "mvn test"
    }

    stage('mvn build'){
        //mvn构建
        sh "mvn clean install -Dmaven.test.skip=true"
    }

    stage('deploy'){
        //执行部署脚本
        echo "deploy ......" 
    }
}