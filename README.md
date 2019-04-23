# esx_inventoryhud
Inventário HUD para ESX. Você pode abrir e fechar o estoque usando F2. Parte do código foi tirada de [es_extended](https://github.com/ESX-Brasil/es_extended) .

## Requisitos
* [es_extended](https://github.com/ESX-Brasil/es_extended)

## Características
- Usando itens
- Soltando itens
- Dando itens
- Pesquisando inventário
- Dinheiro incluído
- Suporte de contas (banco, dinheiro sujo, ...)
- Totalmente configurável(check config.lua and html/js/config.js)
- Arquivos de local incluídos (check locales/ and html/locales/ directories)

## Screens
![screenshot](https://i.imgur.com/PRx3vX3.png)

## Download e Instalação

### Usando o Git
```
cd resources
git clone https://github.com/ESX-Brasil/esx_inventoryhud [esx]/esx_inventoryhud
```

### Manualmente
- Download https://github.com/ESX-Brasil/esx_inventoryhud/archive/master.zip
- Coloque-o no `[esx]` diretório

## Instalação
- Abrar `es_extended`, em seguida, localize e remova este código `client/main.lua`:
```
-- Menu interactions
Citizen.CreateThread(function()
	while true do

		Citizen.Wait(0)

		if IsControlJustReleased(0, Keys['F2']) and IsInputDisabled(0) and not isDead and not ESX.UI.Menu.IsOpen('default', 'es_extended', 'inventory') then
			ESX.ShowInventory()
		end

	end
end)
```
- Adicione isto ao seu `server.cfg`:

```
start esx_inventoryhud
```

## Arquivos de configuração
* config.lua
* html/js/config.js

# Creditos

Trsak

# Discord

[![Join ESX Brasil](https://discordapp.com/api/guilds/432980396070666250/embed.png?style=banner2)](https://discord.gg/8zGbh3T)


# Legal
### License
esx_inventoryhud - esx_inventoryhud ESX

Copyright (C) 2015-2018 ESX-Brasil

This program Is free software: you can redistribute it And/Or modify it under the terms Of the GNU General Public License As published by the Free Software Foundation, either version 3 Of the License, Or (at your option) any later version.

This program Is distributed In the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty Of MERCHANTABILITY Or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License For more details.

You should have received a copy Of the GNU General Public License along with this program. If Not, see http://www.gnu.org/licenses/.
