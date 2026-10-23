
pipeline {
    environment {
        VERCEL_TOKEN = credential("vercel-token")
    }

    stages {
        stage("install"){
            bat "npm run install"
        }
         stage("test"){
            echo "No Testing Found!"
        }
        stage("build"){
            bat "npm run build"
        }
        stage("deploy"){
            bat "npx vercel --prod --yes --token%VERCEL_TOKEN%"
        }
    }
}