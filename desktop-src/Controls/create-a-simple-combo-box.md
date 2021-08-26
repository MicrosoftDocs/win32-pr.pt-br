---
title: Como criar uma caixa de combinação simples
description: Este tópico descreve como criar, adicionar itens e recuperar itens de uma caixa de combinação simples.
ms.assetid: E432AEC0-6C06-40C7-BBFE-B66C21DB8ACA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb1ab672e0beea90d07eadf05f14ffdc4a8181a4da7bf7940af50b00ddc69cde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920806"
---
# <a name="how-to-create-a-simple-combo-box"></a>Como criar uma caixa de combinação simples

Este tópico descreve como criar, adicionar itens e recuperar itens de uma caixa de combinação simples. Especificamente, os exemplos de código que o acompanham demonstram como executar as seguintes funções:

-   Crie dinamicamente uma caixa de combinação simples em uma janela pai.
-   Adicione uma lista de itens à caixa de combinação e exiba um item inicial no campo seleção da caixa de combinação.
-   Detectar quando o usuário selecionou um item da caixa de combinação.
-   Recupere o item selecionado da caixa de combinação.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Programação de interface do usuário

## <a name="instructions"></a>Instruções

### <a name="step-1-create-an-instance-of-the-combo-box"></a>Etapa 1: criar uma instância da caixa de combinação.

O aplicativo de exemplo chama a função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) para criar uma janela filho da janela do aplicativo. O estilo da janela [**\_ ComboBox WC**](common-control-window-classes.md) especifica que é uma caixa de combinação.


```C++
// Create the Combobox
//
// Uses the CreateWindow function to create a child window of 
// the application window. The WC_COMBOBOX window style specifies  
// that it is a combobox.

 int xpos = 100;            // Horizontal position of the window.
 int ypos = 100;            // Vertical position of the window.
 int nwidth = 200;          // Width of the window
 int nheight = 200;         // Height of the window
 HWND hwndParent =  m_hwnd; // Handle to the parent window

 HWND hWndComboBox = CreateWindow(WC_COMBOBOX, TEXT(""), 
     CBS_DROPDOWN | CBS_HASSTRINGS | WS_CHILD | WS_OVERLAPPED | WS_VISIBLE,
     xpos, ypos, nwidth, nheight, hwndParent, NULL, HINST_THISCOMPONENT,
     NULL);

```



### <a name="step-2-load-the-combo-box-with-the-item-list"></a>Etapa 2: carregar a caixa de combinação com a lista de itens.

O aplicativo envia uma mensagem de [**\_ AddString CB**](cb-addstring.md) para cada item na lista. Depois que a lista é carregada, o aplicativo envia a mensagem do [**CB \_ setcurse**](cb-setcursel.md) para exibir um item inicial no campo de seleção da caixa de combinação.


```C++
// load the combobox with item list.  
// Send a CB_ADDSTRING message to load each item

TCHAR Planets[9][10] =  
{
    TEXT("Mercury"), TEXT("Venus"), TEXT("Terra"), TEXT("Mars"), 
    TEXT("Jupiter"), TEXT("Saturn"), TEXT("Uranus"), TEXT("Neptune"), 
    TEXT("Pluto??") 
};
       
TCHAR A[16]; 
int  k = 0; 

memset(&A,0,sizeof(A));       
for (k = 0; k <= 8; k += 1)
{
    wcscpy_s(A, sizeof(A)/sizeof(TCHAR),  (TCHAR*)Planets[k]);

    // Add string to combobox.
    SendMessage(hWndComboBox,(UINT) CB_ADDSTRING,(WPARAM) 0,(LPARAM) A); 
}
  
// Send the CB_SETCURSEL message to display an initial item 
//  in the selection field  
SendMessage(hWndComboBox, CB_SETCURSEL, (WPARAM)2, (LPARAM)0);
```



### <a name="step-3-detect-when-the-user-selects-an-item-and-retrieve-it-from-the-combo-box"></a>Etapa 3: detectar quando o usuário seleciona um item e o recupera da caixa de combinação.

Quando o usuário faz uma seleção na lista, a caixa de combinação envia uma notificação [CBN \_ SELCHANGE](cbn-selchange.md) para a janela pai por meio de uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) . O aplicativo recupera o identificador para a caixa de combinação do campo *lParam* da mensagem de notificação e envia uma mensagem de [**\_ iscurseaction CB**](cb-getcursel.md) para a caixa de combinação para recuperar o índice do item de lista selecionado. Depois de obter o índice de item, o aplicativo envia uma mensagem de [**\_ GETLBTEXT CB**](cb-getlbtext.md) para obter o item. Em seguida, ele exibe o item em uma caixa de mensagem.

> [!Note]  
> A notificação [CBN \_ SELCHANGE](cbn-selchange.md) é enviada e processada antes que o item seja colocado no campo de seleção da caixa de combinação. Como resultado, neste exemplo, o item selecionado não aparecerá no campo de seleção até que a caixa de mensagem seja fechada.

 


```C++
switch (message)
{   
    case WM_COMMAND:

        if(HIWORD(wParam) == CBN_SELCHANGE)
        // If the user makes a selection from the list:
        //   Send CB_GETCURSEL message to get the index of the selected list item.
        //   Send CB_GETLBTEXT message to get the item.
        //   Display the item in a messagebox.
        { 
            int ItemIndex = SendMessage((HWND) lParam, (UINT) CB_GETCURSEL, 
                (WPARAM) 0, (LPARAM) 0);
                TCHAR  ListItem[256];
                (TCHAR) SendMessage((HWND) lParam, (UINT) CB_GETLBTEXT, 
                (WPARAM) ItemIndex, (LPARAM) ListItem);
            MessageBox(hwnd, (LPCWSTR) ListItem, TEXT("Item Selected"), MB_OK);                        
        }
        
        wasHandled = true;
    result = 0;
    break;
```



## <a name="complete-example"></a>Exemplo completo


```C++
// Windows Header Files:
#include <windows.h>
#include <CommCtrl.h>

// C RunTime Header Files
#include <math.h>

#include <objbase.h>

/******************************************************************
*                                                                 *
*  Macros                                                         *
*                                                                 *
******************************************************************/
template<class Interface>
inline void
SafeRelease(
    Interface **ppInterfaceToRelease
    )
{
    if (*ppInterfaceToRelease != NULL)
    {
        (*ppInterfaceToRelease)->Release();

        (*ppInterfaceToRelease) = NULL;
    }
}

#ifndef Assert
#if defined( DEBUG ) || defined( _DEBUG )
#define Assert(b) if (!(b)) {OutputDebugStringA("Assert: " #b "\n");}
#else
#define Assert(b)
#endif //DEBUG || _DEBUG
#endif


#ifndef HINST_THISCOMPONENT
EXTERN_C IMAGE_DOS_HEADER __ImageBase;
#define HINST_THISCOMPONENT ((HINSTANCE)&__ImageBase)
#endif

/******************************************************************
*                                                                 *
*  DemoApp                                                        *
*                                                                 *
******************************************************************/

class DemoApp
{
public:
    DemoApp();
    ~DemoApp();

    HRESULT Initialize();

    void RunMessageLoop();

private:
    HRESULT CreateResources();
    void DiscardResources();

    static LRESULT CALLBACK WndProc(
        HWND hWnd,
        UINT message,
        WPARAM wParam,
        LPARAM lParam
        );

 private:
    HWND m_hwnd;

 };
```


```C++
#include "SimpleComboBox.h"

/******************************************************************
*                                                                 *
*  The application entry point.                                   *
*                                                                 *
******************************************************************/

int WINAPI WinMain(
    HINSTANCE     /* hInstance */,
    HINSTANCE     /* hPrevInstance */,
    LPSTR     /* lpCmdLine */,
    int     /* nCmdShow */
    )
{
    // Ignore the return value because we want to run the program even in the
    // unlikely event that HeapSetInformation fails.
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);
    if (SUCCEEDED(CoInitialize(NULL)))
    {
        {
            DemoApp app;

            if (SUCCEEDED(app.Initialize()))
            {
                app.RunMessageLoop();
            }
        }
        CoUninitialize();
    }

    return 0;
}

/******************************************************************
*                                                                 *
*  DemoApp::DemoApp constructor                                   *
*                                                                 *
*  Initialize member data.                                        *
*                                                                 *
******************************************************************/

DemoApp::DemoApp() :
    m_hwnd(NULL)
{
}

/******************************************************************
*                                                                 *
*  Release resources.                                             *
*                                                                 *
******************************************************************/

DemoApp::~DemoApp()        
{
    // TODO: Release app resource here.
}

/*******************************************************************
*                                                                  *
*  Create the application window and the combobox.                 *
*                                                                  *
*******************************************************************/

HRESULT DemoApp::Initialize()
{
    HRESULT hr;

    // Register the window class.
    WNDCLASSEX wcex = { sizeof(WNDCLASSEX) };
    wcex.style         = CS_HREDRAW | CS_VREDRAW;
    wcex.lpfnWndProc   = DemoApp::WndProc;
    wcex.cbClsExtra    = 0;
    wcex.cbWndExtra    = sizeof(LONG_PTR);
    wcex.hInstance     = HINST_THISCOMPONENT;
    wcex.hbrBackground = (HBRUSH)(COLOR_WINDOW+1);;
    wcex.lpszMenuName  = NULL;
    wcex.hCursor       = LoadCursor(NULL, IDC_ARROW);
    wcex.lpszClassName = TEXT("DemoApp");

    RegisterClassEx(&wcex);

    // Create the application window.
    //
    // Because the CreateWindow function takes its size in pixels, we
    // obtain the system DPI and use it to scale the window size.
    int dpiX = 0;
    int dpiY = 0;
    HDC hdc = GetDC(NULL);
    if (hdc)
    {
        dpiX = GetDeviceCaps(hdc, LOGPIXELSX);
        dpiY = GetDeviceCaps(hdc, LOGPIXELSY);
        ReleaseDC(NULL, hdc);
    }

    m_hwnd = CreateWindow(
        TEXT("DemoApp"),
        TEXT("Simple Combo Box Example"),
        WS_OVERLAPPEDWINDOW,
        CW_USEDEFAULT,
        CW_USEDEFAULT,
        static_cast<UINT>(ceil(640.f * dpiX / 96.f)),
        static_cast<UINT>(ceil(480.f * dpiY / 96.f)),
        NULL,
        NULL,
        HINST_THISCOMPONENT,
        this
        );

    hr = m_hwnd ? S_OK : E_FAIL;
    if (SUCCEEDED(hr))
    {
        ShowWindow(m_hwnd, SW_SHOWNORMAL);
        UpdateWindow(m_hwnd);
    }


    // Create the Combobox
    //
    // Uses the CreateWindow function to create a child window of 
    // the application window. The WC_COMBOBOX window style specifies  
    // that it is a combobox.

     int xpos = 100;            // Horizontal position of the window.
     int ypos = 100;            // Vertical position of the window.
     int nwidth = 200;          // Width of the window
     int nheight = 200;         // Height of the window
     HWND hwndParent =  m_hwnd; // Handle to the parent window

     HWND hWndComboBox = CreateWindow(WC_COMBOBOX, TEXT(""), 
         CBS_DROPDOWN | CBS_HASSTRINGS | WS_CHILD | WS_OVERLAPPED | WS_VISIBLE,
         xpos, ypos, nwidth, nheight, hwndParent, NULL, HINST_THISCOMPONENT,
         NULL);


    
    // load the combobox with item list.  
    // Send a CB_ADDSTRING message to load each item

    TCHAR Planets[9][10] =  
    {
        TEXT("Mercury"), TEXT("Venus"), TEXT("Terra"), TEXT("Mars"), 
        TEXT("Jupiter"), TEXT("Saturn"), TEXT("Uranus"), TEXT("Neptune"), 
        TEXT("Pluto??") 
    };
           
    TCHAR A[16]; 
    int  k = 0; 

    memset(&A,0,sizeof(A));       
    for (k = 0; k <= 8; k += 1)
    {
        wcscpy_s(A, sizeof(A)/sizeof(TCHAR),  (TCHAR*)Planets[k]);

        // Add string to combobox.
        SendMessage(hWndComboBox,(UINT) CB_ADDSTRING,(WPARAM) 0,(LPARAM) A); 
    }
      
    // Send the CB_SETCURSEL message to display an initial item 
    //  in the selection field  
    SendMessage(hWndComboBox, CB_SETCURSEL, (WPARAM)2, (LPARAM)0);

    return hr;
}


/******************************************************************
*                                                                 *
*  The main window's message loop.                                *
*                                                                 *
******************************************************************/

void DemoApp::RunMessageLoop()
{
    MSG msg;

    while (GetMessage(&msg, NULL, 0, 0))
    {
        TranslateMessage(&msg);
        DispatchMessage(&msg);
    }
}


/******************************************************************
*                                                                 *
*  The window's message handler.                                  *
*                                                                 *
******************************************************************/

LRESULT CALLBACK DemoApp::WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    LRESULT result = 0;

    if (message == WM_CREATE)
    {
        LPCREATESTRUCT pcs = (LPCREATESTRUCT)lParam;
        DemoApp *pDemoApp = (DemoApp *)pcs->lpCreateParams;

        ::SetWindowLongPtrW(
            hwnd,
            GWLP_USERDATA,
            PtrToUlong(pDemoApp)
            );

        result = 1;
    }
    else
    {
        DemoApp *pDemoApp = reinterpret_cast<DemoApp *>(static_cast<LONG_PTR>(
            ::GetWindowLongPtrW(
                hwnd,
                GWLP_USERDATA
                )));

        bool wasHandled = false;

        if (pDemoApp)
        {
            switch (message)
            {   
                case WM_COMMAND:

                    if(HIWORD(wParam) == CBN_SELCHANGE)
                    // If the user makes a selection from the list:
                    //   Send CB_GETCURSEL message to get the index of the selected list item.
                    //   Send CB_GETLBTEXT message to get the item.
                    //   Display the item in a messagebox.
                    { 
                        int ItemIndex = SendMessage((HWND) lParam, (UINT) CB_GETCURSEL, 
                            (WPARAM) 0, (LPARAM) 0);
                            TCHAR  ListItem[256];
                            (TCHAR) SendMessage((HWND) lParam, (UINT) CB_GETLBTEXT, 
                            (WPARAM) ItemIndex, (LPARAM) ListItem);
                        MessageBox(hwnd, (LPCWSTR) ListItem, TEXT("Item Selected"), MB_OK);                        
                    }
                    
                    wasHandled = true;
                result = 0;
                break;

            case WM_DISPLAYCHANGE:
                {
                    InvalidateRect(hwnd, NULL, FALSE);
                }
                wasHandled = true;
                result = 0;
                break;

            case WM_DESTROY:
                {
                    PostQuitMessage(0);
                }
                wasHandled = true;
                result = 1;
                break;
            }
        }

        if (!wasHandled)
        {
            result = DefWindowProc(hwnd, message, wParam, lParam);
        }
    }

    return result;
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

 

 