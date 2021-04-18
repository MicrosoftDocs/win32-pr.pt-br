---
title: Evento KeyPress do objeto AxWindowsMediaPlayer
description: O evento KeyPress ocorre quando uma tecla é pressionada e liberada. | Evento KeyPress do objeto AxWindowsMediaPlayer
ms.assetid: 73ecd6f9-1b58-4e28-ad1b-2d930a235e1d
keywords:
- Evento KeyPress do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- KeyPress Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4a01e84b8f765d024c753d08211f3bb84e7f011
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800165"
---
# <a name="keypress-event-of-the-axwindowsmediaplayer-object"></a>Evento KeyPress do objeto AxWindowsMediaPlayer

O evento KeyPress ocorre quando uma tecla é pressionada e liberada.

``` syntax
[C#]
private void player_KeyPressEvent(
  object sender,
  _WMPOCXEvents_KeyPressEvent e
)

[Visual Basic]
Private Sub player_KeyPressEvent(  
  sender As Object,  
  e As _WMPOCXEvents_KeyPressEvent
) Handles player.KeyPressEvent
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyPressEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyPressEvent**, que contém a seguinte propriedade relacionada a este evento.



| Propriedade      | Descrição                                                                        |
|---------------|------------------------------------------------------------------------------------|
| **nKeyAscii** | System. Int16Specifies o código ANSI numérico padrão para o caractere.<br/> |



 

## <a name="remarks"></a>Comentários

Esse evento ocorre quando o pressionamento de tecla resulta em qualquer caractere de teclado imprimível, a tecla CTRL combinada com um caractere do alfabeto padrão ou um de alguns caracteres especiais e a tecla ENTER ou Backspace.

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

 

 





