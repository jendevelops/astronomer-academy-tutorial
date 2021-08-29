# Starting and Stopping Airflow Container

```bash
astro dev start
```
*sometimes this command doesnt work. See issues [below](#docker-buildkit-error-on-start)

```bash
astro dev stop
```

# Issues

# Docker Buildkit Error on Start 
```bash
> astro dev start
Env file ".env" found. Loading...
buildkit not supported by daemon
Error: command 'docker build -t airflow-test_173d2b/airflow:latest failed: failed to execute cmd: exit status 1
```

If you get this error, we want to disable buildkit, to do this run this command:

```bash
DOCKER_BUILDKIT=0 astro dev start
```