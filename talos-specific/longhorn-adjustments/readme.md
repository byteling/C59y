## Notes

edit machineconfig interactively, using:

```sh
talosctl -n IP apply machineconfig --mode=interactive
```

or apply directly using (needs more params)

```sh
talosctl -n <IP> apply-config -f config.yaml
```
