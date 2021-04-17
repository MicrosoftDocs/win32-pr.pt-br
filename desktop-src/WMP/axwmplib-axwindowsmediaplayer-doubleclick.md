---
title: Evento DoubleClick do objeto AxWindowsMediaPlayer
description: O evento DoubleClick ocorre quando o usuário clica duas vezes em um botão do mouse em um controle do Windows Media Player.
ms.assetid: 4f116d8a-1ad5-443a-9c91-66214bbdebcf
keywords:
- Evento DoubleClick do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- DoubleClick Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ac809e8ea61b3abbbc964f6dc9ee2976442fc31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759747"
---
# <a name="doubleclick-event-of-the-axwindowsmediaplayer-object"></a>Evento DoubleClick do objeto AxWindowsMediaPlayer

O evento DoubleClick ocorre quando o usuário clica duas vezes em um botão do mouse em um controle do Windows Media Player.

``` syntax
[C#]
private void player_DoubleClickEvent(
  object sender,
  _WMPOCXEvents_DoubleClickEvent e
)

[Visual Basic]
Private Sub player_DoubleClickEvent(  
  sender As Object,  
  e As _WMPOCXEvents_DoubleClickEvent
) Handles player.DoubleClickEvent
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ DoubleClickEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ DoubleClickEvent**, que contém as propriedades a seguir relacionadas a esse evento.



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

 

 





