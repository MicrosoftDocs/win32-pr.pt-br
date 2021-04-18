---
title: Evento PositionChange do objeto AxWindowsMediaPlayer
description: O evento PositionChange ocorre quando a posição de reprodução atual dentro do item de mídia foi alterada.
ms.assetid: 92d469b9-813a-4148-be68-0fcef2e41491
keywords:
- Evento PositionChange do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- PositionChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 552b748121668e71ee4d2ffb54feed441620a1cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781279"
---
# <a name="positionchange-event-of-the-axwindowsmediaplayer-object"></a>Evento PositionChange do objeto AxWindowsMediaPlayer

O evento PositionChange ocorre quando a posição de reprodução atual dentro do item de mídia foi alterada.

``` syntax
[C#]
private void player_PositionChange(
  object sender,
  _WMPOCXEvents_PositionChangeEvent e
)

[Visual Basic]
Private Sub player_PositionChange(  
  sender As Object,
  e As _WMPOCXEvents_PositionChangeEvent
) Handles player.PositionChange
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ PositionChangeEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ PositionChangeEvent**, que contém as propriedades a seguir relacionadas a esse evento.



| Propriedade    | Descrição                                         |
|-------------|-----------------------------------------------------|
| oldPosition | System. DoubleSpecifies a posição antiga.<br/> |
| newPosition | System. DoubleSpecifies a nova posição.<br/> |



 

## <a name="remarks"></a>Comentários

Esse evento não é gerado rotineiramente durante a reprodução. Isso ocorre apenas quando algo altera ativamente a posição atual do item de mídia em reprodução, como quando o usuário move o identificador de busca ou quando o código é executado que especifica um valor para IWMPControls. **CurrentPosition**.

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

[**IWMPControls. currentPosition (VB e C#)**](wmplibiwmpcontrols-iwmpcontrols-currentposition--vb-and-c.md)
</dt> </dl>

 

 





