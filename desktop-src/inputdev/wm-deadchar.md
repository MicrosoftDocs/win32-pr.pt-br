---
title: WM_DEADCHAR mensagem (Winuser.h)
description: Postado na janela com o foco do teclado quando uma mensagem WM KEYUP é convertida \_ pela função TranslateMessage.
ms.assetid: ada9a61c-dabf-447b-ae13-91803c097f0d
keywords:
- WM_DEADCHAR entrada do mouse e teclado da mensagem
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
ms.openlocfilehash: 4e4921d399c4a1c7a86596bfcc907b52d9c834235d133d6455b88c5a5a40c89a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778746"
---
# <a name="wm_deadchar-message"></a>Mensagem \_ WM DEADCHAR

Postado na janela com o foco do teclado quando uma mensagem [**WM \_ KEYUP**](wm-keyup.md) é convertida pela [**função TranslateMessage.**](/windows/desktop/api/winuser/nf-winuser-translatemessage) **WM \_ DEADCHAR** especifica um código de caractere gerado por uma chave morta. Uma chave morta é uma chave que gera um caractere, como o umlaut (ponto duplo), que é combinado com outro caractere para formar um caractere composto. Por exemplo, o caractere umlaut-O ( ) é gerado digitando a chave morta para o caractere umlaut e digitando a tecla O.


```C++
#define WM_DEADCHAR                     0x0103
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O código de caractere gerado pela chave morta.

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
| 31    | O estado de transição. O valor será 1 se a chave estiver sendo liberada ou será 0 se a chave estiver sendo pressionada.                                                                                                                                                            |

Para obter mais detalhes, consulte [Sinalizadores de mensagem de teclas](about-keyboard-input.md#keystroke-message-flags).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um aplicativo deverá retornar zero se ele processa essa mensagem.

## <a name="remarks"></a>Comentários

A **mensagem \_ WM DEADCHAR** normalmente é usada por aplicativos para dar ao usuário comentários sobre cada tecla pressionada. Por exemplo, um aplicativo pode exibir o destaque na posição do caractere atual sem mover o acento.

Como não há necessariamente uma correspondência um-para-um entre chaves pressionadas e mensagens de caractere geradas, as informações na palavra de ordem alta do parâmetro *lParam* geralmente não são úteis para aplicativos. As informações na palavra de ordem alta se aplica somente à mensagem [**WM \_ KEYDOWN**](wm-keydown.md) mais recente que precede a postagem da mensagem **WM \_ DEADCHAR.**

Para teclados de 101 e 102 teclas aprimorados, as teclas estendidas são a ALT direita e as teclas CTRL à direita na seção principal do teclado; as teclas INS, DEL, HOME, END, PAGE UP, PAGE DOWN e seta nos clusters à esquerda do teclado numérico; e as chaves de divisão (/) e ENTER no teclado numérico. Alguns outros teclados podem dar suporte ao bit de chave estendida no *parâmetro lParam.*

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

[**WM \_ KEYDOWN**](wm-keydown.md)
</dt> <dt>

[**WM \_ KEYUP**](wm-keyup.md)
</dt> <dt>

[**WM \_ SYSDEADCHAR**](wm-sysdeadchar.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Entrada do teclado](keyboard-input.md)
</dt> </dl>

 

