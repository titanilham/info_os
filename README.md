# info_os

## Language:
* Python

```python

class OsSistem:
    def os():
        import wmi
        computer = wmi.WMI()
        computer_info = computer.Win32_ComputerSystem()[0]
        os_info = computer.Win32_OperatingSystem()[0]
        proc_info = computer.Win32_Processor()[0]
        gpu_info = computer.Win32_VideoController()[0]

        os_name = os_info.Name.encode('utf-8').split(b'|')[0]
        os_version = ' '.join([os_info.Version, os_info.BuildNumber])
        system_ram = float(os_info.TotalVisibleMemorySize) / 1048576  
        lol = ("OS: {}".format(os_info.Caption), 'CPU: {0}'.format(proc_info.Name), 'RAM: {0} GB'.format(system_ram), 'GPU: {0}'.format(gpu_info.Name))
        lol = list(lol)
        return "\n".join(lol)

print(OsSistem.os())

```
