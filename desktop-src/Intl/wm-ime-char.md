---
description: Enviado a um aplicativo quando o IME Obtém um caractere do resultado da conversão. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: 1e1353c3-5215-4829-a00a-2fee47a430eb
title: Mensagem de WM_IME_CHAR (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0e2df06d9d837b0c1fbc0f9c9d9eb852252c47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104370779"
---
# <a name="wm_ime_char-message"></a>Mensagem de caracteres do \_ IME do WM \_

Enviado a um aplicativo quando o IME Obtém um caractere do resultado da conversão. Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
 HWND  hwnd,
 WM_IME_CHAR,
 WPARAM wParam,
 LPARAM lParam   
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* 
</dt> <dd>

Um identificador para a janela.

</dd> <dt>

*wParam* 
</dt> <dd>

**DBCS:** Um valor de caractere de byte único ou de byte duplo. Para um caractere de byte duplo, (BYTE) (wParam >> 8) contém o byte de Lead. Observe que os parênteses são necessários porque o operador cast tem precedência mais alta do que o operador shift.

**Unicode:** Um valor de caractere Unicode.

</dd> <dt>

*lParam* 
</dt> <dd>

A contagem de repetição, o código de verificação, o sinalizador de chave estendida, o código de contexto, o sinalizador de estado de chave anterior e o sinalizador de estado de transição, com valores definidos abaixo.



| bit   | Significado                                                                              |
|-------|--------------------------------------------------------------------------------------|
| 0-15  | Contagem de repetições. Como o primeiro byte e o segundo byte são contínuos, isso é sempre 1. |
| 16-23 | Código de verificação de um caractere asiático completo.                                            |
| 24    | Chave estendida.                                                                        |
| 25-28 | Não usado.                                                                            |
| 29    | Código de contexto.                                                                        |
| 30    | Estado de chave anterior.                                                                  |
| 31    | Estado de transição.                                                                    |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao contrário da mensagem do [**WM \_ Char**](../inputdev/wm-char.md) para uma janela não-Unicode, essa mensagem pode incluir valores de caractere de byte duplo e de byte único. Para uma janela Unicode, essa mensagem é igual ao WM \_ Char.

Para uma janela não-Unicode, se a \_ mensagem de caractere IME do WM \_ incluir um caractere de byte duplo e o aplicativo passar essa mensagem para [**DEFWINDOWPROC**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), o IME converterá essa mensagem em duas \_ mensagens do WM Char, cada uma contendo um byte do caractere de byte duplo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Mensagens do Gerenciador de métodos de entrada](input-method-manager-messages.md)
</dt> </dl>

 

 
