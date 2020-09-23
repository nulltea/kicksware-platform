# [![Kicksware logo][]][Kicksware url]

<p align="center">
	<a href="https://kicksware.com">
		<img src="https://img.shields.io/website?label=Visit%20website&down_message=unavailable&up_color=teal&up_message=kicksware.com%20%7C%20online&url=https%3A%2F%2Fkicksware.com">
	</a>
</p>

[![golang badge]](https://golang.org)&nbsp;
[![c# badge]](https://dotnet.microsoft.com/apps/aspnet)&nbsp;
[![js badge]](https://jamstack.org)&ensp;
[![kubernetes badge]](https://kubernetes.io)&nbsp;
[![architecture badge]][microservice article]&ensp;
[![license badge]](https://www.gnu.org/licenses/agpl-3.0)

[![api pipeline]](https://ci.kicksware.com/kicksware/api/-/commits/master)&nbsp;
[![web-app pipeline]](https://ci.kicksware.com/kicksware/web-app/-/commits/master)&nbsp;
[![gitlab badge]](https://ci.kicksware.com/kicksware/kicksware-platform)&nbsp;
[![gateway pipeline]](https://ci.kicksware.com/kicksware/gateway/-/commits/master)&nbsp;
[![tool-stack pipeline]](https://ci.kicksware.com/kicksware/tool-stack/-/commits/master)&nbsp;

## Overview

_**Kicksware**_ is an all-in-one modular end-to-end opensource platform designed by and for the sneakerheads around the globe as part of the luxury fashion worldwide ecosystem.

It designed to provide opportunity, place and services not only to a passionate buyer or a prosperous seller but those who encourage authenticity, sustain individuality, and seeking like-minded personalities to further cooperation and collaboration.

It’s goal is to support use of modern technology in nowadays fashion industry and help building better, more comfortable, more authentic and more creative ecosystem.

## Components

As it was designed as a distributed microservice system _**Kicksware**_ consist of 4 main components, each having it's own dadicated project:

* [**API** - microservices registry, which collectively represents application business-logic, written in Go][api repo]
* [**Web App** - frontend web application which enables users to interact with business-logic via the stylish user interface][web-app repo]
* [**Gateway** - cloud-native reverse proxy and load balancer service based on][gateway repo] [Traefik][traefik repo]
* [**Tool Stack** - complex of additional technologies, services, and databases configured to be a part of Kicksware infrastructure][tool-stack repo]

Together, these components make up a complete software infrastructure designed with scalability in mind, therefore can handle a constantly growing audience and volatile market conditions

## Architecture

Kicksware system design is based on _[**microservice architecture**][microservice article] pattern_ which takes an approach for developing a single application as a suite of small services, each running in its own process and communicating with lightweight mechanisms, often an HTTP resource API.

This particular approach was originally chosen for research and self educational purposes and afterwards my passion for sneakers was used as the soul of a future product. And by all means, this isn't the right way of choosing an architectural design for the upcoming system. Product purpose, budget, team size, need in scalability, market condition and even more factors should be considered while choosing a software architecture pattern.

As for this particular project main goal was to reverce enginier this proccess and build the system that would be the best possible fit for approach of microservices.

## Infrastructure

In order to _deploy_, _maintain_ and be able to effectively _scale_ distributed microservice system such as Kicksware, organized and well-thought infrastructure is required.

**Сloud infrastructure** is a set of components needed for cloud computing, which includes hardware, software, storage, and network resources as well as relation between them. It also includes a hardware abstraction layer that enables the virtualization of resources and helps to drive down costs through economies of scale.

Generally, modern [**cloud-native**][cloud-native] applications are built as a set of services that run in _Docker containers_, and may be orchestrated in _Kubernetes_ and managed and deployed using _DevOps_ and _Git CI_ workflows. This project is no exception as it is also taking advantage of continuous deployment to the Kubernetes cluster triggered by Gitlab CI\CD system.

In terms of scalability, Kicksware is relying on Kuberentes [_Horizontal Pod Autoscaler (HPA)_][k8s hpa] feature and [_Cluster Autoscaler_][digitalocean-vna] provided by _DigitalOcean_.

The following diagram visualy reprsents Kicksware's cloud infrastructure components and relation between them:
[![kicksware infrastructure][]][kicksware-cloudcraft]

## Wrap Up

_**Kicksware**_ is a _noncommercial, research project_ dedicated to be a playground for learning and practicing modern cloud technologies, languages, patterns, and architectures.

And although there aren't any future plans to make a profit from Kicksware as a real-world sneaker resale shop, this isn't the final stop for this project.

Kicksware will continue to exist and adopt new technologies as the time pasts as well as stay open source.

Feel free to contribute your code and ideas. Please make sure to read the Contributing Guide before making a pull request.

## License

Licensed under the [GNU AGPLv3][license file].

[kicksware logo]: https://ci.kicksware.com/kicksware/kicksware-platform/-/raw/master/assets/repo-logo.png
[kicksware url]: https://kicksware.com

[api repo]: https://github.com/timoth-y/kicksware-api
[web-app repo]: https://github.com/timoth-y/kicksware-web-app
[gateway repo]: https://github.com/timoth-y/kicksware-gateway
[tool-stack repo]: https://github.com/timoth-y/kicksware-tool-stack

[Website badge]: https://img.shields.io/website?label=Visit%20website&down_message=unavailable&up_color=teal&up_message=kicksware.com%20%7C%20online&url=https%3A%2F%2Fkicksware.com
[golang badge]: https://img.shields.io/badge/Code-Golang-informational?style=flat&logo=go&logoColor=white&color=6AD7E5
[c# badge]: https://img.shields.io/badge/Code-C%23-informational?style=flat&logo=c-sharp&logoColor=white&color=1E9E25
[js badge]: https://img.shields.io/badge/Code-JavaScript-informational?style=flat&logo=javascript&logoColor=white&color=F7E018
[license badge]: https://img.shields.io/badge/License-AGPL%20v3-blue.svg?color=teal
[architecture badge]: https://img.shields.io/badge/Architecture-Microservices-informational?style=flat&logo=opslevel&logoColor=white&color=teal
[kubernetes badge]: https://img.shields.io/badge/DevOps-Kubernetes-informational?style=flat&logo=kubernetes&logoColor=white&color=316DE6
[gitlab badge]: https://img.shields.io/badge/CI-Gitlab_CE-informational?style=flat&logo=gitlab&logoColor=white&color=FCA326

[api pipeline]: https://ci.kicksware.com/kicksware/api/badges/master/pipeline.svg?key_text=API%20|%20pipeline&key_width=85
[web-app pipeline]: https://ci.kicksware.com/kicksware/web-app/badges/master/pipeline.svg?key_text=Web%20App%20|%20pipeline&key_width=115
[gateway pipeline]: https://ci.kicksware.com/kicksware/gateway/badges/master/pipeline.svg?key_text=Gateway%20|%20pipeline&key_width=115
[tool-stack pipeline]: https://ci.kicksware.com/kicksware/tool-stack/badges/master/pipeline.svg?key_text=Tool%20Stack%20|%20pipeline&key_width=125

[traefik repo]: https://github.com/traefik/traefik/blob/master/README.md
[microservice article]: https://martinfowler.com/articles/microservices.html

[kicksware infrastructure]: https://raw.githubusercontent.com/timoth-y/kicksware-platform/master/assets/kicksware-infrastructure.png
[kicksware-cloudcraft]: https://app.cloudcraft.co/view/06c423b0-2024-47da-a929-135244424429?key=0JqqeWiD_Jx4skCCQIvLFA
[cloud-native]: https://www.cncf.io/
[k8s hpa]: https://kubernetes.io/docs/tasks/run-application/horizontal-pod-autoscale/
[digitalocean-vna]: https://www.digitalocean.com/docs/kubernetes/how-to/autoscale/

[license file]: https://github.com/timoth-y/kicksware-platform/blob/master/LICENSE