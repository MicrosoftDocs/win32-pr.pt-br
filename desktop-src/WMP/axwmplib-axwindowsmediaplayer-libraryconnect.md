---
title: Evento LibraryConnect do objeto AxWindowsMediaPlayer
description: O evento LibraryConnect ocorre quando uma biblioteca fica disponível.
ms.assetid: f67243ce-0e25-43a7-b754-6b0e80d72055
keywords:
- Evento LibraryConnect do objeto AxWindowsMediaPlayer Windows Media Player
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
ms.openlocfilehash: 940eed16004009e928309ae1a2e5d8f792b9fd0cb36fe8e836abfefb89e3ab95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123946"
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

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ Biblioteca \_ WMPOCXEventsConnectEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ LibraryConnectEvent**, que contém a propriedade a seguir relacionada a esse evento.



| Propriedade | Descrição                                                                                |
|----------|--------------------------------------------------------------------------------------------|
| pLibrary | **WMPLib.IWMPLibrary** A interface que representa a biblioteca que se conectou.<br/> |



 

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

 

 





