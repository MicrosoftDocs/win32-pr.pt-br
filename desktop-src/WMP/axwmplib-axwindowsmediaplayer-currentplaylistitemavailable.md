---
title: Evento CurrentPlaylistItemAvailable do objeto AxWindowsMediaPlayer
description: O evento CurrentPlaylistItemAvailable ocorre quando a playlist atual fica disponível. | Evento CurrentPlaylistItemAvailable do objeto AxWindowsMediaPlayer
ms.assetid: 101807c9-b00f-4351-a9a3-5413a52496f4
keywords:
- Evento CurrentPlaylistItemAvailable do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- CurrentPlaylistItemAvailable Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be9362a569fe8296284d92204628627c74ae3b44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810584"
---
# <a name="currentplaylistitemavailable-event-of-the-axwindowsmediaplayer-object"></a>Evento CurrentPlaylistItemAvailable do objeto AxWindowsMediaPlayer

O evento CurrentPlaylistItemAvailable ocorre quando a playlist atual fica disponível.

``` syntax
[C#]
private void player_CurrentPlaylistItemAvailable(
  object sender,
  _WMPOCXEvents_CurrentPlaylistItemAvailableEvent e
)

[Visual Basic]
Private Sub player_CurrentPlaylistItemAvailable(  
  sender As Object,
  e As _WMPOCXEvents_CurrentPlaylistItemAvailableEvent
) Handles player.CurrentPlaylistItemAvailable
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentPlaylistItemAvailableEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentPlaylistItemAvailableEvent**, que contém a seguinte propriedade relacionada a este evento.



| Propriedade         | Descrição                                                    |
|------------------|----------------------------------------------------------------|
| **bstrItemName** | System. StringThe nome do item da playlist atual.<br/> |



 

## <a name="remarks"></a>Comentários

O nome da lista de reprodução atual pode ser usado para recuperar a interface **IWMPPlaylist** correspondente da interface IWMPPlaylistArray que é retornada do método IWMPPlaylistCollection. getByName.

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

[**Interface IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[**Interface IWMPPlaylistArray (VB e C#)**](iwmpplaylistarray--vb-and-c.md)
</dt> <dt>

[**IWMPPlaylistCollection. getByName (VB e C#)**](wmplibiwmpplaylistcollection-iwmpplaylistcollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





