---
title: Gravando com controles MCIWnd
description: Gravando com controles MCIWnd
ms.assetid: 65a57400-aeea-4a27-8d51-37d3d9e9bd55
keywords:
- Função MCIWndCreate
- Macro MCIWndNew
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 814bd9f92b895c03ccbb073f830dbf31dcd2e3c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103915985"
---
# <a name="recording-with-mciwnd-controls"></a><span data-ttu-id="ba208-105">Gravando com controles MCIWnd</span><span class="sxs-lookup"><span data-stu-id="ba208-105">Recording with MCIWnd Controls</span></span>

<span data-ttu-id="ba208-106">O exemplo a seguir registra áudio de forma de onda usando os controles internos da janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="ba208-106">The following example records waveform audio using the built-in controls of the MCIWnd window.</span></span> <span data-ttu-id="ba208-107">O exemplo cria uma janela MCIWnd usando o estilo de \_ janela de registro MCIWNDF com a função [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) para adicionar um botão de **registro** à barra de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="ba208-107">The example creates an MCIWnd window by using the MCIWNDF\_RECORD window style with the [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function to add a **Record** button to the toolbar.</span></span> <span data-ttu-id="ba208-108">A macro [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) indica que um novo arquivo está associado à janela MCIWnd e que um dispositivo de forma de onda-áudio fornecerá seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ba208-108">The [**MCIWndNew**](/windows/desktop/api/Vfw/nf-vfw-mciwndnew) macro indicates a new file is associated with the MCIWnd window and that a waveform-audio device will provide its content.</span></span> <span data-ttu-id="ba208-109">Um segundo comando de menu, \_ a IDM SAVEMCIWND, permite que o usuário salve a gravação e selecione um nome de arquivo usando a macro [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) .</span><span class="sxs-lookup"><span data-stu-id="ba208-109">A second menu command, IDM\_SAVEMCIWND, lets the user save the recording and select a filename by using the [**MCIWndSaveDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) macro.</span></span>


```C++
case WM_COMMAND: 
    switch (wParam) { 
    case IDM_CREATEMCIWND: 
        g_hwndMCIWnd = MCIWndCreate(hwnd, g_hinst, 
            WS_VISIBLE | MCIWNDF_RECORD, NULL); 
        MCIWndNew(g_hwndMCIWnd, "waveaudio"); 
        break;    
    case IDM_SAVEMCIWND: 
        MCIWndSaveDialog(g_hwndMCIWnd); 
        break; 
    } 
```



 

 




