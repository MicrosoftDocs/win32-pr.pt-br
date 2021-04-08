---
description: O exemplo a seguir usa a função ExitWindows para fazer logoff do usuário atual.
ms.assetid: 74be3505-c4bd-4ae2-aaed-700382839006
title: Como fazer logoff do usuário atual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e59ce625ae7da8a2a4a901fbb1429ab0f9b638c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921702"
---
# <a name="how-to-log-off-the-current-user"></a><span data-ttu-id="3559c-103">Como fazer logoff do usuário atual</span><span class="sxs-lookup"><span data-stu-id="3559c-103">How to Log Off the Current User</span></span>

<span data-ttu-id="3559c-104">O exemplo a seguir usa a função [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) para fazer logoff do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="3559c-104">The following example uses the [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows) function to log off the current user.</span></span>

``` syntax
// Log off the current user. 

ExitWindows(0, 0);
```

<span data-ttu-id="3559c-105">O exemplo a seguir usa a função [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) para fazer logoff do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="3559c-105">The following example uses the [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) function to log off the current user.</span></span>

``` syntax
// Log off the current user. 

ExitWindowsEx(EWX_LOGOFF, 0);
```

<span data-ttu-id="3559c-106">O aplicativo recebe a [**mensagem \_ QUERYENDSESSION do WM**](wm-queryendsession.md) e exibe uma caixa de diálogo perguntando se ela está OK para encerrar a sessão.</span><span class="sxs-lookup"><span data-stu-id="3559c-106">The application receives the [**WM\_QUERYENDSESSION**](wm-queryendsession.md) message and displays a dialog box asking the whether it is OK to end the session.</span></span> <span data-ttu-id="3559c-107">Se o usuário clicar em **Sim**, o sistema fará logoff do usuário.</span><span class="sxs-lookup"><span data-stu-id="3559c-107">If the user clicks **Yes**, the system logs off the user.</span></span> <span data-ttu-id="3559c-108">Se o usuário clicar em **não**, o logoff será cancelado.</span><span class="sxs-lookup"><span data-stu-id="3559c-108">If the user clicks **No**, the logoff is canceled.</span></span>

``` syntax
// Process the message in the window procedure. 

case WM_QUERYENDSESSION:  
{ 
    int r; 
    r = MessageBox(NULL,(LPCWSTR)L"End the session?",(LPCWSTR)L"WM_QUERYENDSESSION",MB_YESNO);
 
    // Return TRUE to continue, FALSE to stop. 
 
    return r == IDYES; 
    break; 
}
```

## <a name="related-topics"></a><span data-ttu-id="3559c-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3559c-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3559c-110">Fazendo logoff</span><span class="sxs-lookup"><span data-stu-id="3559c-110">Logging Off</span></span>](logging-off.md)
</dt> </dl>

 

 



