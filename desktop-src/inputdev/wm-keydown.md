---
title: Mensagem de WM_KEYDOWN (WinUser. h)
description: Postado na janela com o foco do teclado quando uma tecla que não é do sistema é pressionada. Uma chave que não seja do sistema é uma chave que é pressionada quando a tecla ALT não é pressionada.
ms.assetid: 0e37149f-445c-4b20-ad68-fdf39428ac91
keywords:
- Entrada de mouse e teclado de mensagem WM_KEYDOWN
topic_type:
- apiref
api_name:
- WM_KEYDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: ee6dc21b4fb90f0d02e80fce8ce6cc17099a0547
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797605"
---
# <a name="wm_keydown-message"></a>Mensagem de KEYDOWN do WM \_

Postado na janela com o foco do teclado quando uma tecla que não é do sistema é pressionada. Uma chave que não seja do sistema é uma chave que é pressionada quando a tecla ALT não é pressionada.


```C++
#define WM_KEYDOWN                      0x0100
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O código de chave virtual da chave que não é do sistema. Consulte [códigos de chave virtual](virtual-key-codes.md).

</dd> <dt>

*lParam* 
</dt> <dd>

A contagem de repetição, o código de verificação, o sinalizador de chave estendida, o código de contexto, o sinalizador de estado de chave anterior e o sinalizador de estado de transição, conforme mostrado a seguir.



| Bits  | Significado                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | A contagem de repetição para a mensagem atual. O valor é o número de vezes que o pressionamento de tecla é repetido de forma automática como resultado do usuário que mantém a chave. Se a tecla de pressionamento for mantida por tempo suficiente, várias mensagens serão enviadas. No entanto, a contagem de repetição não é cumulativa. |
| 16-23 | O código de verificação. O valor depende do OEM.                                                                                                                                                                                                                          |
| 24    | Indica se a chave é uma chave estendida, como as teclas ALT direita e CTRL que aparecem em um teclado avançado de 101 ou 102 teclas. O valor será 1 se for uma chave estendida; caso contrário, será 0.                                                              |
| 25-28 | Reservado Não use.                                                                                                                                                                                                                                                 |
| 29    | O código do contexto. O valor é sempre 0 para uma mensagem do **WM \_ KEYDOWN** .                                                                                                                                                                                                |
| 30    | O estado de chave anterior. O valor será 1 se a chave estiver inoperante antes de a mensagem ser enviada ou for zero se a chave estiver ativa.                                                                                                                                                 |
| 31    | O estado de transição. O valor é sempre 0 para uma mensagem do **WM \_ KEYDOWN** .                                                                                                                                                                                            |

Para obter mais detalhes, consulte [sinalizadores de mensagem de pressionamento de tecla](about-keyboard-input.md#keystroke-message-flags).
 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um aplicativo deve retornar zero se ele processar essa mensagem.

## <a name="example"></a>Exemplo

```cpp
LRESULT CALLBACK HostWndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message) 
    {
    case WM_KEYDOWN:
        if (wParam == VK_ESCAPE)
        {
            if (isFullScreen) 
            {
                GoPartialScreen();
            }
        }
        break;

    // ...
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;  
}

```

Exemplo de [exemplos clássicos do Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Magnification/cpp/Windowed/MagnifierSample.cpp) no github.


## <a name="remarks"></a>Comentários

Se a tecla F10 for pressionada, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) definirá um sinalizador interno. Quando **DefWindowProc** recebe a mensagem do [**WM \_ KEYUP**](wm-keyup.md) , a função verifica se o sinalizador interno está definido e, nesse caso, envia uma mensagem do [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) para a janela de nível superior. O parâmetro **WM \_ SYSCOMMAND** da mensagem é definido como SC \_ keymenu.

Devido ao recurso AutoRepetir, mais de uma mensagem do **WM \_ KEYDOWN** pode ser postada antes que uma mensagem do [**WM \_ KEYUP**](wm-keyup.md) seja postada. O estado de chave anterior (bit 30) pode ser usado para determinar se a mensagem do **WM \_ KEYDOWN** indica a primeira transição para baixo ou uma transição repetida.

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

[**caractere do WM \_**](wm-char.md)
</dt> <dt>

[**o WM \_ KEYUP**](wm-keyup.md)
</dt> <dt>

[**SYSCOMMAND do WM \_**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Entrada de teclado](keyboard-input.md)
</dt> </dl>

 

