---
description: Depois que o usuário clica em Clip no menu, o aplicativo usa as coordenadas do retângulo criado pelo usuário para definir uma região de recorte.
ms.assetid: 5ae60181-c72e-4a28-99eb-e23d35c46685
title: Saída de recorte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7a683fd276165b8c4556881f6aab47931978048b4699496a0f996abd888dbab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119038134"
---
# <a name="clipping-output"></a>Saída de recorte

Depois que o usuário clica em Clip no menu, o aplicativo usa as coordenadas do retângulo criado pelo usuário para definir uma região de recorte. Depois de definir a região de recorte e selecioná-la no contexto do dispositivo do aplicativo, o aplicativo redesenha a imagem mapeada. O aplicativo executa essas tarefas, da seguinte forma.


```C++
// These variables are required for clipping.  
 
static POINT ptUpperLeft; 
static POINT ptLowerRight; 
static POINT aptRect[5]; 
static POINT ptTmp; 
static POINTS ptsTmp; 
static BOOL fDefineRegion; 
static BOOL fRegionExists; 
static HRGN hrgn; 
static RECT rctTmp; 
int i; 
 
case WM_COMMAND: 
    switch (wParam) 
    { 
 
    case IDM_CLIP: 
 
    hdc = GetDC(hwnd); 
 
    // Retrieve the application's client rectangle and paint  
    // with the default (white) brush.  
 
    GetClientRect(hwnd, &rctTmp); 
    FillRect(hdc, &rctTmp, GetStockObject(WHITE_BRUSH)); 
 
    // Use the rect coordinates to define a clipping region.  
 
    hrgn = CreateRectRgn(aptRect[0].x, aptRect[0].y, 
        aptRect[2].x, aptRect[2].y); 
    SelectClipRgn(hdc, hrgn); 
 
    // Transfer (draw) the bitmap into the clipped rectangle.  
 
    BitBlt(hdc, 
       0, 0, 
       bmp.bmWidth, bmp.bmHeight, 
       hdcCompatible, 
       0, 0, 
       SRCCOPY); 
 
    ReleaseDC(hwnd, hdc); 
    break; 
    }
```



 

 



