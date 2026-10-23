
pipeline {
    agent any 
    
    environment {
        VERCEL_TOKEN = credential("vercel-token")
    }

    stages {
        stage("install"){
            steps {
            bat "npm run install"

            }
        }
         stage("test"){
              steps {
            echo "No Testing Found!"
              }
        }
        stage("build"){
              steps {
            bat "npm run build"
              }
        }
        stage("deploy"){
              steps {
            bat "npx vercel --prod --yes --token%VERCEL_TOKEN%"
              }
        }
    }
}