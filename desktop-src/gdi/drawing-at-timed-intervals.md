---
description: Você pode desenhar em intervalos demorados criando um temporizador com a função SetTimer.
ms.assetid: 82f9aa5e-8e42-49cf-bcd0-785bc78fe159
title: Desenhando em intervalos de tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1757aca4e6be8f169aea378c52038420519ee879
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502424"
---
# <a name="drawing-at-timed-intervals"></a>Desenhando em intervalos de tempo

Você pode desenhar em intervalos demorados criando um temporizador com a função [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) . Usando um temporizador para enviar mensagens de [**\_ temporizador do WM**](../winmsg/wm-timer.md) para o procedimento de janela em intervalos regulares, um aplicativo pode executar uma animação simples na área do cliente enquanto outros aplicativos continuam em execução.

No exemplo a seguir, o aplicativo salta uma estrela de lado a lado na área do cliente. Cada vez que o procedimento de janela recebe uma mensagem de [**\_ temporizador do WM**](../winmsg/wm-timer.md) , o procedimento apaga a estrela na posição atual, calcula uma nova posição e desenha a estrela dentro da nova posição. O procedimento inicia o temporizador chamando [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) durante o processamento da mensagem de [**\_ criação do WM**](../winmsg/wm-create.md) .


```C++
RECT rcCurrent = {0,0,20,20}; 
POINT aptStar[6] = {10,1, 1,19, 19,6, 1,6, 19,19, 10,1}; 
int X = 2, Y = -1, idTimer = -1; 
BOOL fVisible = FALSE; 
HDC hdc; 
 
LRESULT APIENTRY WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    PAINTSTRUCT ps; 
    RECT rc; 
 
    switch (message) 
    { 
        case WM_CREATE: 
 
            // Calculate the starting point.  
 
            GetClientRect(hwnd, &rc); 
            OffsetRect(&rcCurrent, rc.right / 2, rc.bottom / 2); 
 
            // Initialize the private DC.  
 
            hdc = GetDC(hwnd); 
            SetViewportOrgEx(hdc, rcCurrent.left, 
                rcCurrent.top, NULL); 
            SetROP2(hdc, R2_NOT); 
 
            // Start the timer.  
 
            SetTimer(hwnd, idTimer = 1, 10, NULL); 
            return 0L; 
 
        case WM_DESTROY: 
            KillTimer(hwnd, 1); 
            PostQuitMessage(0); 
            return 0L; 
 
        case WM_SIZE: 
            switch (wParam) 
            { 
                case SIZE_MINIMIZED: 
 
                    // Stop the timer if the window is minimized. 
 
                    KillTimer(hwnd, 1); 
                    idTimer = -1; 
                    break; 
 
                case SIZE_RESTORED: 
 
                    // Move the star back into the client area  
                    // if necessary.  
 
                    if (rcCurrent.right > (int) LOWORD(lParam)) 
                    {
                        rcCurrent.left = 
                            (rcCurrent.right = 
                                (int) LOWORD(lParam)) - 20; 
                    }
                    if (rcCurrent.bottom > (int) HIWORD(lParam)) 
                    {
                        rcCurrent.top = 
                            (rcCurrent.bottom = 
                                (int) HIWORD(lParam)) - 20; 
                    }
 
                    // Fall through to the next case.  
 
                case SIZE_MAXIMIZED: 
 
                    // Start the timer if it had been stopped.  
 
                    if (idTimer == -1) 
                        SetTimer(hwnd, idTimer = 1, 10, NULL); 
                    break; 
            } 
            return 0L; 
 
        case WM_TIMER: 
 
            // Hide the star if it is visible.  
 
            if (fVisible) 
                Polyline(hdc, aptStar, 6); 
 
            // Bounce the star off a side if necessary.  
 
            GetClientRect(hwnd, &rc); 
            if (rcCurrent.left + X < rc.left || 
                rcCurrent.right + X > rc.right) 
                X = -X; 
            if (rcCurrent.top + Y < rc.top || 
                rcCurrent.bottom + Y > rc.bottom) 
                Y = -Y; 
 
            // Show the star in its new position.  
 
            OffsetRect(&rcCurrent, X, Y); 
            SetViewportOrgEx(hdc, rcCurrent.left, 
                rcCurrent.top, NULL); 
            fVisible = Polyline(hdc, aptStar, 6); 
 
            return 0L; 
 
        case WM_ERASEBKGND: 
 
            // Erase the star.  
 
            fVisible = FALSE; 
            return DefWindowProc(hwnd, message, wParam, lParam); 
 
        case WM_PAINT: 
 
            // Show the star if it is not visible. Use BeginPaint  
            // to clear the update region.  
 
            BeginPaint(hwnd, &ps); 
            if (!fVisible) 
                fVisible = Polyline(hdc, aptStar, 6); 
            EndPaint(hwnd, &ps); 
            return 0L; 
    } 
    return DefWindowProc(hwnd, message, wParam, lParam); 
} 
```



Esse aplicativo usa um contexto de dispositivo privado para minimizar o tempo necessário para preparar o contexto do dispositivo para desenho. O procedimento de janela recupera e inicializa o contexto de dispositivo privado ao processar a mensagem de [**\_ criação do WM**](../winmsg/wm-create.md) , definindo o modo de operação de rasterização binária para permitir que a estrela seja apagada e desenhada usando a mesma chamada para a função [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) . O procedimento de janela também define a origem do visor para permitir que a estrela seja desenhada usando o mesmo conjunto de pontos, independentemente da posição da estrela na área do cliente.

O aplicativo usa a mensagem de [**\_ pintura do WM**](wm-paint.md) para desenhar a estrela sempre que a janela deve ser atualizada. O procedimento de janela só desenha a estrela se ela não estiver visível; ou seja, somente se ele tiver sido apagado pela mensagem [**\_ ERASEBKGND do WM**](../winmsg/wm-erasebkgnd.md) . O procedimento window intercepta a mensagem **\_ ERASEBKGND do WM** para definir a variável *fVisible* , mas passa a mensagem para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para que o sistema possa desenhar o plano de fundo da janela.

O aplicativo usa a mensagem de [**\_ tamanho do WM**](../winmsg/wm-size.md) para parar o timer quando a janela é minimizada e para reiniciar o temporizador quando a janela minimizada é restaurada. O procedimento de janela também usa a mensagem para atualizar a posição atual da estrela se o tamanho da janela tiver sido reduzido para que a estrela não esteja mais na área do cliente. O aplicativo controla a posição atual da estrela usando a estrutura especificada por rcCurrent, que define o retângulo delimitador para a estrela. Manter todos os cantos do retângulo na área do cliente mantém a estrela na área. Inicialmente, o procedimento de janela centraliza a estrela na área do cliente ao processar a mensagem de [**\_ criação do WM**](../winmsg/wm-create.md) .

 

 
