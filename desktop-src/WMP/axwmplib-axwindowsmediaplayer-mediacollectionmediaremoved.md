---
title: Evento MediaCollectionMediaRemoved do objeto AxWindowsMediaPlayer
description: O evento MediaCollectionMediaRemoved ocorre quando um item de mídia é removido da biblioteca local. | Evento MediaCollectionMediaRemoved do objeto AxWindowsMediaPlayer
ms.assetid: 66dae2be-2a71-4d53-b2e2-f106426d4eea
keywords:
- Evento MediaCollectionMediaRemoved do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollectionMediaRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea15ff63fb913cd399a152913a27ffda1090d9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780032"
---
# <a name="mediacollectionmediaremoved-event-of-the-axwindowsmediaplayer-object"></a>Evento MediaCollectionMediaRemoved do objeto AxWindowsMediaPlayer

O evento MediaCollectionMediaRemoved ocorre quando um item de mídia é removido da biblioteca local.

``` syntax
[C#]
private void player_MediaCollectionMediaRemoved(
  object sender,
  _WMPOCXEvents_MediaCollectionMediaRemovedEvent e
)
        
[Visual Basic]
Private Sub player_MediaCollectionMediaRemoved(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionMediaRemovedEvent
) Handles player.MediaCollectionMediaRemoved
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionMediaRemovedEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionMediaRemovedEvent**, que contém a seguinte propriedade relacionada a este evento.



| Propriedade | Descrição                                                                                                                      |
|----------|----------------------------------------------------------------------------------------------------------------------------------|
| pMedia   | Item de mídia System. ObjectThe removido da biblioteca local. Você pode convertê-lo em uma interface IWMPMedia para acessá-lo.<br/> |



 

## <a name="remarks"></a>Comentários

Esse evento ocorre apenas para a biblioteca local.

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

[**Interface IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> </dl>

 

 





