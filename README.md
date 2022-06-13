# xbackup

Export/Backup all IGC files you have uploaded to DHV-XC. In combination
with xccat (https://github.com/abbbi/xccat) can also download published flights
from other persons uploaded to DHV-XC.

![Alt text](screenshot.jpg?raw=true "Screenshot")

# Usage
```
Usage:
  xcbackup [OPTIONS]

Application Options:
  -u, --user= DHV-XC User name
  -p, --pass= DHV-XC User Password
  -d, --dir=  Target directory
  -l, --list  List flights only, do not download
  -i, --id=   Download flight with specific ID only (default: 0)

Help Options:
  -h, --help  Show this help message
```

# Examples

List flights (do not download):
```
# xcbackup -u username -p password -l --dir backup/
INFO[0000] Flight ID: [1543836] Takeoff: [Rottach-Egern, Miesbach, Bayern] Date: [2022-06-11]
INFO[0000] Flight ID: [1541261] Takeoff: [Rottach-Egern, Miesbach, Bayern] Date: [2022-05-26]
INFO[0000] Flight ID: [1541256] Takeoff: [Rottach-Egern, Miesbach, Bayern] Date: [2022-06-06]
```

Complete backup of all flights:
```
# xcbackup -u username -p password --dir backup/
INFO[0003] Saving flight: [1129188] to: [backup/2019-05-24/1129188.igc]
INFO[0003] Saving flight: [1186753] to: [backup/2019-08-30/1186753.igc]
INFO[0003] Saved [159] flights
```

Download specifc flight either from your profile or a public flight
uploaded by another person:

```
# xcbackup -u username -p password  -i 1547554 --dir backup/
INFO[0000] Saving flight: [1547617] to: [backup/today/1547617.igc] 
INFO[0000] Saved [1] flights
```
