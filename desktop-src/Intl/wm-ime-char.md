---
description: Enviado a um aplicativo quando o IME obtém um caractere do resultado da conversão. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: 1e1353c3-5215-4829-a00a-2fee47a430eb
title: WM_IME_CHAR mensagem (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 337ca982cbd755e01f3dfab465d8b82948dfdbf053a4a7c03417a1d508bc42d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146779"
---
# <a name="wm_ime_char-message"></a>Mensagem CHAR \_ do WM IME \_

Enviado a um aplicativo quando o IME obtém um caractere do resultado da conversão. Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

*Hwnd* 
</dt> <dd>

Um alça para janela.

</dd> <dt>

*wParam* 
</dt> <dd>

**DBCS:** Um valor de caractere de byte único ou de dois byte. Para um caractere de byte duplo, (BYTE)(wParam >> 8) contém o byte principal. Observe que os parênteses são necessários porque o operador de cast tem precedência maior do que o operador shift.

**Unicode:** Um valor de caractere Unicode.

</dd> <dt>

*lParam* 
</dt> <dd>

A contagem de repetição, o código de verificação, o sinalizador de chave estendida, o código de contexto, o sinalizador de estado de chave anterior e o sinalizador de estado de transição, com valores conforme definido abaixo.



| bit   | Significado                                                                              |
|-------|--------------------------------------------------------------------------------------|
| 0-15  | Contagem de repetição. Como o primeiro byte e o segundo byte são contínuos, isso é sempre 1. |
| 16-23 | Digitalizar código para um caractere asiático completo.                                            |
| 24    | Chave estendida.                                                                        |
| 25-28 | Não usado.                                                                            |
| 29    | Código de contexto.                                                                        |
| 30    | Estado da chave anterior.                                                                  |
| 31    | Estado de transição.                                                                    |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao contrário [**da mensagem CHAR \_ WM**](../inputdev/wm-char.md) para uma janela não Unicode, essa mensagem pode incluir valores de caractere de byte duplo e de byte único. Para uma janela Unicode, essa mensagem é a mesma que WM \_ CHAR.

Para uma janela não Unicode, se a mensagem CHAR do WM IME incluir um caractere de byte duplo e o aplicativo passar essa mensagem para \_ \_ [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), o IME converterá essa mensagem em duas mensagens WM CHAR, cada uma contendo um byte do caractere de \_ byte duplo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de Métodos de Entrada](input-method-manager.md)
</dt> <dt>

[Mensagens do Gerenciador de Métodos de Entrada](input-method-manager-messages.md)
</dt> </dl>

 

 
