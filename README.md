Steps to reproduce this commit:

```bash
ks init ks-example --api-spec=version:v1.9.0
cd ks-example/
ks generate deployed-service guestbook-ui   --image gcr.io/heptio-images/ks-guestbook-demo:0.1   --type ClusterIP
ks param set guestbook-ui image gcr.io/heptio-images/ks-guestbook-demo:0.2
ks apply default # this works
```
