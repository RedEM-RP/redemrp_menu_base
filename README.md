# redemrp_menu_base
 A Menu Base for RedEM:RP
This script allows you create menu like RDR2.

## 1. Installation
- Be sure you have RedEM and RedEM:RP Installed
if not -> [RedEM](https://github.com/kanersps/redem) --> [RedEM:RP](https://github.com/RedEM-RP/redem_roleplay)
- Clone redemrp_menu_base into [redemrp] folder
- add ```ensure redemrp_menu_base``` after ```ensure redem_roleplay```

![alt text](https://i.imgur.com/713zDs6.png)

![alt text](https://i.imgur.com/Uk0Ls4w.png)

## 2.Usage
Add this on top your client side file
```
MenuData = {}
TriggerEvent("redemrp_menu_base:getData",function(call)
    MenuData = call
end)
```
Example:
```
         MenuData.CloseAll()
        local elements = {
 
                {label = "Test Option", value = 'test' , desc = "Press if you want print text"},
                {label = "Hop Test", value = 0  ,desc = "Look its so fast" , type = "slider" , min =0 , max =100, hop= 5},
        }
 
       MenuData.Open(
 
                'default', GetCurrentResourceName(), 'test_menu',
 
                {
 
                        title    = 'TestMenu',
                        
                        subtext    = 'There is a subtext',
 
                        align    = 'top-left',
 
                        elements = elements,
 
                },
                function(data, menu)

                        if(data.current.value == 'test') then
                               print("test")
                        end
                end,
                
                function(data, menu)
                        menu.close()
              end)  

```

## 3.Credits
- https://github.com/ktos93
- https://github.com/ESX-Org
