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
# <a name="drawing-at-timed-intervals"></a><span data-ttu-id="f5adf-103">Desenhando em intervalos de tempo</span><span class="sxs-lookup"><span data-stu-id="f5adf-103">Drawing at Timed Intervals</span></span>

<span data-ttu-id="f5adf-104">Você pode desenhar em intervalos demorados criando um temporizador com a função [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) .</span><span class="sxs-lookup"><span data-stu-id="f5adf-104">You can draw at timed intervals by creating a timer with the [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) function.</span></span> <span data-ttu-id="f5adf-105">Usando um temporizador para enviar mensagens de [**\_ temporizador do WM**](../winmsg/wm-timer.md) para o procedimento de janela em intervalos regulares, um aplicativo pode executar uma animação simples na área do cliente enquanto outros aplicativos continuam em execução.</span><span class="sxs-lookup"><span data-stu-id="f5adf-105">By using a timer to send [**WM\_TIMER**](../winmsg/wm-timer.md) messages to the window procedure at regular intervals, an application can carry out simple animation in the client area while other applications continue running.</span></span>

<span data-ttu-id="f5adf-106">No exemplo a seguir, o aplicativo salta uma estrela de lado a lado na área do cliente.</span><span class="sxs-lookup"><span data-stu-id="f5adf-106">In the following example, the application bounces a star from side to side in the client area.</span></span> <span data-ttu-id="f5adf-107">Cada vez que o procedimento de janela recebe uma mensagem de [**\_ temporizador do WM**](../winmsg/wm-timer.md) , o procedimento apaga a estrela na posição atual, calcula uma nova posição e desenha a estrela dentro da nova posição.</span><span class="sxs-lookup"><span data-stu-id="f5adf-107">Each time the window procedure receives a [**WM\_TIMER**](../winmsg/wm-timer.md) message, the procedure erases the star at the current position, calculates a new position, and draws the star within the new position.</span></span> <span data-ttu-id="f5adf-108">O procedimento inicia o temporizador chamando [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) durante o processamento da mensagem de [**\_ criação do WM**](../winmsg/wm-create.md) .</span><span class="sxs-lookup"><span data-stu-id="f5adf-108">The procedure starts the timer by calling [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) while processing the [**WM\_CREATE**](../winmsg/wm-create.md) message.</span></span>


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



<span data-ttu-id="f5adf-109">Esse aplicativo usa um contexto de dispositivo privado para minimizar o tempo necessário para preparar o contexto do dispositivo para desenho.</span><span class="sxs-lookup"><span data-stu-id="f5adf-109">This application uses a private device context to minimize the time required to prepare the device context for drawing.</span></span> <span data-ttu-id="f5adf-110">O procedimento de janela recupera e inicializa o contexto de dispositivo privado ao processar a mensagem de [**\_ criação do WM**](../winmsg/wm-create.md) , definindo o modo de operação de rasterização binária para permitir que a estrela seja apagada e desenhada usando a mesma chamada para a função [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) .</span><span class="sxs-lookup"><span data-stu-id="f5adf-110">The window procedure retrieves and initializes the private device context when processing the [**WM\_CREATE**](../winmsg/wm-create.md) message, setting the binary raster operation mode to allow the star to be erased and drawn using the same call to the [**Polyline**](/windows/desktop/api/Wingdi/nf-wingdi-polyline) function.</span></span> <span data-ttu-id="f5adf-111">O procedimento de janela também define a origem do visor para permitir que a estrela seja desenhada usando o mesmo conjunto de pontos, independentemente da posição da estrela na área do cliente.</span><span class="sxs-lookup"><span data-stu-id="f5adf-111">The window procedure also sets the viewport origin to allow the star to be drawn using the same set of points regardless of the star's position in the client area.</span></span>

<span data-ttu-id="f5adf-112">O aplicativo usa a mensagem de [**\_ pintura do WM**](wm-paint.md) para desenhar a estrela sempre que a janela deve ser atualizada.</span><span class="sxs-lookup"><span data-stu-id="f5adf-112">The application uses the [**WM\_PAINT**](wm-paint.md) message to draw the star whenever the window must be updated.</span></span> <span data-ttu-id="f5adf-113">O procedimento de janela só desenha a estrela se ela não estiver visível; ou seja, somente se ele tiver sido apagado pela mensagem [**\_ ERASEBKGND do WM**](../winmsg/wm-erasebkgnd.md) .</span><span class="sxs-lookup"><span data-stu-id="f5adf-113">The window procedure draws the star only if it is not visible; that is, only if it has been erased by the [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message.</span></span> <span data-ttu-id="f5adf-114">O procedimento window intercepta a mensagem **\_ ERASEBKGND do WM** para definir a variável *fVisible* , mas passa a mensagem para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para que o sistema possa desenhar o plano de fundo da janela.</span><span class="sxs-lookup"><span data-stu-id="f5adf-114">The window procedure intercepts the **WM\_ERASEBKGND** message to set the *fVisible* variable, but passes the message to [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) so that the system can draw the window background.</span></span>

<span data-ttu-id="f5adf-115">O aplicativo usa a mensagem de [**\_ tamanho do WM**](../winmsg/wm-size.md) para parar o timer quando a janela é minimizada e para reiniciar o temporizador quando a janela minimizada é restaurada.</span><span class="sxs-lookup"><span data-stu-id="f5adf-115">The application uses the [**WM\_SIZE**](../winmsg/wm-size.md) message to stop the timer when the window is minimized and to restart the timer when the minimized window is restored.</span></span> <span data-ttu-id="f5adf-116">O procedimento de janela também usa a mensagem para atualizar a posição atual da estrela se o tamanho da janela tiver sido reduzido para que a estrela não esteja mais na área do cliente.</span><span class="sxs-lookup"><span data-stu-id="f5adf-116">The window procedure also uses the message to update the current position of the star if the size of the window has been reduced so that the star is no longer in the client area.</span></span> <span data-ttu-id="f5adf-117">O aplicativo controla a posição atual da estrela usando a estrutura especificada por rcCurrent, que define o retângulo delimitador para a estrela.</span><span class="sxs-lookup"><span data-stu-id="f5adf-117">The application keeps track of the star's current position by using the structure specified by rcCurrent, which defines the bounding rectangle for the star.</span></span> <span data-ttu-id="f5adf-118">Manter todos os cantos do retângulo na área do cliente mantém a estrela na área.</span><span class="sxs-lookup"><span data-stu-id="f5adf-118">Keeping all corners of the rectangle in the client area keeps the star in the area.</span></span> <span data-ttu-id="f5adf-119">Inicialmente, o procedimento de janela centraliza a estrela na área do cliente ao processar a mensagem de [**\_ criação do WM**](../winmsg/wm-create.md) .</span><span class="sxs-lookup"><span data-stu-id="f5adf-119">The window procedure initially centers the star in the client area when processing the [**WM\_CREATE**](../winmsg/wm-create.md) message.</span></span>

 

 
