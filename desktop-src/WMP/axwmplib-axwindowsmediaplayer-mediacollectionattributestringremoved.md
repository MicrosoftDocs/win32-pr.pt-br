---
title: Evento MediaCollectionAttributeStringRemoved do objeto AxWindowsMediaPlayer
description: O evento MediaCollectionAttributeStringRemoved ocorre quando um valor de atributo é removido da biblioteca. | Evento MediaCollectionAttributeStringRemoved do objeto AxWindowsMediaPlayer
ms.assetid: 2f264416-0bc5-41d0-8863-32c284393082
keywords:
- Evento MediaCollectionAttributeStringRemoved do objeto AxWindowsMediaPlayer Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollectionAttributeStringRemoved Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f56a6e997ada3296a0ec1df841797c1495ccde0864495dcf77a0a0634ccde5fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118582072"
---
# <a name="mediacollectionattributestringremoved-event-of-the-axwindowsmediaplayer-object"></a>Evento MediaCollectionAttributeStringRemoved do objeto AxWindowsMediaPlayer

O evento MediaCollectionAttributeStringRemoved ocorre quando um valor de atributo é removido da biblioteca.

``` syntax
[C#]
private void player_MediaCollectionAttributeStringRemoved(
  object sender,
  _WMPOCXEvents_MediaCollectionAttributeStringRemovedEvent e
)

[Visual Basic]
Private Sub player_MediaCollectionAttributeStringRemoved(
  sender As Object,
  e As _WMPOCXEvents_MediaCollectionAttributeStringRemovedEvent
) Handles player.MediaCollectionAttributeStringRemoved
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringRemovedEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ MediaCollectionAttributeStringRemovedEvent**, que contém as propriedades a seguir relacionadas a esse evento.



| Propriedade           | Descrição                                                                                                                                                                                  |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **bstrAttribName** | System.StringSpecifica o nome do atributo. Para obter informações sobre os atributos com suporte do Windows Media Player, consulte a [Referência de atributo](attribute-reference.md).<br/> |
| bstrAttribVal      | System.StringSpecifica o valor do atributo.<br/>                                                                                                                                |



 

## <a name="remarks"></a>Comentários

Quando um item de mídia é removido da biblioteca, seus metadados são removidos da **MediaCollection** e esse evento é acionado para cada atributo removido.

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

[**AxWindowsMediaPlayer.mediaCollection (VB e C#)**](axwmplib-axwindowsmediaplayer-mediacollection--vb-and-c.md)
</dt> <dt>

[**Interface IWMPMediaCollection (VB e C#)**](iwmpmediacollection--vb-and-c.md)
</dt> </dl>

 

 





