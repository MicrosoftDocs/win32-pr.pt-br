---
title: Evento EndOfStream do objeto AxWindowsMediaPlayer
description: O evento EndOfStream é reservado para uso futuro.
ms.assetid: 004172e0-abd4-451c-bd5c-6bf0a9277661
keywords:
- Evento EndOfStream do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- EndOfStream Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c74a64eea77af43cd3b33cc7edee2177aee7d15e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762102"
---
# <a name="endofstream-event-of-the-axwindowsmediaplayer-object"></a>Evento EndOfStream do objeto AxWindowsMediaPlayer

O evento EndOfStream é reservado para uso futuro.

``` syntax
[C#]
private void player_EndOfStream(
  object sender,
  _WMPOCXEvents_EndOfStreamEvent e
)

[Visual Basic]
Private Sub player_EndOfStream(  
  sender As Object,  
  e As _WMPOCXEvents_EndOfStreamEvent
) Handles player.EndOfStream
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ EndOfStreamEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ EndOfStreamEvent**, que contém a seguinte propriedade relacionada a este evento.



| Propriedade | Descrição                           |
|----------|---------------------------------------|
| result   | System. Int32Not com suporte.<br/> |



 

## <a name="remarks"></a>Comentários

Esse evento é reservado para uso futuro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





