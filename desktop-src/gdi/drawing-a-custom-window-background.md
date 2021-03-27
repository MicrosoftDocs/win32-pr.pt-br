---
description: Você pode desenhar seu próprio plano de fundo de janela em vez de fazer com que o sistema o desenhe para você.
ms.assetid: 72a342dc-2766-4ec9-b4c6-5ac3c550ea25
title: Desenhando um plano de fundo de janela personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437a88bec680a6f35e84f5444fc90a45f98da533
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967675"
---
# <a name="drawing-a-custom-window-background"></a><span data-ttu-id="7307e-103">Desenhando um plano de fundo de janela personalizada</span><span class="sxs-lookup"><span data-stu-id="7307e-103">Drawing a Custom Window Background</span></span>

<span data-ttu-id="7307e-104">Você pode desenhar seu próprio plano de fundo de janela em vez de fazer com que o sistema o desenhe para você.</span><span class="sxs-lookup"><span data-stu-id="7307e-104">You can draw your own window background rather than having the system draw it for you.</span></span> <span data-ttu-id="7307e-105">A maioria dos aplicativos especifica uma alça de pincel ou um valor de cor do sistema para o pincel de plano de fundo da classe ao registrar a classe de janela; o sistema usa o pincel ou a cor para desenhar o plano de fundo.</span><span class="sxs-lookup"><span data-stu-id="7307e-105">Most applications specify a brush handle or system color value for the class background brush when registering the window class; the system uses the brush or color to draw the background.</span></span> <span data-ttu-id="7307e-106">No entanto, se você definir o pincel de plano de fundo da classe como **nulo**, o sistema enviará uma mensagem do [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) para o procedimento de janela sempre que o plano de fundo da janela precisar ser desenhado, permitindo desenhar um plano de fundo personalizado.</span><span class="sxs-lookup"><span data-stu-id="7307e-106">If you set the class background brush to **NULL**, however, the system sends a [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message to your window procedure whenever the window background must be drawn, letting you draw a custom background.</span></span>

<span data-ttu-id="7307e-107">No exemplo a seguir, o procedimento de janela desenha um padrão quadriculado grande que se ajusta perfeitamente à janela.</span><span class="sxs-lookup"><span data-stu-id="7307e-107">In the following example, the window procedure draws a large checkerboard pattern that fits neatly in the window.</span></span> <span data-ttu-id="7307e-108">O procedimento preenche a área do cliente com um pincel branco e, em seguida, desenha retângulos de 13 20 a 20 usando um pincel cinza.</span><span class="sxs-lookup"><span data-stu-id="7307e-108">The procedure fills the client area with a white brush and then draws thirteen 20-by-20 rectangles using a gray brush.</span></span> <span data-ttu-id="7307e-109">O contexto do dispositivo de vídeo a ser usado ao desenhar o plano de fundo é especificado no parâmetro *wParam* da mensagem.</span><span class="sxs-lookup"><span data-stu-id="7307e-109">The display device context to use when drawing the background is specified in the *wParam* parameter for the message.</span></span>


```C++
HBRUSH hbrWhite, hbrGray; 
 
  . 
  . 
  . 
 
case WM_CREATE: 
    hbrWhite = GetStockObject(WHITE_BRUSH); 
    hbrGray  = GetStockObject(GRAY_BRUSH); 
    return 0L; 
 
case WM_ERASEBKGND: 
    hdc = (HDC) wParam; 
    GetClientRect(hwnd, &rc); 
    SetMapMode(hdc, MM_ANISOTROPIC); 
    SetWindowExtEx(hdc, 100, 100, NULL); 
    SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
    FillRect(hdc, &rc, hbrWhite); 
 
    for (i = 0; i < 13; i++) 
    { 
        x = (i * 40) % 100; 
        y = ((i * 40) / 100) * 20; 
        SetRect(&rc, x, y, x + 20, y + 20); 
        FillRect(hdc, &rc, hbrGray); 
    } 
  return 1L; 
```



<span data-ttu-id="7307e-110">Se o aplicativo desenhar sua própria janela minimizada, o sistema também enviará a mensagem do [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) para o procedimento de janela para desenhar o plano de fundo da janela minimizada.</span><span class="sxs-lookup"><span data-stu-id="7307e-110">If the application draws its own minimized window, the system also sends the [**WM\_ERASEBKGND**](../winmsg/wm-erasebkgnd.md) message to the window procedure to draw the background for the minimized window.</span></span> <span data-ttu-id="7307e-111">Você pode usar a mesma técnica usada pelo [**WM \_ Paint**](wm-paint.md) para determinar se a janela está minimizada ou não, chamar a função [**isicony**](/windows/win32/api/winuser/nf-winuser-isiconic) e verificar o valor de retorno **true**.</span><span class="sxs-lookup"><span data-stu-id="7307e-111">You can use the same technique used by [**WM\_PAINT**](wm-paint.md) to determine whether the window is minimized that is, call the [**IsIconic**](/windows/win32/api/winuser/nf-winuser-isiconic) function and check for the return value **TRUE**.</span></span>

 

 
