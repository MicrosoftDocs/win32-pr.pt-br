---
title: Mensagem de WM_SYSKEYUP (WinUser. h)
description: Postado na janela com o foco do teclado quando o usuário libera uma tecla que foi pressionada enquanto a tecla ALT era mantida pressionada.
ms.assetid: a4f62575-fb84-4390-a1d1-1a62629de55f
keywords:
- Entrada de mouse e teclado de mensagem WM_SYSKEYUP
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
ms.openlocfilehash: 2139c11558eccc3fb3b225f0cc1a87bcf6fb084d
ms.sourcegitcommit: cea2889abb43350c38cd120e877d8471dae78beb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298060"
---
# <a name="wm_syskeyup-message"></a>Mensagem do WM \_ SYSKEYUP

Postado na janela com o foco do teclado quando o usuário libera uma tecla que foi pressionada enquanto a tecla ALT era mantida pressionada. Ele também ocorre quando nenhuma janela tem o foco do teclado no momento; Nesse caso, a mensagem do **WM \_ SYSKEYUP** é enviada para a janela ativa. A janela que recebe a mensagem pode distinguir entre esses dois contextos verificando o código de contexto no parâmetro *lParam* .

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_SYSKEYUP                     0x0105
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O código de chave virtual da chave que está sendo liberada. Consulte [**códigos de chave virtual**](virtual-key-codes.md).

</dd> <dt>

*lParam* 
</dt> <dd>

A contagem de repetição, o código de verificação, o sinalizador de chave estendida, o código de contexto, o sinalizador de estado de chave anterior e o sinalizador de estado de transição, conforme mostrado na tabela a seguir.



| Bits  | Significado                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | A contagem de repetição para a mensagem atual. O valor é o número de vezes que o pressionamento de tecla é repetido de forma automática como resultado do usuário que mantém a chave. A contagem de repetição é sempre uma para uma mensagem do **WM \_ SYSKEYUP** .         |
| 16-23 | O código de verificação. O valor depende do OEM.                                                                                                                                                                                  |
| 24    | Indica se a chave é uma chave estendida, como as teclas ALT direita e CTRL que aparecem em um teclado avançado de 101 ou 102 teclas. O valor será 1 se for uma chave estendida; caso contrário, será zero.                   |
| 25-28 | Reservado Não use.                                                                                                                                                                                                         |
| 29    | O código do contexto. O valor será 1 se a tecla ALT estiver inoperante enquanto a chave for liberada; será zero se a mensagem do **WM \_ SYSKEYUP** for postada na janela ativa porque nenhuma janela tem o foco do teclado. |
| 30    | O estado de chave anterior. O valor é sempre 1 para uma mensagem do **WM \_ SYSKEYUP** .                                                                                                                                                 |
| 31    | O estado de transição. O valor é sempre 1 para uma mensagem do **WM \_ SYSKEYUP** .                                                                                                                                                   |

Para obter mais detalhes, consulte [sinalizadores de mensagem de pressionamento de tecla](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um aplicativo deve retornar zero se ele processar essa mensagem.

## <a name="remarks"></a>Comentários

A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envia uma mensagem do [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) para a janela de nível superior se a tecla F10 ou a tecla Alt foi liberada. O parâmetro *wParam* da mensagem é definido como **sc \_ keymenu**.

Quando o código de contexto for zero, a mensagem poderá ser passada para a função [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) , que o tratará como se fosse uma mensagem de chave normal em vez de uma mensagem de chave de caracteres. Isso permite que as teclas de aceleração sejam usadas com a janela ativa mesmo que a janela ativa não tenha o foco do teclado.

Para teclados avançados de 101 e 102 teclas, as chaves estendidas são as teclas ALT e CTRL pressionadas na seção principal do teclado; as teclas INS, DEL, HOME, END, PAGE UP, PAGE DOWN e Arrow nos clusters à esquerda do teclado numérico; e a divisão (/) e inserir chaves no teclado numérico. Outros teclados podem dar suporte ao bit de chave estendida no parâmetro *lParam* .

Para não-U. S. teclados avançados de 102 teclas, a tecla ALT direita é tratada como uma tecla CTRL + ALT. A tabela a seguir mostra a sequência de mensagens que resultam quando o usuário pressiona e libera essa chave.



| Mensagem                           | Código de chave virtual |
|-----------------------------------|------------------|
| [**o WM \_ KEYDOWN**](wm-keydown.md) | **\_controle VK**  |
| [**o WM \_ KEYDOWN**](wm-keydown.md) | **\_menu VK**     |
| [**o WM \_ KEYUP**](wm-keyup.md)     | **\_controle VK**  |
| **SYSKEYUP do WM \_**                  | **\_menu VK**     |



 

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

[**SYSKEYDOWN do WM \_**](wm-syskeydown.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

