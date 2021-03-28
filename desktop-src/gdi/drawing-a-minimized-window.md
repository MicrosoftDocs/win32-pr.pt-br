---
description: Você pode desenhar suas próprias janelas minimizadas em vez de fazer com que o sistema as desenhe para você.
ms.assetid: 607d987a-5bdc-46bc-bde7-6dc52745ac79
title: Desenhando uma janela minimizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced1f3205243ea098856517590d58caee851329a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370671"
---
# <a name="drawing-a-minimized-window"></a><span data-ttu-id="60897-103">Desenhando uma janela minimizada</span><span class="sxs-lookup"><span data-stu-id="60897-103">Drawing a Minimized Window</span></span>

<span data-ttu-id="60897-104">Você pode desenhar suas próprias janelas minimizadas em vez de fazer com que o sistema as desenhe para você.</span><span class="sxs-lookup"><span data-stu-id="60897-104">You can draw your own minimized windows rather than having the system draw them for you.</span></span> <span data-ttu-id="60897-105">A maioria dos aplicativos define um ícone de classe ao registrar a classe Window para a janela, e o sistema desenha o ícone quando a janela é minimizada.</span><span class="sxs-lookup"><span data-stu-id="60897-105">Most applications define a class icon when registering the window class for the window, and the system draws the icon when the window is minimized.</span></span> <span data-ttu-id="60897-106">No entanto, se você definir o ícone de classe como **nulo**, o sistema enviará uma mensagem de [**\_ pintura do WM**](wm-paint.md) para o procedimento de janela sempre que a janela for minimizada, permitindo que o procedimento de janela desenhe na janela minimizada.</span><span class="sxs-lookup"><span data-stu-id="60897-106">If you set the class icon to **NULL**, however, the system sends a [**WM\_PAINT**](wm-paint.md) message to your window procedure whenever the window is minimized, enabling the window procedure to draw in the minimized window.</span></span>

<span data-ttu-id="60897-107">No exemplo a seguir, o procedimento de janela desenha uma estrela na janela minimizada.</span><span class="sxs-lookup"><span data-stu-id="60897-107">In the following example, the window procedure draws a star in the minimized window.</span></span> <span data-ttu-id="60897-108">O procedimento usa a função [**Isicony**](/windows/win32/api/winuser/nf-winuser-isiconic) para determinar quando a janela é minimizada.</span><span class="sxs-lookup"><span data-stu-id="60897-108">The procedure uses the [**IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) function to determine when the window is minimized.</span></span> <span data-ttu-id="60897-109">Isso garante que a estrela seja desenhada somente quando a janela for minimizada.</span><span class="sxs-lookup"><span data-stu-id="60897-109">This ensures that the star is drawn only when the window is minimized.</span></span>


```C++
POINT aptStar[6] = {50,2, 2,98, 98,33, 2,33, 98,98, 50,2}; 
 
  . 
  . 
  . 
 
case WM_PAINT: 
    hdc = BeginPaint(hwnd, &ps); 
 
    // Determine whether the window is minimized.  
 
    if (IsIconic(hwnd)) 
    { 
        GetClientRect(hwnd, &rc); 
        SetMapMode(hdc, MM_ANISOTROPIC); 
        SetWindowExtEx(hdc, 100, 100, NULL); 
        SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
        Polyline(hdc, aptStar, 6); 
    } 
    else 
    { 
        TextOut(hdc, 0,0, "Hello, Windows!", 15); 
    } 
    EndPaint(hwnd, &ps); 
    return 0L; 
```



<span data-ttu-id="60897-110">Você define o ícone de classe como **nulo** definindo o membro **HIcon** da estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) como **NULL** antes de chamar a função [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) para a classe Window.</span><span class="sxs-lookup"><span data-stu-id="60897-110">You set the class icon to **NULL** by setting the **hIcon** member of the [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) structure to **NULL** before calling the [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) function for the window class.</span></span>

 

 
