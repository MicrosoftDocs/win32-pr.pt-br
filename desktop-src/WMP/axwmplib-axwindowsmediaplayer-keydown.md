---
title: Evento KeyDown do objeto AxWindowsMediaPlayer
description: O evento KeyDown ocorre quando uma tecla é pressionada. | Evento KeyDown do objeto AxWindowsMediaPlayer
ms.assetid: e67b9628-6c53-4893-921a-9487ebfc1cd5
keywords:
- Evento KeyDown do objeto AxWindowsMediaPlayer do Windows Media Player
topic_type:
- apiref
api_name:
- KeyDown Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc89814063e1a43badd22e658b5f19ece7abb074
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796445"
---
# <a name="keydown-event-of-the-axwindowsmediaplayer-object"></a>Evento KeyDown do objeto AxWindowsMediaPlayer

O evento KeyDown ocorre quando uma tecla é pressionada.

``` syntax
[C#]
private void player_KeyDownEvent(
  object sender,
  _WMPOCXEvents_KeyDownEvent e
)

[Visual Basic]
Private Sub player_KeyDownEvent(  
  sender As Object, 
  e As _WMPOCXEvents_KeyDownEvent
) Handles player.KeyDownEvent
```

## <a name="event-data"></a>Dados de evento

O manipulador associado a esse evento é do tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyDownEventHandler**. Esse manipulador recebe um argumento do tipo **AxWMPLib. \_ WMPOCXEvents \_ KeyDownEvent**, que contém as propriedades a seguir relacionadas a esse evento.



| Propriedade    | Descrição                                                                                                                                                                                                                                                                                                                                                                          |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| nKeyCode    | System. Int16Specifies que a chave física é pressionada. Para obter os valores possíveis, consulte comentários.<br/>                                                                                                                                                                                                                                                                                    |
| nShiftState | O campo do sistema. Int16a com os bits menos significativos correspondentes à tecla SHIFT (bit 0), a tecla CTRL (bit 1) e a tecla ALT (bit 2). Esses bits correspondem aos valores 1, 2 e 4, respectivamente. O argumento Shift indica o estado dessas chaves. Alguns, todos ou nenhum dos bits podem ser definidos, indicando que algumas, todas ou nenhuma das chaves são pressionadas.<br/> |



 

## <a name="remarks"></a>Comentários

A propriedade **nKeyCode** especifica uma chave física. As tabelas a seguir mostram os valores possíveis para as chaves principais em um teclado padrão.

Valores para as chaves principais.



| Chave                     | Valor   |
|-------------------------|---------|
| A-Z                     | 65-90   |
| 0-9                     | 48-56   |
| F1-F12                  | 112-123 |
| ESC                     | 27      |
| TAB                     | 9       |
| CAPS LOCK               | 20      |
| SHIFT (esquerda ou direita)   | 16      |
| CTRL (esquerda ou direita)    | 17      |
| ALT (esquerda ou direita)     | 18      |
| SPACE                   | 32      |
| BACKSPACE               | 8       |
| Enter                   | 13      |
| Tecla com o logotipo do Windows, esquerda  | 91      |
| Tecla com o logotipo do Windows, direita | 92      |
| Chave do aplicativo         | 93      |



 

Valores para as chaves do teclado numérico.



| Chave               | Valor  |
|-------------------|--------|
| 0-9               | 96-105 |
| NUM LOCK          | 144    |
| DIVIDIR (/)        | 111    |
| MULTIPLICAr ( \* )     | 106    |
| Subtrair (-)      | 109    |
| ADICIONAR (+)           | 107    |
| Separador (Enter) | 108    |
| DECIMAL (.)       | 110    |



 

Valores para as chaves de navegação.



| Chave         | Valor |
|-------------|-------|
| INSERT      | 45    |
| Delete (excluir)      | 46    |
| HOME        | 36    |
| END         | 35    |
| PAGE UP     | 33    |
| PAGE DOWN   | 34    |
| SETA PARA CIMA    | 38    |
| SETA PARA BAIXO  | 40    |
| SETA PARA A ESQUERDA  | 37    |
| SETA PARA A DIREITA | 39    |



 

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

 

 





