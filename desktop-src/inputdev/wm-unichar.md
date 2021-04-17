---
title: Mensagem de WM_UNICHAR (WinUser. h)
description: A mensagem do WM \_ UNICHAR pode ser usada por um aplicativo para postar a entrada para outras janelas.
ms.assetid: edbfcf14-0371-43ce-9676-eb10d964d0b7
keywords:
- Entrada de mouse e teclado de mensagem WM_UNICHAR
topic_type:
- apiref
api_name:
- WM_UNICHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 833b5cb59095f5aecc8c0172857c8761fd92449a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105770552"
---
# <a name="wm_unichar-message"></a>Mensagem do WM \_ UNICHAR

A mensagem do **WM \_ UNICHAR** pode ser usada por um aplicativo para postar a entrada para outras janelas. Essa mensagem contém o código de caractere da chave que foi pressionada. (Teste se um aplicativo de destino pode processar mensagens do **WM \_ UNICHAR** enviando a mensagem com *wParam* definido como **Unicode \_ nochar**.)


```C++
#define WM_UNICHAR                      0x0109
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O código de caractere da chave.

Se *wParam* for **Unicode \_ nochar** e o aplicativo processar essa mensagem, retornará **true**. A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retornará **false** (o padrão).

Se *wParam* não for **Unicode \_ nochar**, retornará **false**. O Unicode  [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) posta uma mensagem do [**WM \_ Char**](wm-char.md) com os mesmos parâmetros e a função ANSI **DefWindowProc** posta uma ou duas mensagens do **WM \_ Char** com os caracteres ANSI correspondentes.

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

A mensagem do **WM \_ UNICHAR** é semelhante ao [**WM \_ Char**](wm-char.md), mas usa o formato UTF (Unicode transformation Format)-32, enquanto o **WM \_ Char** usa UTF-16.

Essa mensagem foi criada para enviar ou postar caracteres Unicode para janelas ANSI e pode manipular caracteres de plano suplementar Unicode.

Como não há necessariamente uma correspondência de um para um entre as chaves pressionadas e as mensagens de caracteres geradas, as informações na palavra de ordem superior do parâmetro *lParam* geralmente não são úteis para os aplicativos. As informações na palavra de ordem superior aplicam-se apenas à mensagem do [**WM \_ KEYDOWN**](wm-keydown.md) mais recente que precede o lançamento da mensagem do **WM \_ UNICHAR** .

Para teclados avançados de 101 e 102 teclas, as chaves estendidas são as teclas ALT direita e direita na seção principal do teclado; as teclas INS, DEL, HOME, END, PAGE UP, PAGE DOWN e Arrow nos clusters à esquerda do teclado numérico; e a divisão (/) e inserir chaves no teclado numérico. Alguns teclados podem dar suporte ao bit de chave estendida no parâmetro *lParam* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**caractere do WM \_**](wm-char.md)
</dt> <dt>

[**o WM \_ KEYDOWN**](wm-keydown.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

