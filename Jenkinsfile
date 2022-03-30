pipeline {
    agent any
    options { timestamps () }
  // stages and rest of pipeline.
      triggers {
        cron('* * * * *')
    }
    environment {
        def BUILDVERSION = bat(script: "./gradlew -q versionName","echo date +%y%m%d`'$currentBuild.number'", returnStdout: true).trim()
    }

    stages {
        stage("Awesome Stage") {
            steps {
                echo "version name :: $BUILDVERSION"
                echo "version code :: $BUILDVERSION"
            }
        }
        stage("git clone") {
            steps {
                git branch: 'main', credentialsId: 'github13', url: 'https://github.com/venkat90107/prod.git'
            }
        }
        //stage("mvn build") {
          //  steps {
          //   
            //}
        //}
    }
}
;sdf;
aksdjlj