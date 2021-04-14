---
title: Mensagem de WM_KEYUP (WinUser. h)
description: Postado na janela com o foco do teclado quando uma tecla que não é do sistema é liberada. Uma chave que não seja do sistema é uma chave que é pressionada quando a tecla ALT não é pressionada ou uma tecla do teclado pressionada quando uma janela tem o foco do teclado.
ms.assetid: 67d9d82d-fab0-4aec-a337-7a9cb2b0b586
keywords:
- Entrada de mouse e teclado de mensagem WM_KEYUP
topic_type:
- apiref
api_name:
- WM_KEYUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28aa02dd73f1706bb12ae30825f50241be7bb0d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369496"
---
# <a name="wm_keyup-message"></a>Mensagem do WM \_ KEYUP

Postado na janela com o foco do teclado quando uma tecla que não é do sistema é liberada. Uma chave que não seja do sistema é uma chave que é pressionada quando a tecla ALT *não* é pressionada ou uma tecla do teclado pressionada quando uma janela tem o foco do teclado.


```C++
#define WM_KEYUP                        0x0101
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O código de chave virtual da chave que não é do sistema. Consulte [códigos de chave virtual](virtual-key-codes.md).

</dd> <dt>

*lParam* 
</dt> <dd>

A contagem de repetição, o código de verificação, o sinalizador de chave estendida, o código de contexto, o sinalizador de estado de chave anterior e o sinalizador de estado de transição, conforme mostrado na tabela a seguir.



| Bits  | Significado                                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | A contagem de repetição para a mensagem atual. O valor é o número de vezes que o pressionamento de tecla é repetido de forma automática como resultado do usuário que mantém a chave. A contagem de repetição é sempre 1 para uma mensagem do **WM \_ KEYUP** . |
| 16-23 | O código de verificação. O valor depende do OEM.                                                                                                                                                                     |
| 24    | Indica se a chave é uma chave estendida, como as teclas ALT direita e CTRL que aparecem em um teclado avançado de 101 ou 102 teclas. O valor será 1 se for uma chave estendida; caso contrário, será 0.         |
| 25-28 | Reservado Não use.                                                                                                                                                                                            |
| 29    | O código do contexto. O valor é sempre 0 para uma mensagem do **WM \_ KEYUP** .                                                                                                                                             |
| 30    | O estado de chave anterior. O valor é sempre 1 para uma mensagem do **WM \_ KEYUP** .                                                                                                                                       |
| 31    | O estado de transição. O valor é sempre 1 para uma mensagem do **WM \_ KEYUP** .                                                                                                                                         |

Para obter mais detalhes, consulte [sinalizadores de mensagem de pressionamento de tecla](about-keyboard-input.md#keystroke-message-flags).
 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um aplicativo deve retornar zero se ele processar essa mensagem.

## <a name="remarks"></a>Comentários

A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envia uma mensagem do [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) para a janela de nível superior se a tecla F10 ou a tecla Alt foi liberada. O parâmetro *wParam* da mensagem é definido como SC \_ keymenu.

Para teclados avançados de 101 e 102 teclas, as chaves estendidas são as teclas ALT e CTRL pressionadas na seção principal do teclado; as teclas INS, DEL, HOME, END, PAGE UP, PAGE DOWN e Arrow nos clusters à esquerda do teclado numérico; e a divisão (/) e inserir chaves no teclado numérico. Outros teclados podem dar suporte ao bit de chave estendida no parâmetro *lParam* .

Os aplicativos devem passar *wParam* para [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) sem alterá-lo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**o WM \_ KEYDOWN**](wm-keydown.md)
</dt> <dt>

[**SYSCOMMAND do WM \_**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

