<!--
  Licensed to the Apache Software Foundation (ASF) under one or more
  contributor license agreements.  See the NOTICE file distributed with
  this work for additional information regarding copyright ownership.
  The ASF licenses this file to You under the Apache License, Version 2.0
  (the "License"); you may not use this file except in compliance with
  the License.  You may obtain a copy of the License at
      http://www.apache.org/licenses/LICENSE-2.0
  Unless required by applicable law or agreed to in writing, software
  distributed under the License is distributed on an "AS IS" BASIS,
  WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
  See the License for the specific language governing permissions and
  limitations under the License.
-->

# Docker Image Quickstart

## Capabilities
This image currently supports running in unsecured standalone mode

## Building
The Docker image can be built using the following command:

    . ~/Projects/nifi-dev/nifi-registry/nifi-registry-docker/dockerhub/DockerBuild.sh

This will attempt to build and tag an image matching the string in DockerImage.txt

    dockerhub dchaffey$ cat DockerImage.txt
    > apache/nifi-registry:0.1.0
    docker images
    > REPOSITORY               TAG                 IMAGE ID            CREATED             SIZE
    > apache/nifi-registry     0.1.0               751428cbf631        15 minutes ago      342MB

## Running a container

### Standalone Instance, Unsecured
The minimum to run a NiFi Registry instance is as follows:

    . ~/Projects/nifi-dev/nifi-registry/nifi-registry-docker/dockerhub/DockerRun.sh
      
This will provide a running instance, exposing the instance UI to the host system on at port 18080,
viewable at `http://localhost:18080/nifi-registry`.
