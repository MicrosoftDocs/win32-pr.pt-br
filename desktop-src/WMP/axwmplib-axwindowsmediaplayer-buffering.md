---
title: Evento buffer do objeto AxWindowsMediaPlayer
description: O evento de buffer ocorre quando o controle do Windows Media Player começa ou termina o armazenamento em buffer ou o download. | Evento buffer do objeto AxWindowsMediaPlayer
ms.assetid: ad152c4d-1c91-4da1-bec0-46f89f3b8c79
keywords:
- Evento buffer do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- Buffering Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af595443d78a311510df6a7e06b2e716da22ecae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794525"
---
# <a name="buffering-event-of-the-axwindowsmediaplayer-object"></a>Evento buffer do objeto AxWindowsMediaPlayer

O evento de buffer ocorre quando o controle do Windows Media Player começa ou termina o armazenamento em buffer ou o download.

``` syntax
[C#]
private void player_Buffering(
  object sender,
  _WMPOCXEvents_BufferingEvent e
)

[Visual Basic]
Private Sub player_Buffering(
  sender As Object,
  e As _WMPOCXEvents_BufferingEvent
) Handles player.Buffering
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ BufferingEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ BufferingEvent**, que contém a seguinte propriedade relacionada a este evento.



| Propriedade | Descrição                                                                                                                                                         |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Iniciar    | System. BooleanSpecifies se o armazenamento em buffer foi iniciado ou encerrado. Um valor true indica que ele foi iniciado; um valor false indica que ele terminou.<br/> |



 

## <a name="remarks"></a>Comentários

Use esse evento para determinar quando o buffer ou o download é iniciado ou interrompido. Você pode usar o mesmo bloco de eventos para ambos os casos e testar o *IWMPNetwork*. **bufferingProgress** e *IWMPNetwork*. **downloadProgress** para determinar se o Windows Media Player está atualmente armazenando em buffer ou baixando conteúdo.

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

[**IWMPNetwork. bufferingProgress (VB e C#)**](wmplibiwmpnetwork-iwmpnetwork-bufferingprogress--vb-and-c.md)
</dt> <dt>

[**IWMPNetwork. downloadProgress (VB e C#)**](wmplibiwmpnetwork-iwmpnetwork-downloadprogress--vb-and-c.md)
</dt> </dl>

 

 





