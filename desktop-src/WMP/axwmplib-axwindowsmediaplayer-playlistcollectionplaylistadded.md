---
title: Evento PlaylistCollectionPlaylistAdded do objeto AxWindowsMediaPlayer
description: O evento PlaylistCollectionPlaylistAdded ocorre quando uma playlist é adicionada à coleção de playlists. | Evento PlaylistCollectionPlaylistAdded do objeto AxWindowsMediaPlayer
ms.assetid: 13d3bc86-6655-4536-a58f-327eabb2b8f9
keywords:
- Evento PlaylistCollectionPlaylistAdded do objeto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- PlaylistCollectionPlaylistAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5223d5864aa8be9019b2219ef09917a1c63cf16d87a48aef9543246d5197a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118581821"
---
# <a name="playlistcollectionplaylistadded-event-of-the-axwindowsmediaplayer-object"></a>Evento PlaylistCollectionPlaylistAdded do objeto AxWindowsMediaPlayer

O evento PlaylistCollectionPlaylistAdded ocorre quando uma playlist é adicionada à coleção de playlists.

``` syntax
[C#]
private void player_PlaylistCollectionPlaylistAdded(
  object sender,
  _WMPOCXEvents_PlaylistCollectionPlaylistAddedEvent e
)

[Visual Basic]
Private Sub player_PlaylistCollectionPlaylistAdded(
  sender As Object,
  e As _WMPOCXEvents_PlaylistCollectionPlaylistAddedEvent
) Handles player.PlaylistCollectionPlaylistAdded
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistAddedEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistCollectionPlaylistAddedEvent**, que contém a propriedade a seguir relacionada a esse evento.



| Propriedade             | Descrição                                                                |
|----------------------|----------------------------------------------------------------------------|
| **bstrPlaylistName** | System.String Especifica o nome da playlist que foi adicionada.<br/> |



 

## <a name="remarks"></a>Comentários

O nome da playlist que foi adicionada pode ser usado para recuperar a playlist correspondente usando IWMPPlaylistCollection. **Método getByName.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection.getByName (VB e C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





