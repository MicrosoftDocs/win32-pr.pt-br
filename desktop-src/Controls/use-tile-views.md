---
title: Como usar exibições de bloco
description: Este tópico demonstra como definir o modo de exibição de bloco para um controle de exibição de lista.
ms.assetid: BDE17F4B-3A15-48BB-8160-036AD0DC3B41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616a9bb8a2c1707d903f0ebe2b6de86511dc6ce4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103917793"
---
# <a name="how-to-use-tile-views"></a><span data-ttu-id="98719-103">Como usar exibições de bloco</span><span class="sxs-lookup"><span data-stu-id="98719-103">How to Use Tile Views</span></span>

<span data-ttu-id="98719-104">Este tópico demonstra como definir o modo de exibição de bloco para um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="98719-104">This topic demonstrates how to set the tile view for a list-view control.</span></span> <span data-ttu-id="98719-105">No modo de exibição de bloco, cada item é representado por um ícone grande com uma ou mais linhas do texto que o acompanha.</span><span class="sxs-lookup"><span data-stu-id="98719-105">In tile view, each item is represented by a large icon with one or more lines of accompanying text.</span></span> <span data-ttu-id="98719-106">Para obter uma ilustração, consulte [sobre controles de List-View](list-view-controls-overview.md).</span><span class="sxs-lookup"><span data-stu-id="98719-106">For an illustration, see [About List-View Controls](list-view-controls-overview.md).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="98719-107">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="98719-107">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="98719-108">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="98719-108">Technologies</span></span>

-   [<span data-ttu-id="98719-109">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="98719-109">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="98719-110">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="98719-110">Prerequisites</span></span>

-   <span data-ttu-id="98719-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="98719-111">C/C++</span></span>
-   <span data-ttu-id="98719-112">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="98719-112">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="98719-113">Instruções</span><span class="sxs-lookup"><span data-stu-id="98719-113">Instructions</span></span>


<span data-ttu-id="98719-114">Defina os parâmetros de exibição gerais para exibição de bloco usando a macro [**\_ SetTileViewInfo do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileviewinfo) .</span><span class="sxs-lookup"><span data-stu-id="98719-114">Set the general display parameters for tile view by using the [**ListView\_SetTileViewInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileviewinfo) macro.</span></span> <span data-ttu-id="98719-115">Use a estrutura [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo) que é passada para esta macro para especificar a posição do texto em relação ao ícone, o tamanho de cada bloco (incluindo o texto de acompanhamento) e o número máximo de linhas de texto.</span><span class="sxs-lookup"><span data-stu-id="98719-115">Use the [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo) structure that is passed to this macro to specify the position of the text in relation to the icon, the size of each tile (including accompanying text), and the maximum number of lines of text.</span></span>

<span data-ttu-id="98719-116">Se você não quiser que os blocos sejam dimensionados automaticamente, você deve definir **LVTVIF \_ FIXEDSIZE** no membro **dwFlags** e **LVTVIM \_ tileize** no membro **dwMask** de [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo), bem como fornecendo as dimensões no membro **sizeTile** .</span><span class="sxs-lookup"><span data-stu-id="98719-116">If you do not want tiles to be automatically sized, you must set **LVTVIF\_FIXEDSIZE** in the **dwFlags** member and **LVTVIM\_TILESIZE** in the **dwMask** member of [**LVTILEVIEWINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo), as well as providing the dimensions in the **sizeTile** member.</span></span>

<span data-ttu-id="98719-117">O exemplo de código C++ a seguir define as informações de exibição de bloco para um controle de exibição de lista para que um máximo de dois subitens sejam exibidos para cada item.</span><span class="sxs-lookup"><span data-stu-id="98719-117">The following C++ code example sets the tile view info for a list-view control so that a maximum of two subitems are displayed for each item.</span></span> <span data-ttu-id="98719-118">Ele também define o tamanho de cada bloco.</span><span class="sxs-lookup"><span data-stu-id="98719-118">It also sets the size of each tile.</span></span>


```C++
    SIZE size = { 100, 50 };
    LVTILEVIEWINFO tileViewInfo = {0};

    tileViewInfo.cbSize   = sizeof(tileViewInfo);
    tileViewInfo.dwFlags  = LVTVIF_FIXEDSIZE;
    tileViewInfo.dwMask   = LVTVIM_COLUMNS | LVTVIM_TILESIZE;
    tileViewInfo.cLines   = 2;
    tileViewInfo.sizeTile = size;

    ListView_SetTileViewInfo(hWndListView, &tileViewInfo);

```



<span data-ttu-id="98719-119">Para cada item na lista, você pode definir parâmetros adicionais quando o item é inserido na lista ou posteriormente.</span><span class="sxs-lookup"><span data-stu-id="98719-119">For each item in the list, you can set further parameters when the item is inserted in the list, or later.</span></span> <span data-ttu-id="98719-120">A estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) que é usada com [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) contém membros que especificam quais colunas de dados serão exibidas abaixo do item e seu alinhamento.</span><span class="sxs-lookup"><span data-stu-id="98719-120">The [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure that is used with [**ListView\_InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) contains members that specify which columns of data to display below the item, and their alignment.</span></span> <span data-ttu-id="98719-121">Esses mesmos parâmetros de exibição também são encontrados na estrutura [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) usada com [**ListView \_ SetTileInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileinfo).</span><span class="sxs-lookup"><span data-stu-id="98719-121">These same display parameters are also found in the [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) structure used with [**ListView\_SetTileInfo**](/windows/desktop/api/Commctrl/nf-commctrl-listview_settileinfo).</span></span>

> [!Note]  
> <span data-ttu-id="98719-122">"Columns" aqui refere-se a não exibir colunas no modo de exibição de bloco, mas em subitens, que são exibidos em colunas na exibição de detalhes.</span><span class="sxs-lookup"><span data-stu-id="98719-122">"Columns" here refers not to display columns in tile view but rather to subitems, which are displayed in columns in details view.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="98719-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="98719-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98719-124">Referência de controle de exibição de lista</span><span class="sxs-lookup"><span data-stu-id="98719-124">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="98719-125">Sobre controles de List-View</span><span class="sxs-lookup"><span data-stu-id="98719-125">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="98719-126">Usando controles de List-View</span><span class="sxs-lookup"><span data-stu-id="98719-126">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




