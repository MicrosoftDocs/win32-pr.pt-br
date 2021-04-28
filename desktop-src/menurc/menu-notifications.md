---
title: Notificações de menu
description: Notificações de menu
ms.assetid: 8ff5671e-a666-483c-9ac1-f8be6eb58ffa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f593e3007dff82241dc9e917a6cfa140cc443679
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112524"
---
# <a name="menu-notifications"></a><span data-ttu-id="3501c-103">Notificações de menu</span><span class="sxs-lookup"><span data-stu-id="3501c-103">Menu Notifications</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3501c-104">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="3501c-104">In This Section</span></span>

-   [<span data-ttu-id="3501c-105">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="3501c-105">**WM\_COMMAND**</span></span>](wm-command.md)
-   [<span data-ttu-id="3501c-106">**CONTEXTMENU do WM \_**</span><span class="sxs-lookup"><span data-stu-id="3501c-106">**WM\_CONTEXTMENU**</span></span>](wm-contextmenu.md)
-   [<span data-ttu-id="3501c-107">**ENTERMENULOOP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="3501c-107">**WM\_ENTERMENULOOP**</span></span>](wm-entermenuloop.md)
-   [<span data-ttu-id="3501c-108">**EXITMENULOOP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="3501c-108">**WM\_EXITMENULOOP**</span></span>](wm-exitmenuloop.md)
-   [<span data-ttu-id="3501c-109">**GETTITLEBARINFOEX do WM \_**</span><span class="sxs-lookup"><span data-stu-id="3501c-109">**WM\_GETTITLEBARINFOEX**</span></span>](wm-gettitlebarinfoex.md)
-   [<span data-ttu-id="3501c-110">**MENUCOMMAND do WM \_**</span><span class="sxs-lookup"><span data-stu-id="3501c-110">**WM\_MENUCOMMAND**</span></span>](wm-menucommand.md)
-   [<span data-ttu-id="3501c-111">**MENUDRAG do WM \_**</span><span class="sxs-lookup"><span data-stu-id="3501c-111">**WM\_MENUDRAG**</span></span>](wm-menudrag.md)
-   [<span data-ttu-id="3501c-112">**MENUGETOBJECT do WM \_**</span><span class="sxs-lookup"><span data-stu-id="3501c-112">**WM\_MENUGETOBJECT**</span></span>](wm-menugetobject.md)
-   [<span data-ttu-id="3501c-113">**MENURBUTTONUP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="3501c-113">**WM\_MENURBUTTONUP**</span></span>](wm-menurbuttonup.md)
-   [<span data-ttu-id="3501c-114">**NEXTMENU do WM \_**</span><span class="sxs-lookup"><span data-stu-id="3501c-114">**WM\_NEXTMENU**</span></span>](wm-nextmenu.md)
-   [<span data-ttu-id="3501c-115">**UNINITMENUPOPUP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="3501c-115">**WM\_UNINITMENUPOPUP**</span></span>](wm-uninitmenupopup.md)


## <a name="example"></a><span data-ttu-id="3501c-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="3501c-116">Example</span></span>

```c
BOOL AboutDlg (
    HWND hDlg, 
    UINT message, 
    WPARAM wParam, 
    LPARAM lParam)
{
    BOOL bRet = FALSE;
    
    switch (message) 
    {
        case WM_INITDIALOG:
            bRet = TRUE;
            break;

        case WM_COMMAND:
            if (wParam == IDOK ||
                wParam == IDCANCEL) 
            {
                EndDialog(hDlg, TRUE);
                bRet = TRUE;
            }
            break;
    }

    return bRet;
}
```
<span data-ttu-id="3501c-117">Exemplo obtido de [exemplos clássicos do Windows](https://github.com/microsoft/Windows-classic-samples) no github.</span><span class="sxs-lookup"><span data-stu-id="3501c-117">Example taken from [Windows classic samples](https://github.com/microsoft/Windows-classic-samples) on GitHub.</span></span>

 




