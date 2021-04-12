---
title: Como adicionar itens de Tree-View
description: Você adiciona um item a um controle de exibição de árvore enviando a \_ mensagem TVM INSERTITEM para o controle.
ms.assetid: CD6376F4-8B1A-489D-8538-6C1620E98F76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a7da0846b57f422de83984b197df0770286882
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104365631"
---
# <a name="how-to-add-tree-view-items"></a><span data-ttu-id="aa5e6-103">Como adicionar itens de Tree-View</span><span class="sxs-lookup"><span data-stu-id="aa5e6-103">How to Add Tree-View Items</span></span>

<span data-ttu-id="aa5e6-104">Você adiciona um item a um controle de exibição de árvore enviando a mensagem [**TVM \_ INSERTITEM**](tvm-insertitem.md) para o controle.</span><span class="sxs-lookup"><span data-stu-id="aa5e6-104">You add an item to a tree-view control by sending the [**TVM\_INSERTITEM**](tvm-insertitem.md) message to the control.</span></span> <span data-ttu-id="aa5e6-105">A mensagem inclui o endereço de uma estrutura [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) , especificando o item pai, o item após o qual o novo item é inserido e uma estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que define os atributos do item.</span><span class="sxs-lookup"><span data-stu-id="aa5e6-105">The message includes the address of a [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) structure, specifying the parent item, the item after which the new item is inserted, and a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that defines the attributes of the item.</span></span> <span data-ttu-id="aa5e6-106">Os atributos incluem o rótulo do item, suas imagens selecionadas e não selecionadas, e um valor definido pelo aplicativo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="aa5e6-106">The attributes include the item's label, its selected and nonselected images, and a 32-bit application-defined value.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="aa5e6-107">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="aa5e6-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="aa5e6-108">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="aa5e6-108">Technologies</span></span>

-   [<span data-ttu-id="aa5e6-109">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="aa5e6-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="aa5e6-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="aa5e6-110">Prerequisites</span></span>

-   <span data-ttu-id="aa5e6-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="aa5e6-111">C/C++</span></span>
-   <span data-ttu-id="aa5e6-112">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="aa5e6-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="aa5e6-113">Instruções</span><span class="sxs-lookup"><span data-stu-id="aa5e6-113">Instructions</span></span>

### <a name="add-items-to-the-tree-view"></a><span data-ttu-id="aa5e6-114">Adicionar itens ao Tree-View</span><span class="sxs-lookup"><span data-stu-id="aa5e6-114">Add Items to the Tree-View</span></span>

<span data-ttu-id="aa5e6-115">O exemplo nesta seção demonstra como criar um sumário com base nas informações de título do documento que são fornecidas em uma matriz definida pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="aa5e6-115">The example in this section demonstrates how to create a table of contents based on document heading information that is provided in an application-defined array.</span></span> <span data-ttu-id="aa5e6-116">Cada elemento de matriz consiste em uma cadeia de caracteres de título e um inteiro que indica o nível de título.</span><span class="sxs-lookup"><span data-stu-id="aa5e6-116">Each array element consists of a heading string and an integer that indicates the heading level.</span></span> <span data-ttu-id="aa5e6-117">O exemplo dá suporte a três níveis de título (1, 2 e 3).</span><span class="sxs-lookup"><span data-stu-id="aa5e6-117">The example supports three heading levels (1, 2, and 3).</span></span>

<span data-ttu-id="aa5e6-118">O exemplo inclui duas funções.</span><span class="sxs-lookup"><span data-stu-id="aa5e6-118">The example includes two functions.</span></span> <span data-ttu-id="aa5e6-119">A primeira função extrai cada cabeçalho e o nível de título que o acompanha e, em seguida, passa-os para a segunda função.</span><span class="sxs-lookup"><span data-stu-id="aa5e6-119">The first function extracts each heading and accompanying heading level and then passes them to the second function.</span></span>

<span data-ttu-id="aa5e6-120">A segunda função adiciona um item a um controle de exibição de árvore.</span><span class="sxs-lookup"><span data-stu-id="aa5e6-120">The second function adds an item to a tree-view control.</span></span> <span data-ttu-id="aa5e6-121">Ele usa o texto do título como o rótulo do item e usa o nível de título para determinar o item pai do novo item.</span><span class="sxs-lookup"><span data-stu-id="aa5e6-121">It uses the heading text as the item's label, and it uses the heading level to determine the parent item for the new item.</span></span> <span data-ttu-id="aa5e6-122">Um título de nível um é adicionado à raiz do controle de exibição de árvore, um título de nível dois é adicionado como um item filho do nível anterior um item e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="aa5e6-122">A level one heading is added to the root of the tree-view control, a level two heading is added as a child item of the previous level one item, and so on.</span></span> <span data-ttu-id="aa5e6-123">A função atribui uma imagem a um item com base em se ele tem itens filho.</span><span class="sxs-lookup"><span data-stu-id="aa5e6-123">The function assigns an image to an item based on whether it has child items.</span></span> <span data-ttu-id="aa5e6-124">Se um item tiver itens filho, ele obterá uma imagem que representa uma pasta fechada.</span><span class="sxs-lookup"><span data-stu-id="aa5e6-124">If an item has child items, it gets an image that represents a closed folder.</span></span> <span data-ttu-id="aa5e6-125">Caso contrário, ele obtém uma imagem que representa um documento.</span><span class="sxs-lookup"><span data-stu-id="aa5e6-125">Otherwise, it gets an image that represents a document.</span></span> <span data-ttu-id="aa5e6-126">Um item usa a mesma imagem para os Estados selecionados e não selecionados.</span><span class="sxs-lookup"><span data-stu-id="aa5e6-126">An item uses the same image for both the selected and nonselected states.</span></span>


```C++
// Adds items to a tree-view control. 
// Returns the handle to the newly added item. 
// hwndTV - handle to the tree-view control. 
// lpszItem - text of the item to add. 
// nLevel - level at which to add the item. 
//
// g_nClosed, and g_nDocument - global indexes of the images.

HTREEITEM AddItemToTree(HWND hwndTV, LPTSTR lpszItem, int nLevel)
{ 
    TVITEM tvi; 
    TVINSERTSTRUCT tvins; 
    static HTREEITEM hPrev = (HTREEITEM)TVI_FIRST; 
    static HTREEITEM hPrevRootItem = NULL; 
    static HTREEITEM hPrevLev2Item = NULL; 
    HTREEITEM hti; 

    tvi.mask = TVIF_TEXT | TVIF_IMAGE 
               | TVIF_SELECTEDIMAGE | TVIF_PARAM; 

    // Set the text of the item. 
    tvi.pszText = lpszItem; 
    tvi.cchTextMax = sizeof(tvi.pszText)/sizeof(tvi.pszText[0]); 

    // Assume the item is not a parent item, so give it a 
    // document image. 
    tvi.iImage = g_nDocument; 
    tvi.iSelectedImage = g_nDocument; 

    // Save the heading level in the item's application-defined 
    // data area. 
    tvi.lParam = (LPARAM)nLevel; 
    tvins.item = tvi; 
    tvins.hInsertAfter = hPrev; 

    // Set the parent item based on the specified level. 
    if (nLevel == 1) 
        tvins.hParent = TVI_ROOT; 
    else if (nLevel == 2) 
        tvins.hParent = hPrevRootItem; 
    else 
        tvins.hParent = hPrevLev2Item; 

    // Add the item to the tree-view control. 
    hPrev = (HTREEITEM)SendMessage(hwndTV, TVM_INSERTITEM, 
        0, (LPARAM)(LPTVINSERTSTRUCT)&tvins); 

    if (hPrev == NULL)
        return NULL;

    // Save the handle to the item. 
    if (nLevel == 1) 
        hPrevRootItem = hPrev; 
    else if (nLevel == 2) 
        hPrevLev2Item = hPrev; 

    // The new item is a child item. Give the parent item a 
    // closed folder bitmap to indicate it now has child items. 
    if (nLevel > 1)
    { 
        hti = TreeView_GetParent(hwndTV, hPrev); 
        tvi.mask = TVIF_IMAGE | TVIF_SELECTEDIMAGE; 
        tvi.hItem = hti; 
        tvi.iImage = g_nClosed; 
        tvi.iSelectedImage = g_nClosed; 
        TreeView_SetItem(hwndTV, &tvi); 
    } 

    return hPrev; 
} 

// Extracts heading text and heading levels from a global 
// array and passes them to a function that adds them as
// parent and child items to a tree-view control. 
// Returns TRUE if successful, or FALSE otherwise. 
// hwndTV - handle to the tree-view control. 

BOOL InitTreeViewItems(HWND hwndTV)
{ 
    HTREEITEM hti;

    // g_rgDocHeadings is an application-defined global array of 
    // the following structures: 
    //     typedef struct 
    //       { 
    //         TCHAR tchHeading[MAX_HEADING_LEN]; 
    //         int tchLevel; 
    //     } Heading; 
    for (int i = 0; i < ARRAYSIZE(g_rgDocHeadings); i++) 
    { 
        // Add the item to the tree-view control. 
        hti = AddItemToTree(hwndTV, g_rgDocHeadings[i].tchHeading, 
            g_rgDocHeadings[i].tchLevel); 

        if (hti == NULL)
            return FALSE;
    } 
           
    return TRUE; 
}
```



## <a name="related-topics"></a><span data-ttu-id="aa5e6-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="aa5e6-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa5e6-128">Usando controles de Tree-View</span><span class="sxs-lookup"><span data-stu-id="aa5e6-128">Using Tree-View Controls</span></span>](using-treeview.md)
</dt> <dt>

[<span data-ttu-id="aa5e6-129">O exemplo de CustDTv ilustra o desenho personalizado em um controle de Tree-View</span><span class="sxs-lookup"><span data-stu-id="aa5e6-129">CustDTv sample illustrates custom draw in a Tree-View control</span></span>](https://support.microsoft.com/default.aspx?scid=kb;EN-US;q248496)
</dt> </dl>

 

 




