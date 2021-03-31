---
title: Limitando o escopo de reprodução
description: Limitando o escopo de reprodução
ms.assetid: 080ab96f-1cb5-48d4-ac0a-8fd9ba68a31a
keywords:
- Macro MCIWndPlayFrom
- Macro MCIWndPlayTo
- Macro MCIWndPlayFromTo
- Comandos de reprodução MCI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 465bcf7a7b6b5811de8413a1c89f7befcf81037f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822497"
---
# <a name="limiting-the-playback-scope"></a><span data-ttu-id="af216-107">Limitando o escopo de reprodução</span><span class="sxs-lookup"><span data-stu-id="af216-107">Limiting the Playback Scope</span></span>

<span data-ttu-id="af216-108">O controle da reprodução começa com a macro [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) , que reproduz o conteúdo ou o arquivo associado a uma janela MCIWnd da posição de reprodução atual até o final do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="af216-108">Controlling playback begins with the [**MCIWndPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) macro, which plays the content or file associated with an MCIWnd window from the current playback position to the end of the content.</span></span> <span data-ttu-id="af216-109">Se você quiser limitar a reprodução a uma parte específica do conteúdo ou arquivo, poderá escolher entre as outras macros MCIWnd de reprodução: [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom), [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto)e [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto).</span><span class="sxs-lookup"><span data-stu-id="af216-109">If you want to limit playback to a specific portion of the content or file, you can choose from the other playback MCIWnd macros: [**MCIWndPlayFrom**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfrom), [**MCIWndPlayTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayto), and [**MCIWndPlayFromTo**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayfromto).</span></span>

<span data-ttu-id="af216-110">Você também precisa definir um formato de hora apropriado.</span><span class="sxs-lookup"><span data-stu-id="af216-110">You also need to set an appropriate time format.</span></span> <span data-ttu-id="af216-111">O formato de hora determina se o conteúdo é medido em quadros, milissegundos, faixas ou em algumas outras unidades.</span><span class="sxs-lookup"><span data-stu-id="af216-111">The time format determines whether the content is measured in frames, milliseconds, tracks, or some other units.</span></span>

<span data-ttu-id="af216-112">O exemplo a seguir cria uma janela MCIWnd e fornece comandos de menu para executar o último terceiro, primeiro terceiro ou meio do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="af216-112">The following example creates an MCIWnd window and provides menu commands to play the last third, first third, or middle third of the content.</span></span> <span data-ttu-id="af216-113">Esses comandos de menu usam **MCIWndPlayFrom**, **MCIWndPlayTo** e **MCIWndPlayFromTo** para reproduzir os segmentos de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="af216-113">These menu commands use **MCIWndPlayFrom**, **MCIWndPlayTo**, and **MCIWndPlayFromTo** to play the content segments.</span></span> <span data-ttu-id="af216-114">O exemplo também usa as macros [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) e [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) para identificar o início e o final do conteúdo e usa a macro [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) para mover a posição de reprodução para o início do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="af216-114">The example also uses the [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) and [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) macros to identify the beginning and end of the content, and it uses the [**MCIWndHome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) macro to move the playback position to the beginning of the content.</span></span>

<span data-ttu-id="af216-115">A função [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) usa os \_ estilos de legenda WS e MCIWNDF ShowAll além \_ dos estilos de janela padrão para exibir o nome do arquivo, o modo e a posição de reprodução atual na barra de título da janela do MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="af216-115">The [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function uses the WS\_CAPTION and MCIWNDF\_SHOWALL styles in addition to the standard window styles to display the filename, mode, and current playback position in the title bar of the MCIWnd window.</span></span>


```C++
case WM_COMMAND: 
    switch (wParam) 
    { 
        case IDM_CREATEMCIWND: 
            g_hwndMCIWnd = MCIWndCreate(hwnd, 
                g_hinst, 
                WS_CHILD | WS_VISIBLE | WS_CAPTION | 
                MCIWNDF_SHOWALL, 
                "sample.avi"); 
            break;
        case IDM_PLAYFROM:                // plays last third of clip 
            MCIWndUseTime(g_hwndMCIWnd);  // millisecond format 
 
        // Get media start and end positions. 
            lStart = MCIWndGetStart(g_hwndMCIWnd); 
            lEnd = MCIWndGetEnd(g_hwndMCIWnd); 
 
        // Determine playback end position. 
            lPlayStart = 2 * (lEnd - lStart) / 3 + lStart; 
 
            MCIWndPlayFrom(g_hwndMCIWnd, lPlayStart); 
            break; 
        case IDM_PLAYTO:                  // plays first third of clip 
            MCIWndUseTime(g_hwndMCIWnd);  // millisecond format 
 
        // Get media start and end positions. 
            lStart = MCIWndGetStart(g_hwndMCIWnd); 
            lEnd = MCIWndGetEnd(g_hwndMCIWnd); 
 
        // Determine playback start position. 
            lPlayEnd = (lEnd - lStart) / 3 + lStart;
 
            MCIWndHome(g_hwndMCIWnd); 
            MCIWndPlayTo(g_hwndMCIWnd, lPlayEnd); 
            break; 
        case IDM_PLAYSOME:               // plays middle third of clip 
            MCIWndUseTime(g_hwndMCIWnd); // millisecond format 
 
        // Get media start and end positions. 
            lStart = MCIWndGetStart(g_hwndMCIWnd); 
            lEnd = MCIWndGetEnd(g_hwndMCIWnd); 
 
        // Determine playback start and end positions. 
            lPlayStart = (lEnd - lStart) / 3 + lStart;
            lPlayEnd = 2 * (lEnd - lStart) / 3 + lStart; 
 
            MCIWndPlayFromTo(g_hwndMCIWnd, lPlayStart, lPlayEnd); 
            break; 
    
    // Handle other commands here. 
    } 
```



 

 




