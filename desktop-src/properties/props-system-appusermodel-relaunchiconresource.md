---
description: Especifica o ícone usado para o atalho criado na barra de tarefas quando o usuário escolhe fixar um aplicativo na barra de tarefas ou iniciar uma nova instância por meio da lista de atalhos do botão.
ms.assetid: 3559d1f5-988c-41d9-ba9a-dfa4ba643ee2
title: System. AppUserModel. RelaunchIconResource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b43394bd5ee7dca6084526224dac268500f6881317215d63d6fc0e9a126c5b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118970835"
---
# <a name="systemappusermodelrelaunchiconresource"></a>System. AppUserModel. RelaunchIconResource

Especifica o ícone usado para o atalho criado na barra de tarefas quando o usuário escolhe fixar um aplicativo na barra de tarefas ou iniciar uma nova instância por meio da lista de atalhos do botão. Esse é o ícone usado para o grupo da barra de tarefas e é mostrado para um aplicativo fixado, independentemente de o aplicativo estar em execução ou não. Isso deve ser especificado em um dos seguintes formatos:

-   Formato de recurso padrão, como "% systemdir% \\ system32 \\shell32.dll,-128". O caractere '-' antes da ID do recurso é necessário. Não use o caractere ' @ ' na frente da cadeia de caracteres do caminho.
-   caminho direto para um arquivo de ícone, como "% programfiles% \\ Microsoft \\ Bloco de notas \\ Bloco de notas. ico, 0". Observe que, como os arquivos. ico podem conter vários recursos de ícone, uma ID de recurso é necessária na cadeia de caracteres. Se o arquivo. ico for uma única imagem, use "0" (sem o caractere "-") como a ID do recurso.

[System. AppUserModel. RelaunchIconResource]() é uma propriedade opcional. Se não estiver definido, o ícone do destino do comando de reinicialização ([System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md)) será usado. No entanto, como isso pode levar a resultados indesejados, é altamente recomendável que você forneça um ícone explicitamente por meio dessa propriedade.

Essa propriedade só será usada se uma janela tiver uma ID de modelo de usuário de aplicativo explícita (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), definida por meio de [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)). Se a janela não tiver um AppUserModelID explícito (System.AppUserModel.ID), essa propriedade será ignorada e a janela será agrupada e fixada como se fosse parte de seu processo de propriedade. Para obter mais informações sobre a aplicação de AppUserModelIDs explícitas e seu efeito na fixação da barra de tarefas, consulte [IDs do modelo de usuário do aplicativo (AppUserModelIDs)](../shell/appids.md). Essa propriedade deve ser usada por aplicativos ou Windows que desejem fornecer informações de reinicialização não padrão. Para obter mais informações, consulte [System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md).

Se um AppUserModelID explícito for definido na janela, mas essa propriedade não estiver definida, o sistema tentará localizar um atalho com o mesmo AppUserModelID e fixará esse atalho na barra de tarefas para representar a janela. Se esse atalho não puder ser localizado, o executável de backup do processo que o possui será usado.

> [!Note]  
> Essa propriedade será ignorada se [System. AppUserModel. PreventPinning](./props-system-appusermodel-preventpinning.md) for definido. Isso permite que um aplicativo controle o agrupamento de suas janelas atribuindo-lhes AppUserModelIDs explícitas, mas impedindo que essas janelas sejam fixadas.

 

Para definir essa propriedade em uma janela, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) para recuperar o repositório de propriedades da janela e use os métodos do que recuperou o objeto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para definir a propriedade [System. AppUserModel. RelaunchIconResource]() dessa janela.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a>Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1

```
propertyDescription
   name = System.AppUserModel.RelaunchIconResource
   shellPKey = PKEY_AppUserModel_RelaunchIconResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = false
```

## <a name="windows-8-windows-7"></a>Windows 8, Windows 7

```
propertyDescription
   name = System.AppUserModel.RelaunchIconResource
   shellPKey = PKEY_AppUserModel_RelaunchIconResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

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

 

 
