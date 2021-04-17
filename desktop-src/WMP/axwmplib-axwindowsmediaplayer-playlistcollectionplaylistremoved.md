---
title: Evento PlaylistCollectionPlaylistRemoved do objeto AxWindowsMediaPlayer
description: O evento PlaylistCollectionPlaylistRemoved ocorre quando uma playlist é removida da coleção de playlist. | Evento PlaylistCollectionPlaylistRemoved do objeto AxWindowsMediaPlayer
ms.assetid: 96935a9e-4c08-42e9-a63f-7b6cda41b243
keywords:
- Evento PlaylistCollectionPlaylistRemoved do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b982ff566380a7aa5bf4d0b1a1219739b52dd35
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783628"
---
# <a name="playlistcollectionplaylistremoved-event-of-the-axwindowsmediaplayer-object"></a>Evento PlaylistCollectionPlaylistRemoved do objeto AxWindowsMediaPlayer

O evento PlaylistCollectionPlaylistRemoved ocorre quando uma playlist é removida da coleção de playlist.

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistRemoved(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistRemovedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistRemoved(  
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistRemovedEvent
) Handles player.PlaylistCollectionPlaylistRemoved
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistRemovedEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistRemovedEvent**, que contém a seguinte propriedade relacionada a este evento.



| Propriedade             | Descrição                                                                  |
|----------------------|------------------------------------------------------------------------------|
| **bstrPlaylistName** | System. StringSpecifies o nome da lista de reprodução que foi removida.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. getByName (VB e C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





