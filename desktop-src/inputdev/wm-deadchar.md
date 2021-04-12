---
title: Mensagem de WM_DEADCHAR (WinUser. h)
description: Postado na janela com o foco do teclado quando uma \_ mensagem do WM KEYUP é convertida pela função TranslateMessage.
ms.assetid: ada9a61c-dabf-447b-ae13-91803c097f0d
keywords:
- Entrada de mouse e teclado de mensagem WM_DEADCHAR
topic_type:
- apiref
api_name:
- WM_DEADCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6053095b912360e9875fa062c2daba7cafcfd43b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454962"
---
# <a name="wm_deadchar-message"></a>Mensagem do WM \_ DEADCHAR

Postado na janela com o foco do teclado quando uma mensagem do [**WM \_ KEYUP**](wm-keyup.md) é convertida pela função [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) . **WM \_ DEADCHAR** especifica um código de caractere gerado por uma chave inativa. Uma chave inativa é uma chave que gera um caractere, como o trema (ponto duplo), que é combinado com outro caractere para formar um caractere composto. Por exemplo, o caractere de trema () é gerado digitando-se a chave inativa para o caractere de trema e, em seguida, digitando a tecla o.


```C++
#define WM_DEADCHAR                     0x0103
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O código de caractere gerado pela chave inativa.

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
| 29    | O código do contexto. O valor será 1 se a tecla ALT for mantida pressionada enquanto a tecla for pressionada; caso contrário, o valor será 0.                                                                                                                                                     |
| 30    | O estado de chave anterior. O valor será 1 se a chave estiver inoperante antes de a mensagem ser enviada ou for 0 se a chave estiver ativa.                                                                                                                                                    |
| 31    | O estado de transição. O valor será 1 se a chave estiver sendo liberada ou for 0 se a chave estiver sendo pressionada.                                                                                                                                                            |

Para obter mais detalhes, consulte [sinalizadores de mensagem de pressionamento de tecla](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um aplicativo deve retornar zero se ele processar essa mensagem.

## <a name="remarks"></a>Comentários

A mensagem do **WM \_ DEADCHAR** normalmente é usada por aplicativos para fornecer aos comentários do usuário sobre cada tecla pressionada. Por exemplo, um aplicativo pode exibir o acento na posição do caractere atual sem mover o cursor.

Como não há necessariamente uma correspondência de um para um entre as chaves pressionadas e as mensagens de caracteres geradas, as informações na palavra de ordem superior do parâmetro *lParam* geralmente não são úteis para os aplicativos. As informações na palavra de ordem superior aplicam-se apenas à mensagem do [**WM \_ KEYDOWN**](wm-keydown.md) mais recente que precede o lançamento da mensagem do **WM \_ DEADCHAR** .

Para teclados avançados de 101 e 102 teclas, as chaves estendidas são as teclas ALT direita e direita na seção principal do teclado; as teclas INS, DEL, HOME, END, PAGE UP, PAGE DOWN e Arrow nos clusters à esquerda do teclado numérico; e a divisão (/) e inserir chaves no teclado numérico. Alguns teclados podem dar suporte ao bit de chave estendida no parâmetro *lParam* .

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

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**o WM \_ KEYDOWN**](wm-keydown.md)
</dt> <dt>

[**o WM \_ KEYUP**](wm-keyup.md)
</dt> <dt>

[**SYSDEADCHAR do WM \_**](wm-sysdeadchar.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

