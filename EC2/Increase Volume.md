### Parition - Before 

![disk-before](https://user-images.githubusercontent.com/28993140/183415212-34564e6c-6470-42e8-81d9-ed6c65abd9c7.png)

```console
lsblk
```

### Parition - Grow 

![disk-grow](https://user-images.githubusercontent.com/28993140/183415220-0b2936a1-7fad-49e7-8567-d4e2cb7c38e2.png)

```console
sudo growpart /dev/nvme0n1 1
```


### Parition - After

![disk-after](https://user-images.githubusercontent.com/28993140/183415230-eaa0bab4-8771-4b11-9674-906b7183883e.png)

```console
lsblk
```

### File System - Before :

```console
sudo xfs_growfs /
```
![df-before](https://user-images.githubusercontent.com/28993140/183418765-8000a50d-816a-442a-9731-2f1808b7718d.png)


### File System - Grow :

![grow-fs](https://user-images.githubusercontent.com/28993140/183419210-5503e0d9-68fc-4222-8a97-084c30bf22e6.png)

### File System - After :

![df-after](https://user-images.githubusercontent.com/28993140/183419191-65734ffc-469d-4737-8cfb-6d80cbc27d41.png)

