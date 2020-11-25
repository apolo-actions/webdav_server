# Run your WebDAV server using neuro-flow within Neu.ro platform

With this action you may serve your data in Neu.ro cluster (storage folder, disk, etc.) using rclone's WebDAV server.

Check [live.yaml](./.neuro/live.yaml) for the usage example.

#### Inputs:
- `volume_remote` - Reference to the target served volume.
- `http_auth` - Whether to enable Neu.ro platform-based authentication or not.
    If disabled (by default) - your WebDAV will not be protected by Neu.ro SSO.
    It has no impact on `rclone serve webdav` parameters though.
- `port` - Rclone WebDAV server port. Useful if you want to access the server within the cluster, for instance, from another job.
- `extra_params` - Extra parameters for `rclone serve webdav` command invocation.
