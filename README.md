# Insecure Base Image in Dockerfile

This repository demonstrates a common issue in Dockerfiles: using the `ubuntu:latest` image.  While convenient, this approach is insecure as it can lead to unexpected changes in behavior due to updates in the base image.

## The Problem

The provided Dockerfile uses `ubuntu:latest`. This means that the build uses the latest version of Ubuntu at the time of execution. However, new updates to Ubuntu can introduce breaking changes, causing the Docker image to fail unexpectedly.

## The Solution

Instead of using `ubuntu:latest`, specify a specific version of Ubuntu. This guarantees consistent behavior across builds, regardless of updates to the base image.  The solution shows how to use a specific tag (e.g., `22.04`) ensuring reproducibility.