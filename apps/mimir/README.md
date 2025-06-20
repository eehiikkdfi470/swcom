Folder structre explanation for Mimir

apps/
└── mimir/
    ├── base/
    │   ├── kustomization.yaml
    │   └── values-config.yaml   # Common settings for all envs
    └── overlays/
        └── dev/
            ├── kustomization.yaml
            ├── values-dev.yaml  # Dev-specific overrides
            └── mimir-application.yaml  # Argo CD Application manifest

