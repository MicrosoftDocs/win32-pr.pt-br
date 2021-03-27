---
description: Você pode permitir que o usuário desenhe linhas com o mouse fazendo com que o procedimento de janela seja desenhado durante o processamento da \_ mensagem MOUSEMOVE do WM.
ms.assetid: 5e8a54b6-05cc-4446-b82e-2b3e550d780a
title: Desenho com o mouse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ad38e7ef8af5c39918bac7231aea4dde285caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010734"
---
# <a name="drawing-with-the-mouse"></a><span data-ttu-id="05135-103">Desenho com o mouse</span><span class="sxs-lookup"><span data-stu-id="05135-103">Drawing with the Mouse</span></span>

<span data-ttu-id="05135-104">Você pode permitir que o usuário desenhe linhas com o mouse fazendo com que o procedimento de janela seja desenhado durante o processamento da mensagem [**\_ MOUSEMOVE do WM**](../inputdev/wm-mousemove.md) .</span><span class="sxs-lookup"><span data-stu-id="05135-104">You can permit the user to draw lines with the mouse by having your window procedure draw while processing the [**WM\_MOUSEMOVE**](../inputdev/wm-mousemove.md) message.</span></span> <span data-ttu-id="05135-105">O sistema envia a **mensagem \_ MOUSEMOVE do WM** para o procedimento de janela sempre que o usuário move o cursor dentro da janela.</span><span class="sxs-lookup"><span data-stu-id="05135-105">The system sends the **WM\_MOUSEMOVE** message to the window procedure whenever the user moves the cursor within the window.</span></span> <span data-ttu-id="05135-106">Para desenhar linhas, o procedimento de janela pode recuperar um contexto de dispositivo de exibição e desenhar uma linha na janela entre as posições de cursor atual e anterior.</span><span class="sxs-lookup"><span data-stu-id="05135-106">To draw lines, the window procedure can retrieve a display device context and draw a line in the window between the current and previous cursor positions.</span></span>

<span data-ttu-id="05135-107">No exemplo a seguir, o procedimento de janela se prepara para desenhar quando o usuário pressiona e mantém o botão esquerdo do mouse (enviando a mensagem do [**WM \_ LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) ).</span><span class="sxs-lookup"><span data-stu-id="05135-107">In the following example, the window procedure prepares for drawing when the user presses and holds the left mouse button (sending the [**WM\_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) message).</span></span> <span data-ttu-id="05135-108">À medida que o usuário move o cursor dentro da janela, o procedimento de janela recebe uma série de mensagens [**\_ MOUSEMOVE do WM**](../inputdev/wm-mousemove.md) .</span><span class="sxs-lookup"><span data-stu-id="05135-108">As the user moves the cursor within the window, the window procedure receives a series of [**WM\_MOUSEMOVE**](../inputdev/wm-mousemove.md) messages.</span></span> <span data-ttu-id="05135-109">Para cada mensagem, o procedimento de janela desenha uma linha conectando a posição anterior e a posição atual.</span><span class="sxs-lookup"><span data-stu-id="05135-109">For each message, the window procedure draws a line connecting the previous position and the current position.</span></span> <span data-ttu-id="05135-110">Para desenhar a linha, o procedimento usa [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) para recuperar um contexto de dispositivo de exibição; em seguida, assim que o desenho for concluído e antes de retornar da mensagem, o procedimento usará a função [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) para liberar o contexto do dispositivo de exibição.</span><span class="sxs-lookup"><span data-stu-id="05135-110">To draw the line, the procedure uses [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) to retrieve a display device context; then, as soon as drawing is complete and before returning from the message, the procedure uses the [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) function to release the display device context.</span></span> <span data-ttu-id="05135-111">Assim que o usuário libera o botão do mouse, o procedimento de janela limpa o sinalizador e o desenho é interrompido (o que envia a mensagem [**\_ LBUTTONUP do WM**](../inputdev/wm-lbuttonup.md) ).</span><span class="sxs-lookup"><span data-stu-id="05135-111">As soon as the user releases the mouse button, the window procedure clears the flag, and the drawing stops (which sends the [**WM\_LBUTTONUP**](../inputdev/wm-lbuttonup.md) message).</span></span>


```C++
BOOL fDraw = FALSE; 
POINT ptPrevious; 
 
  . 
  . 
  . 
 
case WM_LBUTTONDOWN: 
    fDraw = TRUE; 
    ptPrevious.x = LOWORD(lParam); 
    ptPrevious.y = HIWORD(lParam); 
    return 0L; 
 
case WM_LBUTTONUP: 
    if (fDraw) 
    { 
        hdc = GetDC(hwnd); 
        MoveToEx(hdc, ptPrevious.x, ptPrevious.y, NULL); 
        LineTo(hdc, LOWORD(lParam), HIWORD(lParam)); 
        ReleaseDC(hwnd, hdc); 
    } 
    fDraw = FALSE; 
    return 0L; 
 
case WM_MOUSEMOVE: 
    if (fDraw) 
    { 
        hdc = GetDC(hwnd); 
        MoveToEx(hdc, ptPrevious.x, ptPrevious.y, NULL); 
        LineTo(hdc, ptPrevious.x = LOWORD(lParam), 
          ptPrevious.y = HIWORD(lParam)); 
        ReleaseDC(hwnd, hdc); 
    } 
    return 0L; 
```



<span data-ttu-id="05135-112">Um aplicativo que habilita o desenho, como neste exemplo, normalmente registra os pontos ou linhas para que as linhas possam ser redesenhadas sempre que a janela for atualizada.</span><span class="sxs-lookup"><span data-stu-id="05135-112">An application that enables drawing, as in this example, typically records either the points or lines so that the lines can be redrawn whenever the window is updated.</span></span> <span data-ttu-id="05135-113">Os aplicativos de desenho geralmente usam um contexto de dispositivo de memória e um bitmap associado para armazenar as linhas que foram desenhadas usando um mouse.</span><span class="sxs-lookup"><span data-stu-id="05135-113">Drawing applications often use a memory device context and an associated bitmap to store lines that were drawn by using a mouse.</span></span>

 

 
