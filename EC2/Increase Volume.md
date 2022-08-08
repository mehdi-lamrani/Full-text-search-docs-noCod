### Before 

![disk-before](https://user-images.githubusercontent.com/28993140/183415212-34564e6c-6470-42e8-81d9-ed6c65abd9c7.png)

```console
lsblk
```

### Grow disk

![disk-grow](https://user-images.githubusercontent.com/28993140/183415220-0b2936a1-7fad-49e7-8567-d4e2cb7c38e2.png)

```console
sudo growpart /dev/nvme0n1 1
```

### After

![disk-after](https://user-images.githubusercontent.com/28993140/183415230-eaa0bab4-8771-4b11-9674-906b7183883e.png)

```console
lsblk
```
