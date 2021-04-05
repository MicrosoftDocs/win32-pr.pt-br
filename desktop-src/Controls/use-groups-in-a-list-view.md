---
title: Como usar grupos em um List-View
description: Este tópico descreve como criar uma instância de um grupo e adicioná-lo a um controle de exibição de lista.
ms.assetid: 8486B9A2-C519-4912-9E88-3BAFCC4D51CF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec47d73c3e8b808eaf1909bdafb015c7eebc37de
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103824070"
---
# <a name="how-to-use-groups-in-a-list-view"></a><span data-ttu-id="a0e69-103">Como usar grupos em um List-View</span><span class="sxs-lookup"><span data-stu-id="a0e69-103">How to Use Groups in a List-View</span></span>

<span data-ttu-id="a0e69-104">Este tópico descreve como criar uma instância de um grupo e adicioná-lo a um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="a0e69-104">This topic describes how to create an instance of a group and add it to a list-view control.</span></span> <span data-ttu-id="a0e69-105">O agrupamento permite que um usuário organize listas em grupos de itens que são visualmente divididos na página, usando um divisor horizontal e um título de grupo.</span><span class="sxs-lookup"><span data-stu-id="a0e69-105">Grouping allows a user to arrange lists into groups of items that are visually divided on the page, using a horizontal divider and a group title.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="a0e69-106">O que você precisa saber</span><span class="sxs-lookup"><span data-stu-id="a0e69-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="a0e69-107">Tecnologias</span><span class="sxs-lookup"><span data-stu-id="a0e69-107">Technologies</span></span>

-   [<span data-ttu-id="a0e69-108">Controles do Windows</span><span class="sxs-lookup"><span data-stu-id="a0e69-108">Windows Controls</span></span>](window-controls.md)

### <a name="prerequisites"></a><span data-ttu-id="a0e69-109">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="a0e69-109">Prerequisites</span></span>

-   <span data-ttu-id="a0e69-110">C/C++</span><span class="sxs-lookup"><span data-stu-id="a0e69-110">C/C++</span></span>
-   <span data-ttu-id="a0e69-111">Programação da interface do usuário do Windows</span><span class="sxs-lookup"><span data-stu-id="a0e69-111">Windows User Interface Programming</span></span>

## <a name="instructions"></a><span data-ttu-id="a0e69-112">Instruções</span><span class="sxs-lookup"><span data-stu-id="a0e69-112">Instructions</span></span>


<span data-ttu-id="a0e69-113">Para usar grupos em um controle de exibição de lista, verifique se o controle inclui o estilo de janela [**LVS \_ ALIGNTOP**](list-view-window-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="a0e69-113">To use groups in a list-view control, ensure that the control includes the [**LVS\_ALIGNTOP**](list-view-window-styles.md) window style.</span></span>

<span data-ttu-id="a0e69-114">Quando você adiciona um item à lista, você o atribui a um grupo definindo o membro **iGroupId** da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) do item como o valor do membro **iGroupId** da estrutura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) dos grupos.</span><span class="sxs-lookup"><span data-stu-id="a0e69-114">When you add an item to the list, you assign it to a group by setting the **iGroupId** member of the item's [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure to the value of the **iGroupId** member of the groups's [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure.</span></span> <span data-ttu-id="a0e69-115">Um item que não está atribuído a um grupo não aparece na lista quando o modo de exibição de grupo está habilitado.</span><span class="sxs-lookup"><span data-stu-id="a0e69-115">An item that is not assigned to a group does not appear in the list when group view is enabled.</span></span> <span data-ttu-id="a0e69-116">Para habilitar ou desabilitar a exibição de grupo, use a macro [**\_ EnableGroupView do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview) .</span><span class="sxs-lookup"><span data-stu-id="a0e69-116">To enable or disable group view, use the [**ListView\_EnableGroupView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_enablegroupview) macro.</span></span>

<span data-ttu-id="a0e69-117">O exemplo a seguir mostra como criar um grupo com um cabeçalho e adicioná-lo a um controle de exibição de lista.</span><span class="sxs-lookup"><span data-stu-id="a0e69-117">The following example shows how to create a group with a header and add it to a list-view control.</span></span>


```C++
    LVGROUP group;

    group.cbSize    = sizeof(LVGROUP);
    group.mask      = LVGF_HEADER | LVGF_GROUPID;
    group.pszHeader = TEXT("Dogs");
    group.iGroupId  = 1;

    ListView_InsertGroup(hWndListView, -1, &group);

```



## <a name="related-topics"></a><span data-ttu-id="a0e69-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a0e69-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0e69-119">Referência de controle de exibição de lista</span><span class="sxs-lookup"><span data-stu-id="a0e69-119">List-View Control Reference</span></span>](bumper-list-view-list-view-control-reference.md)
</dt> <dt>

[<span data-ttu-id="a0e69-120">Sobre controles de List-View</span><span class="sxs-lookup"><span data-stu-id="a0e69-120">About List-View Controls</span></span>](list-view-controls-overview.md)
</dt> <dt>

[<span data-ttu-id="a0e69-121">Usando controles de List-View</span><span class="sxs-lookup"><span data-stu-id="a0e69-121">Using List-View Controls</span></span>](using-list-view-controls.md)
</dt> </dl>

 

 




