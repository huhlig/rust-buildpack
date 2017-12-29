CloudFoundry Rust Buildpack
===========================

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

Simple Buildpack designed to deploy Rust WebApplication Servers to CloudFoundry.
Rust is kept up to date via rustup. Artifacts installed in ~/app/bin/ and by default attempts to execute 
~/app/bin/<Cargo.toml/package/name>

### Getting it onto your Cloud Foundry

```bash
$ pwd
/home/ibm/projects/rust-buildpack

$ buildpack-packager --cached 
Cached buildpack created and saved as /home/ibm/projects/rust-buildpack/rust_buildpack-cached-v0.0.1.zip with a size of 8.0K

$ cf create-buildpack rust-buildpack rust_buildpack-v0.0.1.zip 1
Creating buildpack rust-buildpack...
OK

Uploading buildpack rust-buildpack...
Done uploading
OK
```
