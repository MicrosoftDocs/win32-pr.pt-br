---
title: Evento MediaCollectionMediaAdded do objeto AxWindowsMediaPlayer
description: O evento MediaCollectionMediaAdded ocorre quando um item de mídia é adicionado à biblioteca local. | Evento MediaCollectionMediaAdded do objeto AxWindowsMediaPlayer
ms.assetid: ba1779f6-a212-44f4-b52a-c88e22aebcce
keywords:
- Evento MediaCollectionMediaAdded do objeto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollectionMediaAdded Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb48a41970840a45344e2e6fdd578f4e84e23751fd8e337052e66ccd0a058d5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765096"
---
# <a name="mediacollectionmediaadded-event-of-the-axwindowsmediaplayer-object"></a>Evento MediaCollectionMediaAdded do objeto AxWindowsMediaPlayer

O evento MediaCollectionMediaAdded ocorre quando um item de mídia é adicionado à biblioteca local.

``` syntax
[C#]
private void player_MediaCollectionMediaAdded(
  object sender,
  _WMPOCXEvents_MediaCollectionMediaAddedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionMediaAdded(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionMediaAddedEvent
) Handles player.MediaCollectionMediaAdded
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionMediaAddedEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionMediaAddedEvent**, que contém a propriedade a seguir relacionada a esse evento.



| Propriedade | Descrição                                                                                                                  |
|----------|------------------------------------------------------------------------------------------------------------------------------|
| pMedia   | System.ObjectO item de mídia adicionado à biblioteca local. Você pode castiá-lo em uma interface IWMPMedia para acessá-la.<br/> |



 

## <a name="remarks"></a>Comentários

Esse evento ocorre somente para a biblioteca local.

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

[**AxWindowsMediaPlayer.mediaCollection (VB e C#)**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMediaCollection (VB e C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





