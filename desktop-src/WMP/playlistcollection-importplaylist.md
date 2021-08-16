---
title: Método PlaylistCollection.importPlaylist
description: O método importPlaylist adiciona uma playlist estática à biblioteca. | Método PlaylistCollection.importPlaylist
ms.assetid: 0611ba42-fd8f-4fb9-9fbb-809a82775c2a
keywords:
- Método importPlaylist Windows Media Player
- Método importPlaylist Windows Media Player classe , PlaylistCollection
- Classe PlaylistCollection Windows Media Player , método importPlaylist
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
ms.openlocfilehash: 7f6c2a61b6603c0bfb38025548eaa4b0943bcdd1a5e81cb1ac27c17969fe87ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118334802"
---
# <a name="playlistcollectionimportplaylist-method"></a>Método PlaylistCollection.importPlaylist

O **método importPlaylist** adiciona uma playlist estática à biblioteca.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = PlaylistCollection.importPlaylist(
  playlist
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*playlist* \[ Em\]
</dt> <dd>

**Objeto de** playlist a ser adicionado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna o **objeto Playlist** que foi adicionado.

## <a name="remarks"></a>Comentários

As listas de reprodução que não contêm nenhum item de mídia não podem ser adicionadas à biblioteca usando esse método. Para criar uma playlist vazia na biblioteca, use o **método newPlaylist.** Em seguida, você pode preencher a playlist resultante com itens de mídia *usando* Playlist . **appendItem ou** *Playlist*. **insertItem**.

Se você passar para esse método uma playlist automática, a consulta será executada uma vez e o resultado será adicionado à biblioteca como uma playlist estática. Para adicionar uma playlist automática à biblioteca e preservar seu comportamento automático, use *MediaCollection*. **adicione**. Para obter mais informações, consulte [Playlists estáticas e automáticas.](static-and-auto-playlists.md)

Para usar esse método, é necessário ter acesso completo à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Gerenciando playlists**](managing-playlists.md)
</dt> <dt>

[**Objeto MediaCollection**](mediacollection-object.md)
</dt> <dt>

[**MediaCollection.add**](mediacollection-add.md)
</dt> <dt>

[**Playlist.appendItem**](playlist-appenditem.md)
</dt> <dt>

[**Playlist.insertItem**](playlist-insertitem.md)
</dt> <dt>

[**Objeto PlaylistCollection**](playlistcollection-object.md)
</dt> <dt>

[**PlaylistCollection.newPlaylist**](playlistcollection-newplaylist.md)
</dt> <dt>

[**PlaylistCollection.remove**](playlistcollection-remove.md)
</dt> <dt>

[**Configurações.mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações.requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





