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