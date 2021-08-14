---
title: Método Playlist.appendItem
description: O método appendItem adiciona um item de mídia ao final da playlist.
ms.assetid: cc956491-7936-49e7-90ca-1f71e03448cd
keywords:
- Método appendItem Windows Media Player
- método appendItem Windows Media Player , classe Playlist
- Classe de playlist Windows Media Player , método appendItem
topic_type:
- apiref
api_name:
- Playlist.appendItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79361ebcf2ea23b754a7bc86cb6fa4a0af465e4e6619ed692c027bc28eb7aa87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117747115"
---
# <a name="playlistappenditem-method"></a>Método Playlist.appendItem

O **método appendItem** adiciona um item de mídia ao final da playlist.

## <a name="syntax"></a>Sintaxe


```JScript
Playlist.appendItem(
  item
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*item* \[ Em\]
</dt> <dd>

**Objeto de** mídia a ser adicionado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Para usar esse método, é necessário ter acesso completo à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

## <a name="examples"></a>Exemplos

O exemplo de JScript a *seguir* usa Playlist . **appendItem para** adicionar o item de mídia atual à playlist chamada "ThreeList". O **objeto** Player foi criado com ID="Player".


```JScript
// Get the current media item.
var currMedia = Player.currentMedia;

// Get the playlist object by name.
var plThreeList = Player.playlistCollection.getByName("ThreeList").item(0);

// Append the media item to the playlist.
plThreeList.appendItem(currMedia);

```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto Playlist**](playlist-object.md)
</dt> <dt>

[**Configurações.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





