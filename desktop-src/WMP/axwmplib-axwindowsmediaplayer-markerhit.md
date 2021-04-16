---
title: Evento MarkerHit do objeto AxWindowsMediaPlayer
description: O evento MarkerHit ocorre quando um marcador é atingido. | Evento MarkerHit do objeto AxWindowsMediaPlayer
ms.assetid: 247fc22c-18c4-46b6-b42c-4882209a47f4
keywords:
- Evento MarkerHit do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- MarkerHit Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03bad8d9d64b4711937cd984bbd9d335acebfe67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794517"
---
# <a name="markerhit-event-of-the-axwindowsmediaplayer-object"></a>Evento MarkerHit do objeto AxWindowsMediaPlayer

O evento MarkerHit ocorre quando um marcador é atingido.

``` syntax
[C#]
private void player_MarkerHit(
  object sender,
  _WMPOCXEvents_MarkerHitEvent e
)

[Visual Basic]
Private Sub player_MarkerHit(  
  sender As Object,  
  e As _WMPOCXEvents_MarkerHitEvent
) Handles player.MarkerHit
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ MarkerHitEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ MarkerHitEvent**, que contém a seguinte propriedade relacionada a este evento.



| Propriedade      | Descrição                                                             |
|---------------|-------------------------------------------------------------------------|
| **MarkerNum** | System. Int32Indicates o número do marcador que foi atingido.<br/> |



 

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

 

 





