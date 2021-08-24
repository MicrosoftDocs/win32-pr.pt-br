---
description: Você usa as funções BeginPaint e EndPaint para se preparar e concluir o desenho na área cliente.
ms.assetid: ed995bfd-a791-4d73-9a0b-daf65a9f7709
title: Desenho na área do cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5d01331ae60a7814602f6c10c0d9109ae665da39aa140223e31ac03303048b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832016"
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



 

 
