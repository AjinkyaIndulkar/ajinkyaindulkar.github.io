# ajinkyaindulkar.github.io
Repository to maintain my personal blog website. 

## Usage

1. Run local server:

```shell
git clone https://github.com/piharpi/jekyll-klise.git
cd jekyll-klise
bundle install
bundle exec jekyll serve
```

2. Navigate to `localhost:4000`

3. Shutdown local server: First, `ctrl+c` to stop the server, followed by:

```shell
ps aux |grep jekyll |awk '{print $2}' | xargs kill -9
```

Note: The above command is to unbind 4000 port 

### Changelog:

- 28 April 2021: Updated website template to
  [jekyll-klise](https://github.com/piharpi/jekyll-klise)
- 27 April 2021: `v0.1` release with 
  [startbootstrap-resume template](https://github.com/StartBootstrap/startbootstrap-resume)
