# Weaviate website

This repo contains the [Weaviate](https://weaviate.io) website, it's built using [Jekyll](https://jekyllrb.com/).

## Installing & Running

### Dependencies

- Software Dependencies
  - [Ruby](https://www.ruby-lang.org/en/documentation/installation/)
  - Ruby Development Package (aka ruby-dev)

- Installing Dependencies in **Ubuntu/Debian**
  ```bash
  # update repositories & install basic build dependencies
  sudo apt update && sudo apt install -y build-essential bash git rsync

  # update repositories & install rbenv
  sudo apt update && sudo apt install rbenv ruby-build ruby_dev

  # initialize rbenv
  rbenv init

  # updates ruby-build local packages
  git clone https://github.com/rbenv/ruby-build.git "$(rbenv root)"/plugins/ruby-build

  # install ruby 2.7.5
  rbenv install 2.7.5
  ```

- Installing Dependencies Windows
  - Please use [WSL](https://docs.microsoft.com/en-us/windows/wsl/)
  - Read the [documentation](https://docs.microsoft.com/en-us/windows/wsl/install) on installing WSL on Windows.

- Installing Dependencies in macOS
  ```bash
  # install dependencies
  brew install rsync openssl rbenv ruby-build ruby-dev

  # install ruby 2.7.5
  rbenv install 2.7.5
  ```

- Check if dependencies are installed correctly
  ```bash
  ruby -v
  gem -v
  ```

### Setting up the repository
  
- To get the site up and running locally, follow the below steps:

  **PS.:** You need to have a full Bash environment. If you're on Windows, please use WSL.

- Fork the repository
  You can get your own fork/copy of [weaviate.io](https://github.com/semi-technologies/weaviate-io) by using the `Fork` button

- Create a local clone of the website:
  ```
  git clone git@github.com:[YOUR-USERNAME]/weaviate-io.git
  ```
- Change into the weaviate-io directory
  ```
  cd weaviate-io
  ```
- Add upstream URL, this acts as a reference from original weaviate.io's repository
  ```bash
  git remote add upstream git@github.com:semi-technologies/weaviate-io.git
  ```
- Perform the following commands to install dependencies and structure the website properly:
  ```
  ./setup.sh
  ```
- Build the site and make it available on your local server
  ```
  ./run.sh
  ```
- Browse [http://localhost:4000](http://localhost:4000) to view the website.

### OG image generator

OG images for documentation are created and linked automatically. The `og` tag in 
front matter should only be used for manual override. E.g. The `architecture/binary_passage_retrieval.md` image
would be located at `img/og/og-documentation/architecture-binary-passage-retrieval.jpg`.