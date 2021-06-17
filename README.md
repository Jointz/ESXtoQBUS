# QbusToEsx Converting Qbus Scripts to ESX.
---------------------------------------------------------------- ------------------------------------------------
Qbus Foundation And ESX foundation.
 ``
QBCore = nil 

Citizen.CreateThread(function()
 while QBCore == nil do
 TriggerEvent('QBCore:GetObject', function(obj) QBCore = obj end)
 Citizen.Wait(30) -- Second Wait
 end
end)
```
# ABOVE QBUSCORE

# ESX BELOW
``
ESX = nil

Citizen.CreateThread(function()
 while ESX == nil do
 TriggerEvent('esx:getSharedObject', function(obj) ESX = obj end)
 Citizen.Wait(30)-- Second Wait
 end
end)
```
---------------------------------------------------------------- ------------------------------------------------
Gentlemen, this section was added.
Meaning:
The Player's Input Part is required when entering the game, that is, it is the server file.
This event is triggered when the player connects to the server
``
RegisterNetEvent('QBCore:Client:OnPlayerLoaded')
AddEventHandler('QBCore:Client:OnPlayerLoaded',
```
# ABOVE QBUSCORE

# ESX BELOW
``
RegisterNetEvent('esx:playerLoaded')
AddEventHandler('esx:playerLoaded',
```
---------------------------------------------------------------- ------------------------------------------------
Server File, Job Part is Occupation Part.
``
RegisterNetEvent('QBCore:Client:OnJobUptade')
AddEventHandler('QBCore:Client:OnJobUptade', 
```
# ABOVE QBUSCORE

# ESX BELOW
``
RegisterNetEvent('esx:setJob')
AddEventHandler('esx:setJob',
```
---------------------------------------------------------------- ------------------------------------------------
You Can Check Here.
https://esx-framework.github.io/es_extended/common/events/onplayerdeath/#example-client-side-usage
``
RegisterNetEvent('QBCore:Client:OnPlayerUnload')
AddEventHandler('QBCore:Client:OnPlayerUnload',
```
# ABOVE QBUSCORE

# ESX BELOW
``
RegisterNetEvent('esx:onPlayerDeath')
AddEventHandler('esx:onPlayerDeath',
```
---------------------------------------------------------------- ------------------------------------------------
Gentlemen, this section was added.
Meaning:
This function gets the nearest player client id and distance to the player.
``
QBCore.Functions.GetClosestPlayer()
```
# ABOVE QBUSCORE

# ESX BELOW
``
ESX.Game.GetClosestPlayer()
```
---------------------------------------------------------------- ------------------------------------------------
Adding 3D Text, Cilent File. Example : https://media.discordapp.net/attachments/623207764314816562/812096508786507806/image_1.png
``
QBCore.Functions.DrawText3D(1, 1, 1, 'Example')
```
# ABOVE QBUSCORE

# ESX BELOW
``
DrawText3D(1, 1, 1, 'Example') -- (You need to open function below.)
```
---------------------------------------------------------------- ------------------------------------------------
Menu Open Close Menus in ESX & QBCore Examples: https://prnt.sc/u4f7s5
``
QBCore.UI.Menu.Open
QBCore.UI.Menu.CloseAll() -- (you need to install menu default script.)
```
# ABOVE QBUSCORE

# ESX BELOW
``
ESX.UI.Menu.Open
ESX.UI.Menu.CloseAll()
```
---------------------------------------------------------------- ------------------------------------------------
Notification Script Example: https://dosya.turkmmo.com/2020/09/36521_efa54848705a4069cbedfc2770e50cf1.png
``
QBCore.Functions.Notify("Tool locked.", "error")
```
# ABOVE QBUSCORE

# ESX BELOW
``
TriggerEvent('Notification',"Example.")
```
---------------------------------------------------------------- ------------------------------------------------
Inventory Item Section.
``
xPlayer.Functions.GetItemByName 
```
# ABOVE QBUSCORE

# ESX BELOW
``
xPlayer.getInventoryItem
```
---------------------------------------------------------------- ------------------------------------------------
Job Setup Section Code.
``
Player.PlayerData.job.name 
```
# ABOVE QBUSCORE

# ESX BELOW
``
ESX.PlayerData.job.name
```
---------------------------------------------------------------- ------------------------------------------------
Give Money Get Money Section
``
ply.Functions.AddMoney('bank', amount, "Bank deposit") -- bank
ply.Functions.RemoveMoney('cash', amount, "Bank deposit") -- money on it
```
# ABOVE QBUSCORE

# ESX BELOW
``
xPlayer.removeAccountMoney('bank', amount) --remove money
xPlayer.addMoney(amount) -- add money
```
---------------------------------------------------------------- ------------------------------------------------
Money Part Data.
``
ply.PlayerData.money["bank"]
```
# ABOVE QBUSCORE

# ESX BELOW
``
xPlayer.getAccount('bank').money
```
---------------------------------------------------------------- ------------------------------------------------
Inventory Item Deletion Section.
``
xPlayer.Functions.RemoveItem 
```
# ABOVE QBUSCORE

# ESX BELOW
``
xPlayer.removeInventoryItem 
```
---------------------------------------------------------------- ------------------------------------------------
Adding Inventory Items.
``
xPlayer.Functions.AddItem
```
# ABOVE QBUSCORE

# ESX BELOW
``
xPlayer.addInventoryItem
```
---------------------------------------------------------------- ------------------------------------------------
The Character Is Something Like The Id Of The Player.
``
QBCore.Functions.GetPlayer(src)
```
# ABOVE QBUSCORE

# ESX BELOW
``
ESX.GetPlayerFromId(src)
```
---------------------------------------------------------------- ------------------------------------------------
This function trims a text, removing all trailing white spaces. Usually `GetVehicleNumberPlateText()` is used when sanitizing locals.
#sample
``
QBCore.Functions.MathTrim(GetVehicleNumberPlateText(vehicle))
````
#standard
``
QBCore.Functions.MathTrim 
```
# ABOVE QBUSCORE

# ESX BELOW
``
ESX.Math.Trim(value)
```
---------------------------------------------------------------- ------------------------------------------------
Nill is unknown in this will be updated
# SAMPLE
``
QBCore.Functions.MathRound(GetVehicleBodyHealth(vehicle), 1),
```
#standard
``
QBCore.Functions.MathRound()
```
# ABOVE QBUSCORE

# ESX BELOW
# SAMPLE
``
local value - 5.444

print('value:' ..value) - returns 5,444 --
print('value rounded:' .. ESX.Math.Round(value)) -- returns 5
print ('value rounded:' .. ESX.Math.Round(value, 1)) -- returns 5.4
```
#standard
``
ESX.Math.Round(value, numberDecimals)
```
---------------------------------------------------------------- ------------------------------------------------
Car Spawn Part Location Vsb Stuff.
``
QBCore.Functions.SpawnVehicle()
QBCore.Functions.GetVehicleProperties()
QBCore.Functions.GetClosestVehicle()
```
# ABOVE QBUSCORE

# ESX BELOW
``
ESX.Game.SpawnVehicle()
ESX.Game.GetVehicleProperties()
ESX.Game.GetClosestVehicle()
```
--(Almost everything that is ESX.Game is the same as QBCore.Functions.)
---------------------------------------------------------------- ------------------------------------------------
Player Your Character.
``
QBCore.Functions.GetPlayerData()
```
# ABOVE QBUSCORE

# ESX BELOW
``
ESX.GetPlayerData()
```
---------------------------------------------------------------- ------------------------------------------------
Item Creation.
``
QBCore.Functions.CreateUseableItem()
```
# ABOVE QBUSCORE

# ESX BELOW
``
ESX.RegisterUsableItem()
```
---------------------------------------------------------------- ------------------------------------------------
Bank Money Removal.
``
Player.Functions.RemoveMoney()
```
# ABOVE QBUSCORE

# ESX BELOW
``
xPlayer.removeMoney(money)
```
---------------------------------------------------------------- ------------------------------------------------
About Files.
``
QBCore.Functions.CreateCallback()
```
# ABOVE QBUSCORE

# ESX BELOW
``
ESX.RegisterServerCallback()
```
---------------------------------------------------------------- ------------------------------------------------
About Files.
``
QBCore.Functions.TriggerCallback()
```
# ABOVE QBUSCORE

# ESX BELOW
``
ESX.TriggerServerCallback()
```
---------------------------------------------------------------- ------------------------------------------------
identifier is used in cid esx in qb I left a small code block for you to solve the event.
``
QBCore.Functions.CreateCallback('system:fetchStatus', function(source, cb)
 local Player = QBCore.Functions.GetPlayer(source)

 if Player then
 exports['ghmattimysql']:execute('SELECT skills FROM players WHERE citizenid = @citizenid', {
 ['@citizenid'] = Player.PlayerData.citizenid
 }, function(status)
 if status ~= nil then
 cb(json.decode(status))
 else
 cb(nil)
 end
 end)
 else
 cb()
 end
end)
```
# ABOVE QBUSCORE

# ESX BELOW
``
ESX.RegisterServerCallback("system:fetchStatus", function(source, cb)
 local src = source
 local user = ESX.GetPlayerFromId(src)


 local fetch = [[
 SELECT
 skills
 FROM
 users
 WHERE
 identifier = @identifier
 ]]

 MySQL.Async.fetchScalar(fetch, {
 ["@identifier"] = user.identifier

 }, function(status)

 if status ~= nil then
 cb(json.decode(status))
 else
 cb(nil)
 end

 end)
end)
```
---------------------------------------------------------------- ------------------------------------------------
SQL binding part
``
QBCore.Functions.ExecuteSql()
```
# ABOVE QBUSCORE

# ESX BELOW
``
ESX.ExecuteSql() --(ghmattimysql)
MySQL.Async.execute()
```
---------------------------------------------------------------- ------------------------------------------------
RegisterCommand - the chat command part.
``
QBCore.Commands.Add()
```
# ABOVE QBUSCORE

# ESX BELOW
``
RegisterCommand 
```
-- (RegisterCommand also works in qbcore.)
---------------------------------------------------------------- ------------------------------------------------
Character Part Dir Data Test Binding.
``
local Player = QBCore.Functions.GetPlayer(source)
['@citizenid'] = Player.PlayerData.citizenid
```
# ABOVE QBUSCORE

# ESX BELOW
``
local user : ESX.Get.PlayerFromId(src)
["@identifier"] = user.identifier
```
---------------------------------------------------------------- ------------------------------------------------
