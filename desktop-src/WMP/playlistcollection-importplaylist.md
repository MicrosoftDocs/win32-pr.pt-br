---
title: Método playlistcollection. importPlaylist
description: O método importPlaylist adiciona uma lista de reprodução estática à biblioteca. | Método playlistcollection. importPlaylist
ms.assetid: 0611ba42-fd8f-4fb9-9fbb-809a82775c2a
keywords:
- método importPlaylist Windows Media Player
- método importPlaylist Windows Media Player, classe Playlistcollection
- Classe playlistcollection Windows Media Player, método importPlaylist
topic_type:
- apiref
api_name:
- PlaylistCollection.importPlaylist
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736e9afa17f571428fada48660726b606268796a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768227"
---
# <a name="playlistcollectionimportplaylist-method"></a>Método playlistcollection. importPlaylist

O método **importPlaylist** adiciona uma lista de reprodução estática à biblioteca.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = PlaylistCollection.importPlaylist(
  playlist
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lista de reprodução* \[ no\]
</dt> <dd>

Objeto de **playlist** a ser adicionado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna o objeto **playlist** que foi adicionado.

## <a name="remarks"></a>Comentários

As listas de reprodução que não contêm nenhum item de mídia não podem ser adicionadas à biblioteca usando esse método. Para criar uma lista de reprodução vazia na biblioteca, use o método **newPlaylist** . Em seguida, você pode preencher a lista de reprodução resultante com itens de mídia usando a *lista de reprodução*. **appendItem** ou *playlist*. **insertItem**.

Se você passar esse método para uma lista de reprodução automática, a consulta será executada uma vez e o resultado será adicionado à biblioteca como uma lista de reprodução estática. Para adicionar uma lista de reprodução automática à biblioteca e preservar seu comportamento automático, use *mediacollection*. **Adicionar**. Para obter mais informações, consulte [playlists estáticas e automáticas](static-and-auto-playlists.md).

Para usar esse método, é necessário ter acesso completo à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Gerenciando listas de reprodução**](managing-playlists.md)
</dt> <dt>

[**Objeto mediacollection**](mediacollection-object.md)
</dt> <dt>

[**Mediacollection. adicionar**](mediacollection-add.md)
</dt> <dt>

[**Playlist. appendItem**](playlist-appenditem.md)
</dt> <dt>

[**Playlist. insertItem**](playlist-insertitem.md)
</dt> <dt>

[**Objeto playlistcollection**](playlistcollection-object.md)
</dt> <dt>

[**Playlistcollection. newPlaylist**](playlistcollection-newplaylist.md)
</dt> <dt>

[**Playlistcollection. Remove**](playlistcollection-remove.md)
</dt> <dt>

[**Settings. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





