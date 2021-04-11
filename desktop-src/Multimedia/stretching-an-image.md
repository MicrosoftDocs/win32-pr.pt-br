---
title: Alongando uma imagem
description: Alongando uma imagem
ms.assetid: 7cfd91c3-0ebd-47eb-a33d-c81a66f820e5
keywords:
- Macro MCIWndGetDest
- Macro MCIWndPutDest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0296cd31988ba79aeab9221fb41b4fd150ffc09
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292582"
---
# <a name="stretching-an-image"></a><span data-ttu-id="9b977-105">Alongando uma imagem</span><span class="sxs-lookup"><span data-stu-id="9b977-105">Stretching an Image</span></span>

<span data-ttu-id="9b977-106">O exemplo a seguir alonga as imagens de um clipe de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9b977-106">The following example stretches the images of a video clip.</span></span> <span data-ttu-id="9b977-107">Ele aumenta as dimensões do retângulo de destino usando a macro [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) .</span><span class="sxs-lookup"><span data-stu-id="9b977-107">It increases the dimensions of the destination rectangle by using the [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) macro.</span></span> <span data-ttu-id="9b977-108">O tamanho da área de reprodução permanece inalterado, portanto, o resultado é uma imagem distorcida e ampliada.</span><span class="sxs-lookup"><span data-stu-id="9b977-108">The size of the playback area remains unchanged, so the result is a distorted, magnified image.</span></span> <span data-ttu-id="9b977-109">Os exemplos usam a função **MCIWndPutDest** para reposicionar o retângulo de destino em relação à área de reprodução, fornecendo uma maneira de exibir diferentes partes da imagem ampliada.</span><span class="sxs-lookup"><span data-stu-id="9b977-109">The examples uses the **MCIWndPutDest** function to reposition the destination rectangle with respect to the playback area, providing a way to view different portions of the stretched image.</span></span>


```C++
extern RECT rCurrent, rDest; 
 
case WM_COMMAND: 
   switch (wParam) 
   { 
       case IDM_CREATEMCIWND: 
           g_hwndMCIWnd = MCIWndCreate(hwnd, 
               g_hinst, 
               WS_CHILD | WS_VISIBLE, 
               "sample.avi"); 
           break; 
 
       case  IDM_STRETCHIMAGE:      // stretch destination RECT 3:2, 
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT 
           rDest.top = rCurrent.top;               // new boundaries 
           rDest.right = rCurrent.right; 
           rDest.left = rCurrent.left + 
               ((rCurrent.left - rCurrent.right) * 3); 
           rDest.bottom = rCurrent.top + 
               ((rCurrent.bottom - rCurrent.top) * 2); 
           MCIWndPutDest(g_hwndMCIWnd, &rDest); // new destination 
           break; 
       case IDM_MOVEDOWN:           // move toward bottom of image 
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT 
           rCurrent.top -= 100;                    // new boundaries 
           rCurrent.bottom -= 100; 
           MCIWndPutDest(g_hwndMCIWnd, &rCurrent); // new destination
           break; 
       case IDM_MOVEUP:             // move toward top of image 
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT 
           rCurrent.top += 100;                    // new boundaries 
           rCurrent.bottom += 100; 
           MCIWndPutDest(g_hwndMCIWnd, &rCurrent); // new destination 
           break; 
       case IDM_MOVELEFT:           // move toward left edge of image
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT 
           rCurrent.right += 100;                  // new boundaries 
           rCurrent.left += 100; 
           MCIWndPutDest(g_hwndMCIWnd, &rCurrent); // new destination 
           break; 
       case  IDM_MOVERIGHT:         // move toward right edge of image
           MCIWndGetDest(g_hwndMCIWnd, &rCurrent); // destination RECT
           rCurrent.right -= 100;                  // new boundaries 
           rCurrent.left -= 100; 
           MCIWndPutDest(g_hwndMCIWnd, &rCurrent); // new destination 
           break; 
   } 
   break; 
 
   // Handle other messages here. 
```



 

 




