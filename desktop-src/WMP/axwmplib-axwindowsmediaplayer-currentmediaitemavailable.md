---
title: Evento CurrentMediaItemAvailable do objeto AxWindowsMediaPlayer
description: O evento CurrentMediaItemAvailable ocorre quando um item de metadados gráficos no item de mídia atual fica disponível. | Evento CurrentMediaItemAvailable do objeto AxWindowsMediaPlayer
ms.assetid: 7db62e6a-5f20-441a-801f-147ac386c5f8
keywords:
- Evento CurrentMediaItemAvailable do objeto AxWindowsMediaPlayer Windows Media Player
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
ms.openlocfilehash: 6b5bbac6f27dfa7c9de1115eb3c2f5eea85096e0868ac17e0f8b11d81385f344
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118582345"
---
# <a name="currentmediaitemavailable-event-of-the-axwindowsmediaplayer-object"></a>Evento CurrentMediaItemAvailable do objeto AxWindowsMediaPlayer

O evento CurrentMediaItemAvailable ocorre quando um item de metadados gráficos no item de mídia atual fica disponível.

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

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentMediaItemAvailableEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ CurrentMediaItemAvailableEvent**, que contém a propriedade a seguir relacionada a esse evento.



| Propriedade     | Descrição                                                 |
|--------------|-------------------------------------------------------------|
| bstrItemName | System.StringO nome do item de mídia atual.<br/> |



 

## <a name="remarks"></a>Comentários

Como a reprodução pode começar antes que um item de mídia seja totalmente baixado, os gráficos de metadados contidos no item de mídia (como a capa do álbum) podem não estar disponíveis quando ele começar a ser reproduzido. Esse evento alerta você quando um item gráfico de metadados terminar de ser baixado. Em seguida, você pode recuperar a interface **IWMPMedia** passando o valor **de bstrItemName** para *O IWMPMediaCollection*. **Método getByName,** após o qual você pode acessar o item gráfico de metadados usando *IWMPMedia3*. **getItemInfoByType e** especificando **WM/Picture** para o nome do atributo.

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

[**Interface IWMPMedia (VB e C#)**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3.getItemInfoByType (VB e C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> <dt>

[**IWMPMediaCollection.getByName (VB e C#)**](wmplibiwmpmediacollection-iwmpmediacollection-getbyname--vb-and-c.md)
</dt> </dl>

 

 





