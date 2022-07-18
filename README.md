# fluxrepo



## Use with Tanzu Mission Control

### In Continuous Delivery
1. Enable C/D
2. Add a GitRepository using the URL of the repo: https://github.com/BrianRagazzi/fluxrepo
3. Add kustomizations that point to the ./clusters/br-demo2/yelb or other subfolders



### Adjustment the flux objects created by TMC
#### Necessary as of Jul 18, 2022

* update GitRepo with correct branch and interval
  ```
  spec.interval: 5m
  spec.ref.branch: main
  ```

* Adjust interval on kustomization
  ```
  spec.interval: 5m
  ```
