---
title: Como criar um controle de edição de várias linhas
description: Este tópico demonstra como implementar um processador de texto simples adicionando um controle de edição de várias linhas à área do cliente de uma janela.
ms.assetid: B955CC42-F89F-48EB-A19A-ADA6E5273EF6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05133707e9a47a632a70807177c6ec1b63bc842
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103917795"
---
# <a name="how-to-create-a-multiline-edit-control"></a><span data-ttu-id="c9fe3-103">Como criar um controle de edição de várias linhas</span><span class="sxs-lookup"><span data-stu-id="c9fe3-103">How to Create a Multiline Edit Control</span></span>

<span data-ttu-id="c9fe3-104">Este tópico demonstra como implementar um processador de texto simples adicionando um controle de edição de várias linhas à área do cliente de uma janela.</span><span class="sxs-lookup"><span data-stu-id="c9fe3-104">This topic demonstrates how to implement a simple word processor by adding a multiline edit control to the client area of a window.</span></span> <span data-ttu-id="c9fe3-105">Usando o controle de edição de várias linhas, o usuário pode selecionar editar comandos em um menu.</span><span class="sxs-lookup"><span data-stu-id="c9fe3-105">By using the multiline edit control, the user can select edit commands from a menu.</span></span> <span data-ttu-id="c9fe3-106">Esses comandos permitem que o usuário execute operações de edição simples, como desfazer uma ação anterior, recortar ou copiar seleções na área de transferência, colar texto da área de transferência e excluir a seleção atual.</span><span class="sxs-lookup"><span data-stu-id="c9fe3-106">These commands enable the user to perform simple editing operations such as undo a previous action, cut or copy selections to the clipboard, paste text from the clipboard, and delete the current selection.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="c9fe3-107">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="c9fe3-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c9fe3-108">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="c9fe3-108">Technologies</span></span>

-   [<span data-ttu-id="c9fe3-109">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="c9fe3-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="c9fe3-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="c9fe3-110">Prerequisites</span></span>

-   <span data-ttu-id="c9fe3-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="c9fe3-111">C/C++</span></span>
-   <span data-ttu-id="c9fe3-112">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="c9fe3-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="c9fe3-113">Instruções</span><span class="sxs-lookup"><span data-stu-id="c9fe3-113">Instructions</span></span>


<span data-ttu-id="c9fe3-114">Seu aplicativo deve incluir o código para criar uma instância do e inicializar um controle de edição de várias linhas e, em seguida, processar os comandos de edição do usuário.</span><span class="sxs-lookup"><span data-stu-id="c9fe3-114">Your application must include code to create an instance of and initialize a multiline edit control and then process user edit commands.</span></span>

<span data-ttu-id="c9fe3-115">O exemplo de código C++ a seguir implementa grande parte da funcionalidade de um processador de texto simples, adicionando um controle de edição de várias linhas à área do cliente de uma janela.</span><span class="sxs-lookup"><span data-stu-id="c9fe3-115">The following C++ code example implements much of the functionality of a simple word processor by adding a multiline edit control to the client area of a window.</span></span> <span data-ttu-id="c9fe3-116">O sistema executa automaticamente as operações de WordWrap para o controle de edição e também manipula o processamento da barra de rolagem vertical (criada especificando-se [**es \_ AUTOVSCROLL**](edit-control-styles.md) na chamada para a função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ).</span><span class="sxs-lookup"><span data-stu-id="c9fe3-116">The system automatically performs wordwrap operations for the edit control and also handles the processing for the vertical scroll bar (created by specifying [**ES\_AUTOVSCROLL**](edit-control-styles.md) in the call to the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) function).</span></span>

<span data-ttu-id="c9fe3-117">Os comandos de edição de usuário são enviados para o processo de janela por meio de mensagens de notificação de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="c9fe3-117">User edit commands are sent to the window process via [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) notification messages.</span></span>

> [!Note]  
> <span data-ttu-id="c9fe3-118">Se a janela incluir a faixa de faixas do Windows, o tamanho do controle de edição deverá ser ajustado para acomodar a altura da faixa de faixas.</span><span class="sxs-lookup"><span data-stu-id="c9fe3-118">If the window includes the Windows Ribbon, the size of the edit control must be adjusted to accommodate the height of the Ribbon.</span></span> <span data-ttu-id="c9fe3-119">Para obter mais informações, consulte [Windows Ribbon Framework](/windows/desktop/windowsribbon/-uiplat-windowsribbon-entry).</span><span class="sxs-lookup"><span data-stu-id="c9fe3-119">For more information, see [Windows Ribbon Framework](/windows/desktop/windowsribbon/-uiplat-windowsribbon-entry).</span></span>

 



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



## <a name="related-topics"></a><span data-ttu-id="c9fe3-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c9fe3-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9fe3-121">Sobre os controles de edição</span><span class="sxs-lookup"><span data-stu-id="c9fe3-121">About Edit Controls</span></span>](about-edit-controls.md)
</dt> <dt>

[<span data-ttu-id="c9fe3-122">Editar referência de controle</span><span class="sxs-lookup"><span data-stu-id="c9fe3-122">Edit Control Reference</span></span>](bumper-edit-control-edit-control-reference.md)
</dt> <dt>

[<span data-ttu-id="c9fe3-123">Usando controles de edição</span><span class="sxs-lookup"><span data-stu-id="c9fe3-123">Using Edit Controls</span></span>](/windows/desktop/Controls/using-edit-controls)
</dt> <dt>

[<span data-ttu-id="c9fe3-124">Controle de edição</span><span class="sxs-lookup"><span data-stu-id="c9fe3-124">Edit Control</span></span>](edit-controls.md)
</dt> </dl>

 

 