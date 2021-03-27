---
description: Você pode limitar a quantidade de desenho que o aplicativo realiza ao processar a mensagem de pintura do WM \_ determinando o tamanho e o local da região de atualização.
ms.assetid: 3407014d-6427-45e9-8be4-b8037ca5438f
title: Redesenhando na região de atualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4f90518db1a66b98fc7f4bd5961f2cfa581bb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988783"
---
# <a name="redrawing-in-the-update-region"></a>Redesenhando na região de atualização

Você pode limitar a quantidade de desenho que o aplicativo realiza ao processar a mensagem de [**\_ pintura do WM**](wm-paint.md) determinando o tamanho e o local da região de atualização. Como o sistema usa a região de atualização ao criar a região de recorte para o contexto do dispositivo de exibição da janela, você pode determinar indiretamente a região de atualização examinando a região de recorte.

No exemplo a seguir, o procedimento de janela desenha um triângulo, um retângulo, um Pentágono e um hexágono, mas somente se toda ou uma parte de cada figura estiver dentro da região de atualização. O procedimento de janela usa a função [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) e um retângulo 100-por-100 para determinar se uma figura está dentro da região de recorte (e, portanto, a região de atualização) para o contexto de dispositivo comum recuperado por [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint).


```C++
POINT aptTriangle[4]  = {50,2, 98,86,  2,86, 50,2}, 
      aptRectangle[5] = { 2,2, 98,2,  98,98,  2,98, 2,2}, 
      aptPentagon[6]  = {50,2, 98,35, 79,90, 21,90, 2,35, 50,2}, 
      aptHexagon[7]   = {50,2, 93,25, 93,75, 50,98, 7,75, 7,25, 50,2}; 
  . 
  . 
  . 
 
        case WM_PAINT: 
            hdc = BeginPaint(hwnd, &ps); 
            SetRect(&rc, 0, 0, 100, 100); 
 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptTriangle, 4); 
 
            SetViewportOrgEx(hdc, 100, 0, NULL); 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptRectangle, 5); 
 
            SetViewportOrgEx(hdc, 0, 100, NULL); 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptPentagon, 6); 
 
            SetViewportOrgEx(hdc, 100, 100, NULL); 
            if (RectVisible(hdc, &rc)) 
                Polyline(hdc, aptHexagon, 7); 
            EndPaint(hwnd, &ps); 
            return 0L; 
 
  . 
  . 
  . 
```



As coordenadas de cada figura neste exemplo se encontram dentro do mesmo retângulo 100-por-100. Antes de desenhar uma figura, o procedimento de janela define a origem do visor para uma parte diferente da área do cliente usando a função [**SetViewportOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setviewportorgex) . Isso impede que as figuras sejam desenhadas uma na parte superior da outra. Alterar a origem do visor não afeta a região de recorte, mas afeta como as coordenadas do retângulo passado para [**RectVisible**](/windows/desktop/api/Wingdi/nf-wingdi-rectvisible) são interpretadas. A alteração da origem também permite que você use um único retângulo para verificar a região de atualização em vez de retângulos individuais para cada figura.

 

 



