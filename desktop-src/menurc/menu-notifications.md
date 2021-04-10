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

 




