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
# <a name="how-to-subclass-a-combo-box"></a>Como subclasse de uma caixa de combinação

Este tópico demonstra como caixas de combinação de subclasses. O aplicativo de exemplo C++ cria uma janela de barra de ferramentas que contém duas caixas de combinação. Por meio da subclasse dos controles de edição dentro das caixas de combinação, a janela da barra de ferramentas intercepta as teclas TAB, ENTER e ESC que, de outra forma, seriam ignoradas.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Controles do Windows](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Programação da interface do usuário do Windows

## <a name="instructions"></a>Instruções

### <a name="process-the-wm_create-message"></a>Processar a mensagem de criação do WM \_

O aplicativo processa a mensagem de [**\_ criação do WM**](/windows/desktop/winmsg/wm-create) para criar dois controles de caixa de combinação como janelas filhas.


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



O aplicativo, em seguida, subclasseia os controles de edição (campos de seleção) em cada caixa de combinação, porque eles recebem a entrada de caracteres para a caixa de combinação simples e suspensa. Por fim, ele chama a função [**ChildWindowFromPoint**](/windows/desktop/api/winuser/nf-winuser-childwindowfrompoint) para recuperar o identificador para cada controle de edição.

Para subclasses dos controles de edição, o aplicativo chama a função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) , substituindo o ponteiro pelo procedimento da janela de classe por um ponteiro para a função **SubClassProc** definida pelo aplicativo. O ponteiro para o procedimento de janela original é salvo na variável global *lpfnEditWndProc*.

**SubClassProc** INTERCEPTA a guia, Enter e teclas ESC e notifica a janela da barra de ferramentas enviando mensagens definidas pelo aplicativo ( \_ guia WM, o WM \_ ESC e o WM \_ entram). **SubClassProc** usa a função [**CallWindowProc**](/windows/desktop/api/winuser/nf-winuser-callwindowproca) para passar a maioria das mensagens para o procedimento de janela original, *lpfnEditWndProc*.


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



### <a name="process-the-wm_setfocus-message"></a>Processar a mensagem do WM \_ SETFOCUS

Quando a janela da barra de ferramentas recebe o foco de entrada, ela imediatamente define o foco para a primeira caixa de combinação na barra de ferramentas. Para fazer isso, o exemplo chama a função [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) em resposta à mensagem do [**WM \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus) .


```C++
case WM_SETFOCUS: 
    SetFocus(hwndCombo1); 
    break; 
```



### <a name="process-application-defined-messages"></a>Processar Application-Defined mensagens

A função **SubClassProc** envia mensagens definidas pelo aplicativo para a janela da barra de ferramentas quando o usuário pressiona a tecla Tab, Enter ou ESC em uma caixa de combinação. A mensagem da **\_ Guia do WM** é enviada para a tecla Tab, a mensagem do **WM \_ ESC** para a tecla ESC e o **WM \_ inserem** a mensagem para a tecla Enter.

O exemplo processa a mensagem da **\_ Guia do WM** definindo o foco para a próxima caixa de combinação na barra de ferramentas. Ele processa a mensagem do **WM \_ ESC** definindo o foco para a janela principal do aplicativo.


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



Em resposta à mensagem **de \_ entrada do WM** , o exemplo garante que a seleção atual da caixa de combinação seja válida e, em seguida, defina o foco para a janela principal do aplicativo. Se a caixa de combinação não contiver nenhuma seleção atual, o exemplo usará a mensagem [**CB \_ FINDSTRINGEXACT**](cb-findstringexact.md) para procurar um item de lista que corresponda ao conteúdo do campo de seleção. Se houver uma correspondência, o exemplo definirá a seleção atual; caso contrário, ele adicionará um novo item de lista.


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



## <a name="complete-example"></a>Exemplo completo

A seguir, o procedimento de janela para a barra de ferramentas e o procedimento de subclasse para as duas caixas de combinação.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre caixas de combinação](about-combo-boxes.md)
</dt> <dt>

[Referência de controle ComboBox](bumper-combobox-combobox-control-reference.md)
</dt> <dt>

[Usando caixas de combinação](using-combo-boxes.md)
</dt> <dt>

[ComboBox](combo-boxes.md)
</dt> </dl>

 

 