---
title: PDG 3.02 - Persist Data
---

| Status | Created     | Post-History    |
|--------|-------------|-----------------|
| Draft  | 17-Jul-2023 | 'loos' typo fix |
| Active | 07-Mar-2023 |                 |
| Draft  | 02-Jan-2023 | n/a             |
| Moved  | 02-Jan-2023 | content moved   |

## Why

In cases where data has to be persisted (database, uploaded files etc.), Kubernetes **must** be configured to create Persistent Volume that is attached to an storage created by a storage provider, where data remains even after the deletion of the application. Otherwise, an incidental deletion will delete all state.

## Description

Using stateful data requires additional caution to not lose data by accident. Therefore, when a pod/deployment/statefulset resource is removed, data will still be available on the StorageClass's disk that was used.

## How

Example PersistentVolumeClaim:

```yaml
# pvc.yaml
kind: PersistentVolumeClaim
apiVersion: v1
metadata:
  name: pvc-persistent-tmp-demo
spec:
  accessModes:
    - ReadWriteOnce
  resources:
    requests:
      storage: 50Mi
```

This can be referenced in the volumes section of a Pod/Deployment/StatefulSet resource:

```yaml
# deployment.yaml
#...
      volumes:
        - name: pv-tmp-demo
          persistentVolumeClaim:
            claimName: pvc-persistent-tmp-demo
#...
```

:::tip

It is not recommended to directly request the claim in a StatefulSet! Rather create the PVC separately and reference that as an existing claim. See the example in [Bitnami's Postgresql chart](https://github.com/bitnami/charts/tree/main/bitnami/postgresql) where an existing claim can be referenced for the primary database at the [primary.persistence.existingClaim property](https://github.com/bitnami/charts/tree/main/bitnami/postgresql#postgresql-primary-parameters).

:::
