# git - Configuration

Set the user details:
```
git config --global user.name "John Smith"
git config --global user.email "john.smith@email.com"
```

Configure git to work with a proxy:
```
git config --global http.proxy http://proxyUsername:proxyPassword@proxy.server.com:port
```

Unset a proxy:
```
git config --global --unset http.proxy
```
