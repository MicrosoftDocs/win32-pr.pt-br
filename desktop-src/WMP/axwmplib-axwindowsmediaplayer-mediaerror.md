---
title: Evento MediaError do objeto AxWindowsMediaPlayer
description: O evento MediaError ocorre quando um objeto de mídia tem uma condição de erro.
ms.assetid: a1fb3422-85c4-4856-951a-332517599984
keywords:
- Evento MediaError do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- MediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 874b9297846a8f25f25c68545df234aa1be70594
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759744"
---
# <a name="mediaerror-event-of-the-axwindowsmediaplayer-object"></a>Evento MediaError do objeto AxWindowsMediaPlayer

O evento MediaError ocorre quando um objeto de mídia tem uma condição de erro.

``` syntax
[C#]
private void player_MediaError(
  object sender,
  _WMPOCXEvents_MediaErrorEvent e
)

[Visual Basic]
Private Sub player_MediaError(
  sender As Object,
  e As _WMPOCXEvents_MediaErrorEvent
) Handles player.MediaError
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaErrorEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaErrorEvent**, que contém a seguinte propriedade relacionada a este evento.



| Propriedade     | Descrição                                                                                                           |
|--------------|-----------------------------------------------------------------------------------------------------------------------|
| pMediaObject | System. Objectobject que tem uma condição de erro. Você pode convertê-lo em uma interface IWMPMedia para acessá-lo.<br/> |



 

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

[**Interface IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





