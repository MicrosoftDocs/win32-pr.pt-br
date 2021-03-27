---
description: Você usa as funções BeginPaint e EndPaint para se preparar e concluir o desenho na área cliente.
ms.assetid: ed995bfd-a791-4d73-9a0b-daf65a9f7709
title: Desenho na área do cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e14c8492a11a7ad9764416b2453cea3264fbf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827656"
---
# <a name="drawing-in-the-client-area"></a><span data-ttu-id="05c6a-103">Desenho na área do cliente</span><span class="sxs-lookup"><span data-stu-id="05c6a-103">Drawing in the Client Area</span></span>

<span data-ttu-id="05c6a-104">Você usa as funções [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) e [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) para se preparar e concluir o desenho na área cliente.</span><span class="sxs-lookup"><span data-stu-id="05c6a-104">You use the [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) and [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) functions to prepare for and complete the drawing in the client area.</span></span> <span data-ttu-id="05c6a-105">**BeginPaint** retorna um identificador para o contexto do dispositivo de exibição usado para desenhar na área do cliente; **EndPaint** encerra a solicitação de pintura e libera o contexto do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="05c6a-105">**BeginPaint** returns a handle to the display device context used for drawing in the client area; **EndPaint** ends the paint request and releases the device context.</span></span>

<span data-ttu-id="05c6a-106">No exemplo a seguir, o procedimento de janela grava a mensagem "Olá, Windows!"</span><span class="sxs-lookup"><span data-stu-id="05c6a-106">In the following example, the window procedure writes the message "Hello, Windows!"</span></span> <span data-ttu-id="05c6a-107">na área cliente.</span><span class="sxs-lookup"><span data-stu-id="05c6a-107">in the client area.</span></span> <span data-ttu-id="05c6a-108">Para garantir que a cadeia de caracteres fique visível quando a janela for criada pela primeira vez, a função [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) chamará [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) imediatamente após a criação e a exibição da janela.</span><span class="sxs-lookup"><span data-stu-id="05c6a-108">To make sure the string is visible when the window is first created, the [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) function calls [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) immediately after creating and showing the window.</span></span> <span data-ttu-id="05c6a-109">Isso faz com que uma mensagem de [**\_ pintura do WM**](wm-paint.md) seja enviada imediatamente para o procedimento de janela.</span><span class="sxs-lookup"><span data-stu-id="05c6a-109">This causes a [**WM\_PAINT**](wm-paint.md) message to be sent immediately to the window procedure.</span></span>


```C++
LRESULT APIENTRY WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    PAINTSTRUCT ps; 
    HDC hdc; 
 
    switch (message) 
    { 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
            TextOut(hdc, 0, 0, "Hello, Windows!", 15); 
            EndPaint(hwnd, &ps); 
            return 0L; 

        // Process other messages.   
    } 
} 
 
int APIENTRY WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow) 
{ 
    HWND hwnd; 
 
    hwnd = CreateWindowEx( 
        // parameters  
        ); 
 
    ShowWindow(hwnd, SW_SHOW); 
    UpdateWindow(hwnd); 
 
    return msg.wParam; 
} 
```



 

 
