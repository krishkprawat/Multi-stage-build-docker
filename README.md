![git](https://github.com/krishkprawat/Multi-stage-build-docker/assets/47602022/51afc476-0adc-40d8-8886-c6dbaba109c6)

# Multi-stage-build-docker
this repo is for learn about multi stage docker stages
 real advantage of multi stage docker build and distro less images can be understand with a drastic decrease in the Image size.

===================
Distroless Images:
======================
Distroless images are Docker container images that are minimalistic in nature. They contain only the bare essentials required to run an application and exclude unnecessary components such as package managers, shells, and other system tools. These images are typically based on a specific base image, like Alpine Linux, but are stripped down to the smallest possible footprint.

Distroless images are often used to build and deploy containerized applications where security and minimalism are crucial. By excluding unnecessary software components, the attack surface is reduced, making the containers more secure and lightweight. Google introduced Distroless images as part of the gcr.io/distroless project, and they have gained popularity in the containerization community.

==========================
Multi-Stage Docker Builds:
==========================
Multi-stage builds in Docker are a technique used to create more efficient and smaller container images. They involve defining multiple stages or phases in a Dockerfile, each with its own set of instructions. These stages allow you to compile and build your application in one stage and then copy only the necessary artifacts into the final container image in another stage.

The primary benefits of multi-stage builds include:

Reduced image size: You can create a smaller final image by excluding build-time dependencies and intermediate artifacts.
Improved security: By minimizing the components in the final image, you reduce the attack surface.
Simplified build process: You can keep your build dependencies in one stage and only copy the built application into the final image, making it easier to manage.
