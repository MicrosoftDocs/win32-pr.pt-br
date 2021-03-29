---
description: O sistema não é a única fonte de mensagens do WM \_ Paint. A função InvalidateRect ou InvalidateRgn pode gerar indiretamente \_ mensagens de pintura do WM para suas janelas. Essas funções marcam toda ou parte de uma área do cliente como inválida (que deve ser redesenhada).
ms.assetid: 41c2bc07-768b-4d27-a869-69b072f3e033
title: Invalidando a área do cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76fb02be44f600b80f87ec8f05c022fa3c35d827
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988803"
---
# <a name="invalidating-the-client-area"></a><span data-ttu-id="01c46-105">Invalidando a área do cliente</span><span class="sxs-lookup"><span data-stu-id="01c46-105">Invalidating the Client Area</span></span>

<span data-ttu-id="01c46-106">O sistema não é a única fonte de mensagens do [**WM \_ Paint**](wm-paint.md) .</span><span class="sxs-lookup"><span data-stu-id="01c46-106">The system is not the only source of [**WM\_PAINT**](wm-paint.md) messages.</span></span> <span data-ttu-id="01c46-107">A função [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) ou [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) pode gerar indiretamente mensagens de **\_ pintura do WM** para suas janelas.</span><span class="sxs-lookup"><span data-stu-id="01c46-107">The [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) or [**InvalidateRgn**](/windows/desktop/api/Winuser/nf-winuser-invalidatergn) function can indirectly generate **WM\_PAINT** messages for your windows.</span></span> <span data-ttu-id="01c46-108">Essas funções marcam toda ou parte de uma área do cliente como inválida (que deve ser redesenhada).</span><span class="sxs-lookup"><span data-stu-id="01c46-108">These functions mark all or part of a client area as invalid (that must be redrawn).</span></span>

<span data-ttu-id="01c46-109">No exemplo a seguir, o procedimento de janela invalida toda a área do cliente ao processar mensagens do [**WM \_ Char**](../inputdev/wm-char.md) .</span><span class="sxs-lookup"><span data-stu-id="01c46-109">In the following example, the window procedure invalidates the entire client area when processing [**WM\_CHAR**](../inputdev/wm-char.md) messages.</span></span> <span data-ttu-id="01c46-110">Isso permite que o usuário altere a figura digitando um número e exibindo os resultados; Esses resultados são desenhados assim que não há nenhuma outra mensagem na fila de mensagens do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="01c46-110">This allows the user to change the figure by typing a number and view the results; these results are drawn as soon as there are no other messages in the application's message queue.</span></span>


```C++
RECT rc;
POINT aptPentagon[6] = {50,2, 98,35, 79,90, 21,90, 2,35, 50,2}, 
      aptHexagon[7]  = {50,2, 93,25, 93,75, 50,98, 7,75, 7,25, 50,2}; 
POINT *ppt = aptPentagon; 
int cpt = 6; 
 
  . 
  . 
  . 
 
case WM_CHAR: 
    switch (wParam) 
    { 
        case '5': 
            ppt = aptPentagon; 
            cpt = 6; 
            break; 
        case '6': 
            ppt = aptHexagon; 
            cpt = 7; 
            break; 
    } 
    InvalidateRect(hwnd, NULL, TRUE); 
    return 0L; 
 
case WM_PAINT: 
    hdc = BeginPaint(hwnd, &ps); 
    GetClientRect(hwnd, &rc); 
    SetMapMode(hdc, MM_ANISOTROPIC); 
    SetWindowExtEx(hdc, 100, 100, NULL); 
    SetViewportExtEx(hdc, rc.right, rc.bottom, NULL); 
    Polyline(hdc, ppt, cpt); 
    EndPaint(hwnd, &ps); 
    return 0L; 
```



<span data-ttu-id="01c46-111">Neste exemplo, o argumento **nulo** usado pelo [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) especifica a área inteira do cliente; o **verdadeiro** argumento faz com que o plano de fundo seja apagado.</span><span class="sxs-lookup"><span data-stu-id="01c46-111">In this example, the **NULL** argument used by [**InvalidateRect**](/windows/desktop/api/Winuser/nf-winuser-invalidaterect) specifies the entire client area; the **TRUE** argument causes the background to be erased.</span></span> <span data-ttu-id="01c46-112">Se você não quiser que o aplicativo aguarde até que a fila de mensagens do aplicativo não tenha outras mensagens, use a função [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) para forçar a mensagem de [**\_ pintura do WM**](wm-paint.md) a ser enviada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="01c46-112">If you do not want the application to wait until the application's message queue has no other messages, use the [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) function to force the [**WM\_PAINT**](wm-paint.md) message to be sent immediately.</span></span> <span data-ttu-id="01c46-113">Se houver alguma parte inválida da área do cliente, o **UpdateWindow** enviará a mensagem do **WM \_ Paint** para a janela especificada diretamente para o procedimento de janela.</span><span class="sxs-lookup"><span data-stu-id="01c46-113">If there is any invalid part of the client area, **UpdateWindow** sends the **WM\_PAINT** message for the specified window directly to the window procedure.</span></span>

 

 
