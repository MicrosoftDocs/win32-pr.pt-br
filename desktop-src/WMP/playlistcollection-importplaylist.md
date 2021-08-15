---
title: Método playlistcollection. importPlaylist
description: O método importPlaylist adiciona uma lista de reprodução estática à biblioteca. | Método playlistcollection. importPlaylist
ms.assetid: 0611ba42-fd8f-4fb9-9fbb-809a82775c2a
keywords:
- Windows Media Player do método importPlaylist
- método importPlaylist Windows Media Player, classe playlistcollection
- classe playlistcollection Windows Media Player, método importPlaylist
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

## <a name="return-value"></a>Valor retornado

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

[**Configurações. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Configurações. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





