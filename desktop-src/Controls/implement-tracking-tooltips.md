---
title: Como implementar dicas de ferramentas de rastreamento
description: As dicas de ferramentas de rastreamento permanecem visíveis até que sejam explicitamente fechadas pelo aplicativo e podem alterar a posição na tela dinamicamente. Eles têm suporte da versão 4,70 e posterior dos controles comuns.
ms.assetid: 4BE1F9E6-92B6-4CA7-B89A-F2162BC86366
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a614fef7ed69cd8c2763f9370ce0011d51eb0c82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005088"
---
# <a name="how-to-implement-tracking-tooltips"></a><span data-ttu-id="c9441-104">Como implementar dicas de ferramentas de rastreamento</span><span class="sxs-lookup"><span data-stu-id="c9441-104">How to Implement Tracking Tooltips</span></span>

<span data-ttu-id="c9441-105">As dicas de ferramentas de rastreamento permanecem visíveis até que sejam explicitamente fechadas pelo aplicativo e podem alterar a posição na tela dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="c9441-105">Tracking tooltips remain visible until they are explicitly closed by the application, and can change position on the screen dynamically.</span></span> <span data-ttu-id="c9441-106">Eles têm suporte da [versão 4,70](common-control-versions.md) e posterior dos controles comuns.</span><span class="sxs-lookup"><span data-stu-id="c9441-106">They are supported by [version 4.70](common-control-versions.md) and later of the common controls.</span></span>

<span data-ttu-id="c9441-107">Para criar uma dica de ferramenta de rastreamento, inclua o sinalizador de faixa de TTF \_ no membro **uFlags** da estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) ao enviar a mensagem [**TTM \_ addferramenta**](ttm-addtool.md) .</span><span class="sxs-lookup"><span data-stu-id="c9441-107">To create a tracking tooltip, include the TTF\_TRACK flag in the **uFlags** member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure when sending the [**TTM\_ADDTOOL**](ttm-addtool.md) message.</span></span>

<span data-ttu-id="c9441-108">Seu aplicativo deve ativar (Mostrar) e desativar (ocultar) manualmente uma dica de ferramenta de rastreamento enviando uma mensagem [**TTM \_ TRACKACTIVATE**](ttm-trackactivate.md) .</span><span class="sxs-lookup"><span data-stu-id="c9441-108">Your application must manually activate (show) and deactivate (hide) a tracking tooltip by sending a [**TTM\_TRACKACTIVATE**](ttm-trackactivate.md) message.</span></span> <span data-ttu-id="c9441-109">Enquanto uma dica de ferramenta de rastreamento está ativa, seu aplicativo deve especificar o local da dica de ferramenta enviando mensagens [**TTM \_ TRACKPOSITION**](ttm-trackposition.md) para o controle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="c9441-109">While a tracking tooltip is active, your application must specify the location of the tooltip by sending [**TTM\_TRACKPOSITION**](ttm-trackposition.md) messages to the tooltip control.</span></span> <span data-ttu-id="c9441-110">Como o aplicativo lida com tarefas como posicionar a dica de ferramenta, o rastreamento de dicas de ferramenta não usa o sinalizador de **\_ subclasse ttf** ou a mensagem [**TTM \_ RELAYEVENT**](ttm-relayevent.md) .</span><span class="sxs-lookup"><span data-stu-id="c9441-110">Because the application handles tasks such as positioning the tooltip, tracking tooltips do not use the **TTF\_SUBCLASS** flag or the [**TTM\_RELAYEVENT**](ttm-relayevent.md) message.</span></span>

<span data-ttu-id="c9441-111">A mensagem [**TTM \_ TRACKPOSITION**](ttm-trackposition.md) faz com que o controle ToolTip Exiba a janela usando um dos dois estilos de posicionamento:</span><span class="sxs-lookup"><span data-stu-id="c9441-111">The [**TTM\_TRACKPOSITION**](ttm-trackposition.md) message causes the tooltip control to display the window using one of two placement styles:</span></span>

-   <span data-ttu-id="c9441-112">Por padrão, a dica de ferramentas é exibida ao lado da ferramenta correspondente em uma posição que o controle escolhe.</span><span class="sxs-lookup"><span data-stu-id="c9441-112">By default, the tooltip is displayed next to the corresponding tool in a position that the control chooses.</span></span> <span data-ttu-id="c9441-113">O local escolhido é relativo às coordenadas que você fornece usando essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="c9441-113">The location chosen is relative to the coordinates that you provide by using this message.</span></span>
-   <span data-ttu-id="c9441-114">Se você incluir o **valor \_ absoluto de TTF** no membro da estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) , a dica de ferramenta será exibida no local do pixel especificado na mensagem.</span><span class="sxs-lookup"><span data-stu-id="c9441-114">If you include the **TTF\_ABSOLUTE** value in the member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure, the tooltip is displayed at the pixel location specified in the message.</span></span> <span data-ttu-id="c9441-115">Nesse caso, o controle não tenta alterar o local da janela de dica de ferramenta das coordenadas que você fornece.</span><span class="sxs-lookup"><span data-stu-id="c9441-115">In this case, the control does not attempt to change the tooltip window's location from the coordinates you provide.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="c9441-116">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="c9441-116">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="c9441-117">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="c9441-117">Technologies</span></span>

-   [<span data-ttu-id="c9441-118">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="c9441-118">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="c9441-119">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="c9441-119">Prerequisites</span></span>

-   <span data-ttu-id="c9441-120">C/C++</span><span class="sxs-lookup"><span data-stu-id="c9441-120">C/C++</span></span>
-   <span data-ttu-id="c9441-121">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="c9441-121">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="c9441-122">Instruções</span><span class="sxs-lookup"><span data-stu-id="c9441-122">Instructions</span></span>

### <a name="implement-in-place-tooltips"></a><span data-ttu-id="c9441-123">Implementar dicas de ferramentas de In-Place</span><span class="sxs-lookup"><span data-stu-id="c9441-123">Implement In-Place Tooltips</span></span>

<span data-ttu-id="c9441-124">O membro **uFlags** da estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) que é usada no exemplo inclui o sinalizador **\_ Absolute de TTF** .</span><span class="sxs-lookup"><span data-stu-id="c9441-124">The **uFlags** member of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure that is used in the example includes the **TTF\_ABSOLUTE** flag.</span></span> <span data-ttu-id="c9441-125">Sem esse sinalizador, o controle ToolTip escolhe onde exibir a dica de ferramenta, e sua posição relativa à caixa de diálogo pode mudar repentinamente à medida que o ponteiro do mouse se move.</span><span class="sxs-lookup"><span data-stu-id="c9441-125">Without this flag, the tooltip control chooses where to display the tooltip, and its position relative to the dialog box may change suddenly as the mouse pointer moves.</span></span>

> [!Note]  
> <span data-ttu-id="c9441-126">`g_toolItem` é uma estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) global.</span><span class="sxs-lookup"><span data-stu-id="c9441-126">`g_toolItem` is a global [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure.</span></span>

 

<span data-ttu-id="c9441-127">O exemplo a seguir demonstra como criar um controle de dica de ferramenta de rastreamento.</span><span class="sxs-lookup"><span data-stu-id="c9441-127">The following example demonstrates how to create a tracking tooltip control.</span></span> <span data-ttu-id="c9441-128">O exemplo especifica a área inteira do cliente da janela principal como a ferramenta.</span><span class="sxs-lookup"><span data-stu-id="c9441-128">The example specifies the main window's entire client area as the tool.</span></span>


```C++
HWND CreateTrackingToolTip(int toolID, HWND hDlg, WCHAR* pText)
{
    // Create a tooltip.
    HWND hwndTT = CreateWindowEx(WS_EX_TOPMOST, TOOLTIPS_CLASS, NULL, 
                                 WS_POPUP | TTS_NOPREFIX | TTS_ALWAYSTIP, 
                                 CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, CW_USEDEFAULT, 
                                 hDlg, NULL, g_hInst,NULL);

    if (!hwndTT)
    {
      return NULL;
    }

    // Set up the tool information. In this case, the "tool" is the entire parent window.
    
    g_toolItem.cbSize   = sizeof(TOOLINFO);
    g_toolItem.uFlags   = TTF_IDISHWND | TTF_TRACK | TTF_ABSOLUTE;
    g_toolItem.hwnd     = hDlg;
    g_toolItem.hinst    = g_hInst;
    g_toolItem.lpszText = pText;
    g_toolItem.uId      = (UINT_PTR)hDlg;
    
    GetClientRect (hDlg, &g_toolItem.rect);

    // Associate the tooltip with the tool window.
    
    SendMessage(hwndTT, TTM_ADDTOOL, 0, (LPARAM) (LPTOOLINFO) &g_toolItem); 
    
    return hwndTT;
}
            
```



### <a name="window-procedure-implementation"></a><span data-ttu-id="c9441-129">Implementação de procedimento de janela</span><span class="sxs-lookup"><span data-stu-id="c9441-129">Window Procedure Implementation</span></span>

<span data-ttu-id="c9441-130">Quando o ponteiro do mouse estiver dentro da área do cliente, a dica de ferramenta estará ativa e exibirá as coordenadas do cursor, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="c9441-130">When the mouse pointer is within the client area, the tooltip is active and displays the cursor coordinates, as shown in the following illustration.</span></span>

![captura de tela de uma caixa de diálogo; uma dica de ferramenta mostra as coordenadas x e y do ponteiro do mouse](images/tt-tracking.png)

<span data-ttu-id="c9441-132">O código de exemplo a seguir é do procedimento de janela para uma caixa de diálogo que exibe a dica de ferramenta de rastreamento criada no exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="c9441-132">The following example code is from the window procedure for a dialog box that displays the tracking tooltip created in the preceding example.</span></span> <span data-ttu-id="c9441-133">A variável booliana global *g \_ TrackingMouse* é usada para determinar se é necessário reativar a dica de ferramenta e redefinir o controle do mouse para que o aplicativo seja notificado quando o ponteiro do mouse sair da área do cliente da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="c9441-133">The global Boolean variable *g\_TrackingMouse* is used to determine whether it is necessary to reactivate the tooltip and reset mouse tracking so that the application is notified when the mouse pointer leaves the client area of the dialog box.</span></span>


```
//g_hwndTrackingTT is a global HWND variable

case WM_INITDIALOG:

        InitCommonControls();
        g_hwndTrackingTT = CreateTrackingToolTip(IDC_BUTTON1, hDlg, L"");
        return TRUE;

case WM_MOUSELEAVE: // The mouse pointer has left our window. Deactivate the tooltip.
    
    SendMessage(g_hwndTrackingTT, TTM_TRACKACTIVATE, (WPARAM)FALSE, (LPARAM)&g_toolItem);
    g_TrackingMouse = FALSE;
    return FALSE;

case WM_MOUSEMOVE:

    static int oldX, oldY;
    int newX, newY;

    if (!g_TrackingMouse)   // The mouse has just entered the window.
    {                       // Request notification when the mouse leaves.
    
        TRACKMOUSEEVENT tme = { sizeof(TRACKMOUSEEVENT) };
        tme.hwndTrack       = hDlg;
        tme.dwFlags         = TME_LEAVE;
        
        TrackMouseEvent(&tme);

        // Activate the tooltip.
        SendMessage(g_hwndTrackingTT, TTM_TRACKACTIVATE, (WPARAM)TRUE, (LPARAM)&g_toolItem);
        
        g_TrackingMouse = TRUE;
    }

    newX = GET_X_LPARAM(lParam);
    newY = GET_Y_LPARAM(lParam);

    // Make sure the mouse has actually moved. The presence of the tooltip 
    // causes Windows to send the message continuously.
    
    if ((newX != oldX) || (newY != oldY))
    {
        oldX = newX;
        oldY = newY;
            
        // Update the text.
        WCHAR coords[12];
        swprintf_s(coords, ARRAYSIZE(coords), L"%d, %d", newX, newY);
        
        g_toolItem.lpszText = coords;
        SendMessage(g_hwndTrackingTT, TTM_SETTOOLINFO, 0, (LPARAM)&g_toolItem);

        // Position the tooltip. The coordinates are adjusted so that the tooltip does not overlap the mouse pointer.
        
        POINT pt = { newX, newY }; 
        ClientToScreen(hDlg, &pt);
        SendMessage(g_hwndTrackingTT, TTM_TRACKPOSITION, 0, (LPARAM)MAKELONG(pt.x + 10, pt.y - 20));
    }
    return FALSE;
```



## <a name="related-topics"></a><span data-ttu-id="c9441-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c9441-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9441-135">Usando controles de dica de ferramenta</span><span class="sxs-lookup"><span data-stu-id="c9441-135">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 




