---
description: Este tópico mostra como criar e destruir temporizadores e como usar um temporizador para interceptar a entrada do mouse em intervalos especificados.
ms.assetid: eee54078-759f-4fd4-9cf4-10a8bde888b7
title: Usando temporizadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7922be60012ae81ce1971afe6f2300f54689f7a6cc8d7f088df2fb126e834ab5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028304"
---
# <a name="using-timers"></a>Usando temporizadores

Este tópico mostra como criar e destruir temporizadores e como usar um temporizador para interceptar a entrada do mouse em intervalos especificados.

Este tópico inclui as seções a seguir.

-   [Criando um temporizador](#creating-a-timer)
-   [Destruindo um temporizador](#destroying-a-timer)
-   [Usando funções de temporizador para interceptar a entrada do mouse](#using-timer-functions-to-trap-mouse-input)
-   [Tópicos relacionados](#related-topics)

## <a name="creating-a-timer"></a>Criando um temporizador

O exemplo a seguir usa a função [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) para criar dois temporizadores. O primeiro temporizador é definido para cada 10 segundos, o segundo para cada cinco minutos.


```
// Set two timers. 
 
SetTimer(hwnd,             // handle to main window 
    IDT_TIMER1,            // timer identifier 
    10000,                 // 10-second interval 
    (TIMERPROC) NULL);     // no timer callback 
 
SetTimer(hwnd,             // handle to main window 
    IDT_TIMER2,            // timer identifier 
    300000,                // five-minute interval 
    (TIMERPROC) NULL);     // no timer callback 
```



Para processar as mensagens de [**\_ temporizador do WM**](wm-timer.md) geradas por esses temporizadores, adicione uma instrução Case **\_ Timer do WM** ao procedimento de janela para o parâmetro *HWND* .


```
case WM_TIMER: 
 
    switch (wParam) 
    { 
        case IDT_TIMER1: 
            // process the 10-second timer 
 
             return 0; 
 
        case IDT_TIMER2: 
            // process the five-minute timer 

            return 0; 
    } 
```



Um aplicativo também pode criar um temporizador cujas mensagens de [**\_ temporizador do WM**](wm-timer.md) sejam processadas não pelo procedimento da janela principal, mas por uma função de retorno de chamada definida pelo aplicativo, como no exemplo de código a seguir, que cria um temporizador e usa a função de retorno de chamada **MyTimerProc** para processar as mensagens do **\_ temporizador do WM** do temporizador.


```
// Set the timer. 
 
SetTimer(hwnd,                // handle to main window 
    IDT_TIMER3,               // timer identifier 
    5000,                     // 5-second interval 
    (TIMERPROC) MyTimerProc); // timer callback
```



A Convenção de chamada para **MyTimerProc** deve ser baseada na função de retorno de chamada [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) .

Se seu aplicativo criar um temporizador sem especificar um identificador de janela, seu aplicativo deverá monitorar a fila de mensagens para mensagens de [**\_ temporizador do WM**](wm-timer.md) e expedir-as para a janela apropriada.


```
HWND hwndTimer;   // handle to window for timer messages 
MSG msg;          // message structure 
 
    while (GetMessage(&msg, // message structure 
            NULL,           // handle to window to receive the message 
               0,           // lowest message to examine 
               0))          // highest message to examine 
    { 
 
        // Post WM_TIMER messages to the hwndTimer procedure. 
 
        if (msg.message == WM_TIMER) 
        { 
            msg.hwnd = hwndTimer; 
        } 
 
        TranslateMessage(&msg); // translates virtual-key codes 
        DispatchMessage(&msg);  // dispatches message to window 
    } 
```



## <a name="destroying-a-timer"></a>Destruindo um temporizador

Os aplicativos devem usar a função [**KillTimer**](/windows/win32/api/winuser/nf-winuser-killtimer) para destruir temporizadores que não são mais necessários. O exemplo a seguir destrói os temporizadores identificados pelas constantes IDT \_ TIMER1, IDT \_ TIMER2 e IDT \_ TIMER3.


```
// Destroy the timers. 
 
KillTimer(hwnd, IDT_TIMER1); 
KillTimer(hwnd, IDT_TIMER2); 
KillTimer(hwnd, IDT_TIMER3); 
```



## <a name="using-timer-functions-to-trap-mouse-input"></a>Usando funções de temporizador para interceptar a entrada do mouse

Às vezes, é necessário evitar mais entradas enquanto você tem um ponteiro do mouse na tela. Uma maneira de fazer isso é criar uma rotina especial que intercepta a entrada do mouse até que ocorra um evento específico. Muitos desenvolvedores se referem a essa rotina como "criando um ratoeira".

O exemplo a seguir usa as funções [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) e [**KillTimer**](/windows/win32/api/winuser/nf-winuser-killtimer) para interceptar a entrada do mouse. **SetTimer** cria um temporizador que envia uma mensagem do [**\_ temporizador do WM**](wm-timer.md) a cada 10 segundos. Cada vez que o aplicativo recebe uma mensagem de **\_ temporizador do WM** , ele registra o local do ponteiro do mouse. Se o local atual for o mesmo que o local anterior e a janela principal do aplicativo for minimizada, o aplicativo moverá o ponteiro do mouse para o ícone. Quando o aplicativo é fechado, **KillTimer** para o temporizador.


```
HICON hIcon1;               // icon handle 
POINT ptOld;                // previous cursor location 
UINT uResult;               // SetTimer's return value 
HINSTANCE hinstance;        // handle to current instance 
 
//
// Perform application initialization here. 
//
 
wc.hIcon = LoadIcon(hinstance, MAKEINTRESOURCE(400)); 
wc.hCursor = LoadCursor(hinstance, MAKEINTRESOURCE(200)); 
 
// Record the initial cursor position. 
 
GetCursorPos(&ptOld); 
 
// Set the timer for the mousetrap. 
 
uResult = SetTimer(hwnd,             // handle to main window 
    IDT_MOUSETRAP,                   // timer identifier 
    10000,                           // 10-second interval 
    (TIMERPROC) NULL);               // no timer callback 
 
if (uResult == 0) 
{ 
    ErrorHandler("No timer is available."); 
} 
 
LONG APIENTRY MainWndProc( 
    HWND hwnd,          // handle to main window 
    UINT message,       // type of message 
    WPARAM  wParam,     // additional information 
    LPARAM  lParam)     // additional information 
{ 
 
    HDC hdc;        // handle to device context 
    POINT pt;       // current cursor location 
    RECT rc;        // location of minimized window 
 
    switch (message) 
    { 
        //
        // Process other messages. 
        // 
 
        case WM_TIMER: 
        // If the window is minimized, compare the current 
        // cursor position with the one from 10 seconds 
        // earlier. If the cursor position has not changed, 
        // move the cursor to the icon. 
 
            if (IsIconic(hwnd)) 
            { 
                GetCursorPos(&pt); 
 
                if ((pt.x == ptOld.x) && (pt.y == ptOld.y)) 
                { 
                    GetWindowRect(hwnd, &rc); 
                    SetCursorPos(rc.left, rc.top); 
                } 
                else 
                { 
                    ptOld.x = pt.x; 
                    ptOld.y = pt.y; 
                } 
            } 
 
            return 0; 
 
        case WM_DESTROY: 
 
        // Destroy the timer. 
 
            KillTimer(hwnd, IDT_MOUSETRAP); 
            PostQuitMessage(0); 
            break; 
 
        //
        // Process other messages. 
        // 
 
} 
```



Embora o exemplo a seguir também mostre como interceptar a entrada do mouse, ele processa a mensagem do [**\_ temporizador do WM**](wm-timer.md) por meio da função de retorno de chamada definida pelo aplicativo **MyTimerProc**, em vez de por meio da fila de mensagens do aplicativo.


```
UINT uResult;               // SetTimer's return value 
HICON hIcon1;               // icon handle 
POINT ptOld;                // previous cursor location 
HINSTANCE hinstance;        // handle to current instance 
 
//
// Perform application initialization here. 
//
 
wc.hIcon = LoadIcon(hinstance, MAKEINTRESOURCE(400)); 
wc.hCursor = LoadCursor(hinstance, MAKEINTRESOURCE(200)); 
 
// Record the current cursor position. 
 
GetCursorPos(&ptOld); 
 
// Set the timer for the mousetrap. 
 
uResult = SetTimer(hwnd,      // handle to main window 
    IDT_MOUSETRAP,            // timer identifier 
    10000,                    // 10-second interval 
    (TIMERPROC) MyTimerProc); // timer callback 
 
if (uResult == 0) 
{ 
    ErrorHandler("No timer is available."); 
} 
 
LONG APIENTRY MainWndProc( 
    HWND hwnd,          // handle to main window 
    UINT message,       // type of message 
    WPARAM  wParam,     // additional information 
    LPARAM   lParam)    // additional information 
{ 
 
    HDC hdc;            // handle to device context 
 
    switch (message) 
    { 
    // 
    // Process other messages. 
    // 
 
        case WM_DESTROY: 
        // Destroy the timer. 
 
            KillTimer(hwnd, IDT_MOUSETRAP); 
            PostQuitMessage(0); 
            break; 
 
        //
        // Process other messages. 
        // 
 
} 
 
// MyTimerProc is an application-defined callback function that 
// processes WM_TIMER messages. 
 
VOID CALLBACK MyTimerProc( 
    HWND hwnd,        // handle to window for timer messages 
    UINT message,     // WM_TIMER message 
    UINT idTimer,     // timer identifier 
    DWORD dwTime)     // current system time 
{ 
 
    RECT rc; 
    POINT pt; 
 
    // If the window is minimized, compare the current 
    // cursor position with the one from 10 seconds earlier. 
    // If the cursor position has not changed, move the 
    // cursor to the icon. 
 
    if (IsIconic(hwnd)) 
    { 
        GetCursorPos(&pt); 
 
        if ((pt.x == ptOld.x) && (pt.y == ptOld.y)) 
        { 
            GetWindowRect(hwnd, &rc); 
            SetCursorPos(rc.left, rc.top); 
        } 
        else 
        { 
            ptOld.x = pt.x; 
            ptOld.y = pt.y; 
        } 
    } 
} 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre temporizadores](about-timers.md)
</dt> </dl>

 

 
