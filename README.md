# Example of building a docker image where the Dockerfile is not in the same folder as docker context

This is a Git repository that holds a Node application and a Dockerfile. The dockerfile is placed in a subfolder of the project
instead of being at the root folder

## Packaging the Node.js app

To compile and package using Docker 

```bash
docker build . -t my-app -f docker/Dockerfile
```

## Running the docker image

```bash
docker run -p 3000:3000 my-app
```

and then visit http://localhost:3000 in your browser


## To use this project in Codefresh

There is also a [codefresh.yml](codefresh.yml) for easy usage with the [Codefresh](codefresh.io) CI/CD platform.

More details can be found in [Codefresh documentation](https://codefresh.io/docs/docs/yaml-examples/examples/build-an-image-specify-dockerfile-location/).

