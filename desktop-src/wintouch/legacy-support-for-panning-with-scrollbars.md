---
title: Suporte herdado para movimento panorâmico com barras de rolagem
description: Esta seção descreve o suporte para movimento panorâmico usando barras de rolagem em aplicativos baseados no Windows.
ms.assetid: a8906b48-b804-4f3a-bb9b-dc94b632e2f7
keywords:
- Windows Touch, suporte herdado
- movimento panorâmico com barras de rolagem
- Windows Touch, panorâmica com barras de rolagem
- Windows Touch, barras de rolagem
- barras de rolagem, panorâmica
- barras de rolagem, suporte herdado
- Toque do Windows, gestos
- gestos, movimento panorâmico com barras de rolagem
- Windows Touch, movimentos
- movimentos, panorâmicas com barras de rolagem
- movimentos, desabilitando
- Windows Touch, mensagens de roda do mouse
- mensagens de roda do mouse
- Windows Touch, personalizando o movimento panorâmico
- panorâmica, barras de rolagem
- visão panorâmica, suporte herdado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57f6b9dd47821205a6aa5b6f07e5053e31597358
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104564720"
---
# <a name="legacy-support-for-panning-with-scroll-bars"></a><span data-ttu-id="0160d-119">Suporte herdado para movimento panorâmico com barras de rolagem</span><span class="sxs-lookup"><span data-stu-id="0160d-119">Legacy Support for Panning with Scroll Bars</span></span>

<span data-ttu-id="0160d-120">Esta seção descreve o suporte para movimento panorâmico usando barras de rolagem em aplicativos baseados no Windows.</span><span class="sxs-lookup"><span data-stu-id="0160d-120">This section describes support for panning using scroll bars in Windows-based applications.</span></span>

<span data-ttu-id="0160d-121">No Windows 7, gestos de panorâmica geram \_ \* mensagens de rolagem do WM para habilitar o suporte herdado para movimento panorâmico.</span><span class="sxs-lookup"><span data-stu-id="0160d-121">In Windows 7, panning gestures generate WM\_\*SCROLL messages to enable legacy support for panning.</span></span> <span data-ttu-id="0160d-122">Como seus aplicativos podem não dar suporte a todas as \_ \* mensagens de rolagem do WM, o movimento panorâmico pode não funcionar corretamente.</span><span class="sxs-lookup"><span data-stu-id="0160d-122">Because your applications may not support all of the WM\_\*SCROLL messages, panning may not work correctly.</span></span> <span data-ttu-id="0160d-123">Este tópico descreve as etapas que você deve seguir para garantir que a experiência de panorâmica herdada em aplicativos funcione conforme os usuários esperam.</span><span class="sxs-lookup"><span data-stu-id="0160d-123">This topic describes the steps you must take to ensure that the legacy panning experience in applications functions as users expect.</span></span>

## <a name="overview"></a><span data-ttu-id="0160d-124">Visão geral</span><span class="sxs-lookup"><span data-stu-id="0160d-124">Overview</span></span>

<span data-ttu-id="0160d-125">As seções a seguir explicam como habilitar a experiência de panorâmica herdada:</span><span class="sxs-lookup"><span data-stu-id="0160d-125">The following sections explain how to enable the legacy panning experience:</span></span>

-   <span data-ttu-id="0160d-126">Crie um aplicativo com barras de rolagem.</span><span class="sxs-lookup"><span data-stu-id="0160d-126">Create an application with scroll bars.</span></span>
-   <span data-ttu-id="0160d-127">Desabilitar movimentos.</span><span class="sxs-lookup"><span data-stu-id="0160d-127">Disable flicks.</span></span>
-   <span data-ttu-id="0160d-128">Personalize a experiência de panorâmica.</span><span class="sxs-lookup"><span data-stu-id="0160d-128">Customize the panning experience.</span></span>

## <a name="create-an-application-with-scroll-bars"></a><span data-ttu-id="0160d-129">Criar um aplicativo com barras de rolagem</span><span class="sxs-lookup"><span data-stu-id="0160d-129">Create an Application with Scroll Bars</span></span>

<span data-ttu-id="0160d-130">Inicie um novo projeto Win32 usando o assistente de Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0160d-130">Start a new Win32 project using the Microsoft Visual Studio wizard.</span></span> <span data-ttu-id="0160d-131">Verifique se o tipo de aplicativo está definido para o aplicativo do Windows.</span><span class="sxs-lookup"><span data-stu-id="0160d-131">Make sure the application type is set to the Windows application.</span></span> <span data-ttu-id="0160d-132">Você não precisa habilitar o suporte para o Active Template Library (ATL).</span><span class="sxs-lookup"><span data-stu-id="0160d-132">You don't need to enable support for the Active Template Library (ATL).</span></span> <span data-ttu-id="0160d-133">A imagem a seguir mostra qual será a aparência do seu projeto depois de você iniciá-lo.</span><span class="sxs-lookup"><span data-stu-id="0160d-133">The following image shows what your project will look like after you have started it.</span></span>

![captura de tela mostrando uma janela sem barras de rolagem](images/gpd-1.png)

<span data-ttu-id="0160d-135">Em seguida, habilite as barras de rolagem na imagem.</span><span class="sxs-lookup"><span data-stu-id="0160d-135">Next, enable scroll bars on the image.</span></span> <span data-ttu-id="0160d-136">Altere o código de criação da janela em **InitInstance** para que a chamada de função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) crie uma janela com barras de rolagem.</span><span class="sxs-lookup"><span data-stu-id="0160d-136">Change the window creation code in **InitInstance** so that the [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) function call creates a window with scroll bars.</span></span> <span data-ttu-id="0160d-137">O código a seguir mostra como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="0160d-137">The following code shows how to do this.</span></span>


```C++
   hWnd = CreateWindow(
      szWindowClass, 
      szTitle, 
      WS_OVERLAPPEDWINDOW | WS_VSCROLL,  // style
      200,                               // x
      200,                               // y
      550,                               // width
      300,                               // height
      NULL,
      NULL,
      hInstance,
      NULL
    );  
```



<span data-ttu-id="0160d-138">Depois de alterar o código de criação da janela, seu aplicativo terá uma barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="0160d-138">After you have changed the window creation code, your application will have a scroll bar.</span></span> <span data-ttu-id="0160d-139">A imagem a seguir mostra como o aplicativo pode parecer com esse ponto.</span><span class="sxs-lookup"><span data-stu-id="0160d-139">The following image shows how the application might look at this point.</span></span>

![captura de tela mostrando uma janela com uma barra de rolagem vertical, mas sem texto](images/gpd-2.png)

<span data-ttu-id="0160d-141">Depois de alterar o código de criação da janela, adicione um objeto de barra de rolagem ao seu aplicativo e algum texto para rolar.</span><span class="sxs-lookup"><span data-stu-id="0160d-141">After you have changed the window creation code, add a scroll bar object to your application and some text to scroll.</span></span> <span data-ttu-id="0160d-142">Coloque o código a seguir na parte superior do método **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="0160d-142">Place the following code into the top of the **WndProc** method.</span></span>


```C++
    TEXTMETRIC tm;     
    SCROLLINFO si; 
     
    // These variables are required to display text. 
    static int xClient;     // width of client area 
    static int yClient;     // height of client area 
    static int xClientMax;  // maximum width of client area 
     
    static int xChar;       // horizontal scrolling unit 
    static int yChar;       // vertical scrolling unit 
    static int xUpper;      // average width of uppercase letters 
     
    static int xPos;        // current horizontal scrolling position 
    static int yPos;        // current vertical scrolling position 
     
    int i;                  // loop counter 
    int x, y;               // horizontal and vertical coordinates
     
    int FirstLine;          // first line in the invalidated area 
    int LastLine;           // last line in the invalidated area 
    HRESULT hr;
    int abcLength = 0;  // length of an abc[] item

    int lines = 0;

    // Create an array of lines to display. 
    static const int LINES=28;
    static LPCWSTR abc[] = { 
       L"anteater",  L"bear",      L"cougar", 
       L"dingo",     L"elephant",  L"falcon", 
       L"gazelle",   L"hyena",     L"iguana", 
       L"jackal",    L"kangaroo",  L"llama", 
       L"moose",     L"newt",      L"octopus", 
       L"penguin",   L"quail",     L"rat", 
       L"squid",     L"tortoise",  L"urus", 
       L"vole",      L"walrus",    L"xylophone", 
       L"yak",       L"zebra",
       L"This line contains words, but no character. Go figure.",
       L""
     };        
```



<span data-ttu-id="0160d-143">Em seguida, implemente a lógica do aplicativo para configurar os cálculos de texto para métricas de texto.</span><span class="sxs-lookup"><span data-stu-id="0160d-143">Next, implement the application logic for configuring the text calculations for text metrics.</span></span> <span data-ttu-id="0160d-144">O código a seguir deve substituir o caso de **\_ criação** existente do WM na função **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="0160d-144">The following code should replace the existing **WM\_CREATE** case in the **WndProc** function.</span></span>


```C++
    case WM_CREATE : 
        // Get the handle to the client area's device context. 
        hdc = GetDC (hWnd); 
 
        // Extract font dimensions from the text metrics. 
        GetTextMetrics (hdc, &tm); 
        xChar = tm.tmAveCharWidth; 
        xUpper = (tm.tmPitchAndFamily & 1 ? 3 : 2) * xChar/2; 
        yChar = tm.tmHeight + tm.tmExternalLeading; 
 
        // Free the device context. 
        ReleaseDC (hWnd, hdc); 
 
        // Set an arbitrary maximum width for client area. 
        // (xClientMax is the sum of the widths of 48 average 
        // lowercase letters and 12 uppercase letters.) 
        xClientMax = 48 * xChar + 12 * xUpper; 
 
        return 0;
```



<span data-ttu-id="0160d-145">Em seguida, implemente a lógica do aplicativo para recálculo do bloco de texto quando a janela for redimensionada.</span><span class="sxs-lookup"><span data-stu-id="0160d-145">Next, implement the application logic for recalculation of the text block when the window is resized.</span></span> <span data-ttu-id="0160d-146">O código a seguir deve ser colocado na chave de mensagem em **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="0160d-146">The following code should be placed into the message switch in **WndProc**.</span></span>


```C++
    case WM_SIZE: 
 
        // Retrieve the dimensions of the client area. 
        yClient = HIWORD (lParam); 
        xClient = LOWORD (lParam); 
 
        // Set the vertical scrolling range and page size
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = LINES - 1; 
        si.nPage  = yClient / yChar; 
        SetScrollInfo(hWnd, SB_VERT, &si, TRUE); 
 
        // Set the horizontal scrolling range and page size. 
        si.cbSize = sizeof(si); 
        si.fMask  = SIF_RANGE | SIF_PAGE; 
        si.nMin   = 0; 
        si.nMax   = 2 + xClientMax / xChar; 
        si.nPage  = xClient / xChar; 
        SetScrollInfo(hWnd, SB_HORZ, &si, TRUE);            
        return 0;
```



<span data-ttu-id="0160d-147">Em seguida, implemente a lógica do aplicativo para mensagens de rolagem vertical.</span><span class="sxs-lookup"><span data-stu-id="0160d-147">Next, implement the application logic for vertical scroll messages.</span></span> <span data-ttu-id="0160d-148">O código a seguir deve ser colocado na chave de mensagem em **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="0160d-148">The following code should be placed into the message switch in **WndProc**.</span></span>


```C++
        case WM_VSCROLL:
         // Get all the vertical scroll bar information
         si.cbSize = sizeof (si);
         si.fMask  = SIF_ALL;
         GetScrollInfo (hWnd, SB_VERT, &si);
         // Save the position for comparison later on
         yPos = si.nPos;
         switch (LOWORD (wParam))
         {
         // user clicked the HOME keyboard key
         case SB_TOP:
             si.nPos = si.nMin;
             break;
              
         // user clicked the END keyboard key
         case SB_BOTTOM:
             si.nPos = si.nMax;
             break;
              
         // user clicked the top arrow
         case SB_LINEUP:
             si.nPos -= 1;
             break;
              
         // user clicked the bottom arrow
         case SB_LINEDOWN:
             si.nPos += 1;
             break;
              
         // user clicked the scroll bar shaft above the scroll box
         case SB_PAGEUP:
             si.nPos -= si.nPage;
             break;
              
         // user clicked the scroll bar shaft below the scroll box
         case SB_PAGEDOWN:
             si.nPos += si.nPage;
             break;
              
         // user dragged the scroll box
         case SB_THUMBTRACK:
             si.nPos = si.nTrackPos;
             break;

         // user positioned the scroll box
         // This message is the one used by Windows Touch
         case SB_THUMBPOSITION:
             si.nPos = HIWORD(wParam);
             break;
                            
         default:
              break; 
         }
         // Set the position and then retrieve it.  Due to adjustments
         //   by Windows it may not be the same as the value set.
         si.fMask = SIF_POS;
         SetScrollInfo (hWnd, SB_VERT, &si, TRUE);
         GetScrollInfo (hWnd, SB_VERT, &si);
         // If the position has changed, scroll window and update it
         if (si.nPos != yPos)
         {                    
          ScrollWindow(hWnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
          UpdateWindow (hWnd);
         }
         break;
```



<span data-ttu-id="0160d-149">Em seguida, atualize o código para redesenhar a janela.</span><span class="sxs-lookup"><span data-stu-id="0160d-149">Next, update the code to redraw the window.</span></span> <span data-ttu-id="0160d-150">O código a seguir deve substituir o caso de **\_ pintura** padrão do WM em **WndProc**.</span><span class="sxs-lookup"><span data-stu-id="0160d-150">The following code should replace the default **WM\_PAINT** case in **WndProc**.</span></span>


```C++
    case WM_PAINT:
         // Prepare the window for painting
         hdc = BeginPaint (hWnd, &ps);
         // Get vertical scroll bar position
         si.cbSize = sizeof (si);
         si.fMask  = SIF_POS;
         GetScrollInfo (hWnd, SB_VERT, &si);
         yPos = si.nPos;
         // Get horizontal scroll bar position
         GetScrollInfo (hWnd, SB_HORZ, &si);
         xPos = si.nPos;
         // Find painting limits
         FirstLine = max (0, yPos + ps.rcPaint.top / yChar);
         LastLine = min (LINES - 1, yPos + ps.rcPaint.bottom / yChar);
         
         
         
         for (i = FirstLine; i <= LastLine; i++)         
         {
              x = xChar * (1 - xPos);
              y = yChar * (i - yPos);
              
              // Note that "55" in the following depends on the 
              // maximum size of an abc[] item.
              //
              abcLength = wcslen(abc[i]);
              hr = S_OK;
              if ((FAILED(hr)))
              {
                 MessageBox(hWnd, L"err", L"err", NULL);
              }else{
                  TextOut(hdc, x, y, abc[i], abcLength);
              }
              
         }
         // Indicate that painting is finished
         EndPaint (hWnd, &ps);
         return 0;
```



<span data-ttu-id="0160d-151">Agora, quando você cria e executa seu aplicativo, ele deve ter o texto clichê e uma barra de rolagem vertical.</span><span class="sxs-lookup"><span data-stu-id="0160d-151">Now when you build and run your application, it should have the boilerplate text and a vertical scroll bar.</span></span> <span data-ttu-id="0160d-152">A imagem a seguir mostra como o seu aplicativo pode parecer.</span><span class="sxs-lookup"><span data-stu-id="0160d-152">The following image shows how your application might look.</span></span>

![captura de tela mostrando uma janela com uma barra de rolagem vertical e texto](images/gpd-3.png)

## <a name="disable-flicks"></a><span data-ttu-id="0160d-154">Desabilitar movimentos</span><span class="sxs-lookup"><span data-stu-id="0160d-154">Disable Flicks</span></span>

<span data-ttu-id="0160d-155">Para melhorar a experiência de panorâmica em seu aplicativo, você deve desligar os movimentos.</span><span class="sxs-lookup"><span data-stu-id="0160d-155">To improve the panning experience in your application, you should turn off flicks.</span></span> <span data-ttu-id="0160d-156">Para fazer isso, defina as propriedades da janela no valor de *HWND* quando ele for inicializado.</span><span class="sxs-lookup"><span data-stu-id="0160d-156">To do this, set window properties on the *hWnd* value when it is initialized.</span></span> <span data-ttu-id="0160d-157">Os valores usados para movimentos são armazenados no cabeçalho tpcshrd. h, que também deve ser incluído.</span><span class="sxs-lookup"><span data-stu-id="0160d-157">The values used for flicks are stored in the tpcshrd.h header, which also must be included.</span></span> <span data-ttu-id="0160d-158">O código a seguir deve ser colocado em suas diretivas include e na função **InitInstance** depois de você ter criado o *HWND*.</span><span class="sxs-lookup"><span data-stu-id="0160d-158">The following code should be placed in your include directives and in the **InitInstance** function after you have created your *hWnd*.</span></span>

> [!Note]  
> <span data-ttu-id="0160d-159">Isso é útil para aplicativos que exigem comentários imediatos sobre um evento de toque ou caneta, em vez de testar por um limite de tempo ou de distância.</span><span class="sxs-lookup"><span data-stu-id="0160d-159">This is useful for applications that require immediate feedback on a touch or pen down event instead of testing for a time or distance threshold.</span></span>

 


```C++
#include <tpcshrd.h>
```




```C++
[...]
BOOL InitInstance(HINSTANCE hInstance, int nCmdShow){
[...]
  
```




```C++
   const DWORD_PTR dwHwndTabletProperty = 
    TABLET_DISABLE_PRESSANDHOLD | // disables press and hold (right-click) gesture
    TABLET_DISABLE_PENTAPFEEDBACK | // disables UI feedback on pen up (waves)
    TABLET_DISABLE_PENBARRELFEEDBACK | // disables UI feedback on pen button down (circle)
    TABLET_DISABLE_FLICKS; // disables pen flicks (back, forward, drag down, drag up)
   
   SetProp(hWnd, MICROSOFT_TABLETPENSERVICE_PROPERTY, reinterpret_cast<HANDLE>(dwHwndTabletProperty));
```



## <a name="customize-the-panning-experience"></a><span data-ttu-id="0160d-160">Personalizar a experiência de panorâmica</span><span class="sxs-lookup"><span data-stu-id="0160d-160">Customize the Panning Experience</span></span>

<span data-ttu-id="0160d-161">Você pode querer uma experiência de panorâmica diferente do que o Windows 7 oferece por padrão.</span><span class="sxs-lookup"><span data-stu-id="0160d-161">You might want a different panning experience than Windows 7 offers by default.</span></span> <span data-ttu-id="0160d-162">Para melhorar a experiência de panorâmica, você deve adicionar o manipulador para a mensagem de [**\_ gesto do WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="0160d-162">To improve the panning experience, you must add the handler for the [**WM\_GESTURE**](wm-gesture.md) message.</span></span> <span data-ttu-id="0160d-163">Para obter mais informações, consulte [aprimorando a experiência de panorâmica Single-Finger](improving-the-single-finger-panning-experience.md).</span><span class="sxs-lookup"><span data-stu-id="0160d-163">For more information, see [Improving the Single-Finger Panning Experience](improving-the-single-finger-panning-experience.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0160d-164">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0160d-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0160d-165">Gestos de toque do Windows</span><span class="sxs-lookup"><span data-stu-id="0160d-165">Windows Touch Gestures</span></span>](guide-multi-touch-gestures.md)
</dt> </dl>

 

 