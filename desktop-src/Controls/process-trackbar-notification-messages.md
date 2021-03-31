---
title: Como processar mensagens de notificação TrackBar
description: Trackbars Notifique a janela pai das ações do usuário enviando a mensagem pai a WM \_ HSCROLL ou WM \_ VSCROLL.
ms.assetid: 83F47A3E-E607-49C2-A8B5-BC8A321D90BB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c723ad1bebb5c9f3ec8c4e7aefdc658e0881aef6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635404"
---
# <a name="how-to-process-trackbar-notification-messages"></a><span data-ttu-id="6b712-103">Como processar mensagens de notificação TrackBar</span><span class="sxs-lookup"><span data-stu-id="6b712-103">How to Process Trackbar Notification Messages</span></span>

<span data-ttu-id="6b712-104">Trackbars Notifique a janela pai das ações do usuário enviando a mensagem pai a [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL**](wm-vscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="6b712-104">Trackbars notify their parent window of user actions by sending the parent a [**WM\_HSCROLL**](wm-hscroll.md) or [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="6b712-105">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="6b712-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="6b712-106">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="6b712-106">Technologies</span></span>

-   [<span data-ttu-id="6b712-107">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="6b712-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="6b712-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="6b712-108">Prerequisites</span></span>

-   <span data-ttu-id="6b712-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="6b712-109">C/C++</span></span>
-   <span data-ttu-id="6b712-110">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="6b712-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="6b712-111">Instruções</span><span class="sxs-lookup"><span data-stu-id="6b712-111">Instructions</span></span>

### <a name="process-trackbar-notification-messages"></a><span data-ttu-id="6b712-112">Processar mensagens de notificação TrackBar</span><span class="sxs-lookup"><span data-stu-id="6b712-112">Process Trackbar Notification Messages</span></span>

<span data-ttu-id="6b712-113">O exemplo de código a seguir é uma função que é chamada quando a janela pai do TrackBar recebe uma mensagem do [**WM \_ HSCROLL**](wm-hscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="6b712-113">The following code example is a function that is called when the trackbar's parent window receives a [**WM\_HSCROLL**](wm-hscroll.md) message.</span></span> <span data-ttu-id="6b712-114">O TrackBar neste exemplo tem o estilo [**\_ ENABLESELRANGE TBS**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="6b712-114">The trackbar in this example has the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style.</span></span> <span data-ttu-id="6b712-115">A posição do controle deslizante é comparada ao intervalo de seleção e o controle deslizante é movido para a posição inicial ou final do intervalo de seleção, quando necessário.</span><span class="sxs-lookup"><span data-stu-id="6b712-115">The position of the slider is compared to the selection range, and the slider is moved to the starting or ending position of the selection range when necessary.</span></span>


```
// TBNotifications - handles trackbar notifications received 
// in the wParam parameter of WM_HSCROLL. This function simply 
// ensures that the slider remains within the selection range. 

VOID WINAPI TBNotifications( 
    WPARAM wParam,  // wParam of WM_HSCROLL message 
    HWND hwndTrack, // handle of trackbar window 
    UINT iSelMin,   // minimum value of trackbar selection 
    UINT iSelMax)   // maximum value of trackbar selection 
    { 
    DWORD dwPos;    // current position of slider 

    switch (LOWORD(wParam)) { 
    
        case TB_ENDTRACK:
          
            dwPos = SendMessage(hwndTrack, TBM_GETPOS, 0, 0); 
            
            if (dwPos > iSelMax) 
                SendMessage(hwndTrack, TBM_SETPOS, 
                    (WPARAM) TRUE,       // redraw flag 
                    (LPARAM) iSelMax); 
                    
            else if (dwPos < iSelMin) 
                SendMessage(hwndTrack, TBM_SETPOS, 
                    (WPARAM) TRUE,       // redraw flag 
                    (LPARAM) iSelMin); 
            
            break; 

        default: 
        
            break; 
        } 
} 
```



## <a name="remarks"></a><span data-ttu-id="6b712-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b712-116">Remarks</span></span>

<span data-ttu-id="6b712-117">Uma caixa de diálogo que contém um TrackBar de estilo [**\_ vertical do TBS**](trackbar-control-styles.md) pode usar essa função quando recebe uma mensagem do [**WM \_ VSCROLL**](wm-vscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="6b712-117">A dialog box that contains a [**TBS\_VERT**](trackbar-control-styles.md) style trackbar can use this function when it receives a [**WM\_VSCROLL**](wm-vscroll.md) message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b712-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6b712-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b712-119">Usando controles TrackBar</span><span class="sxs-lookup"><span data-stu-id="6b712-119">Using Trackbar Controls</span></span>](using-trackbar-controls.md)
</dt> </dl>

 

 




