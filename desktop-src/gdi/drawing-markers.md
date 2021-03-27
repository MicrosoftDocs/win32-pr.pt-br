---
description: Você pode usar as funções de linha para desenhar marcadores.
ms.assetid: 69114875-f3e0-45e9-8e87-1f4e9de08db1
title: Marcadores de desenho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497b725e3a266e296950394a9bb9b2b76a17cb25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661614"
---
# <a name="drawing-markers"></a><span data-ttu-id="94ad8-103">Marcadores de desenho</span><span class="sxs-lookup"><span data-stu-id="94ad8-103">Drawing Markers</span></span>

<span data-ttu-id="94ad8-104">Você pode usar as funções de linha para desenhar marcadores.</span><span class="sxs-lookup"><span data-stu-id="94ad8-104">You can use the line functions to draw markers.</span></span> <span data-ttu-id="94ad8-105">Um marcador é um símbolo centralizado em um ponto.</span><span class="sxs-lookup"><span data-stu-id="94ad8-105">A marker is a symbol centered over a point.</span></span> <span data-ttu-id="94ad8-106">Os aplicativos de desenho usam marcadores para designar pontos de partida, pontos finais e pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="94ad8-106">Drawing applications use markers to designate starting points, ending points, and control points.</span></span> <span data-ttu-id="94ad8-107">Os aplicativos de planilha usam marcadores para designar pontos de interesse em um gráfico ou grafo.</span><span class="sxs-lookup"><span data-stu-id="94ad8-107">Spreadsheet applications use markers to designate points of interest on a chart or graph.</span></span>

<span data-ttu-id="94ad8-108">No exemplo de código a seguir, a função de marcador definida pelo aplicativo cria um marcador usando as funções [**MoveToEx**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex) e [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) .</span><span class="sxs-lookup"><span data-stu-id="94ad8-108">In the following code sample, the application-defined Marker function creates a marker by using the [**MoveToEx**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex) and [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) functions.</span></span> <span data-ttu-id="94ad8-109">Essas funções desenham duas linhas interseccionadas, 20 pixels de comprimento, centralizadas nas coordenadas do cursor.</span><span class="sxs-lookup"><span data-stu-id="94ad8-109">These functions draw two intersecting lines, 20 pixels in length, centered over the cursor coordinates.</span></span>


```C++
void Marker(LONG x, LONG y, HWND hwnd) 
{ 
    HDC hdc; 
 
    hdc = GetDC(hwnd); 
        MoveToEx(hdc, (int) x - 10, (int) y, (LPPOINT) NULL); 
        LineTo(hdc, (int) x + 10, (int) y); 
        MoveToEx(hdc, (int) x, (int) y - 10, (LPPOINT) NULL); 
        LineTo(hdc, (int) x, (int) y + 10); 

    ReleaseDC(hwnd, hdc); 
} 
```



<span data-ttu-id="94ad8-110">O sistema armazena as coordenadas do cursor no parâmetro *lParam* da mensagem LBUTTONDOWN do [**WM \_**](../inputdev/wm-lbuttondown.md) quando o usuário pressiona o botão esquerdo do mouse.</span><span class="sxs-lookup"><span data-stu-id="94ad8-110">The system stores the coordinates of the cursor in the *lParam* parameter of the [**WM\_LBUTTONDOWN**](../inputdev/wm-lbuttondown.md) message when the user presses the left mouse button.</span></span> <span data-ttu-id="94ad8-111">O código a seguir demonstra como um aplicativo obtém essas coordenadas, determina se elas estão dentro de sua área de cliente e as transmite para a função de marcador para desenhar o marcador.</span><span class="sxs-lookup"><span data-stu-id="94ad8-111">The following code demonstrates how an application gets these coordinates, determines whether they lie within its client area, and passes them to the Marker function to draw the marker.</span></span>


```C++
// Line- and arc-drawing variables  
 
static BOOL bCollectPoints; 
static POINT ptMouseDown[32]; 
static int index; 
POINTS ptTmp; 
RECT rc; 
 
    case WM_LBUTTONDOWN: 
 
 
        if (bCollectPoints && index < 32)
        { 
            // Create the region from the client area.  
 
            GetClientRect(hwnd, &rc); 
            hrgn = CreateRectRgn(rc.left, rc.top, 
                rc.right, rc.bottom); 
 
            ptTmp = MAKEPOINTS((POINTS FAR *) lParam); 
            ptMouseDown[index].x = (LONG) ptTmp.x; 
            ptMouseDown[index].y = (LONG) ptTmp.y; 
 
            // Test for a hit in the client rectangle.  
 
            if (PtInRegion(hrgn, ptMouseDown[index].x, 
                    ptMouseDown[index].y)) 
            { 
                // If a hit occurs, record the mouse coords.  
 
                Marker(ptMouseDown[index].x, ptMouseDown[index].y, 
                    hwnd); 
                index++; 
            } 
        } 
        break; 
```



 

 
