---
title: Evento MouseMove do objeto AxWindowsMediaPlayer
description: O evento MouseMove ocorre quando o ponteiro do mouse é movido. | Evento MouseMove do objeto AxWindowsMediaPlayer
ms.assetid: abf20c86-3bae-4677-8901-0af030a53286
keywords:
- Evento MouseMove do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- MouseMove Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c623bf60f2951b1a82e59a7d63056bcf8a0b5da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794514"
---
# <a name="mousemove-event-of-the-axwindowsmediaplayer-object"></a>Evento MouseMove do objeto AxWindowsMediaPlayer

O evento MouseMove ocorre quando o ponteiro do mouse é movido.

``` syntax
[C#]
private void player_MouseMoveEvent(
  object sender,
  _WMPOCXEvents_MouseMoveEvent e
)

[Visual Basic]
Private Sub player_MouseMoveEvent(
  sender As Object,
  e As _WMPOCXEvents_MouseMoveEvent
) Handles player.MouseMoveEvent
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ MouseMoveEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ MouseMoveEvent**, que contém as propriedades a seguir relacionadas a esse evento.



| Propriedade    | Descrição                                                                                                                                                                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nnovo     | O campo do sistema. Int16a com bits correspondente ao botão esquerdo (bit 0), botão direito (bit 1) e botão do meio (bit 2). Esses bits correspondem aos valores 1, 2 e 4, respectivamente. Apenas um dos bits é definido, indicando o botão que causou o evento.<br/>                                                |
| nShiftState | O campo do sistema. Int16a com os bits menos significativos correspondentes à tecla SHIFT (bit 0), a tecla CTRL (bit 1) e a tecla ALT (bit 2). Esses bits correspondem aos valores 1, 2 e 4, respectivamente. Alguns, todos ou nenhum dos bits podem ser definidos, indicando que algumas, todas ou nenhuma das chaves são pressionadas.<br/> |
| Efeito          | System. Int32The x-coordenada do ponteiro do mouse em relação ao canto superior esquerdo do controle.<br/>                                                                                                                                                                                                                 |
| SAR          | System. Int32The y-coordenada do ponteiro do mouse em relação ao canto superior esquerdo do controle.<br/>                                                                                                                                                                                                                 |



 

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

 

 





