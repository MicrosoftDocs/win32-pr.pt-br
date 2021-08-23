---
title: Método mediacollection. setdeleted
description: O método setdeled move o item de mídia especificado para a pasta itens excluídos. | Método mediacollection. setdeleted
ms.assetid: 3e3c9a16-37e1-41b4-8593-58aaf4541eb9
keywords:
- método setdeled Windows Media Player
- método setdeled Windows Media Player, classe mediacollection
- classe mediacollection Windows Media Player, método setdeleted
topic_type:
- apiref
api_name:
- MediaCollection.setDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63dcb4c0062acbd5f457cd09b9c1370ff9c4f7683fd8758a4a64ce5f510a6948
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119647836"
---
# <a name="mediacollectionsetdeleted-method"></a>Método mediacollection. setdeleted

O método **Setdeled** move o item de mídia especificado para a pasta itens excluídos.

## <a name="syntax"></a>Sintaxe


```JScript
MediaCollection.setDeleted(
  item,
  true
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Item* \[ de no\]
</dt> <dd>

Objeto de **mídia** que está sendo movido.

</dd> <dt>

*verdadeiro* \[ no\]
</dt> <dd>

Sempre Especifique esse valor.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método não remove arquivos do computador do usuário.

Para usar esse método, é necessário ter acesso completo à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

**Windows Media Player 10 Mobile:** Não há suporte para esse método.

## <a name="examples"></a>Exemplos

o exemplo a seguir JScript usa *mediacollection*. **Setdeled** para mover um item de mídia específico, armazenado na variável chamada mediaobject, para a pasta itens excluídos. O *mediacollection*. o método **IsDeleted** testa primeiro se o item já foi excluído. O objeto de **jogador** foi criado com ID = "Player".


```JScript
// Test whether the media item is in the deleted items folder.
if (!Player.mediaCollection.isDeleted(mediaObject)){

    // The item is available to be deleted; move it to 
    // the deleted items folder.
    Player.mediaCollection.setDeleted(mediaObject, true);

    // Inform the user that the operation succeeded.
    alert("Item moved to deleted items folder.");}

else
    // Tell the user the operation is unnecessary.
    alert("Item is already deleted!");
}

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0, Windows Media Player versão 7,1 ou Windows Media Player para Windows XP. não há suporte para esse método no Windows Media Player 9 Series ou posterior.<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                                                              |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de mídia**](media-object.md)
</dt> <dt>

[**Objeto mediacollection**](mediacollection-object.md)
</dt> <dt>

[**Mediacollection. IsDeleted**](mediacollection-isdeleted.md)
</dt> <dt>

[**Configurações. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





