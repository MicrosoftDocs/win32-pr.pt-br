---
title: Melhorando a experiência de panorâmica Single-Finger
description: Se você criar um aplicativo direcionado ao Windows Touch, ele fornecerá automaticamente o suporte básico de panorâmica. No entanto, você pode usar a mensagem de gesto do WM \_ para fornecer suporte aprimorado para o movimento panorâmico com um único dedo.
ms.assetid: eb01a6df-9969-44d1-a657-4f83fb0b67cb
keywords:
- Windows Touch, panorama de um único dedo
- Windows Touch, panorâmica
- Windows Touch, barras de rolagem
- Windows Touch, movimentos
- Toque do Windows, mensagens de Pan do gesto
- Toque do Windows, comentários de limite
- movimento panorâmico com um único dedo
- movimento panorâmico, um único dedo
- panorâmica, comentários de limite
- barras de rolagem, movimento panorâmico de dedo único
- movimentos, panorâmica de dedo único
- barras de rolagem, desabilitando
- movimentos, desabilitando
- gestos, mensagens de panorâmica do gesto
- panorâmica, mensagens de panorâmica do gesto
- Comentários de limite, movimento panorâmico de um único dedo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9081903600918485f1e3241a02c01b5438c1aae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641279"
---
# <a name="improving-the-single-finger-panning-experience"></a><span data-ttu-id="e2075-120">Melhorando a experiência de panorâmica Single-Finger</span><span class="sxs-lookup"><span data-stu-id="e2075-120">Improving the Single-Finger Panning Experience</span></span>

<span data-ttu-id="e2075-121">Se você criar um aplicativo direcionado ao Windows Touch, ele fornecerá automaticamente o suporte básico de panorâmica.</span><span class="sxs-lookup"><span data-stu-id="e2075-121">If you build an application that targets Windows Touch, it automatically provides basic panning support.</span></span> <span data-ttu-id="e2075-122">No entanto, você pode usar a mensagem de [**\_ gesto do WM**](wm-gesture.md) para fornecer suporte aprimorado para o movimento panorâmico com um único dedo.</span><span class="sxs-lookup"><span data-stu-id="e2075-122">However, you can use the [**WM\_GESTURE**](wm-gesture.md) message to provide enhanced support for single-finger panning.</span></span>

## <a name="overview"></a><span data-ttu-id="e2075-123">Visão geral</span><span class="sxs-lookup"><span data-stu-id="e2075-123">Overview</span></span>

<span data-ttu-id="e2075-124">Para melhorar a experiência de panorâmica de um único dedo, use estas etapas, conforme explicado nas seções subsequentes deste tópico:</span><span class="sxs-lookup"><span data-stu-id="e2075-124">To improve the single-finger panning experience, use these steps, as explained in subsequent sections of this topic:</span></span>

-   <span data-ttu-id="e2075-125">Crie um aplicativo com barras de rolagem e com movimentos desabilitados.</span><span class="sxs-lookup"><span data-stu-id="e2075-125">Create an application with scroll bars and with flicks disabled.</span></span>
-   <span data-ttu-id="e2075-126">Adicione suporte para mensagens de Pan de gesto.</span><span class="sxs-lookup"><span data-stu-id="e2075-126">Add support for gesture pan messages.</span></span>
-   <span data-ttu-id="e2075-127">Habilitar o retorno.</span><span class="sxs-lookup"><span data-stu-id="e2075-127">Enable bounce.</span></span>

## <a name="create-an-application-with-scroll-bars-and-with-flicks-disabled"></a><span data-ttu-id="e2075-128">Criar um aplicativo com barras de rolagem e com movimentos desabilitados</span><span class="sxs-lookup"><span data-stu-id="e2075-128">Create an Application with Scroll Bars and with Flicks Disabled</span></span>

<span data-ttu-id="e2075-129">Antes de começar, você deve criar um aplicativo com barras de rolagem.</span><span class="sxs-lookup"><span data-stu-id="e2075-129">Before you begin, you must create an application with scroll bars.</span></span> <span data-ttu-id="e2075-130">A seção [suporte herdado para panorâmica com barras de rolagem](legacy-support-for-panning-with-scrollbars.md) explica esse processo.</span><span class="sxs-lookup"><span data-stu-id="e2075-130">The section [Legacy Support for Panning with Scrollbars](legacy-support-for-panning-with-scrollbars.md) explains this process.</span></span> <span data-ttu-id="e2075-131">Se você quiser começar com o conteúdo de exemplo, vá para essa seção e crie um aplicativo com barras de rolagem e, em seguida, desabilite os movimentos.</span><span class="sxs-lookup"><span data-stu-id="e2075-131">If you want to start with the example content, go to that section and create an application with scroll bars and then disable flicks.</span></span> <span data-ttu-id="e2075-132">Se você já tiver um aplicativo com barras de rolagem em funcionamento, desabilite os movimentos conforme descrito na seção.</span><span class="sxs-lookup"><span data-stu-id="e2075-132">If you already have an application with functioning scroll bars, disable flicks as described in that section.</span></span>

## <a name="add-custom-panning-support-for-gesture-pan-messages"></a><span data-ttu-id="e2075-133">Adicionar suporte personalizado de panorâmica para mensagens de Pan de gesto</span><span class="sxs-lookup"><span data-stu-id="e2075-133">Add Custom Panning Support for Gesture Pan Messages</span></span>

<span data-ttu-id="e2075-134">Para dar suporte a mensagens de Pan de gesto, você deve tratá-las no método **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="e2075-134">To support gesture pan messages, you must handle them in the **WndProc** method.</span></span> <span data-ttu-id="e2075-135">As mensagens de gesto são usadas para determinar os deltas horizontais e verticais para mensagens de Pan.</span><span class="sxs-lookup"><span data-stu-id="e2075-135">The gesture messages are used to determine horizontal and vertical deltas for pan messages.</span></span> <span data-ttu-id="e2075-136">Os deltas são usados para atualizar o objeto da barra de rolagem, que atualiza a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="e2075-136">The deltas are used to update the scroll bar object, which updates the user interface.</span></span>

<span data-ttu-id="e2075-137">Primeiro, atualize as configurações de versão do Windows no arquivo targetver. h para habilitar o Windows Touch.</span><span class="sxs-lookup"><span data-stu-id="e2075-137">First, update the Windows version settings in the targetver.h file to enable Windows Touch.</span></span> <span data-ttu-id="e2075-138">O código a seguir mostra as várias configurações de versão do Windows que devem substituir as em targetver. h.</span><span class="sxs-lookup"><span data-stu-id="e2075-138">The following code shows the various Windows version settings that should replace those in targetver.h.</span></span>


```C++
#ifndef WINVER                  // Specifies that the minimum required platform is Windows Vista.
#define WINVER 0x0601           // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT            // Specifies that the minimum required platform is Windows Vista.
#define _WIN32_WINNT 0x0601     // Change this to the appropriate value to target other versions of Windows.
#endif
```



<span data-ttu-id="e2075-139">Em seguida, adicione o arquivo UXTheme. h ao seu projeto e adicione a biblioteca UxTheme. lib às dependências adicionais do seu projeto.</span><span class="sxs-lookup"><span data-stu-id="e2075-139">Next, add the UXTheme.h file to your project and add the uxtheme.lib library to the additional dependencies of your project.</span></span>


```C++
#include <uxtheme.h>
```



<span data-ttu-id="e2075-140">Em seguida, adicione as variáveis a seguir à parte superior da função **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="e2075-140">Next, add the following variables to the top of the **WndProc** function.</span></span> <span data-ttu-id="e2075-141">Eles serão usados em cálculos para movimento panorâmico.</span><span class="sxs-lookup"><span data-stu-id="e2075-141">These will be used in calculations for panning.</span></span>


```C++
// The following are used for the custom panning handler      
BOOL bResult = FALSE;

static int scale = 8;   // altering the scale value will change how fast the page scrolls
static int lastY = 0;   // used for panning calculations (initial / previous vertical position)
static int lastX = 0;   // used for panning calculations (initial / previous horizontal position)
GESTUREINFO gi;  
```



<span data-ttu-id="e2075-142">Em seguida, adicione o manipulador para a mensagem de [**\_ gesto do WM**](wm-gesture.md) para que as barras de rolagem sejam atualizadas com deltas com base nos gestos de panorâmica.</span><span class="sxs-lookup"><span data-stu-id="e2075-142">Next, add the handler for the [**WM\_GESTURE**](wm-gesture.md) message so that the scroll bars are updated with deltas based on panning gestures.</span></span> <span data-ttu-id="e2075-143">Isso lhe dá um controle muito mais refinado de panorâmica.</span><span class="sxs-lookup"><span data-stu-id="e2075-143">This gives you a much finer-grained control of panning.</span></span>

<span data-ttu-id="e2075-144">O código a seguir obtém a estrutura [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) do *lParam*, salva a última coordenada y da estrutura e determina a alteração na posição para atualizar o objeto da barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="e2075-144">The following code gets the [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) structure from the *lParam*, saves the last y-coordinate from the structure, and determines the change in position to update the scroll bar object.</span></span> <span data-ttu-id="e2075-145">O código a seguir deve ser colocado em sua instrução de comutador **WndProc** .</span><span class="sxs-lookup"><span data-stu-id="e2075-145">The following code should be placed in your **WndProc** switch statement.</span></span>


```C++
    case WM_GESTURE:        
        // Get all the vertial scroll bar information
        si.cbSize = sizeof (si);
        si.fMask  = SIF_ALL;
        GetScrollInfo (hWnd, SB_VERT, &si);
        yPos = si.nPos;

        ZeroMemory(&gi, sizeof(GESTUREINFO));
        gi.cbSize = sizeof(GESTUREINFO);
        bResult = GetGestureInfo((HGESTUREINFO)lParam, &gi);

        if (bResult){
            // now interpret the gesture            
            switch (gi.dwID){
                case GID_BEGIN:
                   lastY = gi.ptsLocation.y;
                   CloseGestureInfoHandle((HGESTUREINFO)lParam);
                   break;                     
                // A CUSTOM PAN HANDLER
                // COMMENT THIS CASE OUT TO ENABLE DEFAULT HANDLER BEHAVIOR
                case GID_PAN:                                                  
                    
                    si.nPos -= (gi.ptsLocation.y - lastY) / scale;

                    si.fMask = SIF_POS;
                    SetScrollInfo (hWnd, SB_VERT, &si, TRUE);
                    GetScrollInfo (hWnd, SB_VERT, &si);                                                        
                                               
                    yOverpan -= lastY - gi.ptsLocation.y;
                    lastY = gi.ptsLocation.y;
                     
                    if (gi.dwFlags & GF_BEGIN){
                        BeginPanningFeedback(hWnd);
                        yOverpan = 0;
                    } else if (gi.dwFlags & GF_END) {
                        EndPanningFeedback(hWnd, TRUE);
                        yOverpan = 0;
                    }
                           
                    if (si.nPos == si.nMin || si.nPos >= (si.nMax - si.nPage)){                    
                        // we reached the bottom / top, pan
                        UpdatePanningFeedback(hWnd, 0, yOverpan, gi.dwFlags & GF_INERTIA);
                    }
                    ScrollWindow(hWnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
                    UpdateWindow (hWnd);                    
                                        
                    return DefWindowProc(hWnd, message, lParam, wParam);
                case GID_ZOOM:
                   // Add Zoom handler 
                   return DefWindowProc(hWnd, message, lParam, wParam);
                default:
                   // You have encountered an unknown gesture
                   return DefWindowProc(hWnd, message, lParam, wParam);
             }          
        }else{
            DWORD dwErr = GetLastError();
            if (dwErr > 0){
                // something is wrong 
                // 87 indicates that you are probably using a bad
                // value for the gi.cbSize
            }
        } 
        return DefWindowProc (hWnd, message, wParam, lParam);
```



<span data-ttu-id="e2075-146">Agora, quando você executar o gesto de panorâmica em sua janela, verá o texto rolar com inércia.</span><span class="sxs-lookup"><span data-stu-id="e2075-146">Now, when you perform the pan gesture on your window, you will see the text scroll with inertia.</span></span> <span data-ttu-id="e2075-147">Neste ponto, talvez você queira alterar o texto para ter mais linhas, de modo que você possa explorar as grandes seções de texto de movimento panorâmico.</span><span class="sxs-lookup"><span data-stu-id="e2075-147">At this point, you might want to change the text to have more lines so that you can explore panning large sections of text.</span></span>

## <a name="boundary-feedback-in-wndproc"></a><span data-ttu-id="e2075-148">Comentários de limite em WndProc</span><span class="sxs-lookup"><span data-stu-id="e2075-148">Boundary Feedback in WndProc</span></span>

<span data-ttu-id="e2075-149">Os comentários de limite são um tipo de comentário visual dado aos usuários quando eles atingem o final de uma área de visão panorâmica.</span><span class="sxs-lookup"><span data-stu-id="e2075-149">Boundary feedback is a type of visual feedback given to users when they reach the end of a pannable area.</span></span> <span data-ttu-id="e2075-150">Ele é disparado pelo aplicativo quando um limite é atingido.</span><span class="sxs-lookup"><span data-stu-id="e2075-150">It is triggered by the application when a boundary is reached.</span></span> <span data-ttu-id="e2075-151">Na implementação de exemplo anterior da mensagem [**de \_ gesto do WM**](wm-gesture.md) , a condição final `(si.nPos == si.yPos)` do caso do **\_ gesto do WM** é usada para testar se você atingiu o final de uma região de visão panorâmica.</span><span class="sxs-lookup"><span data-stu-id="e2075-151">In the previous example implementation of the [**WM\_GESTURE**](wm-gesture.md) message, the end condition `(si.nPos == si.yPos)` from the **WM\_GESTURE** case is used to test that you have reached the end of a pannable region.</span></span> <span data-ttu-id="e2075-152">As variáveis a seguir são usadas para rastrear valores e erros de teste.</span><span class="sxs-lookup"><span data-stu-id="e2075-152">The following variables are used to track values and test errors.</span></span>


```C++
// The following are used for panning feedback (Window Bounce)
static int animCount = 0;
static DWORD dwErr   = 0;

static BOOL isOverpan  = FALSE;
static long xOverpan   = 0;
static long yOverpan   = 0;
```



<span data-ttu-id="e2075-153">O caso de gesto de panorâmica é atualizado para disparar comentários de limite.</span><span class="sxs-lookup"><span data-stu-id="e2075-153">The pan gesture case is updated to trigger boundary feedback.</span></span> <span data-ttu-id="e2075-154">O código a seguir ilustra o caso de **\_ Pan de GID** do manipulador de mensagens de [**\_ gesto do WM**](wm-gesture.md) .</span><span class="sxs-lookup"><span data-stu-id="e2075-154">The following code illustrates the **GID\_PAN** case from the [**WM\_GESTURE**](wm-gesture.md) message handler.</span></span>


```C++
                case GID_PAN:                                                  
                    
                    si.nPos -= (gi.ptsLocation.y - lastY) / scale;

                    si.fMask = SIF_POS;
                    SetScrollInfo (hWnd, SB_VERT, &si, TRUE);
                    GetScrollInfo (hWnd, SB_VERT, &si);                                                        
                                               
                    yOverpan -= lastY - gi.ptsLocation.y;
                    lastY = gi.ptsLocation.y;
                     
                    if (gi.dwFlags & GF_BEGIN){
                        BeginPanningFeedback(hWnd);
                        yOverpan = 0;
                    } else if (gi.dwFlags & GF_END) {
                        EndPanningFeedback(hWnd, TRUE);
                        yOverpan = 0;
                    }
                           
                    if (si.nPos == si.nMin){                    
                        // we reached the top, pan upwards in y direction
                        UpdatePanningFeedback(hWnd, 0, yOverpan, gi.dwFlags & GF_INERTIA);
                    }else if (si.nPos >= (si.nMax - si.nPage)){
                        // we reached the bottom, pan downwards in y direction
                        UpdatePanningFeedback(hWnd, 0, yOverpan, gi.dwFlags & GF_INERTIA);
                    }
                    ScrollWindow(hWnd, 0, yChar * (yPos - si.nPos), NULL, NULL);
                    UpdateWindow (hWnd);                    
                                        
                    return DefWindowProc(hWnd, message, lParam, wParam);
  
```



<span data-ttu-id="e2075-155">Agora, a janela do aplicativo deve ter comentários de limite quando um usuário se desloca sobre a parte inferior da região da barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="e2075-155">Now your application's window should have boundary feedback when a user pans past the bottom of the scroll bar region.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e2075-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e2075-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2075-157">Gestos de toque do Windows</span><span class="sxs-lookup"><span data-stu-id="e2075-157">Windows Touch Gestures</span></span>](guide-multi-touch-gestures.md)
</dt> <dt>

[<span data-ttu-id="e2075-158">**BeginPanningFeedback**</span><span class="sxs-lookup"><span data-stu-id="e2075-158">**BeginPanningFeedback**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-beginpanningfeedback)
</dt> <dt>

[<span data-ttu-id="e2075-159">**EndPanningFeedback**</span><span class="sxs-lookup"><span data-stu-id="e2075-159">**EndPanningFeedback**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-endpanningfeedback)
</dt> <dt>

[<span data-ttu-id="e2075-160">**UpdatePanningFeedback**</span><span class="sxs-lookup"><span data-stu-id="e2075-160">**UpdatePanningFeedback**</span></span>](/windows/win32/api/uxtheme/nf-uxtheme-updatepanningfeedback)
</dt> </dl>

 

 