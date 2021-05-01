---
title: Usando cursores
description: Esta seção fornece exemplos de código que mostram como executar tarefas relacionadas a cursores.
ms.assetid: eab7b781-783e-4fc5-868d-6ff773c40a21
keywords:
- recursos, cursores
- cursores, personalizado
- cursores personalizados
- cursor de ampulheta
- cursores, criando
- cursores, ampulheta
- Criando cursores
- destruindo cursores
- exibindo cursores
- confinando cursores
- cursores, destruindo
- cursores, exibindo
- cursores, confinados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6cf681fd17f3e79e4559e9936be232ae09f8453
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327121"
---
# <a name="using-cursors"></a>Usando cursores

Esta seção aborda os tópicos a seguir.

-   [Criando um cursor](#creating-a-cursor)
-   [Exibindo um cursor](#displaying-a-cursor)
-   [Confinando um cursor](#confining-a-cursor)
-   [Usando funções de cursor para criar um ratoeira](#using-cursor-functions-to-create-a-mousetrap)
-   [Usando o teclado para mover o cursor](#using-the-keyboard-to-move-the-cursor)

## <a name="creating-a-cursor"></a>Criando um cursor

O exemplo a seguir cria duas alças de cursor: uma para o cursor de ampulheta padrão e outra para um cursor personalizado incluído como um recurso no arquivo de definição de recurso do aplicativo.


```
HINSTANCE hinst;            // handle to current instance 
HCURSOR hCurs1, hCurs2;     // cursor handles 
 
// Create a standard hourglass cursor. 
 
hCurs1 = LoadCursor(NULL, IDC_WAIT); 
 
// Create a custom cursor based on a resource. 
 
hCurs2 = LoadCursor(hinst, MAKEINTRESOURCE(240)); 
```



Você deve implementar cursores personalizados como recursos. Em vez de criar os cursores em tempo de execução, use a função [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora), [**LoadCursorFromFile**](/windows/desktop/api/Winuser/nf-winuser-loadcursorfromfilea)ou [**LoadImage**](/windows/desktop/api/Winuser/nf-winuser-loadimagea) para evitar a dependência do dispositivo, para simplificar a localização e para permitir que os aplicativos compartilhem designs de cursores.

O exemplo a seguir usa a função [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor) para criar um cursor personalizado em tempo de execução. O exemplo é incluído aqui para ilustrar como o sistema interpreta máscaras de cursor.


```
HINSTANCE hinst;            // handle to current instance  
HCURSOR hCurs1, hCurs2;     // cursor handles 
 
HCURSOR hCurs3;             // cursor handle 
 
// Yin-shaped cursor AND mask 
 
BYTE ANDmaskCursor[] = 
{ 
    0xFF, 0xFC, 0x3F, 0xFF,   // line 1 
    0xFF, 0xC0, 0x1F, 0xFF,   // line 2 
    0xFF, 0x00, 0x3F, 0xFF,   // line 3 
    0xFE, 0x00, 0xFF, 0xFF,   // line 4 
 
    0xF7, 0x01, 0xFF, 0xFF,   // line 5 
    0xF0, 0x03, 0xFF, 0xFF,   // line 6 
    0xF0, 0x03, 0xFF, 0xFF,   // line 7 
    0xE0, 0x07, 0xFF, 0xFF,   // line 8 
 
    0xC0, 0x07, 0xFF, 0xFF,   // line 9 
    0xC0, 0x0F, 0xFF, 0xFF,   // line 10 
    0x80, 0x0F, 0xFF, 0xFF,   // line 11 
    0x80, 0x0F, 0xFF, 0xFF,   // line 12 
 
    0x80, 0x07, 0xFF, 0xFF,   // line 13 
    0x00, 0x07, 0xFF, 0xFF,   // line 14 
    0x00, 0x03, 0xFF, 0xFF,   // line 15 
    0x00, 0x00, 0xFF, 0xFF,   // line 16 
 
    0x00, 0x00, 0x7F, 0xFF,   // line 17 
    0x00, 0x00, 0x1F, 0xFF,   // line 18 
    0x00, 0x00, 0x0F, 0xFF,   // line 19 
    0x80, 0x00, 0x0F, 0xFF,   // line 20 
 
    0x80, 0x00, 0x07, 0xFF,   // line 21 
    0x80, 0x00, 0x07, 0xFF,   // line 22 
    0xC0, 0x00, 0x07, 0xFF,   // line 23 
    0xC0, 0x00, 0x0F, 0xFF,   // line 24 
 
    0xE0, 0x00, 0x0F, 0xFF,   // line 25 
    0xF0, 0x00, 0x1F, 0xFF,   // line 26 
    0xF0, 0x00, 0x1F, 0xFF,   // line 27 
    0xF8, 0x00, 0x3F, 0xFF,   // line 28 
 
    0xFE, 0x00, 0x7F, 0xFF,   // line 29 
    0xFF, 0x00, 0xFF, 0xFF,   // line 30 
    0xFF, 0xC3, 0xFF, 0xFF,   // line 31 
    0xFF, 0xFF, 0xFF, 0xFF    // line 32 
};
 
// Yin-shaped cursor XOR mask 
 
BYTE XORmaskCursor[] = 
{ 
    0x00, 0x00, 0x00, 0x00,   // line 1 
    0x00, 0x03, 0xC0, 0x00,   // line 2 
    0x00, 0x3F, 0x00, 0x00,   // line 3 
    0x00, 0xFE, 0x00, 0x00,   // line 4 
 
    0x0E, 0xFC, 0x00, 0x00,   // line 5 
    0x07, 0xF8, 0x00, 0x00,   // line 6 
    0x07, 0xF8, 0x00, 0x00,   // line 7 
    0x0F, 0xF0, 0x00, 0x00,   // line 8 
 
    0x1F, 0xF0, 0x00, 0x00,   // line 9 
    0x1F, 0xE0, 0x00, 0x00,   // line 10 
    0x3F, 0xE0, 0x00, 0x00,   // line 11 
    0x3F, 0xE0, 0x00, 0x00,   // line 12 
 
    0x3F, 0xF0, 0x00, 0x00,   // line 13 
    0x7F, 0xF0, 0x00, 0x00,   // line 14 
    0x7F, 0xF8, 0x00, 0x00,   // line 15 
    0x7F, 0xFC, 0x00, 0x00,   // line 16 
 
    0x7F, 0xFF, 0x00, 0x00,   // line 17 
    0x7F, 0xFF, 0x80, 0x00,   // line 18 
    0x7F, 0xFF, 0xE0, 0x00,   // line 19 
    0x3F, 0xFF, 0xE0, 0x00,   // line 20 
 
    0x3F, 0xC7, 0xF0, 0x00,   // line 21 
    0x3F, 0x83, 0xF0, 0x00,   // line 22 
    0x1F, 0x83, 0xF0, 0x00,   // line 23 
    0x1F, 0x83, 0xE0, 0x00,   // line 24 
 
    0x0F, 0xC7, 0xE0, 0x00,   // line 25 
    0x07, 0xFF, 0xC0, 0x00,   // line 26 
    0x07, 0xFF, 0xC0, 0x00,   // line 27 
    0x01, 0xFF, 0x80, 0x00,   // line 28 
 
    0x00, 0xFF, 0x00, 0x00,   // line 29 
    0x00, 0x3C, 0x00, 0x00,   // line 30 
    0x00, 0x00, 0x00, 0x00,   // line 31 
    0x00, 0x00, 0x00, 0x00    // line 32 
};
 
// Create a custom cursor at run time. 
 
hCurs3 = CreateCursor( hinst,   // app. instance 
             19,                // horizontal position of hot spot 
             2,                 // vertical position of hot spot 
             32,                // cursor width 
             32,                // cursor height 
             ANDmaskCursor,     // AND mask 
             XORmaskCursor );   // XOR mask 
```



Para criar o cursor, [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor) aplica a seguinte tabela da verdade às máscaras **e** e **XOR** .



| E máscara | Máscara XOR | Monitor        |
|----------|----------|----------------|
| 0        | 0        | Preto          |
| 0        | 1        | Branca          |
| 1        | 0        | Tela         |
| 1        | 1        | Tela reversa |



 

Para obter mais informações, consulte [bitmaps](/windows/desktop/gdi/bitmaps).

Antes de fechar, você deve usar a função [**DestroyCursor**](/windows/desktop/api/Winuser/nf-winuser-destroycursor) para destruir os cursores criados com [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor). Não é necessário destruir cursores criados por outras funções.

## <a name="displaying-a-cursor"></a>Exibindo um cursor

O sistema exibe automaticamente o cursor de classe (o cursor associado à janela à qual o cursor está apontando). Você pode atribuir um cursor de classe ao registrar uma classe de janela. O exemplo a seguir ilustra isso atribuindo um identificador de cursor ao membro **hCursor** da estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) identificada pelo parâmetro *WC* .


```
WNDCLASS  wc; 
 
// Fill the window class structure with parameters that 
// describe the main window. 
 
wc.style = NULL;                        // class style(s) 
wc.lpfnWndProc = (WNDPROC) MainWndProc; // window procedure 
wc.cbClsExtra = 0;           // no per-class extra data 
wc.cbWndExtra = 0;           // no per-window extra data 
wc.hInstance = hinst;        // application that owns the class 
wc.hIcon = LoadIcon(NULL, IDI_APPLICATION);     // class icon 
wc.hCursor = LoadCursor(hinst, MAKEINTRESOURCE(230)); // class cursor 
wc.hbrBackground = GetStockObject(WHITE_BRUSH); // class background 
wc.lpszMenuName =  "GenericMenu";               // class menu 
wc.lpszClassName = "GenericWClass"              // class name 
 
// Register the window class. 
 
return RegisterClass(&wc); 
```



Quando a classe Window é registrada, o cursor identificado por 230 no arquivo de definição de recurso do aplicativo é o cursor padrão para todas as janelas baseadas na classe.

Seu aplicativo pode alterar o design do cursor usando a função [**SetCursor**](/windows/desktop/api/Winuser/nf-winuser-setcursor) e especificando um identificador de cursor diferente. No entanto, quando o cursor se move, o sistema redesenha o cursor de classe no novo local. Para impedir que o cursor de classe seja redesenhado, você deve processar a mensagem [**\_ SetCursor do WM**](wm-setcursor.md) . Cada vez que o cursor se move e a entrada do mouse não é capturada, o sistema envia essa mensagem para a janela na qual o cursor está se movendo.

Você pode especificar cursores diferentes para diferentes condições ao processar o [**WM \_ SetCursor**](wm-setcursor.md). Por exemplo, o exemplo a seguir mostra como exibir o cursor sempre que o cursor se move sobre o ícone de um aplicativo minimizado.


```
case WM_SETCURSOR: 
 
    // If the window is minimized, draw the hCurs3 cursor. 
    // If the window is not minimized, draw the default 
    // cursor (class cursor). 
 
    if (IsIconic(hwnd)) 
    { 
        SetCursor(hCurs3); 
        break; 
    } 
```



Quando a janela não é minimizada, o sistema exibe o cursor de classe.

Você pode substituir um cursor de classe usando a função [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) . Essa função altera as configurações de janela padrão para todas as janelas de uma classe especificada. O exemplo a seguir substitui o cursor de classe existente pelo `hCurs2` cursor.


```
// Change the cursor for window class represented by hwnd. 
 
SetClassLongPtr(hwnd,    // window handle 
    GCLP_HCURSOR,        // change cursor 
    (LONG_PTR) hCurs2);  // new cursor 
```



Para obter mais informações, consulte [classes de janela](/windows/desktop/winmsg/window-classes) e [entrada do mouse](/windows/desktop/inputdev/mouse-input).

## <a name="confining-a-cursor"></a>Confinando um cursor

O exemplo a seguir ajusta o cursor para a janela do aplicativo e restaura o cursor para sua janela anterior. O exemplo usa a função [**GetClipCursor**](/windows/desktop/api/Winuser/nf-winuser-getclipcursor) para registrar a área na qual o cursor pode se mover e a função [**ClipCursor**](/windows/desktop/api/Winuser/nf-winuser-clipcursor) para confinar e restaurar o cursor.


```
RECT rcClip;           // new area for ClipCursor
RECT rcOldClip;        // previous area for ClipCursor
 
// Record the area in which the cursor can move. 
 
GetClipCursor(&rcOldClip); 
 
// Get the dimensions of the application's window. 
 
GetWindowRect(hwnd, &rcClip); 
 
// Confine the cursor to the application's window. 
 
ClipCursor(&rcClip); 
 
   // 
   // Process input from the confined cursor. 
   // 
 
// Restore the cursor to its previous area. 
 
ClipCursor(&rcOldClip); 
```



Como há apenas um cursor de cada vez disponível no sistema, um aplicativo que confina o cursor deve restaurar o cursor antes de ceder o controle a outra janela.

## <a name="using-cursor-functions-to-create-a-mousetrap"></a>Usando funções de cursor para criar um ratoeira

O exemplo a seguir usa as funções [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos), [**GetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos), [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor) [**, LoadCursor e**](/windows/desktop/api/Winuser/nf-winuser-loadcursora) [**SetCursor**](/windows/desktop/api/Winuser/nf-winuser-setcursor) para criar um ratoeira simples. Ele também usa as funções cursor e timer para monitorar a posição do cursor a cada 10 segundos. Se a posição do cursor não tiver sido alterada nos últimos 10 segundos e a janela principal do aplicativo for minimizada, o aplicativo alterará o cursor e o moverá para o ícone de ratoeira.

Um exemplo de um ratoeira semelhante é incluído em [ícones](icons.md). Ele usa as funções [**LoadCursor**](/windows/desktop/api/Winuser/nf-winuser-loadcursora) e [**LoadIcon**](/windows/desktop/api/Winuser/nf-winuser-loadicona) em vez das funções [**CreateCursor**](/windows/desktop/api/Winuser/nf-winuser-createcursor) e [**CreateIcon**](/windows/desktop/api/Winuser/nf-winuser-createicon) dependentes de dispositivos.


```
HICON hIcon1;               // icon handles 
POINT ptOld;                // previous cursor location 
HCURSOR hCurs1;             // cursor handle 
 
 
// The following cursor masks are defined in a code 
// example that appears earlier in this section. 
 
// Yin-shaped cursor AND and XOR masks 
 
BYTE ANDmaskCursor[] = ... 
BYTE XORmaskCursor[] = ... 
 
// Yang-shaped icon AND mask 
 
BYTE ANDmaskIcon[] = {0xFF, 0xFF, 0xFF, 0xFF,  // line 1 
                      0xFF, 0xFF, 0xC3, 0xFF,  // line 2 
                      0xFF, 0xFF, 0x00, 0xFF,  // line 3 
                      0xFF, 0xFE, 0x00, 0x7F,  // line 4 
 
                      0xFF, 0xFC, 0x00, 0x1F,  // line 5 
                      0xFF, 0xF8, 0x00, 0x0F,  // line 6 
                      0xFF, 0xF8, 0x00, 0x0F,  // line 7 
                      0xFF, 0xF0, 0x00, 0x07,  // line 8 
 
                      0xFF, 0xF0, 0x00, 0x03,  // line 9 
                      0xFF, 0xE0, 0x00, 0x03,  // line 10 
                      0xFF, 0xE0, 0x00, 0x01,  // line 11 
                      0xFF, 0xE0, 0x00, 0x01,  // line 12 
 
                      0xFF, 0xF0, 0x00, 0x01,  // line 13 
                      0xFF, 0xF0, 0x00, 0x00,  // line 14 
                      0xFF, 0xF8, 0x00, 0x00,  // line 15 
                      0xFF, 0xFC, 0x00, 0x00,  // line 16 
 
                      0xFF, 0xFF, 0x00, 0x00,  // line 17 
                      0xFF, 0xFF, 0x80, 0x00,  // line 18 
                      0xFF, 0xFF, 0xE0, 0x00,  // line 19 
                      0xFF, 0xFF, 0xE0, 0x01,  // line 20 
 
                      0xFF, 0xFF, 0xF0, 0x01,  // line 21 
                      0xFF, 0xFF, 0xF0, 0x01,  // line 22 
                      0xFF, 0xFF, 0xF0, 0x03,  // line 23 
                      0xFF, 0xFF, 0xE0, 0x03,  // line 24 
 
                      0xFF, 0xFF, 0xE0, 0x07,  // line 25 
                      0xFF, 0xFF, 0xC0, 0x0F,  // line 26 
                      0xFF, 0xFF, 0xC0, 0x0F,  // line 27 
                      0xFF, 0xFF, 0x80, 0x1F,  // line 28 
 
                      0xFF, 0xFF, 0x00, 0x7F,  // line 29 
                      0xFF, 0xFC, 0x00, 0xFF,  // line 30 
                      0xFF, 0xF8, 0x03, 0xFF,  // line 31 
                      0xFF, 0xFC, 0x3F, 0xFF}; // line 32 
 
// Yang-shaped icon XOR mask 
 
BYTE XORmaskIcon[] = {0x00, 0x00, 0x00, 0x00,  // line 1 
                      0x00, 0x00, 0x00, 0x00,  // line 2 
                      0x00, 0x00, 0x00, 0x00,  // line 3 
                      0x00, 0x00, 0x00, 0x00,  // line 4 
 
                      0x00, 0x00, 0x00, 0x00,  // line 5 
                      0x00, 0x00, 0x00, 0x00,  // line 6 
                      0x00, 0x00, 0x00, 0x00,  // line 7 
                      0x00, 0x00, 0x38, 0x00,  // line 8 
 
                      0x00, 0x00, 0x7C, 0x00,  // line 9 
                      0x00, 0x00, 0x7C, 0x00,  // line 10 
                      0x00, 0x00, 0x7C, 0x00,  // line 11  
                      0x00, 0x00, 0x38, 0x00,  // line 12 
 
                      0x00, 0x00, 0x00, 0x00,  // line 13 
                      0x00, 0x00, 0x00, 0x00,  // line 14 
                      0x00, 0x00, 0x00, 0x00,  // line 15 
                      0x00, 0x00, 0x00, 0x00,  // line 16 
 
                      0x00, 0x00, 0x00, 0x00,  // line 17 
                      0x00, 0x00, 0x00, 0x00,  // line 18 
                      0x00, 0x00, 0x00, 0x00,  // line 19 
                      0x00, 0x00, 0x00, 0x00,  // line 20 
 
                      0x00, 0x00, 0x00, 0x00,  // line 21 
                      0x00, 0x00, 0x00, 0x00,  // line 22 
                      0x00, 0x00, 0x00, 0x00,  // line 23 
                      0x00, 0x00, 0x00, 0x00,  // line 24 
 
                      0x00, 0x00, 0x00, 0x00,  // line 25 
                      0x00, 0x00, 0x00, 0x00,  // line 26 
                      0x00, 0x00, 0x00, 0x00,  // line 27 
                      0x00, 0x00, 0x00, 0x00,  // line 28 
 
                      0x00, 0x00, 0x00, 0x00,  // line 29 
                      0x00, 0x00, 0x00, 0x00,  // line 30 
                      0x00, 0x00, 0x00, 0x00,  // line 31 
                      0x00, 0x00, 0x00, 0x00}; // line 32 
 
hIcon1 = CreateIcon(hinst, // handle to app. instance 
             32,           // icon width 
             32,           // icon height 
             1,            // number of XOR planes 
             1,            // number of bits per pixel 
             ANDmaskIcon,  // AND mask 
             XORmaskIcon); // XOR mask 
 
hCurs1 = CreateCursor(hinst, // handle to app. instance
             19,             // horizontal position of hot spot 
             2,              // vertical position of hot spot 
             32,             // cursor width 
             32,             // cursor height 
             ANDmaskCursor,  // AND mask 
             XORmaskCursor); // XOR mask 
 
// Fill in the window class structure. 
 
WNDCLASS  wc; 
 
wc.hIcon = hIcon1;                        // class icon 
wc.hCursor = LoadCursor(NULL, IDC_ARROW); // class cursor 
 
//
// Register the window class and perform 
// other application initialization. 
//
 
// Set a timer for the mousetrap. 
 
GetCursorPos(&ptOld); 
 
SetTimer(hwnd, IDT_CURSOR, 10000, (TIMERPROC) NULL); 
 
LONG APIENTRY MainWndProc( 
    HWND hwnd,          // window handle 
    UINT message,       // type of message 
    UINT wParam,        // additional information 
    LONG lParam)        // additional information 
{ 
 
    HDC hdc;            // handle to device context 
    POINT pt;           // current cursor location 
    RECT rc;            // minimized window location 
 
    switch (message) 
    { 
        //
        // Process other messages. 
        // 
        case WM_TIMER: 
        // If the window is minimized, compare the 
        // current cursor position with the one 10 
        // seconds before. If the cursor position has 
        // not changed, move the cursor to the icon. 
 
            if (IsIconic(hwnd)) 
            { 
                GetCursorPos(&pt); 
 
                if ((pt.x == ptOld.x) && (pt.y == ptOld.y)) 
                { 
                    GetWindowRect(hwnd, &rc); 
                    SetCursorPos(rc.left + 20, rc.top + 4); 
 
                    // Note that the additional constants 
                    // (20 and 4) are application-specific 
                    // values to align the yin-shaped cursor 
                    // and the yang-shaped icon. 
 
                } 
                else 
                { 
                    ptOld.x = pt.x; 
                    ptOld.y = pt.y; 
                } 
            } 
 
            return 0; 
 
        case WM_SETCURSOR: 
        // If the window is minimized, draw hCurs1. 
        // If the window is not minimized, draw the 
        // default cursor (class cursor). 
 
            if (IsIconic(hwnd)) 
            { 
                SetCursor(hCurs1); 
                break; 
            } 
 
        case WM_DESTROY: 
        // Destroy timer. 
 
            KillTimer(hwnd, IDT_CURSOR); 
 
            PostQuitMessage(0); 
            break; 
    } 
} 
```



## <a name="using-the-keyboard-to-move-the-cursor"></a>Usando o teclado para mover o cursor

Como o sistema não requer um mouse, um aplicativo deve ser capaz de simular ações do mouse com o teclado. O exemplo a seguir mostra como conseguir isso usando as funções [**GetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-getcursorpos) e [**SetCursorPos**](/windows/desktop/api/Winuser/nf-winuser-setcursorpos) e processando a entrada das teclas de direção.


```
HCURSOR hCurs1, hCurs2;    // cursor handles 
 
POINT pt;                  // cursor location  
RECT rc;                   // client area coordinates 
static int repeat = 1;     // repeat key counter 
 
// 
// Other declarations and initialization. 
// 
 
switch (message) 
{ 
// 
// Process other messages. 
// 
 
    case WM_KEYDOWN: 
 
        if (wParam != VK_LEFT && wParam != VK_RIGHT && 
        wParam != VK_UP && wParam != VK_DOWN) 
        { 
            break; 
        } 
 
        GetCursorPos(&pt); 
 
        // Convert screen coordinates to client coordinates. 
 
        ScreenToClient(hwnd, &pt); 
 
        switch (wParam) 
        { 
        // Move the cursor to reflect which 
        // arrow keys are pressed. 
 
            case VK_LEFT:               // left arrow 
                pt.x -= repeat; 
                break; 
 
            case VK_RIGHT:              // right arrow 
                pt.x += repeat; 
                break; 
 
            case VK_UP:                 // up arrow 
                pt.y -= repeat; 
                break; 
 
            case VK_DOWN:               // down arrow 
                pt.y += repeat; 
                break; 
 
            default: 
                return 0; 
        } 
 
        repeat++;           // Increment repeat count. 
 
        // Keep the cursor in the client area. 
 
        GetClientRect(hwnd, &rc); 
 
        if (pt.x >= rc.right) 
        { 
            pt.x = rc.right - 1; 
        } 
        else 
        { 
            if (pt.x < rc.left) 
            { 
                pt.x = rc.left; 
            } 
        } 
 
        if (pt.y >= rc.bottom) 
            pt.y = rc.bottom - 1; 
        else 
            if (pt.y < rc.top) 
                pt.y = rc.top; 
 
        // Convert client coordinates to screen coordinates. 
 
        ClientToScreen(hwnd, &pt); 
        SetCursorPos(pt.x, pt.y); 
        return 0; 

 
    case WM_KEYUP: 
 
        repeat = 1;            // Clear repeat count. 
        return 0; 
 
} 
```



 

 
