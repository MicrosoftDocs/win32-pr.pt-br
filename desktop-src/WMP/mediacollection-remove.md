---
title: Método mediacollection. Remove
description: O método remove remove um item da coleção de mídia.
ms.assetid: 7d4c03ed-01c8-4112-90b6-5de52eacb199
keywords:
- remover método Windows Media Player
- Método Remove Windows Media Player, classe Mediacollection
- Classe mediacollection Windows Media Player, remover método
topic_type:
- apiref
api_name:
- MediaCollection.remove
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6667a5b95920ac63f38d3a581e6f8e05bdf8d233
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782981"
---
# <a name="mediacollectionremove-method"></a>Método mediacollection. Remove

O método **Remove** remove um item da coleção de mídia.

## <a name="syntax"></a>Sintaxe


```JScript
MediaCollection.remove(
  item,
  delete
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Item* \[ de no\]
</dt> <dd>

Objeto de **mídia** a ser removido.

</dd> <dt>

*excluir* \[ no\]
</dt> <dd>

**Booliano** que indica se o item deve ser removido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método exclui um item da biblioteca. Esse método não exclui arquivos do computador do usuário.

Para usar esse método, é necessário ter acesso completo à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="examples"></a>Exemplos

O exemplo de JScript a seguir, depois de solicitar o usuário, exclui permanentemente o primeiro item de mídia na coleção de mídia usando *mediacollection*. **remover**. O objeto de **jogador** foi criado com ID = "Player".


```JScript
// Retrieve the first item from the media collection.
var mediaObject = Player.mediaCollection.getAll().item(0);

// Store the name of the retrieved object.
var mediaName = mediaObject.name;

// Prompt the user for permission to delete the object.
var answer = confirm("OK to permanently delete " + mediaName + "?");

// Check the user response.
if (answer){

    // Permanently delete the item.
    Player.mediaCollection.remove(mediaObject, true);

    // Report that the item was deleted.
    alert("Deleted item " + mediaName);
}

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

[**Objeto mediacollection**](mediacollection-object.md)
</dt> <dt>

[**Mediacollection. adicionar**](mediacollection-add.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





