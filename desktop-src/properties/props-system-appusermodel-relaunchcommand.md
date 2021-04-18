---
description: Especifica um comando que pode ser executado por meio de ShellExecute para iniciar um aplicativo quando ele é fixado na barra de tarefas ou quando uma nova instância do aplicativo é iniciada por meio da lista de atalhos do aplicativo.
ms.assetid: 83aab060-0629-48e3-a2db-9ba96a8631e5
title: System. AppUserModel. RelaunchCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84049f605896ba5e99a98f33557e6ee4dea37df5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771511"
---
# <a name="systemappusermodelrelaunchcommand"></a>System. AppUserModel. RelaunchCommand

Especifica um comando que pode ser executado por meio de [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) para iniciar um aplicativo quando ele é fixado na barra de tarefas ou quando uma nova instância do aplicativo é iniciada por meio da lista de atalhos do aplicativo.

Os exemplos incluem o seguinte:


```
shell:::{ED228FDF-9EA8-4870-83B1-96B02CFE0D52}

virtualhost.exe /virtualapp:12345

notepad.exe
```



Essa propriedade só será usada se uma janela tiver uma ID de modelo de usuário de aplicativo explícita (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), definida por meio de [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)). Se a janela não tiver um AppUserModelID explícito, essa propriedade será ignorada e a janela será agrupada e fixada como se fosse parte do processo que a possui. Para obter mais informações sobre a aplicação de AppUserModelIDs explícitas e seu efeito na fixação da barra de tarefas, consulte [IDs do modelo de usuário do aplicativo (AppUserModelIDs)](../shell/appids.md).

Essa propriedade deve ser usada por aplicativos ou Windows que desejem fornecer informações de reinicialização não padrão.

> [!Note]  
> [System. AppUserModel. RelaunchCommand]() e [System. AppUserModel. RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) devem sempre ser definidos juntos. Se uma dessas propriedades não for definida, nenhuma será usada.

 

Essa propriedade, junto com [System. AppUserModel. RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md) e [System. AppUserModel. RelaunchIconResource](./props-system-appusermodel-relaunchiconresource.md) , pode ser usada para definir visualmente uma janela como um aplicativo para o usuário. Isso é útil para cenários de aplicativos host, em que uma única instância de host executa vários aplicativos filho. Por exemplo, uma máquina virtual que hospeda vários aplicativos virtualizados pode querer que esses aplicativos virtualizados apareçam como aplicativos individuais para o usuário. A máquina virtual pode rotular cada janela com um AppUserModelID explícito e as propriedades de reinicialização apropriadas para torná-los exibidos como aplicativos. O usuário poderia fixá-los na barra de tarefas e "reinicializar" a instância fixada.

> [!Note]  
> Essa propriedade será ignorada se [System. AppUserModel. PreventPinning](./props-system-appusermodel-preventpinning.md) for definido. Isso permite que um aplicativo controle o agrupamento de suas janelas atribuindo-lhes AppUserModelIDs explícitas, mas impedindo que essas janelas sejam fixadas.

 

Para definir essa propriedade em uma janela, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) para recuperar o repositório de propriedades da janela e use os métodos do que recuperou o objeto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para definir a propriedade [System. AppUserModel. RelaunchCommand]() dessa janela.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.AppUserModel.RelaunchCommand
   shellPKey = PKEY_AppUserModel_RelaunchCommand
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 2
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="remarks"></a>Comentários

Os valores de PKEY são definidos em Propkey. h.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[IDs de modelo de usuário de aplicativo (AppUserModelIDs)](../shell/appids.md)
</dt> <dt>

[System.AppUserModel.ID](./props-system-appusermodel-id.md)
</dt> <dt>

[propertyDescriptionList](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

[propertyDescription](./propdesc-schema-propertydescription.md)
</dt> <dt>

[searchInfo](./propdesc-schema-searchinfo.md)
</dt> <dt>

[labelInfo](./propdesc-schema-labelinfo.md)
</dt> <dt>

[typeInfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[aliasInfo](./propdesc-schema-aliasinfo.md)
</dt> <dt>

[stringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[booleanFormat](./propdesc-schema-booleanformat.md)
</dt> <dt>

[numberFormat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[enumeratedList](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[enumera](./propdesc-schema-enum.md)
</dt> <dt>

[enumRange](./propdesc-schema-enumrange.md)
</dt> <dt>

[imagem](./propdesc-schema-image.md)
</dt> <dt>

[drawControl](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[editControl](./propdesc-schema-editcontrol.md)
</dt> <dt>

[filterControl](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[queryControl](./propdesc-schema-querycontrol.md)
</dt> <dt>

[relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[relatedProperty](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
