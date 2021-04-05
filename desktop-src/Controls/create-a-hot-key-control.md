---
title: Como criar um controle de tecla de atalho
description: Este tópico demonstra como criar um controle de tecla de atalho. Você cria um controle de tecla quente usando a função CreateWindowEx, especificando a classe de janela de classe de tecla de atalho \_ .
ms.assetid: A6723D4E-B8F6-4365-8FCD-99B73D2C0470
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 498005efcdfbbf001283551bbeea4906ebc854cf
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103824077"
---
# <a name="how-to-create-a-hot-key-control"></a>Como criar um controle de tecla de atalho

Este tópico demonstra como criar um controle de tecla de atalho. Você cria um controle de tecla quente usando a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando a classe de janela de classe de tecla de atalho \_ .

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções


Antes de criar o controle de teclas de acesso, verifique se a DLL de controles comuns está carregada.

No exemplo de código C++ a seguir, a função definida pelo aplicativo chama a função [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) para carregar a DLL de controle comum. Em seguida, ele chama a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especificando a classe de janela de **\_ classe de tecla de atalho** para criar um controle de tecla de atalho. Ele usa as mensagens [**hkm \_ SetRules**](hkm-setrules.md) e [**hkm \_**](hkm-sethotkey.md) set para inicializar o controle e retorna um identificador para o controle.

Esse controle de teclas de acesso não permite que o usuário escolha uma tecla de atalho que seja uma única chave não modificada, nem permite que o usuário escolha apenas SHIFT e uma chave. Essas regras impedem efetivamente que o usuário escolha uma tecla de atalho que pode ser inserida acidentalmente ao digitar o texto.



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

[Referência de controle de teclas de acesso](bumper-hot-key-hot-key-control-reference.md)
</dt> <dt>

[Sobre os controles de tecla de atalho](hot-key-controls.md)
</dt> <dt>

[Usando controles de tecla quente](using-hot-key-controls.md)
</dt> </dl>

 

 