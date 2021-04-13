---
title: Mensagem de WM_SYSCHAR (WinUser. h)
description: Postado na janela com o foco do teclado quando uma \_ mensagem do WM SYSKEYDOWN é convertida pela função TranslateMessage.
ms.assetid: 55987105-3c53-42e5-8fab-a3c9f2ca7273
keywords:
- WM_SYSCHAR menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_SYSCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d14d2f8829cfd199049d3a1b254065918393c18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499835"
---
# <a name="wm_syschar-message"></a>Mensagem do WM \_ SYSCHAR

Postado na janela com o foco do teclado quando uma mensagem do [**WM \_ SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) é convertida pela função [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) . Especifica o código de caractere de uma chave de caractere do sistema que é uma tecla de caractere que é pressionada enquanto a tecla ALT está inativa.


```C++
#define WM_SYSCHAR                      0x0106
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O código de caractere da tecla de menu da janela.

</dd> <dt>

*lParam* 
</dt> <dd>

A contagem de repetição, o código de verificação, o sinalizador de chave estendida, o código de contexto, o sinalizador de estado de chave anterior e o sinalizador de estado de transição, conforme mostrado na tabela a seguir.



| Bits                                                                             | Significado                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 15</dt> </dl>  | A contagem de repetição para a mensagem atual. O valor é o número de vezes que o pressionamento de tecla foi repetido automaticamente como resultado do usuário que mantém a chave. Se a tecla de pressionamento for mantida por tempo suficiente, várias mensagens serão enviadas. No entanto, a contagem de repetição não é cumulativa.<br/> |
| <dl> <dt>16 23</dt> </dl> | O código de verificação. O valor depende do OEM (fabricante original do equipamento).<br/>                                                                                                                                                                                          |
| <dl> <dt>24</dt> </dl>    | Indica se a chave é uma chave estendida, como as teclas ALT direita e CTRL que aparecem em um teclado avançado de 101 ou 102 teclas. O valor será 1 se for uma chave estendida; caso contrário, será 0.<br/>                                                                |
| <dl> <dt>25 28</dt> </dl> | Reservado Não use.<br/>                                                                                                                                                                                                                                                   |
| <dl> <dt>29</dt> </dl>    | O código do contexto. O valor será 1 se a tecla ALT for mantida pressionada enquanto a tecla for pressionada; caso contrário, o valor será 0.<br/>                                                                                                                                                       |
| <dl> <dt>30</dt> </dl>    | O estado de chave anterior. O valor será 1 se a chave estiver inoperante antes de a mensagem ser enviada ou for 0 se a chave estiver ativa.<br/>                                                                                                                                                      |
| <dl> <dt>31</dt> </dl>    | O estado de transição. O valor será 1 se a chave estiver sendo liberada ou for 0 se a chave estiver sendo pressionada.<br/>                                                                                                                                                              |

Para obter mais detalhes, consulte [sinalizadores de mensagem de pressionamento de tecla](../inputdev/about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um aplicativo deve retornar zero se ele processar essa mensagem.

## <a name="remarks"></a>Comentários

Quando o código de contexto for zero, a mensagem poderá ser passada para a função [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) , que o tratará como se fosse uma mensagem de chave padrão em vez de uma mensagem de chave de caractere do sistema. Isso permite que as teclas de aceleração sejam usadas com a janela ativa mesmo que a janela ativa não tenha o foco do teclado.

Para teclados avançados de 101 e 102 teclas, as chaves estendidas são as teclas ALT e CTRL pressionadas na seção principal do teclado; as teclas INS, DEL, HOME, END, PAGE UP, PAGE DOWN e Arrow nos clusters à esquerda do teclado numérico; a chave de SCRN de impressão; a chave de interrupção; a tecla NUMLOCK; e a divisão (/) e inserir chaves no teclado numérico. Outros teclados podem dar suporte ao bit de chave estendida no parâmetro.

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

[**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**SYSKEYDOWN do WM \_**](/windows/desktop/inputdev/wm-syskeydown)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

