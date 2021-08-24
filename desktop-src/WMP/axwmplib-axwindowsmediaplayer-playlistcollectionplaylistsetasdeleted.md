---
title: Evento PlaylistCollectionPlaylistSetAsDeleted do objeto AxWindowsMediaPlayer
description: O evento PlaylistCollectionPlaylistSetAsDeleted é reservado para uso futuro.
ms.assetid: 6c0a4d2c-e965-4a88-acd4-2a2a12265e36
keywords:
- Evento PlaylistCollectionPlaylistSetAsDeleted do objeto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistSetAsDeleted Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b11187ffaf6e16612ba7edb573e0b0bc71e9d2abf44ee509db2404026e3ed570
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864568"
---
# <a name="playlistcollectionplaylistsetasdeleted-event-of-the-axwindowsmediaplayer-object"></a>Evento PlaylistCollectionPlaylistSetAsDeleted do objeto AxWindowsMediaPlayer

O evento PlaylistCollectionPlaylistSetAsDeleted é reservado para uso futuro.

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistSetAsDeleted(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistSetAsDeletedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistSetAsDeleted(
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistSetAsDeletedEvent
) Handles player.PlaylistCollectionPlaylistSetAsDeleted
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistSetAsDeletedEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistSetAsDeletedEvent**, que contém as propriedades a seguir relacionadas a esse evento.



| Propriedade         | Descrição                                 |
|------------------|---------------------------------------------|
| bstrPlaylistName | **System.String** Sem suporte.<br/>  |
| varfIsDeleted    | **System.Boolean** Sem suporte.<br/> |



 

## <a name="remarks"></a>Comentários

Esse evento é reservado para uso futuro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





