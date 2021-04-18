---
title: Mensagem de WM_SYSKEYDOWN (WinUser. h)
description: Postado na janela com o foco do teclado quando o usuário pressiona a tecla F10 (que ativa a barra de menus) ou mantém a tecla ALT pressionada e, em seguida, pressiona outra tecla.
ms.assetid: a3c03dbf-1be7-49ff-b931-1981786b74ce
keywords:
- Entrada de mouse e teclado de mensagem WM_SYSKEYDOWN
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
ms.openlocfilehash: b3053c5933a0388e3c8522b0d7201b491aaa4fa2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105794567"
---
# <a name="wm_syskeydown-message"></a>Mensagem do WM \_ SYSKEYDOWN

Postado na janela com o foco do teclado quando o usuário pressiona a tecla F10 (que ativa a barra de menus) ou mantém a tecla ALT pressionada e, em seguida, pressiona outra tecla. Ele também ocorre quando nenhuma janela tem o foco do teclado no momento; Nesse caso, a mensagem do **WM \_ SYSKEYDOWN** é enviada para a janela ativa. A janela que recebe a mensagem pode distinguir entre esses dois contextos verificando o código de contexto no parâmetro *lParam* .


```C++
#define WM_SYSKEYDOWN                   0x0104
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O código de chave virtual da chave que está sendo pressionada. Consulte [**códigos de chave virtual**](virtual-key-codes.md).

</dd> <dt>

*lParam* 
</dt> <dd>

A contagem de repetição, o código de verificação, o sinalizador de chave estendida, o código de contexto, o sinalizador de estado de chave anterior e o sinalizador de estado de transição, conforme mostrado na tabela a seguir.



| Bits  | Significado                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | A contagem de repetição para a mensagem atual. O valor é o número de vezes que o pressionamento de tecla é repetido de forma automática como resultado do usuário que mantém a chave. Se a tecla de pressionamento for mantida por tempo suficiente, várias mensagens serão enviadas. No entanto, a contagem de repetição não é cumulativa. |
| 16-23 | O código de verificação. O valor depende do OEM.                                                                                                                                                                                                                          |
| 24    | Indica se a chave é uma chave estendida, como as teclas ALT direita e CTRL que aparecem em um teclado avançado de 101 ou 102 teclas. O valor será 1 se for uma chave estendida; caso contrário, será 0.                                                              |
| 25-28 | Reservado Não use.                                                                                                                                                                                                                                                 |
| 29    | O código do contexto. O valor será 1 se a tecla ALT estiver inoperante enquanto a tecla for pressionada; será 0 se a mensagem do **WM \_ SYSKEYDOWN** for postada na janela ativa porque nenhuma janela tem o foco do teclado.                                                                  |
| 30    | O estado de chave anterior. O valor será 1 se a chave estiver inoperante antes de a mensagem ser enviada ou for 0 se a chave estiver ativa.                                                                                                                                                    |
| 31    | O estado de transição. O valor é sempre 0 para uma mensagem do **WM \_ SYSKEYDOWN** .                                                                                                                                                                                         |

Para obter mais detalhes, consulte [sinalizadores de mensagem de pressionamento de tecla](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um aplicativo deve retornar zero se ele processar essa mensagem.

## <a name="remarks"></a>Comentários

A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) examina a chave especificada e gera uma mensagem do [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) se a chave for Tab ou Enter.

Quando o código de contexto for zero, a mensagem poderá ser passada para a função [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) , que o tratará como se fosse uma mensagem de chave normal em vez de uma mensagem de chave de caracteres. Isso permite que as teclas de aceleração sejam usadas com a janela ativa mesmo que a janela ativa não tenha o foco do teclado.

Devido à repetição automática, mais de uma mensagem do **WM \_ SYSKEYDOWN** pode ocorrer antes de uma mensagem do [**WM \_ SYSKEYUP**](wm-syskeyup.md) ser enviada. O estado de chave anterior (bit 30) pode ser usado para determinar se a mensagem do **WM \_ SYSKEYDOWN** indica a primeira transição para baixo ou uma transição repetida.

Para teclados avançados de 101 e 102 teclas, as chaves avançadas são as teclas ALT e CTRL na seção principal do teclado; as teclas INS, DEL, HOME, END, PAGE UP, PAGE DOWN e Arrow nos clusters à esquerda do teclado numérico; e a divisão (/) e inserir chaves no teclado numérico. Outros teclados podem dar suporte ao bit de chave estendida no parâmetro *lParam* .

Essa mensagem também é enviada sempre que o usuário pressiona a tecla F10 sem a tecla ALT.

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

[**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**SYSCOMMAND do WM \_**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[**SYSKEYUP do WM \_**](wm-syskeyup.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

