---
title: Evento DurationUnitChange do objeto AxWindowsMediaPlayer
description: O evento DurationUnitChange é reservado para uso futuro.
ms.assetid: d8d7da21-bc61-49f8-91bd-4c232295c1ac
keywords:
- Evento DurationUnitChange do objeto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- DurationUnitChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1efa872389ad88a236808de64ed299dd3afc123cee59f39f1215f7a16bcb589f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136039"
---
# <a name="durationunitchange-event-of-the-axwindowsmediaplayer-object"></a>Evento DurationUnitChange do objeto AxWindowsMediaPlayer

O evento DurationUnitChange é reservado para uso futuro.

``` syntax
[C#]
private void player_DurationUnitChange(
  object sender,
  _WMPOCXEvents_DurationUnitChangeEvent e
)

[Visual Basic]
Private Sub player_DurationUnitChange(  
  sender As Object,  
  e As _WMPOCXEvents_DurationUnitChangeEvent
) Handles player.DurationUnitChange
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ DurationUnitChangeEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ DurationUnitChangeEvent**, que contém a propriedade a seguir relacionada a esse evento.



| Propriedade        | Descrição                               |
|-----------------|-------------------------------------------|
| newDurationUnit | **System.Int32** Sem suporte.<br/> |



 

## <a name="remarks"></a>Comentários

Esse evento é reservado para uso futuro.

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

 

 





