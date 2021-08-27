---
title: Como usar Tree-View Infotips
description: Quando você aplica o \_ estilo INFOTIP de TVs a um controle de exibição de árvore, ele gera \_ notificações TVN GETINFOTIP quando o cursor está sobre um item no modo de exibição de árvore. Ao responder a essa notificação, você pode definir o texto que aparece na InfoTip.
ms.assetid: 779BEAC1-877E-43DD-AE1C-6D71C3013384
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ff9273b28b614e7935f6ac507288a5733271fb455a6be1e85b52c5b0ba8bbb3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120132026"
---
# <a name="how-to-use-tree-view-infotips"></a>Como usar Tree-View Infotips

Quando você aplica o [**estilo \_ INFOTIP de TVs**](tree-view-control-window-styles.md) a um controle de exibição de árvore, ele gera notificações [TVN \_ GETINFOTIP](tvn-getinfotip.md) quando o cursor está sobre um item no modo de exibição de árvore. Ao responder a essa notificação, você pode definir o texto que aparece na InfoTip.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Programação de interface do usuário

## <a name="instructions"></a>Instruções

### <a name="use-tree-view-infotips"></a>Usar Tree-View Infotips

O código de exemplo a seguir mostra como um aplicativo pode responder à notificação. Para simplificar, o exemplo apenas copia o texto do item para o InfoTip.


```
  case WM_NOTIFY:
    switch (((LPNMHDR) lParam)->code)
    {
    case TVN_GETINFOTIP:
        {
          LPNMTVGETINFOTIP pTip = (LPNMTVGETINFOTIP)lParam;
          HWND hTree            = GetDlgItem(hDlg, IDC_TREE1);
          HTREEITEM item        = pTip->hItem;

          // Get the text for the item.
          TVITEM tvitem;
          tvitem.mask       = TVIF_TEXT;
          tvitem.hItem      = item;
          TCHAR temp[1024];
          tvitem.pszText    = infoTipBuf;
          tvitem.cchTextMax = sizeof(temp) / sizeof(TCHAR);
          TreeView_GetItem(hTree, &tvitem);

          // Copy the text to the infotip.
          wcscpy_s(pTip->pszText, pTip->cchTextMax, tvitem.pszText);
          break;
        }
      }
      return TRUE;
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando controles de Tree-View](using-treeview.md)
</dt> <dt>

[O exemplo de CustDTv ilustra o desenho personalizado em um controle de Tree-View](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




