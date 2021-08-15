---
title: Melhorando a experiência de panorâmica Single-Finger
description: se você criar um aplicativo que tenha como alvo Windows toque, ele fornecerá automaticamente o suporte básico de panorâmica. No entanto, você pode usar a mensagem de gesto do WM \_ para fornecer suporte aprimorado para o movimento panorâmico com um único dedo.
ms.assetid: eb01a6df-9969-44d1-a657-4f83fb0b67cb
keywords:
- Windows Toque, panorâmica de dedo único
- Windows Toque, panorâmica
- Windows Toque, barras de rolagem
- Windows Toque, movimentos
- Windows Toque, mensagens de Pan do gesto
- Windows Toque, comentários de limite
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
ms.openlocfilehash: cf740d673e8bd2d2711238902d3de6c89d21a01fe330524b910db050011872f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118435439"
---
# <a name="improving-the-single-finger-panning-experience"></a>Melhorando a experiência de panorâmica Single-Finger

se você criar um aplicativo que tenha como alvo Windows toque, ele fornecerá automaticamente o suporte básico de panorâmica. No entanto, você pode usar a mensagem de [**\_ gesto do WM**](wm-gesture.md) para fornecer suporte aprimorado para o movimento panorâmico com um único dedo.

## <a name="overview"></a>Visão geral

Para melhorar a experiência de panorâmica de um único dedo, use estas etapas, conforme explicado nas seções subsequentes deste tópico:

-   Crie um aplicativo com barras de rolagem e com movimentos desabilitados.
-   Adicione suporte para mensagens de Pan de gesto.
-   Habilitar o retorno.

## <a name="create-an-application-with-scroll-bars-and-with-flicks-disabled"></a>Criar um aplicativo com barras de rolagem e com movimentos desabilitados

Antes de começar, você deve criar um aplicativo com barras de rolagem. A seção [suporte herdado para panorâmica com barras de rolagem](legacy-support-for-panning-with-scrollbars.md) explica esse processo. Se você quiser começar com o conteúdo de exemplo, vá para essa seção e crie um aplicativo com barras de rolagem e, em seguida, desabilite os movimentos. Se você já tiver um aplicativo com barras de rolagem em funcionamento, desabilite os movimentos conforme descrito na seção.

## <a name="add-custom-panning-support-for-gesture-pan-messages"></a>Adicionar suporte personalizado de panorâmica para mensagens de Pan de gesto

Para dar suporte a mensagens de Pan de gesto, você deve tratá-las no método **WndProc** . As mensagens de gesto são usadas para determinar os deltas horizontais e verticais para mensagens de Pan. Os deltas são usados para atualizar o objeto da barra de rolagem, que atualiza a interface do usuário.

primeiro, atualize as configurações de versão Windows no arquivo targetver. h para habilitar Windows Touch. o código a seguir mostra as várias configurações de versão Windows que devem substituir aquelas em targetver. h.


```C++
#ifndef WINVER                  // Specifies that the minimum required platform is Windows Vista.
#define WINVER 0x0601           // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT            // Specifies that the minimum required platform is Windows Vista.
#define _WIN32_WINNT 0x0601     // Change this to the appropriate value to target other versions of Windows.
#endif
```



Em seguida, adicione o arquivo UXTheme. h ao seu projeto e adicione a biblioteca UxTheme. lib às dependências adicionais do seu projeto.


```C++
#include <uxtheme.h>
```



Em seguida, adicione as variáveis a seguir à parte superior da função **WndProc** . Eles serão usados em cálculos para movimento panorâmico.


```C++
// The following are used for the custom panning handler      
BOOL bResult = FALSE;

static int scale = 8;   // altering the scale value will change how fast the page scrolls
static int lastY = 0;   // used for panning calculations (initial / previous vertical position)
static int lastX = 0;   // used for panning calculations (initial / previous horizontal position)
GESTUREINFO gi;  
```



Em seguida, adicione o manipulador para a mensagem de [**\_ gesto do WM**](wm-gesture.md) para que as barras de rolagem sejam atualizadas com deltas com base nos gestos de panorâmica. Isso lhe dá um controle muito mais refinado de panorâmica.

O código a seguir obtém a estrutura [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) do *lParam*, salva a última coordenada y da estrutura e determina a alteração na posição para atualizar o objeto da barra de rolagem. O código a seguir deve ser colocado em sua instrução de comutador **WndProc** .


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



Agora, quando você executar o gesto de panorâmica em sua janela, verá o texto rolar com inércia. Neste ponto, talvez você queira alterar o texto para ter mais linhas, de modo que você possa explorar as grandes seções de texto de movimento panorâmico.

## <a name="boundary-feedback-in-wndproc"></a>Comentários de limite em WndProc

Os comentários de limite são um tipo de comentário visual dado aos usuários quando eles atingem o final de uma área de visão panorâmica. Ele é disparado pelo aplicativo quando um limite é atingido. Na implementação de exemplo anterior da mensagem [**de \_ gesto do WM**](wm-gesture.md) , a condição final `(si.nPos == si.yPos)` do caso do **\_ gesto do WM** é usada para testar se você atingiu o final de uma região de visão panorâmica. As variáveis a seguir são usadas para rastrear valores e erros de teste.


```C++
// The following are used for panning feedback (Window Bounce)
static int animCount = 0;
static DWORD dwErr   = 0;

static BOOL isOverpan  = FALSE;
static long xOverpan   = 0;
static long yOverpan   = 0;
```



O caso de gesto de panorâmica é atualizado para disparar comentários de limite. O código a seguir ilustra o caso de **\_ Pan de GID** do manipulador de mensagens de [**\_ gesto do WM**](wm-gesture.md) .


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



Agora, a janela do aplicativo deve ter comentários de limite quando um usuário se desloca sobre a parte inferior da região da barra de rolagem.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Gestos de toque](guide-multi-touch-gestures.md)
</dt> <dt>

[**BeginPanningFeedback**](/windows/win32/api/uxtheme/nf-uxtheme-beginpanningfeedback)
</dt> <dt>

[**EndPanningFeedback**](/windows/win32/api/uxtheme/nf-uxtheme-endpanningfeedback)
</dt> <dt>

[**UpdatePanningFeedback**](/windows/win32/api/uxtheme/nf-uxtheme-updatepanningfeedback)
</dt> </dl>

 

 