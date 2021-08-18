---
title: Evento KeyUp do objeto AxWindowsMediaPlayer
description: O evento KeyUp ocorre quando uma chave é liberada. | Evento KeyUp do objeto AxWindowsMediaPlayer
ms.assetid: db814481-6099-4dbd-8ab1-808e1875ae35
keywords:
- Evento KeyUp do objeto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- KeyUp Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3a2666268e2c12e74c6498446ff49bde69dd30cf9819a7899e88a8b8ee4466
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136009"
---
# <a name="keyup-event-of-the-axwindowsmediaplayer-object"></a>Evento KeyUp do objeto AxWindowsMediaPlayer

O evento KeyUp ocorre quando uma chave é liberada.

``` syntax
[C#]
private void player_KeyUpEvent(
  object sender,
  _WMPOCXEvents_KeyUpEvent e
)

[Visual Basic]
Private Sub player_KeyUpEvent(
    sender As Object,
    e As _WMPOCXEvents_KeyUpEvent
) Handles player.KeyUpEvent
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyUpEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyUpEvent**, que contém as propriedades a seguir relacionadas a esse evento.



| Propriedade    | Descrição                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nKeyCode    | System. Int16Specifies que a chave física é pressionada. Para obter os valores possíveis, consulte a seção comentários do evento KeyDown.<br/>                                                                                                                                                                                                                                                   |
| nShiftState | O campo do sistema. Int16a com os bits menos significativos correspondentes à tecla SHIFT (bit 0), a tecla CTRL (bit 1) e a tecla ALT (bit 2). Esses bits correspondem aos valores 1, 2 e 4, respectivamente. O argumento Shift indica o estado dessas chaves. Alguns, todos ou nenhum dos bits podem ser definidos, indicando que algumas, todas ou nenhuma das chaves são pressionadas.<br/> |



 

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

 

 





