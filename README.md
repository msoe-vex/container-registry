# container-registry
This repository serves as a registry to store any Docker and/or Singularity images used by the team. This repository is responsible for holding the files used to create the images, as well as automatically publishing to a public or private registry.

### Pushing to the Container Registry

The following commands can be used to push to our container registry:

```
docker tag local-image:tagname raiderrobotics/container-registry:repo-tagname
docker push raiderrobotics/container-registry:repo-tagname
```

In this case, `repo-tagname` should be the same value as the folder the Dockerfile is located within.