# iOS-backup-tool
- A Linux CLI tool to backup and restore your iOS device.
- Tested on iPhone 14 plus, iOS 26.0 (23A341)
# Features
- Automatic device detection
- Encrypted backup support
- Automatic cleanup of old backups
- Comprehensive logging
- Configuration management
- Device information display
- Cross-distribution support

# Security Notes
- Backups are stored in your home directory
- Encryption uses Apple's built-in encryption when enabled
- Always test restores with non-critical data first

# How to use
## Install the tool:
```chmod +x install.sh```
```./install.sh```

## Install dependencies
ios-backup-tool install-deps

*you may also need to run but may not be required*
sudo apt install libimobiledevice6 libimobiledevice-utils 

## Backup your iOS device
ios-backup-tool backup

*if phone is not being detected, run below commands*
sudo systemctl stop usbmuxd
sudo systemctl start usbmuxd

## List available backups:
ios-backup-tool list

## Restore from backup
ios-backup-tool restore /path/to/backup

## Clean up old backups
ios-backup-tool clean 5
