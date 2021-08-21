---
title: WM_SYSDEADCHAR mensagem (Winuser.h)
description: Enviado para a janela com o foco do teclado quando uma mensagem WM \_ SYSKEYDOWN é convertida pela função TranslateMessage.
ms.assetid: cf9a1171-a47c-4d7b-b351-31f41a893b20
keywords:
- WM_SYSDEADCHAR entrada do mouse e teclado da mensagem
topic_type:
- apiref
api_name:
- WM_SYSDEADCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e7ddf63ab4643ef59e45a4850a18a9823753c16a59b4519fe099326fe071704
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118757218"
---
# <a name="wm_sysdeadchar-message"></a>Mensagem \_ WM SYSDEADCHAR

Enviado para a janela com o foco do teclado quando uma mensagem [**WM \_ SYSKEYDOWN**](wm-syskeydown.md) é convertida pela [**função TranslateMessage.**](/windows/desktop/api/winuser/nf-winuser-translatemessage) **WM \_ SYSDEADCHAR** especifica o código de caractere de uma chave morta do sistema, ou seja, uma tecla morta pressionada enquanto mantém pressionada a tecla ALT.


```C++
#define WM_SYSDEADCHAR                  0x0107
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O código de caractere gerado pela chave morta do sistema, ou seja, uma tecla morta pressionada enquanto mantém pressionada a tecla ALT.

</dd> <dt>

*lParam* 
</dt> <dd>

A contagem de repetição, o código de verificação, o sinalizador de chave estendida, o código de contexto, o sinalizador de estado de chave anterior e o sinalizador de estado de transição, conforme mostrado na tabela a seguir.



| Bits  | Significado                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | A contagem de repetição para a mensagem atual. O valor é o número de vezes que o comutado de tecla é autoreado como resultado do usuário manter a chave. Se o tipo de tecla for mantido por tempo suficiente, várias mensagens serão enviadas. No entanto, a contagem de repetição não é cumulativa. |
| 16-23 | O código de verificação. O valor depende do OEM.                                                                                                                                                                                                                          |
| 24    | Indica se a chave é uma tecla estendida, como as teclas ALT e CTRL à direita que aparecem em um teclado aprimorado de 101 ou 102 teclas. O valor será 1 se for uma chave estendida; caso contrário, será 0.                                                              |
| 25-28 | Reservado; não use.                                                                                                                                                                                                                                                 |
| 29    | O código de contexto. O valor será 1 se a tecla ALT for mantida pressionada enquanto a tecla é pressionada; caso contrário, o valor será 0.                                                                                                                                                     |
| 30    | O estado da chave anterior. O valor será 1 se a chave estiver inoperante antes que a mensagem seja enviada ou será 0 se a chave estiver inoperante.                                                                                                                                                    |
| 31    | Estado de transição. O valor será 1 se a chave estiver sendo liberada ou será 0 se a chave estiver sendo pressionada.                                                                                                                                                                |

Para obter mais detalhes, consulte [Sinalizadores de mensagem de teclas](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um aplicativo deverá retornar zero se ele processa essa mensagem.

## <a name="remarks"></a>Comentários

Para teclados de 101 e 102 teclas aprimorados, as teclas estendidas são as teclas ALT e CTRL corretas na seção principal do teclado; as teclas INS, DEL, HOME, END, PAGE UP, PAGE DOWN e seta nos clusters à esquerda do teclado numérico; e as chaves de divisão (/) e ENTER no teclado numérico. Outros teclados podem dar suporte ao bit de chave estendida no *parâmetro lParam.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**Translatemessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**WM \_ DEADCHAR**](wm-deadchar.md)
</dt> <dt>

[**WM \_ SYSKEYDOWN**](wm-syskeydown.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Entrada do teclado](keyboard-input.md)
</dt> </dl>

 

