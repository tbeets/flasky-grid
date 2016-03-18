# flasky-grid

Demonstrate image-based deployment of a Python web application using the popular Flask web
framework.

Based on commit tag 4b of the [git repository](https://github.com/miguelgrinberg/flasky) for the O'Reilly book [Flask Web Development](http://www.flaskbook.com) used under MIT license.
 
# Local Deploy and Execution (Source)

## Pre-requisites

    Python 2.7 (platform dependent)

    virtualenv --python=python2.7 venv
    source venv/bin/activate
    pip install -r ./requirements.txt

## Application execution

    gunicorn --workers 2 --bind 0.0.0.0:5000 app:app

# Local Deploy and Execution (Image)

## Pre-requisites

    Docker (platform dependent)
    
## Application execution

    docker pull tbeets/flasky-grid:latest
    docker run -i -t -p 5000:5000 tbeets/flasky-grid:latest
    
# Local Image Build and Execution (Optional)

## Pre-requisites

    Docker (platform dependent)
    
## Image build

    docker build -t flasky-grid .
    
## Application execution

    docker run -i -t -p 5000:5000 flasky-grid
