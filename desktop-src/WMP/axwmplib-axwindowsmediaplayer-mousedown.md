---
title: Evento MouseDown do objeto AxWindowsMediaPlayer
description: O evento MouseDown ocorre quando o usuário pressiona um botão do mouse. | Evento MouseDown do objeto AxWindowsMediaPlayer
ms.assetid: 3dfbd034-67d4-4b7e-88d8-a77d301c5df7
keywords:
- Evento MouseDown do objeto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- MouseDown Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73259fab6ffd268e1c9a581a4b7ba18fdfba6c1647b57ef12bcae1c3ab8c04a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119509446"
---
# <a name="mousedown-event-of-the-axwindowsmediaplayer-object"></a>Evento MouseDown do objeto AxWindowsMediaPlayer

O evento MouseDown ocorre quando o usuário pressiona um botão do mouse.

``` syntax
[C#]
private void player_MouseDownEvent(
  object sender,
  _WMPOCXEvents_MouseDownEvent e
)

[Visual Basic]
Private Sub player_MouseDownEvent(  
  sender As Object,
  e As _WMPOCXEvents_MouseDownEvent
) Handles player.MouseDownEvent
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ MouseDownEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ MouseDownEvent**, que contém as propriedades a seguir relacionadas a esse evento.



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

 

 





