---
title: Evento LibraryConnect do objeto AxWindowsMediaPlayer
description: O evento LibraryConnect ocorre quando uma biblioteca fica disponível.
ms.assetid: f67243ce-0e25-43a7-b754-6b0e80d72055
keywords:
- Evento LibraryConnect do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- LibraryConnect Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33353b8438c61e28a3d52975fe90b06f14f03a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794519"
---
# <a name="libraryconnect-event-of-the-axwindowsmediaplayer-object"></a>Evento LibraryConnect do objeto AxWindowsMediaPlayer

O evento LibraryConnect ocorre quando uma biblioteca fica disponível.

``` syntax
[C#]
private void player_LibraryConnect(
  object sender,
  _WMPOCXEvents_LibraryConnectEvent e
)

[Visual Basic]
Private Sub player_LibraryConnect(  
  sender As Object,
  e As _WMPOCXEvents_LibraryConnectEvent
) Handles player.LibraryConnect
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ LibraryConnectEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ LibraryConnectEvent**, que contém a seguinte propriedade relacionada a este evento.



| Propriedade | Descrição                                                                                |
|----------|--------------------------------------------------------------------------------------------|
| pLibrary | **WMPLib. IWMPLibrary** A interface que representa a biblioteca conectada.<br/> |



 

## <a name="remarks"></a>Comentários

Esse evento não ocorre para a biblioteca local.

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

[**Interface IWMPLibrary (VB e C#)**](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





