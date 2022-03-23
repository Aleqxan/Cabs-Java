def gv

pipeline {
    agent any
    tools {
        maven 'Maven'
    }
    stages {
        stage("init") {
            steps {
                script {
                    gv = load "scipt.groovy"
                }
            }
        }
        stage("buildjar") {
            steps {
                script { 
                   gv.buildJar()
                }
            }
        }
        stage("buildimage") {
            steps {
                script {
                    gv.buildImage()
                }
            }
        }
        stage("deploy") {
            steps {
                script {
                    gv.deployApp()
                }
            }
        }
    }
}