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
# <a name="drawing-in-the-client-area"></a>Desenho na área do cliente

Você usa as funções [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) e [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) para se preparar e concluir o desenho na área cliente. **BeginPaint** retorna um identificador para o contexto do dispositivo de exibição usado para desenhar na área do cliente; **EndPaint** encerra a solicitação de pintura e libera o contexto do dispositivo.

No exemplo a seguir, o procedimento de janela grava a mensagem "Olá, Windows!" na área cliente. Para garantir que a cadeia de caracteres fique visível quando a janela for criada pela primeira vez, a função [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) chamará [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) imediatamente após a criação e a exibição da janela. Isso faz com que uma mensagem de [**\_ pintura do WM**](wm-paint.md) seja enviada imediatamente para o procedimento de janela.


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



 

 
