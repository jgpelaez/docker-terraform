# jgpelaez/terraform

## What is terraform

Terraform provides a common configuration to launch infrastructure — from physical and virtual servers to email and DNS providers. Once launched, Terraform safely and efficiently changes infrastructure as the configuration is evolved.

Simple file based configuration gives you a single view of your entire infrastructure.

[http://www.terraform.io/](http://www.terraform.io/)

## Dockerfile

[**Trusted Build**](https://registry.hub.docker.com/u/jgpelaez/terraform/)

This Docker image is based on the official [ubuntu:15.10
](https://registry.hub.docker.com/_/ubuntu) base image.

## How to use this image

```
docker run --rm jgpelaez/terraform [--version] [--help] <command> [<args>]

```

## Using

**Please note: Create by your Terraform configuration files (.tf) is `/data` directory**

### terraform apply

```
docker run --rm -v /data:/data -v /etc/ssl/certs:/etc/ssl/certs:ro --net=host jgpelaez/terraform apply [options]
```

### terraform destroy

```
docker run --rm -v /data:/data jgpelaez/terraform destroy [options] [DIR]
```

### terraform get

```
docker run --rm -v /data:/data jgpelaez/terraform get [options] PATH
```

### terraform graph

```
docker run --rm -v /data:/data jgpelaez/terraform graph [options]
```

### terraform init

```
docker run --rm -v /data:/data jgpelaez/terraform init [options] SOURCE [PATH]
```

### terraform output

```
docker run --rm -v /data:/data jgpelaez/terraform output [options] NAME
```

### terraform plan

```
docker run --rm -v /data:/data -v /etc/ssl/certs:/etc/ssl/certs:ro --net=host jgpelaez/terraform plan [options]
```

### terraform push

```
docker run --rm -v /data:/data -v /etc/ssl/certs:/etc/ssl/certs:ro --net=host jgpelaez/terraform push [options]
```

### terraform refresh

```
docker run --rm -v /data:/data -v /etc/ssl/certs:/etc/ssl/certs:ro --net=host jgpelaez/terraform refresh [options]
```

### terraform remote

```
docker run --rm -v /data:/data -v /etc/ssl/certs:/etc/ssl/certs:ro --net=host jgpelaez/terraform remote [options]
```

### terraform show

```
docker run --rm -v /data:/data jgpelaez/terraform show terraform.tfstate [options]
```

### terraform taint

```
docker run --rm -v /data:/data -v /etc/ssl/certs:/etc/ssl/certs:ro --net=host jgpelaez/terraform taint [options] name
```

### terraform version

```
docker run --rm jgpelaez/terraform version
```