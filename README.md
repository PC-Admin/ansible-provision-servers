# Ansible Provision Servers

The provision stage configures the DigitalOcean servers that a Matrix service can exist in. 

A playbook I created to speed up testing.


## Setup Servers

1) Configure the inventory files for all the desired hosts appropriately.

2) Run the setup.yml playbook:

`$ ansible-playbook -v -i inventory/hosts setup.yml`

Or even easier, provision a server with automatic CloudFlare DNS configuration:

`$ ansible-playbook -v -i inventory/hosts --tags "cloudflare-dns" setup.yml`


## Removing Servers

`$ ansible-playbook -v -i inventory/hosts remove.yml`

Or remove a server and it's CloudFlare DNS record automatically:

`$ ansible-playbook -v -i inventory/hosts --tags "cloudflare-dns" remove.yml`


## License

Copyright 2022 Michael Collins

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
