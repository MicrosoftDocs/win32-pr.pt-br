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
# <a name="menu-notifications"></a>Notificações de menu

## <a name="in-this-section"></a>Nesta seção

-   [**comando do WM \_**](wm-command.md)
-   [**CONTEXTMENU do WM \_**](wm-contextmenu.md)
-   [**ENTERMENULOOP do WM \_**](wm-entermenuloop.md)
-   [**EXITMENULOOP do WM \_**](wm-exitmenuloop.md)
-   [**GETTITLEBARINFOEX do WM \_**](wm-gettitlebarinfoex.md)
-   [**MENUCOMMAND do WM \_**](wm-menucommand.md)
-   [**MENUDRAG do WM \_**](wm-menudrag.md)
-   [**MENUGETOBJECT do WM \_**](wm-menugetobject.md)
-   [**MENURBUTTONUP do WM \_**](wm-menurbuttonup.md)
-   [**NEXTMENU do WM \_**](wm-nextmenu.md)
-   [**UNINITMENUPOPUP do WM \_**](wm-uninitmenupopup.md)


## <a name="example"></a>Exemplo

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
Exemplo obtido de [exemplos clássicos do Windows](https://github.com/microsoft/Windows-classic-samples) no github.

 




