---
title: Método MediaCollection.remove
description: O método remove remove um item da coleção de mídias.
ms.assetid: 7d4c03ed-01c8-4112-90b6-5de52eacb199
keywords:
- remover o método Windows Media Player
- classe remove method Windows Media Player , MediaCollection
- Classe MediaCollection Windows Media Player , remover método
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
ms.openlocfilehash: a8dd0643741a15bf114acfef63459e67c332b06b33e6284b032979d4ad15c1d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574603"
---
# <a name="mediacollectionremove-method"></a>Método MediaCollection.remove

O **método remove** remove um item da coleção de mídias.

## <a name="syntax"></a>Sintaxe


```JScript
MediaCollection.remove(
  item,
  delete
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*item* \[ Em\]
</dt> <dd>

**Objeto de** mídia a ser removido.

</dd> <dt>

*excluir* \[ Em\]
</dt> <dd>

**Booliana** que indica se o item deve ser removido.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método exclui um item da biblioteca. Esse método não exclui arquivos do computador do usuário.

Para usar esse método, é necessário ter acesso completo à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

## <a name="examples"></a>Exemplos

O exemplo JScript a seguir, depois de solicitar ao usuário, exclui permanentemente o primeiro item de mídia na coleção de mídias usando *MediaCollection*. **remover**. O **objeto** Player foi criado com ID = "Player".


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
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto de mídia**](media-object.md)
</dt> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**MediaCollection.add**](mediacollection-add.md)
</dt> <dt>

[**Configurações.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





