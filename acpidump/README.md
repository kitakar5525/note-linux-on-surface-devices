- dump tables
```
sudo acpidump > acpidump.dat
```

- extract all the tables
```
acpixtract -a acpidump.dat
```

- move `acpidump.dat` to another location
```
mv acpidump.dat ../
```

- disassemble the tables
```
iasl -d *
```

- disassemble the dsdt table with external symbol resolution
```
iasl -e ssdt* -d dsdt.dat
```