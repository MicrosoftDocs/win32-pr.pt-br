---
title: WM_SYSKEYUP mensagem (Winuser.h)
description: Postado na janela com o foco do teclado quando o usuário libera uma tecla que foi pressionada enquanto a tecla ALT era pressionada.
ms.assetid: a4f62575-fb84-4390-a1d1-1a62629de55f
keywords:
- WM_SYSKEYUP entrada do mouse e teclado da mensagem
topic_type:
- apiref
api_name:
- WM_SYSKEYUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e35a0267d29e473a3c2e5a6a00a0635a466f46c2917b913c3950aa6567e3cd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829856"
---
# <a name="wm_syskeyup-message"></a>Mensagem \_ WM SYSKEYUP

Postado na janela com o foco do teclado quando o usuário libera uma tecla que foi pressionada enquanto a tecla ALT era pressionada. Isso também ocorre quando nenhuma janela tem o foco do teclado no momento; nesse caso, a mensagem **WM \_ SYSKEYUP** é enviada para a janela ativa. A janela que recebe a mensagem pode distinguir entre esses dois contextos verificando o código de contexto no *parâmetro lParam.*

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_SYSKEYUP                     0x0105
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O código de chave virtual da chave que está sendo liberada. Consulte [**Códigos de chave virtual.**](virtual-key-codes.md)

</dd> <dt>

*lParam* 
</dt> <dd>

A contagem de repetição, o código de verificação, o sinalizador de chave estendida, o código de contexto, o sinalizador de estado de chave anterior e o sinalizador de estado de transição, conforme mostrado na tabela a seguir.



| Bits  | Significado                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | A contagem de repetição para a mensagem atual. O valor é o número de vezes que o comutado de tecla é autoreado como resultado do usuário manter a chave. A contagem de repetição é sempre uma para uma **\_ mensagem WM SYSKEYUP.**         |
| 16-23 | O código de verificação. O valor depende do OEM.                                                                                                                                                                                  |
| 24    | Indica se a chave é uma tecla estendida, como as teclas ALT e CTRL à direita que aparecem em um teclado aprimorado de 101 ou 102 teclas. O valor será 1 se for uma chave estendida; caso contrário, será zero.                   |
| 25-28 | Reservado; não use.                                                                                                                                                                                                         |
| 29    | O código de contexto. O valor será 1 se a tecla ALT estiver inobada enquanto a chave é liberada; será zero se a mensagem **WM \_ SYSKEYUP** for postada na janela ativa porque nenhuma janela tem o foco do teclado. |
| 30    | O estado da chave anterior. O valor é sempre 1 para uma mensagem **\_ WM SYSKEYUP.**                                                                                                                                                 |
| 31    | O estado de transição. O valor é sempre 1 para uma mensagem **\_ WM SYSKEYUP.**                                                                                                                                                   |

Para obter mais detalhes, consulte [Sinalizadores de mensagem de teclas](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um aplicativo deverá retornar zero se ele processa essa mensagem.

## <a name="remarks"></a>Comentários

A [**função DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) enviará uma mensagem [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) para a janela de nível superior se a tecla F10 ou a tecla ALT tiver sido liberada. O *parâmetro wParam* da mensagem é definido como **SC \_ KEYMENU.**

Quando o código de contexto é zero, a mensagem pode ser passada para a função [**TranslateAccelerator,**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) que o tratará como se fosse uma mensagem de chave normal em vez de uma mensagem de chave de caractere. Isso permite que as teclas de acelerador sejam usadas com a janela ativa, mesmo que a janela ativa não tenha o foco do teclado.

Para teclados de 101 e 102 teclas aprimorados, as teclas estendidas são as teclas ALT e CTRL corretas na seção principal do teclado; as teclas INS, DEL, HOME, END, PAGE UP, PAGE DOWN e seta nos clusters à esquerda do teclado numérico; e as chaves de divisão (/) e ENTER no teclado numérico. Outros teclados podem dar suporte ao bit de chave estendida no *parâmetro lParam.*

Para não EUA teclados de 102 teclas aprimorados, a tecla ALT direita é tratada como uma tecla CTRL+ALT. A tabela a seguir mostra a sequência de mensagens que resultam quando o usuário pressiona e libera essa chave.



| Mensagem                           | Código de chave virtual |
|-----------------------------------|------------------|
| [**WM \_ KEYDOWN**](wm-keydown.md) | **CONTROLE \_ de VK**  |
| [**WM \_ KEYDOWN**](wm-keydown.md) | **MENU da VK \_**     |
| [**WM \_ KEYUP**](wm-keyup.md)     | **CONTROLE \_ de VK**  |
| **WM \_ SYSKEYUP**                  | **MENU da VK \_**     |



 

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

[**Defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**Translateaccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[**WM \_ SYSKEYDOWN**](wm-syskeydown.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Entrada do teclado](keyboard-input.md)
</dt> </dl>

 

