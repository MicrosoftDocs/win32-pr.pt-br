---
title: Janela da área de trabalho (referência de elemento de interface do usuário MSAA)
description: A janela da área de trabalho exibe o modo de exibição de lista de desktops (que contém ícones como Meu Computador) e a barra de tarefas que contém o botão Iniciar.
ms.assetid: 3668c26e-6462-4219-95d3-507811ed7f3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d58208b3993964a367d093174d58d705beda23d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363754"
---
# <a name="desktop-window-msaa-ui-element-reference"></a><span data-ttu-id="fd3cc-103">Janela da área de trabalho (referência de elemento de interface do usuário MSAA)</span><span class="sxs-lookup"><span data-stu-id="fd3cc-103">Desktop Window (MSAA UI Element Reference)</span></span>

<span data-ttu-id="fd3cc-104">A janela da área de trabalho exibe o modo de exibição de lista de desktops (que contém ícones como Meu Computador) e a barra de tarefas que contém o botão **Iniciar** .</span><span class="sxs-lookup"><span data-stu-id="fd3cc-104">The desktop window displays the desktop list view (which contains icons such as My Computer) and the taskbar that contains the **Start** button.</span></span>

<span data-ttu-id="fd3cc-105">Esse objeto raramente é consultado pelos clientes, pois a exibição de lista e a barra de tarefas cobrem toda a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="fd3cc-105">This object is rarely queried by clients because the list view and the taskbar cover the entire desktop.</span></span> <span data-ttu-id="fd3cc-106">O objeto da área de trabalho é recuperado quando você faz logon, antes de o Shell do sistema operacional exibir o modo de exibição de lista e a barra de tarefas.</span><span class="sxs-lookup"><span data-stu-id="fd3cc-106">The desktop object is retrieved when you log on, before the operating system shell displays the list view and taskbar.</span></span> <span data-ttu-id="fd3cc-107">Em alguns casos, a área de trabalho é obtida ao navegar de outros objetos.</span><span class="sxs-lookup"><span data-stu-id="fd3cc-107">In some cases, the desktop is obtained when navigating from other objects.</span></span>

<span data-ttu-id="fd3cc-108">O nome da classe da janela da área de trabalho é " \# 32769".</span><span class="sxs-lookup"><span data-stu-id="fd3cc-108">The window class name for the desktop window is "\#32769".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="fd3cc-109">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="fd3cc-109">IAccessible Methods</span></span>

<span data-ttu-id="fd3cc-110">A janela da área de trabalho dá suporte aos seguintes métodos de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="fd3cc-110">The desktop window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="fd3cc-111">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="fd3cc-111">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="fd3cc-112">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="fd3cc-112">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="fd3cc-113">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="fd3cc-113">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="fd3cc-114">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="fd3cc-114">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="fd3cc-115">Propriedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="fd3cc-115">IAccessible Properties</span></span>

<span data-ttu-id="fd3cc-116">A janela da área de trabalho dá suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="fd3cc-116">The desktop window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="fd3cc-117">Propriedade</span><span class="sxs-lookup"><span data-stu-id="fd3cc-117">Property</span></span>                                                                 | <span data-ttu-id="fd3cc-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd3cc-118">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fd3cc-119">**obter \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="fd3cc-119">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="fd3cc-120">**obter \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="fd3cc-120">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="fd3cc-121">**obter \_ accName**</span><span class="sxs-lookup"><span data-stu-id="fd3cc-121">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="fd3cc-122">A propriedade Name é "desktop".</span><span class="sxs-lookup"><span data-stu-id="fd3cc-122">The Name property is "Desktop".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="fd3cc-123">**obter \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="fd3cc-123">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="fd3cc-124">A propriedade **role** é [**\_ \_ cliente do sistema de função**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="fd3cc-124">The **Role** property is [**ROLE\_SYSTEM\_CLIENT**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="fd3cc-125">**obter \_ accSelection**</span><span class="sxs-lookup"><span data-stu-id="fd3cc-125">**get\_accSelection**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="fd3cc-126">**obter \_ accState**</span><span class="sxs-lookup"><span data-stu-id="fd3cc-126">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="fd3cc-127">A propriedade de **estado** é uma combinação de um ou mais dos seguintes [valores](object-state-constants.md):[**estado \_ sistema \_ invisível**](object-state-constants.md) \| [**estado \_ sistema \_ indisponível**](object-state-constants.md) sistema de estado \| [**\_ \_ focalizado**](object-state-constants.md) sistema estado \| [**\_ \_ foco**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="fd3cc-127">The **State** property is a combination of one or more of the following [values](object-state-constants.md):[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="fd3cc-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fd3cc-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd3cc-129">Interface IAccessible</span><span class="sxs-lookup"><span data-stu-id="fd3cc-129">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





