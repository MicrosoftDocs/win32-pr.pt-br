---
title: Evento CdromErrorMediaError do objeto AxWindowsMediaPlayer
description: O evento CdromErrorMediaError ocorre quando ocorre um erro ao gravar um item de mídia individual em um CD.
ms.assetid: 0847a8a2-1fef-41a0-affb-9fa6bd10b925
keywords:
- Evento CdromErrorMediaError do objeto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- CdromBurnMediaError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba161945edcda7409b842987ab97768c30a6e1f0ba011772cf7f3757d3f61c33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765259"
---
# <a name="cdromburnmediaerror-event-of-the-axwindowsmediaplayer-object"></a>Evento CdromErrorMediaError do objeto AxWindowsMediaPlayer

O evento CdromErrorMediaError ocorre quando ocorre um erro ao gravar um item de mídia individual em um CD.

``` syntax
[C#]
private void player_CdromBurnMediaError(
  object sender,
  _WMPOCXEvents_CdromBurnMediaErrorEvent e
)

[Visual Basic]
Private Sub player_CdromBurnMediaError(
  sender As Object,
  e As _WMPOCXEvents_CdromBurnMediaErrorEvent
) Handles player.CdromBurnMediaError
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromErrorMediaErrorEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromErrorErrorEvent**, que contém as propriedades a seguir relacionadas a esse evento.



| Propriedade   | Descrição                                                                                                             |
|------------|-------------------------------------------------------------------------------------------------------------------------|
| pCdrom Ltda | WMPLib.IWMPCdromRomThe interface que representa a operação de gravação que gerou o erro.<br/>               |
| pMedia     | System.ObjectO item de mídia que gerou o erro. Você pode castiá-lo em uma interface IWMPMedia para acessá-la.<br/> |



 

## <a name="remarks"></a>Comentários

Para capturar erros genéricos, manipular o AxWMPLib. \_ Evento WMPOCXEvents \_ CdromError.

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

[**Evento AxWindowsMediaPlayer.CdromError (VB e C#)**](axwmplib-axwindowsmediaplayer-cdromburnerror.md)
</dt> <dt>

[**Interface IWMPCdrom Ltda (VB e C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





