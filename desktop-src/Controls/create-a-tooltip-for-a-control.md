---
title: Como criar uma dica de ferramenta para um controle
description: A função de exemplo a seguir cria uma dica de ferramenta e a associa ao controle cuja ID de recurso é passada.
ms.assetid: FDA3B2A0-1256-4DAC-86CF-8F123894E760
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f341c1be1e749c4e0d6f18caf97a3f897cf429e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005095"
---
# <a name="how-to-create-a-tooltip-for-a-control"></a><span data-ttu-id="40f8f-103">Como criar uma dica de ferramenta para um controle</span><span class="sxs-lookup"><span data-stu-id="40f8f-103">How to Create a Tooltip for a Control</span></span>

<span data-ttu-id="40f8f-104">A função de exemplo a seguir cria uma dica de ferramenta e a associa ao controle cuja ID de recurso é passada.</span><span class="sxs-lookup"><span data-stu-id="40f8f-104">The following example function creates a tooltip and associates it with the control whose resource ID is passed in.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="40f8f-105">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="40f8f-105">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="40f8f-106">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="40f8f-106">Technologies</span></span>

-   [<span data-ttu-id="40f8f-107">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="40f8f-107">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="40f8f-108">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="40f8f-108">Prerequisites</span></span>

-   <span data-ttu-id="40f8f-109">C/C++</span><span class="sxs-lookup"><span data-stu-id="40f8f-109">C/C++</span></span>
-   <span data-ttu-id="40f8f-110">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="40f8f-110">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="40f8f-111">Instruções</span><span class="sxs-lookup"><span data-stu-id="40f8f-111">Instructions</span></span>

### <a name="create-a-tooltip-for-a-control"></a><span data-ttu-id="40f8f-112">Criar uma dica de ferramenta para um controle</span><span class="sxs-lookup"><span data-stu-id="40f8f-112">Create a Tooltip for a Control</span></span>

<span data-ttu-id="40f8f-113">A função de exemplo a seguir cria uma dica de ferramenta e a associa ao controle cuja ID de recurso é passada.</span><span class="sxs-lookup"><span data-stu-id="40f8f-113">The following example function creates a tooltip and associates it with the control whose resource ID is passed in.</span></span>


```C++
// Description:
//   Creates a tooltip for an item in a dialog box. 
// Parameters:
//   idTool - identifier of an dialog box item.
//   nDlg - window handle of the dialog box.
//   pszText - string to use as the tooltip text.
// Returns:
//   The handle to the tooltip.
//
HWND CreateToolTip(int toolID, HWND hDlg, PTSTR pszText)
{
    if (!toolID || !hDlg || !pszText)
    {
        return FALSE;
    }
    // Get the window of the tool.
    HWND hwndTool = GetDlgItem(hDlg, toolID);
    
    // Create the tooltip. g_hInst is the global instance handle.
    HWND hwndTip = CreateWindowEx(NULL, TOOLTIPS_CLASS, NULL,
                              WS_POPUP |TTS_ALWAYSTIP | TTS_BALLOON,
                              CW_USEDEFAULT, CW_USEDEFAULT,
                              CW_USEDEFAULT, CW_USEDEFAULT,
                              hDlg, NULL, 
                              g_hInst, NULL);
    
   if (!hwndTool || !hwndTip)
   {
       return (HWND)NULL;
   }                              
                              
    // Associate the tooltip with the tool.
    TOOLINFO toolInfo = { 0 };
    toolInfo.cbSize = sizeof(toolInfo);
    toolInfo.hwnd = hDlg;
    toolInfo.uFlags = TTF_IDISHWND | TTF_SUBCLASS;
    toolInfo.uId = (UINT_PTR)hwndTool;
    toolInfo.lpszText = pszText;
    SendMessage(hwndTip, TTM_ADDTOOL, 0, (LPARAM)&toolInfo);

    return hwndTip;
}
```



## <a name="related-topics"></a><span data-ttu-id="40f8f-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="40f8f-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40f8f-115">Usando controles de dica de ferramenta</span><span class="sxs-lookup"><span data-stu-id="40f8f-115">Using Tooltip Controls</span></span>](using-tooltip-contro.md)
</dt> </dl>

 

 




