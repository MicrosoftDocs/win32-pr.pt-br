---
title: Evento CdromMediaChange do objeto AxWindowsMediaPlayer
description: O evento CdromMediaChange ocorre quando um CD ou DVD é inserido ou ejetado de uma unidade de CD ou DVD. | Evento CdromMediaChange do objeto AxWindowsMediaPlayer
ms.assetid: 0a6378c1-59e4-4be3-8764-d5c4ab478b6c
keywords:
- Evento CdromMediaChange do objeto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- CdromMediaChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55dac05b3ca8a8675bfae431d3f2e8ffbb38db8701a2501fa80d282cd3c976ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054994"
---
# <a name="cdrommediachange-event-of-the-axwindowsmediaplayer-object"></a>Evento CdromMediaChange do objeto AxWindowsMediaPlayer

O **evento CdromMediaChange** ocorre quando um CD ou DVD é inserido ou ejetado de uma unidade de CD ou DVD.

``` syntax
[C#]
private void player_CdromMediaChange(
  object sender,
  _WMPOCXEvents_CdromMediaChangeEvent e
)

[Visual Basic]
Private Sub player_CdromMediaChange(  
  sender As Object,
  e As _WMPOCXEvents_CdromMediaChangeEvent
) Handles player.CdromMediaChange
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromMediaChangeEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ CdromMediaChangeEvent**, que contém a propriedade a seguir relacionada a esse evento.



| Propriedade | Descrição                                                        |
|----------|--------------------------------------------------------------------|
| CdromNum | System.Int32 Especifica o índice da unidade de CD ou DVD.<br/> |



 

## <a name="remarks"></a>Comentários

O índice da unidade de CD corresponde ao índice de uma interface IWMPCdrom acessível por meio da interface IWMPCdromCollection.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**Interface IWMPCdrom (VB e C#)**](iwmpcdrom--vb-and-c.md)
</dt> <dt>

[**Interface IWMPCdromCollection (VB e C#)**](iwmpcdromcollection--vb-and-c.md)
</dt> </dl>

 

 





