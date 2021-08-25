---
title: Evento CdromBurnError do objeto AxWindowsMediaPlayer
description: O evento CdromBurnError ocorre quando um erro genérico ocorre durante uma operação de gravação de CD.
ms.assetid: 512a3417-c8f3-42c7-ab2e-bea35cadbd4e
keywords:
- Evento CdromBurnError do objeto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- CdromBurnError Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37ea2ca4c510685e8a9d23a3fdc507e055f30c8916c7bf8bbbfbb30a5c4591b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864736"
---
# <a name="cdromburnerror-event-of-the-axwindowsmediaplayer-object"></a>Evento CdromBurnError do objeto AxWindowsMediaPlayer

O evento CdromBurnError ocorre quando um erro genérico ocorre durante uma operação de gravação de CD.

``` syntax
[C#]
private void player_CdromBurnError(
  object sender,
  _WMPOCXEvents_CdromBurnErrorEvent e
)

[Visual Basic]
Private Sub player_CdromBurnError(  
  sender As Object,
  e As _WMPOCXEvents_CdromBurnErrorEvent
) Handles player.CdromBurnError
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnErrorEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnErrorEvent**, que contém as propriedades a seguir relacionadas a esse evento.



| Propriedade   | Descrição                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------|
| hrError    | **System. Int32** O erro que gerou o evento.<br/>                                               |
| pCdromBurn | A interface WMPLib. IWMPCdromBurnThe que representa a operação de gravação que gerou o erro.<br/> |



 

## <a name="remarks"></a>Comentários

Para capturar erros de mídia específicos, manipule o AxWMPLib. \_ \_Evento WMPOCXEvents CdromBurnMediaError.

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

[**Evento AxWindowsMediaPlayer. CdromBurnMediaError (VB e C#)**](axwmplib-axwindowsmediaplayer-cdromburnmediaerror.md)
</dt> <dt>

[**Interface IWMPCdromBurn (VB e C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





