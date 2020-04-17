# esx_service

## 下载 & 安装

### 使用 Git
```
cd resources
git clone https://github.com/ESX-CN/esx_service [esx]/esx_service
```

### 手动
- 下载 https://github.com/ESX-CN/esx_service/archive/master.zip
- 解压至 `[esx]` 目录

## 安装
- 添加下列内容至你的 `server.cfg`:
```
start esx_service
```
## 使用教程
```lua
-- Enable service
ESX.TriggerServerCallback('esx_service:enableService', function(canTakeService, maxInService, inServiceCount)

  if canTakeService then
    ESX.ShowNotification('You enabled service')
  else
    ESX.ShowNotification('Service is full: ' .. inServiceCount .. '/' .. maxInService)
  end

end, 'taxi')

-- Disable service
TriggerServerEvent('esx_service:disableService', 'taxi')
```

# Legal
### License
esx_service - be in service

Copyright (C) 2015-2020 Jérémie N'gadi

This program Is free software: you can redistribute it And/Or modify it under the terms Of the GNU General Public License As published by the Free Software Foundation, either version 3 Of the License, Or (at your option) any later version.

This program Is distributed In the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty Of MERCHANTABILITY Or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License For more details.

You should have received a copy Of the GNU General Public License along with this program. If Not, see http://www.gnu.org/licenses/.
