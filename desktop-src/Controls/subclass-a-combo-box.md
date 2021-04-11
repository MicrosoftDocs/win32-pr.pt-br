---
title: Como subclasse de uma caixa de combinação
description: Este tópico demonstra como caixas de combinação de subclasses.
ms.assetid: 9897EA94-1BF7-4711-AED6-5E9C863C287A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b48301309597c53f02ca87d1d1748ab1fe05139
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008465"
---
# <a name="how-to-subclass-a-combo-box"></a><span data-ttu-id="368c9-103">Como subclasse de uma caixa de combinação</span><span class="sxs-lookup"><span data-stu-id="368c9-103">How to Subclass a Combo Box</span></span>

<span data-ttu-id="368c9-104">Este tópico demonstra como caixas de combinação de subclasses.</span><span class="sxs-lookup"><span data-stu-id="368c9-104">This topic demonstrates how to subclass combo boxes.</span></span> <span data-ttu-id="368c9-105">O aplicativo de exemplo C++ cria uma janela de barra de ferramentas que contém duas caixas de combinação.</span><span class="sxs-lookup"><span data-stu-id="368c9-105">The C++ example application creates a toolbar window that contains two combo boxes.</span></span> <span data-ttu-id="368c9-106">Por meio da subclasse dos controles de edição dentro das caixas de combinação, a janela da barra de ferramentas intercepta as teclas TAB, ENTER e ESC que, de outra forma, seriam ignoradas.</span><span class="sxs-lookup"><span data-stu-id="368c9-106">By subclassing the edit controls within the combo boxes, the toolbar window intercepts TAB, ENTER, and ESC keys that would otherwise be ignored.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="368c9-107">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="368c9-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="368c9-108">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="368c9-108">Technologies</span></span>

-   [<span data-ttu-id="368c9-109">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="368c9-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="368c9-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="368c9-110">Prerequisites</span></span>

-   <span data-ttu-id="368c9-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="368c9-111">C/C++</span></span>
-   <span data-ttu-id="368c9-112">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="368c9-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="368c9-113">Instruções</span><span class="sxs-lookup"><span data-stu-id="368c9-113">Instructions</span></span>

### <a name="process-the-wm_create-message"></a><span data-ttu-id="368c9-114">Processar a mensagem de criação do WM \_</span><span class="sxs-lookup"><span data-stu-id="368c9-114">Process the WM\_CREATE Message</span></span>

<span data-ttu-id="368c9-115">O aplicativo processa a mensagem de [**\_ criação do WM**](/windows/desktop/winmsg/wm-create) para criar dois controles de caixa de combinação como janelas filhas.</span><span class="sxs-lookup"><span data-stu-id="368c9-115">The application processes the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message to create two combo box controls as child windows.</span></span>


```C++
//  Create two combo box child windows. 
dwBaseUnits = GetDialogBaseUnits(); 
 
hwndCombo1 = CreateWindow(L"COMBOBOX", L"", 
    CBS_DROPDOWN | WS_CHILD | WS_VISIBLE, 
    (6 * LOWORD(dwBaseUnits)) / 4, 
    (2 * HIWORD(dwBaseUnits)) / 8, 
    (100 * LOWORD(dwBaseUnits)) / 4, 
    (50 * HIWORD(dwBaseUnits)) / 8, 
    hwnd, NULL, NULL, NULL);  
 
hwndCombo2 = CreateWindow(L"COMBOBOX", L"", 
    CBS_DROPDOWN | WS_CHILD | WS_VISIBLE, 
    (112 * LOWORD(dwBaseUnits)) / 4, 
    (2 * HIWORD(dwBaseUnits)) / 8, 
    (100 * LOWORD(dwBaseUnits)) / 4, 
    (50 * HIWORD(dwBaseUnits)) / 8, 
    hwnd, NULL, hInst, NULL); 
```



<span data-ttu-id="368c9-116">O aplicativo, em seguida, subclasseia os controles de edição (campos de seleção) em cada caixa de combinação, porque eles recebem a entrada de caracteres para a caixa de combinação simples e suspensa.</span><span class="sxs-lookup"><span data-stu-id="368c9-116">The application then subclasses the edit controls (selection fields) in each combo box, because they receive the character input for simple and drop-down combo box.</span></span> <span data-ttu-id="368c9-117">Por fim, ele chama a função [**ChildWindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-childwindowfrompoint) para recuperar o identificador para cada controle de edição.</span><span class="sxs-lookup"><span data-stu-id="368c9-117">Finally, it calls the [**ChildWindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-childwindowfrompoint) function to retrieve the handle to each edit control.</span></span>

<span data-ttu-id="368c9-118">Para subclasses dos controles de edição, o aplicativo chama a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) , substituindo o ponteiro pelo procedimento da janela de classe por um ponteiro para a função **SubClassProc** definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="368c9-118">To subclass the edit controls, the application calls the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function, replacing the pointer to the class window procedure with a pointer to the application-defined **SubClassProc** function.</span></span> <span data-ttu-id="368c9-119">O ponteiro para o procedimento de janela original é salvo na variável global *lpfnEditWndProc*.</span><span class="sxs-lookup"><span data-stu-id="368c9-119">The pointer to the original window procedure is saved in the global variable *lpfnEditWndProc*.</span></span>

<span data-ttu-id="368c9-120">**SubClassProc** INTERCEPTA a guia, Enter e teclas ESC e notifica a janela da barra de ferramentas enviando mensagens definidas pelo aplicativo ( \_ guia WM, o WM \_ ESC e o WM \_ entram).</span><span class="sxs-lookup"><span data-stu-id="368c9-120">**SubClassProc** intercepts TAB, ENTER, and ESC keys and notifies the toolbar window by sending application-defined messages (WM\_TAB, WM\_ESC, and WM\_ENTER).</span></span> <span data-ttu-id="368c9-121">**SubClassProc** usa a função [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) para passar a maioria das mensagens para o procedimento de janela original, *lpfnEditWndProc*.</span><span class="sxs-lookup"><span data-stu-id="368c9-121">**SubClassProc** uses the [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) function to pass most messages to the original window procedure, *lpfnEditWndProc*.</span></span>


```C++
//  Get the edit window handle to each combo box. 
pt.x = 1; 
pt.y = 1; 
hwndEdit1 = ChildWindowFromPoint(hwndCombo1, pt); 
hwndEdit2 = ChildWindowFromPoint(hwndCombo2, pt); 
 
//  Change the window procedure for both edit windows 
//  to the subclass procedure. 
lpfnEditWndProc = (WNDPROC) SetWindowLongPtr(hwndEdit1, 
    GWLP_WNDPROC, (LONG_PTR) SubClassProc); 
 
SetWindowLongPtr(hwndEdit2, GWLP_WNDPROC, (LONG_PTR) SubClassProc); 
```



### <a name="process-the-wm_setfocus-message"></a><span data-ttu-id="368c9-122">Processar a mensagem do WM \_ SETFOCUS</span><span class="sxs-lookup"><span data-stu-id="368c9-122">Process the WM\_SETFOCUS Message</span></span>

<span data-ttu-id="368c9-123">Quando a janela da barra de ferramentas recebe o foco de entrada, ela imediatamente define o foco para a primeira caixa de combinação na barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="368c9-123">When the toolbar window receives the input focus, it immediately sets the focus to the first combo box in the toolbar.</span></span> <span data-ttu-id="368c9-124">Para fazer isso, o exemplo chama a função [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) em resposta à mensagem do [**WM \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus) .</span><span class="sxs-lookup"><span data-stu-id="368c9-124">To do this, the example calls the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function in response to the [**WM\_SETFOCUS**](/windows/desktop/inputdev/wm-setfocus) message.</span></span>


```C++
case WM_SETFOCUS: 
    SetFocus(hwndCombo1); 
    break; 
```



### <a name="process-application-defined-messages"></a><span data-ttu-id="368c9-125">Processar Application-Defined mensagens</span><span class="sxs-lookup"><span data-stu-id="368c9-125">Process Application-Defined Messages</span></span>

<span data-ttu-id="368c9-126">A função **SubClassProc** envia mensagens definidas pelo aplicativo para a janela da barra de ferramentas quando o usuário pressiona a tecla Tab, Enter ou ESC em uma caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="368c9-126">The **SubClassProc** function sends application-defined messages to the toolbar window when the user presses the TAB, ENTER, or ESC key in a combo box.</span></span> <span data-ttu-id="368c9-127">A mensagem da **\_ Guia do WM** é enviada para a tecla Tab, a mensagem do **WM \_ ESC** para a tecla ESC e o **WM \_ inserem** a mensagem para a tecla Enter.</span><span class="sxs-lookup"><span data-stu-id="368c9-127">The **WM\_TAB** message is sent for the TAB key, the **WM\_ESC** message for the ESC key, and the **WM\_ENTER** message for the ENTER key.</span></span>

<span data-ttu-id="368c9-128">O exemplo processa a mensagem da **\_ Guia do WM** definindo o foco para a próxima caixa de combinação na barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="368c9-128">The example processes the **WM\_TAB** message by setting the focus to the next combo box in the toolbar.</span></span> <span data-ttu-id="368c9-129">Ele processa a mensagem do **WM \_ ESC** definindo o foco para a janela principal do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="368c9-129">It processes the **WM\_ESC** message by setting the focus to the main application window.</span></span>


```C++
  case WM_TAB: 
      if (GetFocus() == hwndEdit1) 
          SetFocus(hwndCombo2); 
      else 
          SetFocus(hwndCombo1); 
      break; 
 
  case WM_ESC: 
       hwndCombo = GetFocus() == hwndEdit1 ? hwndCombo1 : hwndCombo2; 
 
       // Clear the current selection. 
       SendMessage(hwndCombo, CB_SETCURSEL, 
          (WPARAM) (-1), 0); 
 
      //  Set the focus to the main window. 
      SetFocus(hwndMain); 
      break;
```



<span data-ttu-id="368c9-130">Em resposta à mensagem **de \_ entrada do WM** , o exemplo garante que a seleção atual da caixa de combinação seja válida e, em seguida, defina o foco para a janela principal do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="368c9-130">In response to the **WM\_ENTER** message, the example ensures that the current selection for the combo box is valid and then sets the focus to the main application window.</span></span> <span data-ttu-id="368c9-131">Se a caixa de combinação não contiver nenhuma seleção atual, o exemplo usará a mensagem [**CB \_ FINDSTRINGEXACT**](cb-findstringexact.md) para procurar um item de lista que corresponda ao conteúdo do campo de seleção.</span><span class="sxs-lookup"><span data-stu-id="368c9-131">If the combo box contains no current selection, the example uses the [**CB\_FINDSTRINGEXACT**](cb-findstringexact.md) message to search for a list item that matches the contents of the selection field.</span></span> <span data-ttu-id="368c9-132">Se houver uma correspondência, o exemplo definirá a seleção atual; caso contrário, ele adicionará um novo item de lista.</span><span class="sxs-lookup"><span data-stu-id="368c9-132">If there is a match, the example sets the current selection; otherwise, it adds a new list item.</span></span>


```C++
case WM_ENTER: 
    hwndCombo = GetFocus() == hwndEdit1 ? hwndCombo1 : hwndCombo2; 
    SetFocus(hwndMain); 
 
    //  If there is no current selection, set one. 
    if (SendMessage(hwndCombo, CB_GETCURSEL, 0, 0) 
            == CB_ERR) 
    { 
        if (SendMessage(hwndCombo, WM_GETTEXT, 
                sizeof(achTemp), (LPARAM) achTemp) == 0) 
            break;      //  Empty selection field 
        dwIndex = SendMessage(hwndCombo, 
            CB_FINDSTRINGEXACT, (WPARAM) (-1), 
            (LPARAM) achTemp); 
 
        //  Add the string, if necessary, and select it. 
        if (dwIndex == CB_ERR) 
            dwIndex = SendMessage(hwndCombo, CB_ADDSTRING, 
                0, (LPARAM) achTemp); 
        if (dwIndex != CB_ERR) 
            SendMessage(hwndCombo, CB_SETCURSEL, 
                dwIndex, 0); 
    } 
    break; 
       
    // . 
    // .  Process additional messages. 
    // . 
 
default: 
    return DefWindowProc(hwnd, msg, wParam, lParam); 
```



## <a name="complete-example"></a><span data-ttu-id="368c9-133">Exemplo completo</span><span class="sxs-lookup"><span data-stu-id="368c9-133">Complete example</span></span>

<span data-ttu-id="368c9-134">A seguir, o procedimento de janela para a barra de ferramentas e o procedimento de subclasse para as duas caixas de combinação.</span><span class="sxs-lookup"><span data-stu-id="368c9-134">Following are the window procedure for the toolbar and the subclass procedure for the two combo boxes.</span></span>


```C++
#define WM_TAB (WM_USER) 
#define WM_ESC (WM_USER + 1) 
#define WM_ENTER (WM_USER + 2) 

//  Global variables
HWND    hwndMain; 
WNDPROC lpfnEditWndProc; //  Original wndproc for the combo box 

//  Prototypes
LRESULT CALLBACK SubClassProc( HWND, UINT, WPARAM, LPARAM );
 
/******************************************************** 
 
    FUNCTION:   ToolbarWindowProc 
 
    PURPOSE:    Window procedure for the toolbar window 
 
*********************************************************/ 
 
LRESULT CALLBACK ToolbarWindowProc(HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam) 
{ 
    static HWND   hwndEdit1; 
    static HWND   hwndEdit2; 
    static HWND   hwndCombo1; 
    static HWND   hwndCombo2; 
    POINT       pt; 
    DWORD       dwBaseUnits; 
    HWND        hwndCombo; 
    DWORD       dwIndex; 
    char achTemp[256];       //  Temporary buffer 
 
    switch (msg) 
    { 
        case WM_CREATE: 
            //  Create two combo box child windows. 
            dwBaseUnits = GetDialogBaseUnits(); 
 
            hwndCombo1 = CreateWindow(L"COMBOBOX", L"", 
                CBS_DROPDOWN | WS_CHILD | WS_VISIBLE, 
                (6 * LOWORD(dwBaseUnits)) / 4, 
                (2 * HIWORD(dwBaseUnits)) / 8, 
                (100 * LOWORD(dwBaseUnits)) / 4, 
                (50 * HIWORD(dwBaseUnits)) / 8, 
                hwnd, NULL, NULL, NULL);  
 
            hwndCombo2 = CreateWindow(L"COMBOBOX", L"", 
                CBS_DROPDOWN | WS_CHILD | WS_VISIBLE, 
                (112 * LOWORD(dwBaseUnits)) / 4, 
                (2 * HIWORD(dwBaseUnits)) / 8, 
                (100 * LOWORD(dwBaseUnits)) / 4, 
                (50 * HIWORD(dwBaseUnits)) / 8, 
                hwnd, NULL, hInst, NULL); 
            
            //  Get the edit window handle to each combo box. 
            pt.x = 1; 
            pt.y = 1; 
            hwndEdit1 = ChildWindowFromPoint(hwndCombo1, pt); 
            hwndEdit2 = ChildWindowFromPoint(hwndCombo2, pt); 
 
            //  Change the window procedure for both edit windows 
            //  to the subclass procedure. 
            lpfnEditWndProc = (WNDPROC) SetWindowLongPtr(hwndEdit1, 
                GWLP_WNDPROC, (LONG_PTR) SubClassProc); 
 
            SetWindowLongPtr(hwndEdit2, GWLP_WNDPROC, (LONG_PTR) SubClassProc); 

            break; 

        case WM_SETFOCUS: 
            SetFocus(hwndCombo1); 
            break; 

        case WM_TAB: 
            if (GetFocus() == hwndEdit1) 
                SetFocus(hwndCombo2); 
            else 
                SetFocus(hwndCombo1); 
            break; 
 
        case WM_ESC: 
             hwndCombo = GetFocus() == hwndEdit1 ? hwndCombo1 : hwndCombo2; 
 
             // Clear the current selection. 
             SendMessage(hwndCombo, CB_SETCURSEL, 
                (WPARAM) (-1), 0); 
 
            //  Set the focus to the main window. 
            SetFocus(hwndMain); 
            break;

        case WM_ENTER: 
            hwndCombo = GetFocus() == hwndEdit1 ? hwndCombo1 : hwndCombo2; 
            SetFocus(hwndMain); 
 
            //  If there is no current selection, set one. 
            if (SendMessage(hwndCombo, CB_GETCURSEL, 0, 0) 
                    == CB_ERR) 
            { 
                if (SendMessage(hwndCombo, WM_GETTEXT, 
                        sizeof(achTemp), (LPARAM) achTemp) == 0) 
                    break;      //  Empty selection field 
                dwIndex = SendMessage(hwndCombo, 
                    CB_FINDSTRINGEXACT, (WPARAM) (-1), 
                    (LPARAM) achTemp); 
 
                //  Add the string, if necessary, and select it. 
                if (dwIndex == CB_ERR) 
                    dwIndex = SendMessage(hwndCombo, CB_ADDSTRING, 
                        0, (LPARAM) achTemp); 
                if (dwIndex != CB_ERR) 
                    SendMessage(hwndCombo, CB_SETCURSEL, 
                        dwIndex, 0); 
            } 
            break; 
       
            // . 
            // .  Process additional messages. 
            // . 
 
        default: 
            return DefWindowProc(hwnd, msg, wParam, lParam); 
    } 
    return 0; 
} 
 
 
/******************************************************** 
 
    FUNCTION:   SubClassProc 
 
    PURPOSE:    Process TAB and ESCAPE keys, and pass all 
                other messages to the class window 
                procedure. 
 
*********************************************************/ 
LRESULT CALLBACK SubClassProc(HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam) 
{ 
    switch (msg) 
    { 
        case WM_KEYDOWN: 
            switch (wParam) 
            { 
                case VK_TAB: 
                    SendMessage(hwndMain, WM_TAB, 0, 0); 
                    return 0; 
                case VK_ESCAPE: 
                    SendMessage(hwndMain, WM_ESC, 0, 0); 
                    return 0; 
                case VK_RETURN: 
                    SendMessage(hwndMain, WM_ENTER, 0, 0); 
                    return 0; 
            } 
            break; 
 
        case WM_KEYUP: 
        case WM_CHAR: 
            switch (wParam) 
            { 
                case VK_TAB: 
                case VK_ESCAPE: 
                case VK_RETURN: 
                    return 0; 
            } 
    } 
 
    //  Call the original window procedure for default processing. 
     return CallWindowProc(lpfnEditWndProc, hwnd, msg, wParam, lParam); 
} 
```



## <a name="related-topics"></a><span data-ttu-id="368c9-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="368c9-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="368c9-136">Sobre caixas de combinação</span><span class="sxs-lookup"><span data-stu-id="368c9-136">About Combo Boxes</span></span>](about-combo-boxes.md)
</dt> <dt>

[<span data-ttu-id="368c9-137">Referência de controle ComboBox</span><span class="sxs-lookup"><span data-stu-id="368c9-137">ComboBox Control Reference</span></span>](bumper-combobox-combobox-control-reference.md)
</dt> <dt>

[<span data-ttu-id="368c9-138">Usando caixas de combinação</span><span class="sxs-lookup"><span data-stu-id="368c9-138">Using Combo Boxes</span></span>](using-combo-boxes.md)
</dt> <dt>

[<span data-ttu-id="368c9-139">ComboBox</span><span class="sxs-lookup"><span data-stu-id="368c9-139">ComboBox</span></span>](combo-boxes.md)
</dt> </dl>

 

 