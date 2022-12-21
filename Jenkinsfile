/* 
Jenkins Pipeline Version 1.0.0
Updated: 2022-12-21

YOU shouldn't need to edit this!! 
If you want to add environments to the choices, add it to the library
 */

@Library('shared-library@master') _

properties([
    parameters ([
        //default false, if a manual deploy then select true
        choice(choices: ['false', 'true'].join('\n'), 
            description: 'Select deploy type. false -  default. true - manual build by a human', 
            name: 'HUMAN_TRIGGERED'),
        //Take Environments from library
        choice(choices: choiceEnvironments(), 
            description: 'Select environment', 
            name: 'CLOUDHUB_ENVIRONMENT_OVERRIDE'),
        choice(choices: ['false', 'true'], 
            description: 'If true - will drop all Maven cache-Danger use with caution', 
            name: 'CLEAN_MAVEN_CACHE')
    ])
])

mulesoftPipeline()