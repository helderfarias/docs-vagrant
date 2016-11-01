# Running Vagrant behind a proxy

### Install proxyconf
```bash
vagrant plugin install vagrant-proxyconf
```

### Configure your Vagrantfile
```bash
Vagrant.configure(2) do |config|
  ....
  config.proxy.http     = "http://<HOST>:<PORT>"
  config.proxy.https    = "http://<HOST>:<PORT>"
  config.proxy.no_proxy = "localhost,127.0.0.1"
  ....
end
```
