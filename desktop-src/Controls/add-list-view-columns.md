---
title: Como adicionar colunas de List-View
description: Este tópico demonstra como adicionar colunas a um controle de exibição de lista.
ms.assetid: 9DBDFF56-7CD6-467C-AD2E-64213615E241
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75e478c57a31fdd7ad91e0089106e93c24c47d5c
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104008617"
---
# <a name="how-to-add-list-view-columns"></a><span data-ttu-id="9707e-103">Como adicionar colunas de List-View</span><span class="sxs-lookup"><span data-stu-id="9707e-103">How to Add List-View Columns</span></span>

<span data-ttu-id="9707e-104">Este tópico demonstra como adicionar colunas a um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="9707e-104">This topic demonstrates how to add columns to a list-view control.</span></span> <span data-ttu-id="9707e-105">As colunas são usadas para exibir os itens e subitens quando um controle de exibição de lista está no modo de exibição de relatório (detalhes).</span><span class="sxs-lookup"><span data-stu-id="9707e-105">Columns are used to display the items and subitems when a list-view control is in report (details) view.</span></span> <span data-ttu-id="9707e-106">O texto das colunas selecionadas também pode ser exibido na exibição de bloco.</span><span class="sxs-lookup"><span data-stu-id="9707e-106">Text from selected columns can also be displayed in tile view.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="9707e-107">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="9707e-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="9707e-108">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="9707e-108">Technologies</span></span>

-   [<span data-ttu-id="9707e-109">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="9707e-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="9707e-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="9707e-110">Prerequisites</span></span>

-   <span data-ttu-id="9707e-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="9707e-111">C/C++</span></span>
-   <span data-ttu-id="9707e-112">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="9707e-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="9707e-113">Instruções</span><span class="sxs-lookup"><span data-stu-id="9707e-113">Instructions</span></span>


<span data-ttu-id="9707e-114">Para adicionar uma coluna a um controle de exibição de lista, envie a mensagem [**LVM \_ INSERTCOLUMN**](lvm-insertcolumn.md) ou use a macro [**\_ INSERTCOLUMN do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) .</span><span class="sxs-lookup"><span data-stu-id="9707e-114">To add a column to a list-view control, send the [**LVM\_INSERTCOLUMN**](lvm-insertcolumn.md) message or use the [**ListView\_InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) macro.</span></span> <span data-ttu-id="9707e-115">Para excluir uma coluna, use a mensagem [**LVM \_ DELETECOLUMN**](lvm-deletecolumn.md) .</span><span class="sxs-lookup"><span data-stu-id="9707e-115">To delete a column, use the [**LVM\_DELETECOLUMN**](lvm-deletecolumn.md) message.</span></span>

<span data-ttu-id="9707e-116">O exemplo de código C++ a seguir chama a macro [**ListView \_ InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) para adicionar colunas a um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="9707e-116">The following C++ code example calls the [**ListView\_InsertColumn**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) macro to add columns to a list-view control.</span></span> <span data-ttu-id="9707e-117">Os títulos de coluna são definidos no arquivo de cabeçalho do aplicativo como recursos de cadeia de caracteres, que são numerados consecutivamente começando com IDS \_ FIRSTCOLUMN.</span><span class="sxs-lookup"><span data-stu-id="9707e-117">The column headings are defined in the application's header file as string resources, which are numbered consecutively starting with IDS\_FIRSTCOLUMN.</span></span> <span data-ttu-id="9707e-118">O número de colunas é definido no arquivo de cabeçalho como **\_ colunas C**.</span><span class="sxs-lookup"><span data-stu-id="9707e-118">The number of columns is defined in the header file as **C\_COLUMNS**.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="9707e-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9707e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9707e-120">Referência de controle de exibição de lista</span><span class="sxs-lookup"><span data-stu-id="9707e-120">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="9707e-121">Sobre controles de List-View</span><span class="sxs-lookup"><span data-stu-id="9707e-121">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="9707e-122">Usando controles de List-View</span><span class="sxs-lookup"><span data-stu-id="9707e-122">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




