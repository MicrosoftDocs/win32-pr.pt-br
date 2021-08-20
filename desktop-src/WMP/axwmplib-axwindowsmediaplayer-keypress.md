---
title: Evento KeyPress do objeto AxWindowsMediaPlayer
description: O evento KeyPress ocorre quando uma tecla é pressionada e liberada. | Evento KeyPress do objeto AxWindowsMediaPlayer
ms.assetid: 73ecd6f9-1b58-4e28-ad1b-2d930a235e1d
keywords:
- Evento KeyPress do objeto AxWindowsMediaPlayer Windows Media Player
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
ms.openlocfilehash: 45b8022feacda910b28d68636c1abdcb2f6c1c9d3c2e799f762f25f5060b2b82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119618786"
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

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyPressEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyPressEvent**, que contém a propriedade a seguir relacionada a esse evento.



| Propriedade      | Descrição                                                                        |
|---------------|------------------------------------------------------------------------------------|
| **nKeyAscii** | System.Int16 Especifica o código ANSI numérico padrão para o caractere.<br/> |



 

## <a name="remarks"></a>Comentários

Esse evento ocorre quando o toque de tecla resulta em qualquer caractere de teclado imprimível, a tecla CTRL combinada com um caractere do alfabeto padrão ou um de alguns caracteres especiais e a tecla ENTER ou BACKSPACE.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                          |
| Namespace<br/> | **AxWMPLib**<br/>                                                                                                    |
| Assembly<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto AxWindowsMediaPlayer (VB e C#)**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





