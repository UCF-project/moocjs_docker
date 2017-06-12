# UCF MOOC VISH Docker

This project describe a way to build a docker image for the UCF fork
of VISH.

:warning: DO NOT USE THIS IN PRODUCTION :warning:

This image is built with the development configuration and should be
used only testing purposes.

To build the docker image:

```bash
# Clone this repository
git clone git@git.rnd.alterway.fr:UCF/vish_docker.git
cd vish_docker

# Create a ssh key that has access to project repository git@git.rnd.alterway.fr:UCF/vish.git
ssh-keygen -t rsa -f ./id_rsa

# Build docker image
docker build -t vish:ucf  ./

# Start container
docker run -d -p 3000:3000 vish:ucf
```

Now you can access http://localhost:3000 at your browser.

