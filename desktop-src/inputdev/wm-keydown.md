---
title: WM_KEYDOWN mensagem (Winuser.h)
description: Postado na janela com o foco do teclado quando uma tecla não sistema é pressionada. Uma chave não sistema é uma tecla pressionada quando a tecla ALT não é pressionada.
ms.assetid: 0e37149f-445c-4b20-ad68-fdf39428ac91
keywords:
- WM_KEYDOWN entrada do mouse e teclado da mensagem
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
ms.openlocfilehash: 9f54d0cad58a378d12247127d1ed70ab48653e18f4cceeb3c801efcf2aaae66d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717196"
---
# <a name="wm_keydown-message"></a>Mensagem WM \_ KEYDOWN

Postado na janela com o foco do teclado quando uma tecla não sistema é pressionada. Uma chave não sistema é uma tecla pressionada quando a tecla ALT não é pressionada.


```C++
#define WM_KEYDOWN                      0x0100
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O código de chave virtual da chave não sistema. Consulte [Códigos de chave virtual.](virtual-key-codes.md)

</dd> <dt>

*lParam* 
</dt> <dd>

A contagem de repetição, o código de verificação, o sinalizador de chave estendida, o código de contexto, o sinalizador de estado de chave anterior e o sinalizador de estado de transição, conforme mostrado a seguir.



| Bits  | Significado                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0-15  | A contagem de repetição para a mensagem atual. O valor é o número de vezes que o comutado de tecla é autoreado como resultado do usuário manter a chave. Se o tipo de tecla for mantido por tempo suficiente, várias mensagens serão enviadas. No entanto, a contagem de repetição não é cumulativa. |
| 16-23 | O código de verificação. O valor depende do OEM.                                                                                                                                                                                                                          |
| 24    | Indica se a chave é uma tecla estendida, como as teclas ALT e CTRL à direita que aparecem em um teclado aprimorado de 101 ou 102 teclas. O valor será 1 se for uma chave estendida; caso contrário, será 0.                                                              |
| 25-28 | Reservado; não use.                                                                                                                                                                                                                                                 |
| 29    | O código de contexto. O valor é sempre 0 para uma mensagem **WM \_ KEYDOWN.**                                                                                                                                                                                                |
| 30    | O estado da chave anterior. O valor será 1 se a chave estiver inoperante antes que a mensagem seja enviada ou será zero se a chave estiver para cima.                                                                                                                                                 |
| 31    | O estado de transição. O valor é sempre 0 para uma mensagem **WM \_ KEYDOWN.**                                                                                                                                                                                            |

Para obter mais detalhes, consulte [Sinalizadores de mensagem de teclas](about-keyboard-input.md#keystroke-message-flags).
 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um aplicativo deverá retornar zero se ele processa essa mensagem.

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

Exemplo de [Windows exemplos clássicos](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Magnification/cpp/Windowed/MagnifierSample.cpp) em GitHub.


## <a name="remarks"></a>Comentários

Se a tecla F10 for pressionada, a [**função DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) define um sinalizador interno. Quando **DefWindowProc** recebe a mensagem [**WM \_ KEYUP,**](wm-keyup.md) a função verifica se o sinalizador interno está definido e, em caso afirmativo, envia uma mensagem [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) para a janela de nível superior. O **parâmetro WM \_ SYSCOMMAND** da mensagem é definido como SC \_ KEYMENU.

Devido ao recurso de autoepeat, mais de uma mensagem **WM \_ KEYDOWN** pode ser postada antes que uma mensagem [**WM \_ KEYUP**](wm-keyup.md) seja postada. O estado da chave anterior (bit 30) pode ser usado para determinar se a mensagem **WM \_ KEYDOWN** indica a primeira transição para baixo ou uma transição para baixo repetida.

Para teclados de 101 e 102 teclas aprimorados, as teclas estendidas são as teclas ALT e CTRL corretas na seção principal do teclado; as teclas INS, DEL, HOME, END, PAGE UP, PAGE DOWN e seta nos clusters à esquerda do teclado numérico; e as chaves de divisão (/) e ENTER no teclado numérico. Outros teclados podem dar suporte ao bit de chave estendida no *parâmetro lParam.*

Os aplicativos *devem passar wParam* [**para TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) sem alterá-lo.

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

[**Translatemessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[**WM \_ CHAR**](wm-char.md)
</dt> <dt>

[**WM \_ KEYUP**](wm-keyup.md)
</dt> <dt>

[**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Entrada do teclado](keyboard-input.md)
</dt> </dl>

 

