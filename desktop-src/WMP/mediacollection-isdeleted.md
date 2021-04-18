---
title: Método mediacollection. IsDeleted
description: O método IsDeleted recupera um valor que indica se o item de mídia especificado está na pasta itens excluídos.
ms.assetid: bb3ce9c9-9e43-45a5-8802-dc6783cf2ad7
keywords:
- método IsDeleted Windows Media Player
- método IsDeleted Windows Media Player, classe Mediacollection
- Classe mediacollection Windows Media Player, método IsDeleted
topic_type:
- apiref
api_name:
- MediaCollection.isDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd3cdc27c84c88eb65df5b7635f34c79c1b4fe82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813147"
---
# <a name="mediacollectionisdeleted-method"></a>Método mediacollection. IsDeleted

O método **IsDeleted** recupera um valor que indica se o item de mídia especificado está na pasta itens excluídos.

## <a name="syntax"></a>Sintaxe


```JScript
bRetVal = MediaCollection.isDeleted(
  item
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Item* \[ de no\]
</dt> <dd>

Objeto de **mídia** que pode ser excluído.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um **valor booleano**.

## <a name="remarks"></a>Comentários

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

**Windows Media Player 10 Mobile:** Esse método sempre retorna **false**.

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir usa *mediacollection*. **IsDeleted** para testar se um item de mídia específico, armazenado na variável chamada mediaobject, está na pasta itens excluídos. Se o item de mídia ainda não tiver sido excluído, ele será movido para a pasta itens excluídos. O objeto de **jogador** foi criado com ID = "Player".


```JScript
// Test whether the media item is in the deleted items folder.
if (!Player.mediaCollection.isDeleted(mediaObject)){

    // The media item is available to be deleted, move it to 
    // the deleted items folder.
    Player.mediaCollection.setDeleted(mediaObject, true);

    // Inform the user that the operation succeeded.
    alert("Media item moved to deleted items folder.");}

else
    // Tell the user the operation is unnecessary.
    alert("Item is already deleted!");
}

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0, Windows Media Player versão 7,1 ou Windows Media Player para Windows XP. Esse método não tem suporte no Windows Media Player 9 Series ou posterior.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                                                              |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de mídia**](media-object.md)
</dt> <dt>

[**Objeto mediacollection**](mediacollection-object.md)
</dt> <dt>

[**Mediacollection. setdeleted**](mediacollection-setdeleted.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





