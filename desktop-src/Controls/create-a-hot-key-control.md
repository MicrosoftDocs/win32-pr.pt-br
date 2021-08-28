---
title: Como criar um controle de tecla quente
description: Este tópico demonstra como criar um controle de tecla de acesso. Você cria um controle de teclas de acesso usando a função CreateWindowEx, especificando a classe de janela HOTKEY \_ CLASS.
ms.assetid: A6723D4E-B8F6-4365-8FCD-99B73D2C0470
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081db39f07e8d80fcbb5a437bc8cbe83473b4299282c8b2437d95acda02b2db9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577036"
---
# <a name="how-to-create-a-hot-key-control"></a>Como criar um controle de tecla quente

Este tópico demonstra como criar um controle de tecla de acesso. Você cria um controle de teclas de acesso usando a [**função CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) especificando a classe de janela HOTKEY \_ CLASS.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Interface do Usuário programação

## <a name="instructions"></a>Instruções


Antes de criar o controle de tecla quente, verifique se a DLL de controles comuns está carregada.

No exemplo de código C++ a seguir, a função definida pelo aplicativo chama a função [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) para carregar a DLL de controle comum. Em seguida, ele chama a [**função CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) especificando a classe de janela **HOTKEY \_ CLASS,** para criar um controle de tecla quente. Ele usa as [**mensagens HKM \_ SETRULES**](hkm-setrules.md) e [**HKM \_ SETHOTKEY**](hkm-sethotkey.md) para inicializar o controle e retorna um alça para o controle .

Esse controle de teclas de acesso não permite que o usuário escolha uma tecla de acesso que seja uma única chave não modificada, nem permite que o usuário escolha apenas SHIFT e uma chave. Essas regras impedem efetivamente que o usuário escolha uma tecla quente que pode ser inserida acidentalmente ao digitar texto.



```C++
// Creates a hot key control and sets rules and default settings for it.
// 
// Returns the handle of the hot key control. 
//
// Parameter
//     hwndDlg - Handle of the parent window (dialog box). 
// 
// Global variable 
//     g_hinst - Handle of the application instance. 

extern HINSTANCE g_hinst; 

HWND WINAPI InitializeHotkey(HWND hwndDlg) 
{ 
    HWND hwndHot = NULL;
    
    // Ensure that the common control DLL is loaded. 
    INITCOMMONCONTROLSEX icex;  //declare an INITCOMMONCONTROLSEX Structure
    icex.dwSize = sizeof(INITCOMMONCONTROLSEX);
    icex.dwICC = ICC_HOTKEY_CLASS;   //set dwICC member to ICC_HOTKEY_CLASS    
                                     // this loads the Hot Key control class.
    InitCommonControlsEx(&icex);  
 
    hwndHot = CreateWindowEx(0,                        // no extended styles 
                             HOTKEY_CLASS,             // class name 
                             TEXT(""),                 // no title (caption) 
                             WS_CHILD | WS_VISIBLE,    // style 
                             15, 10,                   // position 
                             200, 20,                  // size 
                             hwndDlg,                  // parent window 
                             NULL,                     // uses class menu 
                             g_hinst,                  // instance 
                             NULL);                    // no WM_CREATE parameter 
 
    SetFocus(hwndHot); 
 
    // Set rules for invalid key combinations. If the user does not supply a
    // modifier key, use ALT as a modifier. If the user supplies SHIFT as a 
    // modifier key, use SHIFT + ALT instead.
    SendMessage(hwndHot, 
                HKM_SETRULES, 
                (WPARAM) HKCOMB_NONE | HKCOMB_S,   // invalid key combinations 
                MAKELPARAM(HOTKEYF_ALT, 0));       // add ALT to invalid entries 
 
    // Set CTRL + ALT + A as the default hot key for this window. 
    // 0x41 is the virtual key code for 'A'. 
    SendMessage(hwndHot, 
                HKM_SETHOTKEY, 
                MAKEWORD(0x41, HOTKEYF_CONTROL | HOTKEYF_ALT), 
                0); 
 
    return hwndHot; 
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de controle de tecla de acesso](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[Sobre controles de teclas de acesso](hot-key-controls.md)
</dt> <dt>

[Usando controles de teclas de acesso](using-hot-key-controls.md)
</dt> </dl>

 

 