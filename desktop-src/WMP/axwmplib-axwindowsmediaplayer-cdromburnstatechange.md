---
title: Evento CdromBurnStateChange do objeto AxWindowsMediaPlayer
description: O evento CdromBurnStateChange ocorre quando uma operação de gravação de CD muda de estado.
ms.assetid: fec8a8e5-e282-454e-9713-fd9bb131df6a
keywords:
- Evento CdromBurnStateChange do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- CdromBurnStateChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc679a96600bff5aa4ca805018d364a6aeea8174
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811355"
---
# <a name="cdromburnstatechange-event-of-the-axwindowsmediaplayer-object"></a>Evento CdromBurnStateChange do objeto AxWindowsMediaPlayer

O evento CdromBurnStateChange ocorre quando uma operação de gravação de CD muda de estado.

``` syntax
[C#]
private void player_CdromBurnStateChange(
  object sender,
  _WMPOCXEvents_CdromBurnStateChangeEvent e
)

[Visual Basic]
Private Sub player_CdromBurnStateChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromBurnStateChangeEvent
) Handles player.CdromBurnStateChange
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnStateChangeEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromBurnStateChangeEvent**, que contém as propriedades a seguir relacionadas a esse evento.



| Propriedade   | Descrição                                                                                               |
|------------|-----------------------------------------------------------------------------------------------------------|
| pCdromBurn | A interface WMPLib. IWMPCdromBurnThe que representa a operação de gravação que gerou o erro.<br/> |
| wmpbs      | Valor de enumeração WMPLib. WMPBurnStateThe que indica o novo estado.<br/>                         |



 

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

[**Interface IWMPCdromBurn (VB e C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**WMPBurnState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





