---
title: Introdução com gestos de toque do Windows
description: Esta seção descreve as etapas básicas para usar gestos do multitoque.
ms.assetid: 0ffe222a-a0ac-498b-a4ca-85cfb1caba93
keywords:
- Toque do Windows, gestos
- Windows Touch, mensagens
- gestos, sobre
- gestos, mensagens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 506fee0667e6eb38469bda10af9ded0ea6d3439f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363703"
---
# <a name="getting-started-with-windows-touch-gestures"></a>Introdução com gestos de toque do Windows

Esta seção descreve as etapas básicas para usar gestos do multitoque.

As etapas a seguir normalmente são executadas ao usar gestos do Windows Touch:

1.  Configure uma janela para o recebimento de gestos.
2.  Manipule as mensagens de gesto.
3.  Interprete as mensagens de gesto.

## <a name="setting-up-a-window-to-receive-gestures"></a>Configurando uma janela para receber gestos

Por padrão, você recebe mensagens de [**\_ gesto do WM**](wm-gesture.md) .

> [!Note]  
> Se você chamar [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), você deixará de receber mensagens de [**\_ gesto do WM**](wm-gesture.md) . Se você não estiver recebendo mensagens de **\_ gesto do WM** , certifique-se de que você não chamou **RegisterTouchWindow**.

 

O código a seguir mostra uma implementação simples de InitInstance.


```C++
#include <windows.h>


BOOL InitInstance(HINSTANCE hInstance, int nCmdShow)
{
   HWND hWnd;

   hInst = hInstance; // Store instance handle in our global variable

   hWnd = CreateWindow(szWindowClass, szTitle, WS_OVERLAPPEDWINDOW,
      CW_USEDEFAULT, 0, CW_USEDEFAULT, 0, NULL, NULL, hInstance, NULL);

   if (!hWnd)
   {
      return FALSE;
   }

   ShowWindow(hWnd, nCmdShow);
   UpdateWindow(hWnd);

   return TRUE;
}
```



## <a name="handling-gesture-messages"></a>Manipulando mensagens de gesto

Semelhante ao tratamento de mensagens de entrada do Windows Touch, você pode lidar com mensagens de gesto de várias maneiras. Se você estiver usando o Win32, poderá verificar a mensagem [**de \_ gesto do WM**](wm-gesture.md) em WndProc. Se você estiver criando outro tipo de aplicativo, poderá adicionar a mensagem **de \_ gesto do WM** ao mapa de mensagens e, em seguida, implementar um manipulador personalizado.

O código a seguir mostra como as mensagens de gesto podem ser manipuladas.


```C++
LRESULT CALLBACK WndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    int wmId, wmEvent;
    PAINTSTRUCT ps;
    HDC hdc;

    switch (message)
    {    
    case WM_GESTURE:
            // Insert handler code here to interpret the gesture.            
            return DecodeGesture(hWnd, message, wParam, lParam);            
```



## <a name="interpreting-the-gesture-messages"></a>Interpretando as mensagens de gesto

A função [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) é usada para interpretar uma mensagem de gesto em uma estrutura que descreve o gesto. A estrutura, [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo), tem informações sobre o gesto, como o local onde o gesto foi executado e o tipo de gesto. O código a seguir mostra como você pode recuperar e interpretar uma mensagem de gesto.


```C++
  LRESULT DecodeGesture(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam){
    // Create a structure to populate and retrieve the extra message info.
    GESTUREINFO gi;  
    
    ZeroMemory(&gi, sizeof(GESTUREINFO));
    
    gi.cbSize = sizeof(GESTUREINFO);

    BOOL bResult  = GetGestureInfo((HGESTUREINFO)lParam, &gi);
    BOOL bHandled = FALSE;

    if (bResult){
        // now interpret the gesture
        switch (gi.dwID){
           case GID_ZOOM:
               // Code for zooming goes here     
               bHandled = TRUE;
               break;
           case GID_PAN:
               // Code for panning goes here
               bHandled = TRUE;
               break;
           case GID_ROTATE:
               // Code for rotation goes here
               bHandled = TRUE;
               break;
           case GID_TWOFINGERTAP:
               // Code for two-finger tap goes here
               bHandled = TRUE;
               break;
           case GID_PRESSANDTAP:
               // Code for roll over goes here
               bHandled = TRUE;
               break;
           default:
               // A gesture was not recognized
               break;
        }
    }else{
        DWORD dwErr = GetLastError();
        if (dwErr > 0){
            //MessageBoxW(hWnd, L"Error!", L"Could not retrieve a GESTUREINFO structure.", MB_OK);
        }
    }
    if (bHandled){
        return 0;
    }else{
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
  }
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gestos de toque do Windows](guide-multi-touch-gestures.md)
</dt> </dl>

 

 




