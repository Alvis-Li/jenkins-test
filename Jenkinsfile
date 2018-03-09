#!groovy

properties([
  disableConcurrentBuilds(),
  [$class: 'RebuildSettings', autoRebuild: true, rebuildDisabled: false],
  parameters(
    [
     choice(choices: 'development\nqa\nstaging\nproduction', description: '', name: 'TargetEnv'),
     choice(choices: 'Regression Test\nSmoke Test', description: '', name: 'TargetType'),
     string(name: 'TargetFiles', defaultValue: '', description: '')
    ]
  ),
  pipelineTriggers([])
])

node('cloud') {
  timestamps {
    echo "Node label"
  }
}
