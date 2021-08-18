---
title: Evento buffer do objeto AxWindowsMediaPlayer
description: o evento de buffer ocorre quando o controle de Windows Media Player começa ou termina o buffer ou o download. | Evento buffer do objeto AxWindowsMediaPlayer
ms.assetid: ad152c4d-1c91-4da1-bec0-46f89f3b8c79
keywords:
- Evento de buffer do objeto AxWindowsMediaPlayer Windows Media Player
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
ms.openlocfilehash: 30cca5d7ebe91859162bd729cc32cc03f36f9e3c59ba4474d41311befcce1d21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765246"
---
# <a name="buffering-event-of-the-axwindowsmediaplayer-object"></a>Evento buffer do objeto AxWindowsMediaPlayer

o evento de buffer ocorre quando o controle de Windows Media Player começa ou termina o buffer ou o download.

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

Use esse evento para determinar quando o buffer ou o download é iniciado ou interrompido. Você pode usar o mesmo bloco de eventos para ambos os casos e testar o *IWMPNetwork*. **bufferingProgress** e *IWMPNetwork*. **downloadProgress** para determinar se Windows Media Player está atualmente armazenando em buffer ou baixando conteúdo.

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

 

 





