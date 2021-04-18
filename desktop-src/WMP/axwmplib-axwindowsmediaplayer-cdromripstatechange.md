---
title: Evento CdromRipStateChange do objeto AxWindowsMediaPlayer
description: O evento CdromRipStateChange ocorre quando uma operação de cópia de CD muda de estado.
ms.assetid: 0a0bd11f-a685-4c4e-8704-8eabe80d6f86
keywords:
- Evento CdromRipStateChange do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- CdromRipStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20fae9eb1fa6d5f65876e3f6758a7594f0bdbb19
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760471"
---
# <a name="cdromripstatechange-event-of-the-axwindowsmediaplayer-object"></a>Evento CdromRipStateChange do objeto AxWindowsMediaPlayer

O evento CdromRipStateChange ocorre quando uma operação de cópia de CD muda de estado.

``` syntax
[C#]
private void player_CdromRipStateChange(
  object sender,
  _WMPOCXEvents_CdromRipStateChangeEvent e
)

[Visual Basic]
Private Sub player_CdromRipStateChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromRipStateChangeEvent
) Handles player.CdromRipStateChange
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromRipStateChangeEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromRipStateChangeEvent**, que contém as propriedades a seguir relacionadas a esse evento.



| Propriedade  | Descrição                                                                                              |
|-----------|----------------------------------------------------------------------------------------------------------|
| pCdromRip | A interface WMPLib. IWMPCdromRipThe que representa a operação de cópia de CDs que gerou o erro.<br/> |
| wmprs     | Valor de enumeração WMPLib. WMPRipStateThe que indica o novo estado.<br/>                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 11<br/>                                                                                         |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interface IWMPCdromRip (VB e C#)**](iwmpcdromrip--vb-and-c.md)
</dt> <dt>

[**WMPRipState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)
</dt> </dl>

 

 





