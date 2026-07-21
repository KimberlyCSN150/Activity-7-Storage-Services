# Activity 7: Storage Services

Working with Disk Management on the domain controller: shrinking volumes, creating new ones, and covering the different volume/RAID types.

## Steps

- [ ] Boot the domain controller
- [ ] Open Computer Management → Disk Management
- [ ] Shrink the C: volume by 1000 MB to free up unallocated space
- [ ] On the 1000 MB unallocated space, create a **simple volume** of 500 MB
  - Assign drive letter **E** (avoid A/B — reserved historically for floppy drives)
  - Choose between NTFS and ReFS (Resilient File System — enhanced NTFS with better data protection/scalability)
  - Format as NTFS, quick format
  - Capture a screenshot
- [ ] On the remaining 500 MB unallocated space, review volume type options (see below) before creating one
- [ ] Extend the E: drive by 250 MB (right-click → Extend Volume)
- [ ] Capture a screenshot
- [ ] Right-click Disk 0 and review the option to convert to a dynamic disk

## Volume types covered
| Type | Description |
|---|---|
| **Simple** | Single physical volume |
| **Spanned** | Combines space across more than one physical disk into a single volume |
| **Striped (RAID 0)** | 2+ disks, data spread for high read performance, no redundancy |
| **Mirrored (RAID 1)** | 2 disks holding identical data, for redundancy |
| **RAID 5** | 3+ disks; parity spread across disks — balances protection and performance; a single drive failure is recoverable from parity data, at some write-performance cost |

## Basic vs. Dynamic disks
- **Basic disk** — partition info stored with the OS; the standard, widely compatible option
- **Dynamic disk** — partition info stored on the disk itself; not compatible with OS versions before Windows 2000; converting back to basic requires wiping the disk first

<img width="973" height="1100" alt="image" src="https://github.com/user-attachments/assets/08d29198-4043-4d0f-bb50-aa63de534809" />

<img width="973" height="1083" alt="image" src="https://github.com/user-attachments/assets/6c716379-561f-45a7-a4b2-a3b24f1a6e04" />

<img width="975" height="1102" alt="image" src="https://github.com/user-attachments/assets/35de7bc8-97f9-4d53-b83b-7cf77a5c1d26" />





## Screenshots to capture
- [ ] Simple volume creation (E: drive)
- [ ] Extended E: drive at 250 MB
