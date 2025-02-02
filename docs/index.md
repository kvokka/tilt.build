---
title: Tilt User Guide
layout: docs
---

Local Kubernetes development with no stress.

[Tilt]({{site.landingurl}}) helps you develop your microservices locally.
Run `tilt up` to start working on your services in a complete dev environment
configured for your team.

Tilt watches your files for edits, automatically builds your container images,
and applies any changes to bring your environment
up-to-date in real-time. Think `docker build && kubectl apply` or `docker-compose up`.

The screencast below demonstrates what a typical Tilt session looks like:
starting multiple microservices, making changes to them, and seeing any new errors
or logs right in your terminal.

<div class="block u-marginTop2 u-marginBottom2 u-padding16">
<iframe class="u-boxShadow" width="560" height="315" src="https://www.youtube.com/embed/oSljj0zHd7U" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>

## Install Tilt

Download the latest Tilt release from
[GitHub](https://github.com/windmilleng/tilt/releases). Read the [Installation Guide](install.html) for details and prerequistes.

## Describe Your Workflow

A Tiltfile is a program that connects your existing Docker and Kubernetes configurations:

```python
# Example Tiltfile for a k8s app with two microservices

# Deploy: tell Tilt what YAML to apply
k8s_yaml('app.yaml')

# Build: tell Tilt what images to build from which directories
docker_build('companyname/frontend', 'frontend')
docker_build('companyname/backend', 'backend')
```

Set up Tilt in 15 minutes with the [Tutorial](tutorial.html).

## See More
Stop playing 20 questions with `kubectl`. Tilt's UI pulls relevant data to the surface, automatically.

You fix faster when you know what's broken.

## Community

Questions? Comments? Just want to say hi? Find us on the Kubernetes slack. Get an invite at [slack.k8s.io](http://slack.k8s.io) and find
us in [the **#tilt** channel](https://kubernetes.slack.com/messages/CESBL84MV/).

We tweet [@tilt_dev](https://twitter.com/tilt_dev) and
blog about building Tilt at [blog.tilt.dev](https://blog.tilt.dev).

Tilt is Open Source, developed on [GitHub](https://github.com/windmilleng/tilt).

We expect everyone in our community (users, contributors, and employees alike) to abide by our [**Code of Conduct**](code_of_conduct.html).
