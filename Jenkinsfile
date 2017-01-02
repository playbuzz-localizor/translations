#!/usr/bin/env groovy

node {
   // Mark the code checkout 'stage'....
   //stage 'Checkout'

   // Get some code from a GitHub repository
   //git credentialsId: 'bf7cb5fb-f7b9-4d05-b852-603d5b044426', url: 'https://github.com/buzzdan/translations'
   echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL} --"

   stage 'Deploy'
   aws s3 cp 'playbuzz' 's3://playbuzz-cdn/translations/playbuzz/staging/'
}