---
title: Evento AudioLanguageChange do objeto AxWindowsMediaPlayer
description: O evento AudioLanguageChange ocorre quando o idioma de áudio atual é alterado. | Evento AudioLanguageChange do objeto AxWindowsMediaPlayer
ms.assetid: 35e4ff82-fc59-4d28-b7fc-1527fb46b960
keywords:
- Evento AudioLanguageChange do objeto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- AudioLanguageChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a40538dad18c4cb6767a034ab5d163f16d1822d9149e15c07ca1130f5eb17f30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118582721"
---
# <a name="audiolanguagechange-event-of-the-axwindowsmediaplayer-object"></a>Evento AudioLanguageChange do objeto AxWindowsMediaPlayer

O evento AudioLanguageChange ocorre quando o idioma de áudio atual é alterado.

``` syntax
[C#]
private void player_AudioLanguageChange(
  object sender,
  _WMPOCXEvents_AudioLanguageChangeEvent e
)

[Visual Basic]
Private Sub player_AudioLanguageChange(
  sender As Object,
  e As _WMPOCXEvents_AudioLanguageChangeEvent
) Handles player.AudioLanguageChange
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ AudioLanguageChangeEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ AudioLanguageChangeEvent**, que contém a seguinte propriedade relacionada a este evento.



| Propriedade   | Descrição                                                                                    |
|------------|------------------------------------------------------------------------------------------------|
| **langID** | **System. Int32** Identifica exclusivamente um dialeto de idioma específico, chamado de localidade.<br/> |



 

## <a name="remarks"></a>Comentários

Um LCID (identificador de localidade) identifica exclusivamente um dialeto de idioma específico, chamado de localidade.

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

[**IWMPControls3. currentAudioLanguage (VB e C#)**](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> </dl>

 

 





