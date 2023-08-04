# Info os :desktop_computer:

### Language and module:

* Python
<img src="https://raw.githubusercontent.com/devicons/devicon/1119b9f84c0290e0f0b38982099a2bd027a48bf1/icons/python/python-original.svg" width="40" height="40"/>
* WMI 1.5.1
-----

### Cod:

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
------

<div id="badges">
  <a href="https://vk.com/aniime_guy">
    <img src="https://img.icons8.com/?size=512&id=13977&format=png"width="40" height="40"/>
  </a>
  <a href="https://t.me/Ilham06">
    <img src="https://img.icons8.com/?size=512&id=63306&format=png"width="40" height="40"/>
  </a>
  <a href="https://www.youtube.com/channel/UC9m1N5x0OXWihGpR50Yk35g">
    <img src="https://img.icons8.com/?size=512&id=13983&format=png"width="40" height="40" />
  </a>
</div>
