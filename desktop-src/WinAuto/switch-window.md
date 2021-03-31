---
title: Alternar janela (referência de elemento de interface do usuário do MSAA)
description: A janela comutador é exibida sempre que um usuário pressiona ALT + TAB para alternar para um aplicativo diferente. A janela switch contém um ícone para cada aplicativo em execução no momento.
ms.assetid: 77b32eb1-7722-410b-b141-ac09fc7fdffb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eead618e23f8a56c90b37eae2386f16a90f6dd67
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637111"
---
# <a name="switch-window-msaa-ui-element-reference"></a><span data-ttu-id="c5c31-104">Alternar janela (referência de elemento de interface do usuário do MSAA)</span><span class="sxs-lookup"><span data-stu-id="c5c31-104">Switch Window (MSAA UI Element Reference)</span></span>

<span data-ttu-id="c5c31-105">A janela comutador é exibida sempre que um usuário pressiona ALT + TAB para alternar para um aplicativo diferente.</span><span class="sxs-lookup"><span data-stu-id="c5c31-105">The switch window displays whenever a user presses ALT+TAB to switch to a different application.</span></span> <span data-ttu-id="c5c31-106">A janela switch contém um ícone para cada aplicativo em execução no momento.</span><span class="sxs-lookup"><span data-stu-id="c5c31-106">The switch window contains an icon for each application currently running.</span></span>

<span data-ttu-id="c5c31-107">O nome da classe de janela da janela de comutador é " \# 32771".</span><span class="sxs-lookup"><span data-stu-id="c5c31-107">The window class name for the switch window is "\#32771".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="c5c31-108">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="c5c31-108">IAccessible Methods</span></span>

<span data-ttu-id="c5c31-109">A janela switch dá suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="c5c31-109">The switch window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>



| <span data-ttu-id="c5c31-110">Método</span><span class="sxs-lookup"><span data-stu-id="c5c31-110">Method</span></span>                                                                    | <span data-ttu-id="c5c31-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5c31-111">Comments</span></span>                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5c31-112">**accDoDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="c5c31-112">**accDoDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | <span data-ttu-id="c5c31-113">O objeto de janela de opção em si não tem uma propriedade **DefaultAction** .</span><span class="sxs-lookup"><span data-stu-id="c5c31-113">The switch window object itself does not have a **DefaultAction** property.</span></span> <span data-ttu-id="c5c31-114">O método [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) para cada item na janela de comutador ativa o item especificado.</span><span class="sxs-lookup"><span data-stu-id="c5c31-114">The [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) method for each item in the switch window activates the specified item.</span></span> |
| [<span data-ttu-id="c5c31-115">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="c5c31-115">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="c5c31-116">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="c5c31-116">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="c5c31-117">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="c5c31-117">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="c5c31-118">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="c5c31-118">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                   |



 

## <a name="iaccessible-properties"></a><span data-ttu-id="c5c31-119">Propriedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="c5c31-119">IAccessible Properties</span></span>

<span data-ttu-id="c5c31-120">A janela switch dá suporte às seguintes propriedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="c5c31-120">The switch window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



|                                                                                |                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5c31-121">**obter \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="c5c31-121">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | <span data-ttu-id="c5c31-122">A propriedade **ChildCount** é zero.</span><span class="sxs-lookup"><span data-stu-id="c5c31-122">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="c5c31-123">**obter \_ accDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="c5c31-123">**get\_accDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | <span data-ttu-id="c5c31-124">O objeto de janela de opção em si não tem uma propriedade **DefaultAction** .</span><span class="sxs-lookup"><span data-stu-id="c5c31-124">The switch window object itself does not have a **DefaultAction** property.</span></span> <span data-ttu-id="c5c31-125">A propriedade **DefaultAction** para cada item na janela switch é "switch".</span><span class="sxs-lookup"><span data-stu-id="c5c31-125">The **DefaultAction** property for each item in the switch window is "Switch".</span></span>                                                                     |
| [<span data-ttu-id="c5c31-126">**obter \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="c5c31-126">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 | <span data-ttu-id="c5c31-127">O objeto pai da janela de comutador não pode receber o foco; somente os filhos individuais podem receber o foco.</span><span class="sxs-lookup"><span data-stu-id="c5c31-127">The switch window parent object cannot receive focus; only the individual children can receive focus.</span></span>                                                                                                                          |
| [<span data-ttu-id="c5c31-128">**obter \_ accName**</span><span class="sxs-lookup"><span data-stu-id="c5c31-128">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | <span data-ttu-id="c5c31-129">O objeto de janela de opção em si não tem uma propriedade **Name** .</span><span class="sxs-lookup"><span data-stu-id="c5c31-129">The switch window object itself does not have a **Name** property.</span></span> <span data-ttu-id="c5c31-130">A propriedade **Name** para cada ícone de aplicativo na janela switch é igual ao nome do aplicativo exibido.</span><span class="sxs-lookup"><span data-stu-id="c5c31-130">The **Name** property for each application icon in the switch window is the same as the displayed application name.</span></span>                                         |
| [<span data-ttu-id="c5c31-131">**obter \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="c5c31-131">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | <span data-ttu-id="c5c31-132">O próprio objeto Window do switch tem uma propriedade **role** de "Window \[ 32771 \] ".</span><span class="sxs-lookup"><span data-stu-id="c5c31-132">The switch window object itself has a **Role** property of "window \[32771\]".</span></span> <span data-ttu-id="c5c31-133">Além disso, cada ícone de aplicativo na **janela de comutador tem a função** de Propriedade do [**\_ sistema \_ ListItem**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="c5c31-133">Also, each application icon in the switch window has the **Role** property [**ROLE\_SYSTEM\_LISTITEM**](object-roles.md).</span></span> |
| [<span data-ttu-id="c5c31-134">**obter \_ accState**</span><span class="sxs-lookup"><span data-stu-id="c5c31-134">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | <span data-ttu-id="c5c31-135">O objeto de janela de switch em si não oferece suporte à propriedade **State** .</span><span class="sxs-lookup"><span data-stu-id="c5c31-135">The switch window object itself does not support the **State** property.</span></span> <span data-ttu-id="c5c31-136">O valor de **estado** para os itens de exibição de lista é de [**estado do \_ sistema \_**](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="c5c31-136">The **State** value for the list view items is [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md).</span></span>                     |



 

## <a name="related-topics"></a><span data-ttu-id="c5c31-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c5c31-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5c31-138">Interface IAccessible</span><span class="sxs-lookup"><span data-stu-id="c5c31-138">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




