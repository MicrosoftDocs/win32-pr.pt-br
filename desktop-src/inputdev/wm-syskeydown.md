---
title: WM_SYSKEYDOWN mensagem (Winuser.h)
description: Postado na janela com o foco do teclado quando o usuário pressiona a tecla F10 (que ativa a barra de menus) ou mantém a tecla ALT pressionada e pressiona outra tecla.
ms.assetid: a3c03dbf-1be7-49ff-b931-1981786b74ce
keywords:
- WM_SYSKEYDOWN entrada do mouse e teclado da mensagem
topic_type:
- apiref
api_name:
- WM_SYSKEYDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30b1398d843711e868a6b5b96cf6a66893bf74fef1e50bfdd61fa36f81f05c13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119611316"
---
# <a name="wm_syskeydown-message"></a>Mensagem \_ WM SYSKEYDOWN

Postado na janela com o foco do teclado quando o usuário pressiona a tecla F10 (que ativa a barra de menus) ou mantém a tecla ALT pressionada e pressiona outra tecla. Isso também ocorre quando nenhuma janela tem o foco do teclado no momento; nesse caso, a mensagem **WM \_ SYSKEYDOWN** é enviada para a janela ativa. A janela que recebe a mensagem pode distinguir entre esses dois contextos verificando o código de contexto no *parâmetro lParam.*


```C++
#define WM_SYSKEYDOWN                   0x0104
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O código de chave virtual da chave que está sendo pressionada. Consulte [**Códigos de chave virtual.**](virtual-key-codes.md)

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
| 29    | O código de contexto. O valor será 1 se a tecla ALT estiver inobada enquanto a tecla é pressionada; será 0 se a mensagem **WM \_ SYSKEYDOWN** for postada na janela ativa porque nenhuma janela tem o foco do teclado.                                                                  |
| 30    | O estado da chave anterior. O valor será 1 se a chave estiver inoperante antes que a mensagem seja enviada ou será 0 se a chave estiver inoperante.                                                                                                                                                    |
| 31    | O estado de transição. O valor é sempre 0 para uma **mensagem WM \_ SYSKEYDOWN.**                                                                                                                                                                                         |

Para obter mais detalhes, consulte [Sinalizadores de mensagem de teclas](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um aplicativo deverá retornar zero se ele processa essa mensagem.

## <a name="remarks"></a>Comentários

A [**função DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) examina a chave especificada e gera uma mensagem [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) se a chave for TAB ou ENTER.

Quando o código de contexto é zero, a mensagem pode ser passada para a função [**TranslateAccelerator,**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) que o tratará como se fosse uma mensagem de chave normal em vez de uma mensagem de chave de caractere. Isso permite que as teclas de acelerador sejam usadas com a janela ativa, mesmo que a janela ativa não tenha o foco do teclado.

Devido à repetição automática, mais de uma mensagem **WM \_ SYSKEYDOWN** pode ocorrer antes que uma mensagem [**WM \_ SYSKEYUP**](wm-syskeyup.md) seja enviada. O estado da chave anterior (bit 30) pode ser usado para determinar se a mensagem **WM \_ SYSKEYDOWN** indica a primeira transição para baixo ou uma transição para baixo repetida.

Para teclados de 101 e 102 teclas aprimorados, as teclas aprimoradas são as teclas ALT e CTRL corretas na seção principal do teclado; as teclas INS, DEL, HOME, END, PAGE UP, PAGE DOWN e seta nos clusters à esquerda do teclado numérico; e as chaves de divisão (/) e ENTER no teclado numérico. Outros teclados podem dar suporte ao bit de chave estendida no *parâmetro lParam.*

Essa mensagem também é enviada sempre que o usuário pressiona a tecla F10 sem a tecla ALT.

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

[**WM \_ SYSKEYUP**](wm-syskeyup.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Entrada do teclado](keyboard-input.md)
</dt> </dl>

 

