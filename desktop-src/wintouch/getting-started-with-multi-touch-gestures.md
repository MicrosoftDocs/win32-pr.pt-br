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
# <a name="getting-started-with-windows-touch-gestures"></a><span data-ttu-id="4e68d-107">Introdução com gestos de toque do Windows</span><span class="sxs-lookup"><span data-stu-id="4e68d-107">Getting Started with Windows Touch Gestures</span></span>

<span data-ttu-id="4e68d-108">Esta seção descreve as etapas básicas para usar gestos do multitoque.</span><span class="sxs-lookup"><span data-stu-id="4e68d-108">This section describes the basic steps for using multitouch gestures.</span></span>

<span data-ttu-id="4e68d-109">As etapas a seguir normalmente são executadas ao usar gestos do Windows Touch:</span><span class="sxs-lookup"><span data-stu-id="4e68d-109">The following steps are typically performed when using Windows Touch gestures:</span></span>

1.  <span data-ttu-id="4e68d-110">Configure uma janela para o recebimento de gestos.</span><span class="sxs-lookup"><span data-stu-id="4e68d-110">Set up a window for receiving gestures.</span></span>
2.  <span data-ttu-id="4e68d-111">Manipule as mensagens de gesto.</span><span class="sxs-lookup"><span data-stu-id="4e68d-111">Handle the gesture messages.</span></span>
3.  <span data-ttu-id="4e68d-112">Interprete as mensagens de gesto.</span><span class="sxs-lookup"><span data-stu-id="4e68d-112">Interpret the gesture messages.</span></span>

## <a name="setting-up-a-window-to-receive-gestures"></a><span data-ttu-id="4e68d-113">Configurando uma janela para receber gestos</span><span class="sxs-lookup"><span data-stu-id="4e68d-113">Setting up a Window to Receive Gestures</span></span>

<span data-ttu-id="4e68d-114">Por padrão, você recebe mensagens de [**\_ gesto do WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="4e68d-114">By default, you receive [**WM\_GESTURE**](wm-gesture.md) messages.</span></span>

> [!Note]  
> <span data-ttu-id="4e68d-115">Se você chamar [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), você deixará de receber mensagens de [**\_ gesto do WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="4e68d-115">If you call [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow), you will stop receiving [**WM\_GESTURE**](wm-gesture.md) messages.</span></span> <span data-ttu-id="4e68d-116">Se você não estiver recebendo mensagens de **\_ gesto do WM** , certifique-se de que você não chamou **RegisterTouchWindow**.</span><span class="sxs-lookup"><span data-stu-id="4e68d-116">If you are not receiving **WM\_GESTURE** messages, make sure that you haven't called **RegisterTouchWindow**.</span></span>

 

<span data-ttu-id="4e68d-117">O código a seguir mostra uma implementação simples de InitInstance.</span><span class="sxs-lookup"><span data-stu-id="4e68d-117">The following code shows a simple InitInstance implementation.</span></span>


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



## <a name="handling-gesture-messages"></a><span data-ttu-id="4e68d-118">Manipulando mensagens de gesto</span><span class="sxs-lookup"><span data-stu-id="4e68d-118">Handling Gesture Messages</span></span>

<span data-ttu-id="4e68d-119">Semelhante ao tratamento de mensagens de entrada do Windows Touch, você pode lidar com mensagens de gesto de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="4e68d-119">Similar to handling Windows Touch input messages, you can handle gesture messages in many ways.</span></span> <span data-ttu-id="4e68d-120">Se você estiver usando o Win32, poderá verificar a mensagem [**de \_ gesto do WM**](wm-gesture.md) em WndProc.</span><span class="sxs-lookup"><span data-stu-id="4e68d-120">If you are using Win32, you can check for the [**WM\_GESTURE**](wm-gesture.md) message in WndProc.</span></span> <span data-ttu-id="4e68d-121">Se você estiver criando outro tipo de aplicativo, poderá adicionar a mensagem **de \_ gesto do WM** ao mapa de mensagens e, em seguida, implementar um manipulador personalizado.</span><span class="sxs-lookup"><span data-stu-id="4e68d-121">If you are creating another type of application, you can add the **WM\_GESTURE** message to the message map and then implement a custom handler.</span></span>

<span data-ttu-id="4e68d-122">O código a seguir mostra como as mensagens de gesto podem ser manipuladas.</span><span class="sxs-lookup"><span data-stu-id="4e68d-122">The following code shows how gesture messages could be handled.</span></span>


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



## <a name="interpreting-the-gesture-messages"></a><span data-ttu-id="4e68d-123">Interpretando as mensagens de gesto</span><span class="sxs-lookup"><span data-stu-id="4e68d-123">Interpreting the Gesture Messages</span></span>

<span data-ttu-id="4e68d-124">A função [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) é usada para interpretar uma mensagem de gesto em uma estrutura que descreve o gesto.</span><span class="sxs-lookup"><span data-stu-id="4e68d-124">The [**GetGestureInfo**](/windows/desktop/api/winuser/nf-winuser-getgestureinfo) function is used to interpret a gesture message into a structure describing the gesture.</span></span> <span data-ttu-id="4e68d-125">A estrutura, [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo), tem informações sobre o gesto, como o local onde o gesto foi executado e o tipo de gesto.</span><span class="sxs-lookup"><span data-stu-id="4e68d-125">The structure, [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo), has information about the gesture such as the location where the gesture was performed and the type of gesture.</span></span> <span data-ttu-id="4e68d-126">O código a seguir mostra como você pode recuperar e interpretar uma mensagem de gesto.</span><span class="sxs-lookup"><span data-stu-id="4e68d-126">The following code shows how you can retrieve and interpret a gesture message.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="4e68d-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4e68d-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e68d-128">Gestos de toque do Windows</span><span class="sxs-lookup"><span data-stu-id="4e68d-128">Windows Touch Gestures</span></span>](guide-multi-touch-gestures.md)
</dt> </dl>

 

 




