---
title: Como criar uma interface de teclado para barras de rolagem padrão
description: Embora um controle de barra de rolagem forneça uma interface de teclado interna, uma barra de rolagem padrão não.
ms.assetid: 249D0077-6E61-479A-91D5-A4BD9752B82E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f25994639a40a6380bbf2f9cc0075e8a78b9e15787dbdf1babf0e6a15550faf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698736"
---
# <a name="how-to-create-a-keyboard-interface-for-standard-scroll-bars"></a>Como criar uma interface de teclado para barras de rolagem padrão

Embora um controle de barra de rolagem forneça uma interface de teclado interna, uma barra de rolagem padrão não. Para implementar uma interface de teclado para uma barra de rolagem padrão, um procedimento de janela deve processar a mensagem do [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) e examinar o código de chave virtual especificado pelo parâmetro *wParam* . Se o código de chave virtual corresponder a uma tecla de direção, o procedimento de janela enviará a si mesmo uma mensagem do [**WM \_ HSCROLL**](wm-hscroll.md) ou do [**WM \_ VSCROLL**](wm-vscroll.md) com a palavra de ordem inferior do parâmetro *wParam* definido como o código de solicitação da barra de rolagem apropriada.

Por exemplo, quando o usuário pressiona a tecla de seta para cima, o procedimento de janela recebe uma mensagem do [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) com *wParam* igual a VK \_ up. Em resposta, o procedimento de janela envia a si mesmo uma mensagem do [**WM \_ VSCROLL**](wm-vscroll.md) com a palavra de ordem inferior do *wParam* definido para o código de solicitação da linha do SB \_ .

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Programação de interface do usuário

## <a name="instructions"></a>Instruções

### <a name="create-a-keyboard-interface-for-a-standard-scroll-bar"></a>Criar uma interface de teclado para uma barra de rolagem padrão

O exemplo de código a seguir demonstra como incluir uma interface de teclado para uma barra de rolagem padrão.


```C++
    case WM_KEYDOWN: 
    {
        WORD wScrollNotify = 0xFFFF;

        switch (wParam) 
        { 
            case VK_UP: 
                wScrollNotify = SB_LINEUP; 
                break; 
 
            case VK_PRIOR: 
                wScrollNotify = SB_PAGEUP; 
                break; 
 
            case VK_NEXT: 
                wScrollNotify = SB_PAGEDOWN; 
                break; 
 
            case VK_DOWN: 
                wScrollNotify = SB_LINEDOWN; 
                break; 
 
            case VK_HOME: 
                wScrollNotify = SB_TOP; 
                break; 
 
            case VK_END: 
                wScrollNotify = SB_BOTTOM; 
                break; 
        } 
 
        if (wScrollNotify != -1) 
            SendMessage(hwnd, WM_VSCROLL, MAKELONG(wScrollNotify, 0), 0L); 
 
        break; 
    }
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando barras de rolagem](using-scroll-bars.md)
</dt> <dt>

[Windows de demonstração de controles comuns (CppWindowsCommonControls)](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/OneCodeTeam/Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/%5BC++%5D-Windows%20common%20controls%20demo%20(CppWindowsCommonControls)/C++/CppWindowsCommonControls)
</dt> </dl>

 

 