---
title: Evento PlaylistChange do objeto AxWindowsMediaPlayer
description: O evento PlaylistChange ocorre quando uma playlist é muda. | Evento PlaylistChange do objeto AxWindowsMediaPlayer
ms.assetid: e4166d81-a205-401a-94c4-a1619e764647
keywords:
- Evento PlaylistChange do objeto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- PlaylistChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 994c16ef79ad308e363e8cad4586cdbf0cca90a168d9bcb59ae6f943d108b74d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118841215"
---
# <a name="playlistchange-event-of-the-axwindowsmediaplayer-object"></a>Evento PlaylistChange do objeto AxWindowsMediaPlayer

O evento PlaylistChange ocorre quando uma playlist é muda.

``` syntax
[C#]
private void player_PlaylistChange(
  object sender,
  _WMPOCXEvents_PlaylistChangeEvent e
)

[Visual Basic]
Private Sub player_PlaylistChange(
  sender As Object,
  e As _WMPOCXEvents_PlaylistChangeEvent
) Handles player.PlaylistChange
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistChangeEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ PlaylistChangeEvent**, que contém as propriedades a seguir relacionadas a esse evento.



| Propriedade     | Descrição                                                                                                                   |
|--------------|-------------------------------------------------------------------------------------------------------------------------------|
| **Lista** | System.ObjectO objeto que foi alterado. Você pode castiá-lo em uma interface IWMPPlaylist para acessá-la.<br/>                |
| **change**   | Valor de enumeração WMPLib.WMPPlaylistChangeEventTypeAn indicando o tipo de alteração que ocorreu na playlist.<br/> |



 

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

[**Interface IWMPPlaylist (VB e C#)**](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





