```
    1  mkdir /mnt/blobfusetmp
    2  chown $USER /mnt/blobfusetmp
    3  export AZURE_STORAGE_ACCOUNT=backuptestaccount
    4  export AZURE_STORAGE_ACCESS_KEY="some_long_secret"
    5  echo $AZURE_STORAGE_ACCESS_KEY 
    6  mkdir -p /mount/this
    7  blobfuse /mount/this/ --tmp-path=/mnt/blobfusetmp/  -o attr_timeout=240 -o entry_timeout=240 -o negative_timeout=120 --log-level=LOG_DEBUG --file-cache-timeout-in-seconds=120
    8  blobfuse /mount/this/ --tmp-path=/mnt/blobfusetmp/  -o attr_timeout=240 -o entry_timeout=240 -o negative_timeout=120 --log-level=LOG_DEBUG --file-cache-timeout-in-seconds=120 --container-name=containerbackuptest
    9  blobfuse /mount/this/ --tmp-path=/mnt/blobfusetmp/ -o allow_root -o attr_timeout=240 -o entry_timeout=240 -o negative_timeout=120 --log-level=LOG_DEBUG --file-cache-timeout-in-seconds=120 --container-name=containerbackuptest

```
