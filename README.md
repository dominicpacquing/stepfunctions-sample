### Pre-requisites

    brew install nodeenv

### Setup

Only on first usage

1. Create node environment

        nodeenv --node=12.16.1 nodenv

2. Create python environment

        python3 -m venv pyenv
        
### Usage

1. Activate python environment

        source pyenv/bin/activate
  
2. Activate node environment

        source nodenv/bin/activate

3. Install nodejs and python packages

        npm install
        pip install -r requirements.txt
        
4. Deactivate

        deactivate # python
        deactivate_node # node
        
        
### Serverless

Deploy

       AWS_PROFILE=personal node_modules/.bin/sls deploy

Invoking state machine

        AWS_PROFILE=personal node_modules/.bin/sls invoke stepf --name simple-maths --data '{"x":42, "y": 13}'