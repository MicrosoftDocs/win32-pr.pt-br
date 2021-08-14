---
title: Melhorando a experiência Single-Finger panorâmico
description: Se você criar um aplicativo destinado ao Windows Touch, ele fornece automaticamente suporte a panorâmico básico. No entanto, você pode usar a mensagem WM \_ GESTURE para fornecer suporte aprimorado para o panorâmico de um dedo.
ms.assetid: eb01a6df-9969-44d1-a657-4f83fb0b67cb
keywords:
- Windows Toque, panorâmico de dedo único
- Windows Toque, panorâmico
- Windows Toque, barras de rolagem
- Windows Toque, movimento
- Windows Toque, mensagens de painel de gestos
- Windows Toque, comentários de limite
- panorâmico de dedo único
- panning,single-finger
- panning,comentários de limite
- barras de rolagem, panorâmico de dedo único
- movimento, panorâmico de dedo único
- barras de rolagem, desabilitando
- movimento, desabilitação
- gestos, mensagens de painel de gestos
- panning, mensagens de panorâmico de gestos
- comentários de limite, panorâmico de dedo único
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf740d673e8bd2d2711238902d3de6c89d21a01fe330524b910db050011872f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118435439"
---
# <a name="improving-the-single-finger-panning-experience"></a>Melhorando a experiência Single-Finger panorâmico

Se você criar um aplicativo destinado ao Windows Touch, ele fornece automaticamente suporte a panorâmico básico. No entanto, você pode usar a [**mensagem WM \_ GESTURE**](wm-gesture.md) para fornecer suporte aprimorado para o panorâmico de um dedo.

## <a name="overview"></a>Visão geral

Para melhorar a experiência de panorâmico de dedo único, use estas etapas, conforme explicado nas seções subsequentes deste tópico:

-   Crie um aplicativo com barras de rolagem e com movimento desabilitado.
-   Adicione suporte para mensagens de painel de gestos.
-   Habilitar o ressalto.

## <a name="create-an-application-with-scroll-bars-and-with-flicks-disabled"></a>Criar um aplicativo com barras de rolagem e com movimento desabilitado

Antes de começar, você deve criar um aplicativo com barras de rolagem. A seção [Suporte herdada para panorâmico com barras de rolagem](legacy-support-for-panning-with-scrollbars.md) explica esse processo. Se você quiser começar com o conteúdo de exemplo, vá para essa seção e crie um aplicativo com barras de rolagem e desabilite os movimento. Se você já tiver um aplicativo com barras de rolagem em funcionamento, desabilite os movimento conforme descrito nesta seção.

## <a name="add-custom-panning-support-for-gesture-pan-messages"></a>Adicionar suporte de panorâmico personalizado para mensagens de panorâmico de gesto

Para dar suporte a mensagens de painel de gestos, você deve lidar com elas no **método WndProc.** As mensagens de gesto são usadas para determinar deltas horizontais e verticais para mensagens de panor lado a lado. Os deltas são usados para atualizar o objeto da barra de rolagem, que atualiza a interface do usuário.

Primeiro, atualize as Windows de versão no arquivo targetver.h para habilitar Windows Touch. O código a seguir mostra as várias Windows de versão que devem substituir aquelas em targetver.h.


```C++
#ifndef WINVER                  // Specifies that the minimum required platform is Windows Vista.
#define WINVER 0x0601           // Change this to the appropriate value to target other versions of Windows.
#endif

#ifndef _WIN32_WINNT            // Specifies that the minimum required platform is Windows Vista.
#define _WIN32_WINNT 0x0601     // Change this to the appropriate value to target other versions of Windows.
#endif
```



Em seguida, adicione o arquivo UXTheme.h ao seu projeto e adicione a biblioteca uxtheme.lib às dependências adicionais do seu projeto.


```C++
#include <uxtheme.h>
```



Em seguida, adicione as seguintes variáveis à parte superior da **função WndProc.** Eles serão usados em cálculos para panorâmico.


```C++
// The following are used for the custom panning handler      
BOOL bResult = FALSE;

static int scale = 8;   // altering the scale value will change how fast the page scrolls
static int lastY = 0;   // used for panning calculations (initial / previous vertical position)
static int lastX = 0;   // used for panning calculations (initial / previous horizontal position)
GESTUREINFO gi;  
```



Em seguida, adicione o manipulador para a mensagem [**WM \_ GESTURE**](wm-gesture.md) para que as barras de rolagem sejam atualizadas com deltas com base em gestos de panorâmico. Isso oferece um controle muito mais fino de panorâmico.

O código a seguir obtém a estrutura [**GESTUREINFO**](/windows/win32/api/winuser/ns-winuser-gestureinfo) do *lParam*, salva a última coordenada y da estrutura e determina a alteração na posição para atualizar o objeto da barra de rolagem. O código a seguir deve ser colocado na **instrução switch WndProc.**


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



Agora, ao executar o gesto de panorônomos na janela, você verá a rolagem de texto com inércia. Neste ponto, talvez você queira alterar o texto para ter mais linhas para que você possa explorar o panorâmico de grandes seções de texto.

## <a name="boundary-feedback-in-wndproc"></a>Comentários de limite no WndProc

Os comentários de limite são um tipo de comentários visuais dados aos usuários quando eles chegam ao final de uma área pannizável. Ele é disparado pelo aplicativo quando um limite é atingido. No exemplo anterior de implementação da mensagem [**WM \_ GESTURE,**](wm-gesture.md) a condição final do caso WM GESTURE é usada para testar se você atingiu o final de uma `(si.nPos == si.yPos)` região pannizável. **\_** As variáveis a seguir são usadas para rastrear valores e testar erros.


```C++
// The following are used for panning feedback (Window Bounce)
static int animCount = 0;
static DWORD dwErr   = 0;

static BOOL isOverpan  = FALSE;
static long xOverpan   = 0;
static long yOverpan   = 0;
```



O caso do gesto de panorualizações é atualizado para disparar comentários de limite. O código a seguir ilustra o caso **DO \_ GID PAN** do manipulador de mensagens WM [**\_ GESTURE.**](wm-gesture.md)


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



Agora, a janela do aplicativo deve ter comentários de limite quando um usuário passa pela parte inferior da região da barra de rolagem.

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

 

 