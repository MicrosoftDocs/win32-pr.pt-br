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
# <a name="drawing-markers"></a>Marcadores de desenho

Você pode usar as funções de linha para desenhar marcadores. Um marcador é um símbolo centralizado em um ponto. Os aplicativos de desenho usam marcadores para designar pontos de partida, pontos finais e pontos de controle. Os aplicativos de planilha usam marcadores para designar pontos de interesse em um gráfico ou grafo.

No exemplo de código a seguir, a função de marcador definida pelo aplicativo cria um marcador usando as funções [**MoveToEx**](/windows/desktop/api/Wingdi/nf-wingdi-movetoex) e [**LineTo**](/windows/desktop/api/Wingdi/nf-wingdi-lineto) . Essas funções desenham duas linhas interseccionadas, 20 pixels de comprimento, centralizadas nas coordenadas do cursor.


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



O sistema armazena as coordenadas do cursor no parâmetro *lParam* da mensagem LBUTTONDOWN do [**WM \_**](../inputdev/wm-lbuttondown.md) quando o usuário pressiona o botão esquerdo do mouse. O código a seguir demonstra como um aplicativo obtém essas coordenadas, determina se elas estão dentro de sua área de cliente e as transmite para a função de marcador para desenhar o marcador.


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



 

 
