[![Project Supported by CyVerse](https://de.cyverse.org/Powered-By-CyVerse-blue.svg)](https://learning.cyverse.org/projects/vice/en/latest/) [![Project Status: Active – The project has reached a stable, usable state and is being actively developed.](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active) [![DOI]()]()
 [![license](https://img.shields.io/badge/license-BSD3-red.svg?style=flat-square)](https://opensource.org/licenses/BSD-3-Clause) ![GitHub all releases](https://img.shields.io/github/downloads/cyverse-vice/matlab/total?style=flat-square)

# Matlab

[Mathworks Matlab]() with additional CyVerse tools

Based on [Official Matlab Docker image](https://hub.docker.com/r/mathworks/matlab) with additional CyVerse specific tools (iCommands).

quick launch | size | 
------------ | ---- | 
<a href="https://de.cyverse.org/apps/de/478d4c5c-bda5-11eb-9b6c-008cfa5ae621/launch?quick-launch-id=27836c84-31fd-43ad-a81c-d564d49c5695" target="_blank"><img src="https://img.shields.io/badge/Matlab-2021a-blue?style=plastic&logo=mathworks"></a> | [![SIZE](https://img.shields.io/docker/image-size/cyversevice/matlab/latest.svg)](https://img.shields.io/docker/image-size/cyversevice/matlab/latest) |


# Instructions


## Run Docker locally or on a Virtual Machine

Unless you plan on making changes to this container, you should use the existing launch buttons above.

To test the container locally:

```
docker run -it --rm -p 5901:5901 -p 6080:6080 -e REDIRECT_URL=http://localhost:6080 harbor.cyverse.org/matlab/2021a:latest
```

To build your own container with a Dockerfile and additional dependencies, pull the pre-built image from DockerHub:

```
FROM harbor.cyverse.org/matlab/2021a:latest
```

Follow the instructions in the [VICE manual for integrating your own tools and apps](https://cyverse-visual-interactive-computing-environment.readthedocs-hosted.com/en/latest/developer_guide/building.html).
