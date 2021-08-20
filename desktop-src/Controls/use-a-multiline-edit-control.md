---
title: Como criar um controle de edição de várias linhas
description: Este tópico demonstra como implementar um processador de texto simples adicionando um controle de edição de várias linhas à área do cliente de uma janela.
ms.assetid: B955CC42-F89F-48EB-A19A-ADA6E5273EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11100d4d6f82c7a352d4ddacaa7fc05694b4d54125febc766a6d3f1c68376e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829067"
---
# <a name="how-to-create-a-multiline-edit-control"></a>Como criar um controle de edição de várias linhas

Este tópico demonstra como implementar um processador de texto simples adicionando um controle de edição de várias linhas à área do cliente de uma janela. Usando o controle de edição de várias linhas, o usuário pode selecionar editar comandos em um menu. Esses comandos permitem que o usuário execute operações de edição simples, como desfazer uma ação anterior, recortar ou copiar seleções na área de transferência, colar texto da área de transferência e excluir a seleção atual.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Programação de interface do usuário

## <a name="instructions"></a>Instruções


Seu aplicativo deve incluir o código para criar uma instância do e inicializar um controle de edição de várias linhas e, em seguida, processar os comandos de edição do usuário.

O exemplo de código C++ a seguir implementa grande parte da funcionalidade de um processador de texto simples, adicionando um controle de edição de várias linhas à área do cliente de uma janela. O sistema executa automaticamente as operações de WordWrap para o controle de edição e também manipula o processamento da barra de rolagem vertical (criada especificando-se [**es \_ AUTOVSCROLL**](edit-control-styles.md) na chamada para a função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ).

Os comandos de edição de usuário são enviados para o processo de janela por meio de mensagens de notificação de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .

> [!Note]  
> se a janela incluir a faixa de Windows, o tamanho do controle de edição deverá ser ajustado para acomodar a altura da faixa de faixas. para obter mais informações, consulte [Windows estrutura da faixa](/windows/desktop/windowsribbon/-uiplat-windowsribbon-entry)de visualização.

 



```C++
#define ID_EDITCHILD 100
 
LRESULT CALLBACK MainWndProc(HWND hwnd,      // window handle 
                             UINT message,   // type of message 
                             WPARAM wParam,  // additional information 
                             LPARAM lParam)  // additional information 
{ 
    static HWND hwndEdit; 
 
    TCHAR lpszLatin[] =  L"Lorem ipsum dolor sit amet, consectetur "
                         L"adipisicing elit, sed do eiusmod tempor " 
                         L"incididunt ut labore et dolore magna " 
                         L"aliqua. Ut enim ad minim veniam, quis " 
                         L"nostrud exercitation ullamco laboris nisi " 
                         L"ut aliquip ex ea commodo consequat. Duis " 
                         L"aute irure dolor in reprehenderit in " 
                         L"voluptate velit esse cillum dolore eu " 
                         L"fugiat nulla pariatur. Excepteur sint " 
                         L"occaecat cupidatat non proident, sunt " 
                         L"in culpa qui officia deserunt mollit " 
                         L"anim id est laborum."; 
 
    switch (message) 
    { 
        case WM_CREATE: 
            hwndEdit = CreateWindowEx(
                                0, L"EDIT",   // predefined class 
                                NULL,         // no window title 
                                WS_CHILD | WS_VISIBLE | WS_VSCROLL | 
                                ES_LEFT | ES_MULTILINE | ES_AUTOVSCROLL, 
                                0, 0, 0, 0,   // set size in WM_SIZE message 
                                hwnd,         // parent window 
                                (HMENU) ID_EDITCHILD,   // edit control ID 
                                (HINSTANCE) GetWindowLongPtr(hwnd, GWLP_HINSTANCE), 
                                NULL);        // pointer not needed 
 
            // Add text to the window. 
            SendMessage(hwndEdit, WM_SETTEXT, 0, (LPARAM) lpszLatin); 
 
            return 0; 
 
        case WM_COMMAND: 
            switch (wParam) 
            { 
                case IDM_EDUNDO: 
                    // Send WM_UNDO only if there is something to be undone. 
 
                    if (SendMessage(hwndEdit, EM_CANUNDO, 0, 0)) 
                        SendMessage(hwndEdit, WM_UNDO, 0, 0); 
                    else 
                    {
                        MessageBox(hwndEdit, 
                                   L"Nothing to undo.", 
                                   L"Undo notification", 
                                   MB_OK); 
                    }
                    break; 
 
                case IDM_EDCUT: 
                    SendMessage(hwndEdit, WM_CUT, 0, 0); 
                    break; 
 
                case IDM_EDCOPY: 
                    SendMessage(hwndEdit, WM_COPY, 0, 0); 
                    break; 
 
                case IDM_EDPASTE: 
                    SendMessage(hwndEdit, WM_PASTE, 0, 0); 
                    break; 
 
                case IDM_EDDEL: 
                    SendMessage(hwndEdit, WM_CLEAR, 0, 0); 
                    break; 

                case IDM_ABOUT: 
                    DialogBox(hInst,                // current instance 
                              L"AboutBox",           // resource to use 
                              hwnd,                 // parent handle 
                              (DLGPROC) About); 
                    break; 

                default: 
                    return DefWindowProc(hwnd, message, wParam, lParam); 
            } 
            break; 

        case WM_SETFOCUS: 
            SetFocus(hwndEdit); 
            return 0; 

        case WM_SIZE: 
            // Make the edit control the size of the window's client area. 

            MoveWindow(hwndEdit, 
                       0, 0,                  // starting x- and y-coordinates 
                       LOWORD(lParam),        // width of client area 
                       HIWORD(lParam),        // height of client area 
                       TRUE);                 // repaint window 
            return 0; 

        case WM_DESTROY: 
            PostQuitMessage(0); 
            return 0; 

        default: 
            return DefWindowProc(hwnd, message, wParam, lParam); 
    } 
    return NULL; 
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre os controles de edição](about-edit-controls.md)
</dt> <dt>

[Editar referência de controle](bumper-edit-control-edit-control-reference.md)
</dt> <dt>

[Usando controles de edição](/windows/desktop/Controls/using-edit-controls)
</dt> <dt>

[Controle de edição](edit-controls.md)
</dt> </dl>

 

 