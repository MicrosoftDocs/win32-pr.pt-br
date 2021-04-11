---
description: Especifica o nome de exibição usado para o atalho criado na barra de tarefas quando o usuário opta por fixar um aplicativo na barra de tarefas ou iniciar uma nova instância na lista de atalhos de seu botão.
ms.assetid: a149838b-83b6-44ce-b705-e2804efb3d31
title: System. AppUserModel. RelaunchDisplayNameResource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d79c22d0ccecb8bac86fe5ca3636ed10ed2ca50b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169586"
---
# <a name="systemappusermodelrelaunchdisplaynameresource"></a>System. AppUserModel. RelaunchDisplayNameResource

Especifica o nome de exibição usado para o atalho criado na barra de tarefas quando o usuário opta por fixar um aplicativo na barra de tarefas ou iniciar uma nova instância na lista de atalhos de seu botão. O valor dessa propriedade deve ser um dos seguintes:

-   Uma cadeia de caracteres de recurso indireto, como "@% systemdir% \\ system32 \\shell32.dll,-19263". Observe que o caractere ' @ ' é necessário para distinguir uma cadeia de caracteres indireta de uma cadeia de caracteres de texto sem formatação (descrita no próximo parágrafo com marcadores). Essa cadeia de caracteres indireta consiste em um arquivo binário e uma ID de recurso da cadeia de caracteres contida nesse binário. É altamente recomendável que você use esse formulário de cadeia de caracteres indireta, o que garante que o nome de exibição seja alterado adequadamente quando o idioma do sistema for alterado por meio da MUI (Multilingual User interface). O caractere '-' antes da ID do recurso é necessário.
-   Uma cadeia de caracteres de texto sem formatação que não aponta para um recurso. Isso só deve ser usado quando o nome de exibição é dinamicamente calculado ou obtido de uma fonte de dados que não oferece suporte a MUI. Por exemplo, a cadeia de caracteres pode ser o nome de um dispositivo, como "Microsoft Zune", em casos em que o aplicativo aparece quando o dispositivo é anexado ao computador.

> [!Note]  
> [System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md) e [System. AppUserModel. RelaunchDisplayNameResource]() devem sempre ser definidos juntos. Se uma dessas propriedades não for definida, nenhuma será usada.

 

Essa propriedade só será usada se uma janela tiver uma ID de modelo de usuário de aplicativo explícita (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), definida por meio de [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)). Se a janela não tiver um AppUserModelID explícito, essa propriedade será ignorada e a janela será agrupada e fixada como se fosse parte do processo que a possui. Para obter mais informações sobre a aplicação de AppUserModelIDs explícitas e seu efeito na fixação da barra de tarefas, consulte [IDs do modelo de usuário do aplicativo (AppUserModelIDs)](../shell/appids.md). Essa propriedade deve ser usada por aplicativos ou Windows que desejem fornecer informações de reinicialização não padrão. Para obter mais informações, consulte [System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).

> [!Note]  
> Essa propriedade será ignorada se [System. AppUserModel. PreventPinning](./props-system-appusermodel-preventpinning.md) for definido. Isso permite que um aplicativo controle o agrupamento de suas janelas atribuindo-lhes AppUserModelIDs explícitas, mas impedindo que essas janelas sejam fixadas.

 

Para definir essa propriedade em uma janela, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) para recuperar o repositório de propriedades da janela e use os métodos do que recuperou o objeto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para definir a propriedade [System. AppUserModel. RelaunchDisplayNameResource]() dessa janela.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.AppUserModel.RelaunchDisplayNameResource
   shellPKey = PKEY_AppUserModel_RelaunchDisplayNameResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 4
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

 

 
