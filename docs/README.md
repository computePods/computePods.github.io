# ComputePods

The ComputePods Project provides the tools needed to distribute any simple
[embarrassingly
parallelisable](https://en.wikipedia.org/wiki/Embarrassingly_paralle>)
computational task (such as, but not limited to, compilation of source
code) across multiple computers.

A ComputePods "pod" is an coordinated collection of
[OCI](https://opencontainers.org/) containers. These ComputePods can be
run rootless using [Podman](https://podman.io/)
[Pod](http://docs.podman.io/en/latest/pod.html) (on a private collection
of computers to which a user has access) or as a
[Kubernetes](https://kubernetes.io/)
[Pod](https://kubernetes.io/docs/concepts/workloads/pods/) (in a more
specialised production environment).

Each pod consists of:

- A [NATS](https://nats.io/) container used to provide inter/intra pod
  communication.

- A [MajorDomo](majorDomo) to coordinate the dependency analysis and
  subsequent "build".

- A collection of different [Chef](chef) (worker) containers, one or more
  for each computational task. These chefs consist of a Python asyncio
  based controller process which pulls files from one or more pods as
  needed and then forks "tasks" consisting of any containerisable
  computational "command line" process.

Suitably programmed computational tasks can interact with the NATS
"back-plane" to initiate, and wait for sub-tasks to be run.
