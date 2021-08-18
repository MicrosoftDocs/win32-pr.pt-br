---
title: Evento DoubleClick do objeto AxWindowsMediaPlayer
description: O evento DoubleClick ocorre quando o usuário clica duas vezes em um botão do mouse em um Windows Media Player controle.
ms.assetid: 4f116d8a-1ad5-443a-9c91-66214bbdebcf
keywords:
- Evento DoubleClick do objeto AxWindowsMediaPlayer Windows Media Player
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
ms.openlocfilehash: cb01a5d0d5b9dd750c1232badb913000218a088d1ba6b41bc22e4e5dd49a6230
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136099"
---
# <a name="doubleclick-event-of-the-axwindowsmediaplayer-object"></a>Evento DoubleClick do objeto AxWindowsMediaPlayer

O evento DoubleClick ocorre quando o usuário clica duas vezes em um botão do mouse em um Windows Media Player controle.

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
| nButton     | System.Int16A bitfield com bits correspondentes ao botão esquerdo (bit 0), botão direito (bit 1) e botão central (bit 2). Esses bits correspondem aos valores 1, 2 e 4, respectivamente. Apenas um dos bits está definido, indicando o botão que causou o evento.<br/>                                                |
| nShiftState | Campo de bits System.Int16A com os bits menos significativos correspondentes à tecla SHIFT (bit 0), à tecla CTRL (bit 1) e à tecla ALT (bit 2). Esses bits correspondem aos valores 1, 2 e 4, respectivamente. Alguns, todos ou nenhum dos bits podem ser definidos, indicando que algumas, todas ou nenhuma das chaves são pressionadas.<br/> |
| Fx          | System.Int32A coordenada x do ponteiro do mouse em relação ao canto superior esquerdo do controle.<br/>                                                                                                                                                                                                                 |
| Fy          | System.Int32A coordenada y do ponteiro do mouse em relação ao canto superior esquerdo do controle.<br/>                                                                                                                                                                                                                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





