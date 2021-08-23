---
title: Media.name
description: A propriedade Name especifica ou recupera o nome do item de mídia.
ms.assetid: 68aba78a-86fd-4411-9ac4-58f38d915e2c
keywords:
- Windows Media Player Media.name
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
ms.openlocfilehash: 3abe6df00b5674cfbd443a5838b208814e30c5ecf75875586907314fc3a39d9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119616852"
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

o exemplo a seguir JScript usa *mídia*. **nome** para alterar o nome do item de mídia atual. Um elemento de entrada de texto HTML chamado NameText permite que o usuário insira uma cadeia de texto para o novo nome. O objeto de **jogador** foi criado com ID = "Player".


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

[**Configurações. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





