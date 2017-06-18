## Preparation

First, install Ruby2.3.3.


And then

`$ bundler install --path vendor/bundle --binstubs`

`$ bin/berks vendor`


that's all.


## Usage


`$ bin/knife zero bootstrap [[hostname]] -x vagrant -E development --sudo -N [[client_server_name]]`

`$ bin/knife node environment_set [[client_server_name]] development`

`$ bin/knife node run_list add [[client_server_name]] 'role[linux-servers]'`

`$ bin/knife zero converge 'name:[[client_server_name]]' -x vagrant --ssh-password vagrant --attribute knife_zero.host`

※ caution
Replace [[hostname]] and [[client_server_name]] with yours.
Role is already exsists in `roles/linux-servers.json`, so, all you have to do is adding role of `linux-servers` to the node you added manually.
