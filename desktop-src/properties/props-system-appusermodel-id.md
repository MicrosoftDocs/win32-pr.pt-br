---
description: Um AppUserModelID (ID do modelo de usuário) do aplicativo explícito usado para associar processos, arquivos e janelas a um aplicativo específico.
ms.assetid: 07858b3c-e601-40ec-a87a-d66612d5473a
title: System.AppUserModel.ID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd60b64598a620221ec2b610b10cbc05002f38aaf633e51e788b24797620cab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033734"
---
# <a name="systemappusermodelid"></a>System.AppUserModel.ID

Um AppUserModelID (ID do modelo de usuário) do aplicativo explícito usado para associar processos, arquivos e janelas a um aplicativo específico. Em alguns casos, é suficiente contar com o AppUserModelID interno atribuído a um processo pelo sistema. No entanto, um aplicativo que possui vários processos ou um aplicativo que está sendo executado em um processo de host pode precisar se identificar explicitamente por meio dessa propriedade para que ele possa agrupar suas janelas diferentes em um único botão da barra de tarefas e controlar o conteúdo da lista de atalhos desse aplicativo.

Para definir essa propriedade em uma janela, use [**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) para recuperar o repositório de propriedades da janela e use os métodos do que recuperou o objeto [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para definir a propriedade [System.AppUserModel.ID]() dessa janela.

Para obter mais informações, consulte [IDs de modelo de usuário de aplicativo (AppUserModelIDs)](../shell/appids.md).

No momento em que a propriedade [System.AppUserModel.ID]() é definida, a barra de tarefas é notificada para atualizar suas informações na janela ou no atalho dado a este AppUserModelID.

Outras propriedades de janela e de atalho podem ser usadas em conjunto com um AppUserModelID explícito para controlar ainda mais o agrupamento e a fixação associados a uma janela, o nome de exibição e o ícone usado para ele na barra de tarefas e o comando para iniciar um aplicativo fixado na barra de tarefas ou uma nova instância do aplicativo por meio da lista de atalhos desse aplicativo. Essas propriedades devem ser definidas antes da definição da propriedade [System.AppUserModel.ID]() . Para obter mais informações, consulte estes tópicos:

-   [System. AppUserModel. PreventPinning](./props-system-appusermodel-preventpinning.md)
-   [System. AppUserModel. RelaunchCommand](./props-system-appusermodel-relaunchcommand.md)
-   [System. AppUserModel. RelaunchDisplayNameResource](./props-system-appusermodel-relaunchdisplaynameresource.md)
-   [System. AppUserModel. RelaunchIconResource](./props-system-appusermodel-relaunchiconresource.md)

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, versão 1703, Windows 10, versão 1607, Windows 10, versão 1511, Windows 10, versão 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.AppUserModel.ID
   shellPKey = PKEY_AppUserModel_ID
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 5
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

[**SHGetPropertyStoreForWindow**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)
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

 

 
