---
title: Evento ModeChange do objeto AxWindowsMediaPlayer
description: O evento ModeChange ocorre quando um modo do Windows Media Player é alterado. | Evento ModeChange do objeto AxWindowsMediaPlayer
ms.assetid: 56308425-dce5-4691-8970-c0807744abef
keywords:
- Evento ModeChange do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- ModeChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c06575fc986f4223056244964c2d070874c890b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813381"
---
# <a name="modechange-event-of-the-axwindowsmediaplayer-object"></a>Evento ModeChange do objeto AxWindowsMediaPlayer

O evento ModeChange ocorre quando um modo do Windows Media Player é alterado.

``` syntax
[C#]
private void player_ModeChange(
  object sender,
  _WMPOCXEvents_ModeChangeEvent e
)

[Visual Basic]
Private Sub player_ModeChange( 
  sender As Object,
  e As _WMPOCXEvents_ModeChangeEvent
) Handles player.ModeChange
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ ModeChangeEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ ModeChangeEvent**, que contém as propriedades a seguir relacionadas a esse evento.



| Propriedade | Descrição                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| modeName | System. StringIndicates o modo que foi alterado. Para obter os valores possíveis, consulte comentários.<br/> |
| newValue | System. BooleanIndicates o novo estado do modo especificado.<br/>                        |



 

## <a name="remarks"></a>Comentários

A tabela a seguir mostra os valores possíveis para a propriedade modeName.



| String  | Descrição                                         |
|---------|-----------------------------------------------------|
| ordem aleatória | As faixas são reproduzidas em ordem aleatória.                  |
| loop    | A sequência inteira de faixas é reproduzida repetidamente. |



 

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

[**IWMPSettings. GetMode (VB e C#)**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. setMode (VB e C#)**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





