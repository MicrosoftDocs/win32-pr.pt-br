---
title: Criando uma janela MCIWnd
description: Criando uma janela MCIWnd
ms.assetid: bd45e813-5807-43cd-bef1-03285df9a018
keywords:
- Janela MCIWnd, criando
- Função MCIWndCreate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c205e87acf3e5f529d4b5cc9c9163b7fe887fe04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105789759"
---
# <a name="creating-an-mciwnd-window"></a><span data-ttu-id="6b145-105">Criando uma janela MCIWnd</span><span class="sxs-lookup"><span data-stu-id="6b145-105">Creating an MCIWnd Window</span></span>

<span data-ttu-id="6b145-106">A função [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) registra e cria uma janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="6b145-106">The [**MCIWndCreate**](/windows/desktop/api/Vfw/nf-vfw-mciwndcreatea) function registers and creates an MCIWnd window.</span></span> <span data-ttu-id="6b145-107">A janela pode ser uma janela pai, filho ou pop-up.</span><span class="sxs-lookup"><span data-stu-id="6b145-107">The window can be a parent, child, or pop-up window.</span></span> <span data-ttu-id="6b145-108">O exemplo a seguir cria uma janela MCIWnd como uma janela filho e permite que o controle de usuário seja reproduzido fornecendo acesso aos botões TrackBar e **Play**, **Stop** e **menu** .</span><span class="sxs-lookup"><span data-stu-id="6b145-108">The following example creates an MCIWnd window as a child window and lets the user control playback by providing access to the trackbar and the **Play**, **Stop**, and **Menu** buttons.</span></span> <span data-ttu-id="6b145-109">O exemplo especifica um identificador de uma janela pai e especifica **NULL** para os estilos de janela, de modo que os estilos de janela padrão de WS \_ Child, WS \_ Border e WS \_ Visible são usados para criar a janela MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="6b145-109">The example specifies a handle of a parent window and specifies **NULL** for the window styles, so the default window styles of WS\_CHILD, WS\_BORDER, and WS\_VISIBLE are used to create the MCIWnd window.</span></span>


```C++
// Global variable and constants 
// extern HINSTANCE g_hinst;       instance handle 
// extern HWND g_hwndMCIWnd;       MCIWnd window handle 
 
case WM_COMMAND: 
    switch (wParam) { 
    case IDM_CREATEMCIWND: 
        g_hwndMCIWnd = MCIWndCreate(hwnd, g_hinst, NULL, 
            "sample.avi"); 
        break;    
    } 
    break; 
```



> [!Note]  
> <span data-ttu-id="6b145-110">Você também pode especificar **NULL** para o identificador de janela pai e os estilos de janela; nesse caso, os estilos de janela padrão seriam WS \_ Overlapped e WS \_ Visible.</span><span class="sxs-lookup"><span data-stu-id="6b145-110">You could also specify **NULL** for both the parent window handle and the window styles, in which case the default window styles would be WS\_OVERLAPPED and WS\_VISIBLE.</span></span>

 

 

 




