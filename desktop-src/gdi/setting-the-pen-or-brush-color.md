---
description: O exemplo a seguir mostra como um aplicativo pode alterar a cor da caneta DC usando a função GetStockObject ou SetDCPenColor e as funções SetDCBrushColor.
ms.assetid: d1be1db8-e6b6-4d60-8a4a-ce218f8d52fc
title: Definindo a caneta ou cor do pincel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b5d095a41dc01bcf2023ddb431679cce01f7c60a2110ef3faf078411334aaf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965226"
---
# <a name="setting-the-pen-or-brush-color"></a>Definindo a caneta ou cor do pincel

O exemplo a seguir mostra como um aplicativo pode alterar a cor da caneta DC usando a função [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) ou [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor) e as funções [**SetDCBrushColor.**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)


```C++
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {
    case WM_COMMAND:
        wmId    = LOWORD(wParam);
        wmEvent = HIWORD(wParam);
        // Parse the menu selections:
        switch (wmId)
        {
        case IDM_ABOUT:
            DialogBox(hInst, MAKEINTRESOURCE(IDD_ABOUTBOX), hWnd, About);
            break;
        case IDM_EXIT:
            DestroyWindow(hWnd);
            break;
        default:
            return DefWindowProc(hWnd, message, wParam, lParam);
        }
        break;
    case WM_PAINT:
        
        {    
            hdc = BeginPaint(hWnd, &ps);
        //    Initializing original object
            HGDIOBJ original = NULL;
        
        //    Saving the original object
            original = SelectObject(hdc,GetStockObject(DC_PEN));

        //    Rectangle function is defined as...
        //    BOOL Rectangle(hdc, xLeft, yTop, yRight, yBottom);
    
        //    Drawing a rectangle with just a black pen
        //    The black pen object is selected and sent to the current device context
        //  The default brush is WHITE_BRUSH
            SelectObject(hdc, GetStockObject(BLACK_PEN));
            Rectangle(hdc,0,0,200,200);

        //    Select DC_PEN so you can change the color of the pen with
        //    COLORREF SetDCPenColor(HDC hdc, COLORREF color)
            SelectObject(hdc, GetStockObject(DC_PEN));

        //    Select DC_BRUSH so you can change the brush color from the 
        //    default WHITE_BRUSH to any other color
            SelectObject(hdc, GetStockObject(DC_BRUSH));

        //    Set the DC Brush to Red
        //    The RGB macro is declared in "Windowsx.h"
            SetDCBrushColor(hdc, RGB(255,0,0));

        //    Set the Pen to Blue
            SetDCPenColor(hdc, RGB(0,0,255));
        
        //    Drawing a rectangle with the current Device Context    
            Rectangle(hdc,100,300,200,400);

        //    Changing the color of the brush to Green
            SetDCBrushColor(hdc, RGB(0,255,0));
            Rectangle(hdc,300,150,500,300);

        //    Restoring the original object
            SelectObject(hdc,original);

        // It is not necessary to call DeleteObject to delete stock objects.
        }
        
        break;
    case WM_DESTROY:
        PostQuitMessage(0);
        break;
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;
}
```



 

 



