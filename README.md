# aws-cli

AWS CLI for local env

use alias to have a aws command to start container each time

## add below to ~/.profile for mac to save the alias

alias aws='docker run --rm -ti -v $HOME/.aws:/root/.aws -v $PWD:/aws amazon/aws-cli'

## then source ~/.profile

source ~/.profile

## then run aws cli via docker

aws s3 ls
aws s3 sync . s3://wzq.huicheng.com.au
aws ec2 describe-instances
