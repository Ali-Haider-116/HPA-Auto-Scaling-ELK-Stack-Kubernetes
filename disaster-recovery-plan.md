# Disaster Recovery Plan

## Critical Components for Backups
- MySQL Database
- ConfigMaps
- Secrets

## Backup Strategy
- Daily MySQL backups using `mysqldump`.
- Weekly backups of ConfigMaps and Secrets.

## Backup Commands
```bash
# MySQL backup command
mysqldump -u root -p crudmysql > /backups/mydatabase-$(date +%F).sql

# Backup ConfigMaps and Secrets
kubectl get configmaps --namespace myapp -o yaml > configmap.yml
kubectl get secrets --namespace myapp -o yaml > secrets.yml
