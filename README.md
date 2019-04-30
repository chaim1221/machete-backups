inside container...

```
   $  export AZURE_STORAGE_ACCOUNT=backuptestaccount
   $  export AZURE_STORAGE_ACCESS_KEY="some_long_secret"
   $  echo $AZURE_STORAGE_ACCESS_KEY 
   $  blobfuse /mount/this/ --tmp-path=/mnt/blobfusetmp/ -o allow_root -o attr_timeout=240 -o entry_timeout=240 -o negative_timeout=120 --log-level=LOG_DEBUG --file-cache-timeout-in-seconds=120 --container-name=containerbackuptest
```

skipping actual run command but basically for Chef you just have to mount the backups volume as /mount/backups...
