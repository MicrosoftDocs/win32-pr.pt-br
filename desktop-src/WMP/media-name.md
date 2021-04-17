---
title: Media.name
description: A propriedade Name especifica ou recupera o nome do item de mídia.
ms.assetid: 68aba78a-86fd-4411-9ac4-58f38d915e2c
keywords:
- Media.name Windows Media Player
topic_type:
- apiref
api_name:
- Media.name
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9de8095d88c3ddec9049e0b43461adcf5553ec74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105763841"
---
# <a name="medianame"></a>Media.name

A propriedade **Name** especifica ou recupera o nome do item de mídia.

## <a name="syntax"></a>Syntax

*Player*. *currentMedia*. **nome** do

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é uma **cadeia de caracteres** de leitura/gravação que contém o nome do item de mídia.

## <a name="remarks"></a>Comentários

Para recuperar o valor dessa propriedade, é necessário ter acesso de leitura à biblioteca. Para especificar o valor dessa propriedade, é necessário ter acesso completo à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

Antes de usar esse método para especificar o nome de um item de mídia, use **isReadOnlyItem** para determinar se o nome pode ser definido.

**Windows Media Player 10 Mobile:** Esta propriedade é somente leitura.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa *mídia*. **nome** para alterar o nome do item de mídia atual. Um elemento de entrada de texto HTML chamado NameText permite que o usuário insira uma cadeia de texto para o novo nome. O objeto de **jogador** foi criado com ID = "Player".


```JScript
<!<entity type="mdash"/>-Create an HTML BUTTON element to execute the name change. -->
<INPUT type = "BUTTON"  id = "NewName"  name = "NewName"  value = "Change Name" 
    onClick = "

        /* Store the current media item. */
        var cm = Player.currentMedia;

        /* Change the name. */
        cm.name = NameText.value;
">

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de mídia**](media-object.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





