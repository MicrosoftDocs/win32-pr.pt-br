---
title: Mensagem de WM_CHAR (WinUser. h)
description: Postado na janela com o foco do teclado quando uma \_ mensagem do WM KEYDOWN é convertida pela função TranslateMessage. A mensagem do WM \_ Char contém o código de caractere da chave que foi pressionada.
ms.assetid: 7e45dc6f-ff68-4534-9e52-46e5f4110532
keywords:
- Entrada de mouse e teclado de mensagem WM_CHAR
topic_type:
- apiref
api_name:
- WM_CHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/28/2020
ms.openlocfilehash: 8d174f64fa776b506814540d4f2c97635fba38a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785298"
---
# <a name="wm_char-message"></a>Mensagem do WM \_ Char

Postado na janela com o foco do teclado quando uma mensagem do [**WM \_ KEYDOWN**](wm-keydown.md) é convertida pela função [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) . A mensagem do **WM \_ Char** contém o código de caractere da chave que foi pressionada.


```C++
#define WM_CHAR                         0x0102
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O código de caractere da chave.

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

## <a name="example"></a>Exemplo

```cpp
LRESULT CALLBACK WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
   
    // ...

    case WM_CHAR:
        OnKeyPress(wParam);
        break;

    default:
        return DefWindowProc(hwnd, message, wParam, lParam);
    }
    return 0;
}
```
Exemplo de [exemplos clássicos do Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback/winmain.cpp) no github.

## <a name="remarks"></a>Comentários

A mensagem do **WM \_ Char** usa o formato UTF (Unicode Transformation Format)-16.

Não há necessariamente uma correspondência de um para um entre as chaves pressionadas e as mensagens de caracteres geradas e, portanto, as informações na palavra de ordem superior do parâmetro *lParam* geralmente não são úteis para os aplicativos. As informações na palavra de ordem superior aplicam-se apenas à mensagem do [**WM \_ KEYDOWN**](wm-keydown.md) mais recente que precede o lançamento da mensagem do **WM \_ Char** .

Para teclados avançados de 101 e 102 teclas, as chaves estendidas são as teclas ALT direita e direita na seção principal do teclado; as teclas INS, DEL, HOME, END, PAGE UP, PAGE DOWN e Arrow nos clusters à esquerda do teclado numérico; e a divisão (/) e inserir chaves no teclado numérico. Alguns teclados podem dar suporte ao bit de chave estendida no parâmetro *lParam* .

A mensagem do [**WM \_ UNICHAR**](wm-unichar.md) é igual à do **WM \_ Char**, exceto pelo uso de UTF-32. Ele foi projetado para enviar ou postar caracteres Unicode para janelas ANSI e pode manipular caracteres de plano suplementar Unicode.

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

[**UNICHAR do WM \_**](wm-unichar.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

