---
title: Evento de aviso do objeto AxWindowsMediaPlayer
description: O evento de aviso é reservado para uso futuro.
ms.assetid: 3de63756-2726-4864-8988-fd614f23bcad
keywords:
- Evento de aviso do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- Warning Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a868ba7f619287cd96929c62d89dee3555d908b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761120"
---
# <a name="warning-event-of-the-axwindowsmediaplayer-object"></a>Evento de aviso do objeto AxWindowsMediaPlayer

O evento de aviso é reservado para uso futuro.

``` syntax
[C#]
private void player_Warning(
  object sender,
  _WMPOCXEvents_WarningEvent e
)

[Visual Basic]
Private Sub player_Warning(
  sender As Object,
  e As _WMPOCXEvents_WarningEvent
) Handles player.Warning
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ WarningEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ WarningEvent**, que contém as propriedades a seguir relacionadas a esse evento.



| Propriedade    | Descrição                                |
|-------------|--------------------------------------------|
| aviso de | **System. Int32** Sem suporte.<br/>  |
| param       | **System. Int32** Sem suporte.<br/>  |
| descrição | **System. String** Sem suporte.<br/> |



 

## <a name="remarks"></a>Comentários

Esse evento é reservado para uso futuro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





