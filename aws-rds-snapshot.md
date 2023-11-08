### Creating A Snapshot

```sh
 aws rds create-db-snapshot \
    --db-snapshot-identifier my-manual-snapshot \
    --db-instance-identifier db-example
```

### Viewing Snapshots

```sh
aws rds describe-db-snapshots \
    --db-snapshot-identifier my-manual-snapshot
```

```sh
aws rds describe-db-snapshots
```

### Deleting a Snapshot

```sh
aws rds delete-db-snapshot \
    --db-snapshot-identifier my-manual-snapshot
```

### Copying a Snapshot to Another Region

```sh
aws rds copy-db-snapshot \
    --source-db-snapshot-identifier arn:aws:rds:us-west-2:123456789012:snapshot:mydbsnapshot \
    --target-db-snapshot-identifier mydbsnapshot-copy \
    --source-region us-west-2 \
    --region us-east-1
```

### Restoring a Database from a Snapshot

```sh
aws rds restore-db-instance-from-db-snapshot \
    --db-instance-identifier db-example \
    --db-snapshot-identifier db-snap
```

### Modifying a Database Instance

```sh
aws rds modify-db-instance \
    --db-instance-identifier mydbinstance \
    --backup-retention-period 7 \
    --preferred-backup-window 00:00-03:00 \
    --apply-immediately

```