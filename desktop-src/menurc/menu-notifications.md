---
title: Notificações de menu
description: .
ms.assetid: 8ff5671e-a666-483c-9ac1-f8be6eb58ffa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d61f5303253fd3201fd9a4510ecf90fa76c10524
ms.sourcegitcommit: e98f40bef170ae9ce30d91ba96b90600b0446a24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/28/2020
ms.locfileid: "104293873"
---
# <a name="menu-notifications"></a><span data-ttu-id="c4c4f-103">Notificações de menu</span><span class="sxs-lookup"><span data-stu-id="c4c4f-103">Menu Notifications</span></span>

## <a name="in-this-section"></a><span data-ttu-id="c4c4f-104">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="c4c4f-104">In This Section</span></span>

-   [<span data-ttu-id="c4c4f-105">**comando do WM \_**</span><span class="sxs-lookup"><span data-stu-id="c4c4f-105">**WM\_COMMAND**</span></span>](wm-command.md)
-   [<span data-ttu-id="c4c4f-106">**CONTEXTMENU do WM \_**</span><span class="sxs-lookup"><span data-stu-id="c4c4f-106">**WM\_CONTEXTMENU**</span></span>](wm-contextmenu.md)
-   [<span data-ttu-id="c4c4f-107">**ENTERMENULOOP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="c4c4f-107">**WM\_ENTERMENULOOP**</span></span>](wm-entermenuloop.md)
-   [<span data-ttu-id="c4c4f-108">**EXITMENULOOP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="c4c4f-108">**WM\_EXITMENULOOP**</span></span>](wm-exitmenuloop.md)
-   [<span data-ttu-id="c4c4f-109">**GETTITLEBARINFOEX do WM \_**</span><span class="sxs-lookup"><span data-stu-id="c4c4f-109">**WM\_GETTITLEBARINFOEX**</span></span>](wm-gettitlebarinfoex.md)
-   [<span data-ttu-id="c4c4f-110">**MENUCOMMAND do WM \_**</span><span class="sxs-lookup"><span data-stu-id="c4c4f-110">**WM\_MENUCOMMAND**</span></span>](wm-menucommand.md)
-   [<span data-ttu-id="c4c4f-111">**MENUDRAG do WM \_**</span><span class="sxs-lookup"><span data-stu-id="c4c4f-111">**WM\_MENUDRAG**</span></span>](wm-menudrag.md)
-   [<span data-ttu-id="c4c4f-112">**MENUGETOBJECT do WM \_**</span><span class="sxs-lookup"><span data-stu-id="c4c4f-112">**WM\_MENUGETOBJECT**</span></span>](wm-menugetobject.md)
-   [<span data-ttu-id="c4c4f-113">**MENURBUTTONUP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="c4c4f-113">**WM\_MENURBUTTONUP**</span></span>](wm-menurbuttonup.md)
-   [<span data-ttu-id="c4c4f-114">**NEXTMENU do WM \_**</span><span class="sxs-lookup"><span data-stu-id="c4c4f-114">**WM\_NEXTMENU**</span></span>](wm-nextmenu.md)
-   [<span data-ttu-id="c4c4f-115">**UNINITMENUPOPUP do WM \_**</span><span class="sxs-lookup"><span data-stu-id="c4c4f-115">**WM\_UNINITMENUPOPUP**</span></span>](wm-uninitmenupopup.md)


## <a name="example"></a><span data-ttu-id="c4c4f-116">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c4c4f-116">Example</span></span>

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
<span data-ttu-id="c4c4f-117">Exemplo obtido de [exemplos clássicos do Windows](https://github.com/microsoft/Windows-classic-samples) no github.</span><span class="sxs-lookup"><span data-stu-id="c4c4f-117">Example taken from [Windows classic samples](https://github.com/microsoft/Windows-classic-samples) on GitHub.</span></span>

 




