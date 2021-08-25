---
title: Como adicionar colunas de List-View
description: Este tópico demonstra como adicionar colunas a um controle de exibição de lista.
ms.assetid: 9DBDFF56-7CD6-467C-AD2E-64213615E241
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee71065729502410d189493527af0e3e37663a4a2aaf541852454af7fa4a5aac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922076"
---
# <a name="how-to-add-list-view-columns"></a>Como adicionar colunas de List-View

Este tópico demonstra como adicionar colunas a um controle de exibição de lista. As colunas são usadas para exibir os itens e subitens quando um controle de exibição de lista está no modo de exibição de relatório (detalhes). O texto das colunas selecionadas também pode ser exibido na exibição de bloco.

## <a name="what-you-need-to-know"></a>O que você precisa saber

### <a name="technologies"></a>Tecnologias

-   [Windows Controles](window-controls.md)

### <a name="prerequisites"></a>Pré-requisitos

-   C/C++
-   Windows Programação de interface do usuário

## <a name="instructions"></a>Instruções


Para adicionar uma coluna a um controle de exibição de lista, envie a mensagem [**LVM \_ INSERTCOLUMN**](lvm-insertcolumn.md) ou use a macro [**\_ INSERTCOLUMN do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) . Para excluir uma coluna, use a mensagem [**LVM \_ DELETECOLUMN**](lvm-deletecolumn.md) .

O exemplo de código C++ a seguir chama a macro [**ListView \_ InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) para adicionar colunas a um controle de exibição de lista. Os títulos de coluna são definidos no arquivo de cabeçalho do aplicativo como recursos de cadeia de caracteres, que são numerados consecutivamente começando com IDS \_ FIRSTCOLUMN. O número de colunas é definido no arquivo de cabeçalho como **\_ colunas C**.


```C++
// InitListViewColumns: Adds columns to a list-view control.
// hWndListView:        Handle to the list-view control. 
// Returns TRUE if successful, and FALSE otherwise. 
BOOL InitListViewColumns(HWND hWndListView) 
{ 
    WCHAR szText[256];     // Temporary buffer.
    LVCOLUMN lvc;
    int iCol;

    // Initialize the LVCOLUMN structure.
    // The mask specifies that the format, width, text,
    // and subitem members of the structure are valid.
    lvc.mask = LVCF_FMT | LVCF_WIDTH | LVCF_TEXT | LVCF_SUBITEM;

    // Add the columns.
    for (iCol = 0; iCol < C_COLUMNS; iCol++)
    {
        lvc.iSubItem = iCol;
        lvc.pszText = szText;
        lvc.cx = 100;               // Width of column in pixels.

        if ( iCol < 2 )
            lvc.fmt = LVCFMT_LEFT;  // Left-aligned column.
        else
            lvc.fmt = LVCFMT_RIGHT; // Right-aligned column.

        // Load the names of the column headings from the string resources.
        LoadString(g_hInst,
                   IDS_FIRSTCOLUMN + iCol,
                   szText,
                   sizeof(szText)/sizeof(szText[0]));

        // Insert the columns into the list view.
        if (ListView_InsertColumn(hWndListView, iCol, &lvc) == -1)
            return FALSE;
    }
    
    return TRUE;
} 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de controle de exibição de lista](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[Sobre controles de List-View](list-view-controls-overview.md)
</dt> <dt>

[Usando controles de List-View](using-list-view-controls.md)
</dt> </dl>

 

 




