grafana Cookbook
================
Installs [Grafana](https://github.com/grafana/grafana) with nginx or apache backend.

Requirements
------------
#### cookbooks
- [git](https://github.com/opscode-cookbooks/git) 
- [apache](https://github.com/opscode-cookbooks/apache2) 
- [nginx](https://github.com/opscode-cookbooks/nginx)

Attributes
----------
- `default['grafana']['revision']` - the revision to install, default: f5e8f9334be707c54f2080a2df3cb0f20e4d995a
- `default['grafana']['install_dir']` - installation directory, default: "/opt/grafana"
- `default['grafana']['repo']` - repository to checkout from, default: "https://github.com/grafana/grafana.git"
- `default['grafana']['elasticsearch_url']` - elasticserach url. there is a possiblity to use js as well. default: '"http://"+window.location.hostname+":9200"'
- `default['grafana']['graphite_url']` - graphite url. there is a possiblity to use js as well. '"http://"+window.location.hostname+":8080"'
- `default['grafana']['port']` - port the web server will listen to. defaults to 80.
e.g.

Usage
-----
First include grafana::default which clones the grafana repository from github and changes the configuration based on the given attributes. 
Then you could ether include grafana::nginx or grafana::apache to install a server. Feel free to only include the default recipe and use any other server/cookbook.


License and Authors
-------------------
Authors: Fewbytes
