# B ArgoCD repository

## Details
- we use app-of-apps approach(root app)
- initially ArgoCD is installed with TF from [begames-eu-tf](git@gitlab.dev.clover.tech:devops/begames-eu-infra.git)
- then ArgoCD manages itself by its own :)
## Folder structure
```csharp
.
├── README.md
├── apps
│   ├── Chart.yaml // root app
│   └── templates
│       └── root.yaml // root app(i.e. app-of-apps approach)
│       └──  ..... // other apps(ext-dns/aws-load-balancer/etc)
└── charts
    └── argo-cd // ArgoCD is managed by ArgoCD though the chart
        ├── Chart.lock
```
