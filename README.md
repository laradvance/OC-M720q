# OC-M720q
Opencore for lenovo m720q
Core i5 8700T
BCM943224PCIEBT2 Wifi Card
Big Sur 11.2.3


Enable HiDPI:
1. bash -c "$(curl -fsSL https://raw.githubusercontent.com/xzhih/one-key-hidpi/master/hidpi.sh)"

Optimize power management using CPUFriend

1. Download [ssdtprgen](https://github.com/ibash/ssdtPRGen.sh/archive/coffee_lake.zip)
2. Unzip and copy the files to ~/Library/ssdtPRGen
3. Under ssdtprgen/Data folder, open user defined.cfg file and add your cpu details below
the text gUserDefinedCPUList=(
i5-8400T,35,1200,1700,3300,6,6
4. Go to ssdtprgen folder and run the command ./ssdtprgen.sh It will generate dsl and aml. 
5. Download [cpufriend](https://github.com/acidanthera/CPUFriend/releases/download/1.2.2/CPUFriend-1.2.2-RELEASE.zip) extract and run the command
./ResourceConverter.sh --kext <drag the aml file generated above here> cpufrienddataprovider kext will be created
6. Include cpufriend kext and cpufrienddataprovider kext in your bootloader
