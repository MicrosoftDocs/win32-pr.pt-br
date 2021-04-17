---
title: Evento CurrentMediaItemAvailable do objeto AxWindowsMediaPlayer
description: O evento CurrentMediaItemAvailable ocorre quando um item de metadados gráfico no item de mídia atual fica disponível. | Evento CurrentMediaItemAvailable do objeto AxWindowsMediaPlayer
ms.assetid: 7db62e6a-5f20-441a-801f-147ac386c5f8
keywords:
- Evento CurrentMediaItemAvailable do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- CurrentMediaItemAvailable Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 547622424194e63733cec6166d813d42ebf577ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759749"
---
# <a name="currentmediaitemavailable-event-of-the-axwindowsmediaplayer-object"></a>Evento CurrentMediaItemAvailable do objeto AxWindowsMediaPlayer

O evento CurrentMediaItemAvailable ocorre quando um item de metadados gráfico no item de mídia atual fica disponível.

``` syntax
[C#]
private void player_CurrentMediaItemAvailable(
  object sender,
  _WMPOCXEvents_CurrentMediaItemAvailableEvent e
)

[Visual Basic]
Private Sub player_CurrentMediaItemAvailable(
  sender As Object,  
  e As _WMPOCXEvents_CurrentMediaItemAvailableEvent
) Handles player.CurrentMediaItemAvailable
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentMediaItemAvailableEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentMediaItemAvailableEvent**, que contém a seguinte propriedade relacionada a este evento.



| Propriedade     | Descrição                                                 |
|--------------|-------------------------------------------------------------|
| bstrItemName | System. StringThe nome do item de mídia atual.<br/> |



 

## <a name="remarks"></a>Comentários

Como a reprodução pode começar antes que um item de mídia seja totalmente baixado, todos os gráficos de metadados contidos no item de mídia (como arte de capa do álbum) podem não estar disponíveis quando começam a ser reproduzidos. Esse evento alerta quando um item gráfico de metadados termina o download. Em seguida, você pode recuperar a interface **IWMPMedia** passando o valor de **BstrItemName** para o *IWMPMediaCollection*. método **getByName** , depois do qual você pode acessar o item gráfico de metadados usando *IWMPMedia3*. **getItemInfoByType** e especificando o **WM/Picture** para o nome do atributo.

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

[**Interface IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. getItemInfoByType (VB e C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection. getByName (VB e C#)**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





