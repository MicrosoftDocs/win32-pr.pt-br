---
title: Controle ToolTip (referência de elemento de interface do usuário do MSAA)
description: Um controle ToolTip exibe uma pequena janela pop-up que contém uma linha de texto que descreve a finalidade de uma ferramenta, representada como um objeto gráfico, em um aplicativo.
ms.assetid: d3a65d7b-b882-4a1a-bac2-6995b64cf4af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37557fd116084fc9ac53e8567afc90eda339750d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822640"
---
# <a name="tooltip-control-msaa-ui-element-reference"></a><span data-ttu-id="05c6e-103">Controle ToolTip (referência de elemento de interface do usuário do MSAA)</span><span class="sxs-lookup"><span data-stu-id="05c6e-103">ToolTip Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="05c6e-104">Este tópico descreve objetos de **controle de dica de ferramenta** para fins de referência de elemento da interface do usuário do MSAA.</span><span class="sxs-lookup"><span data-stu-id="05c6e-104">This topic describes **ToolTip Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="05c6e-105">Como criar objetos de **controle de dica de ferramenta** em várias estruturas de interface do usuário não é descrito aqui.</span><span class="sxs-lookup"><span data-stu-id="05c6e-105">How to create **ToolTip Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="05c6e-106">Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.</span><span class="sxs-lookup"><span data-stu-id="05c6e-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="05c6e-107">Um controle ToolTip exibe uma pequena janela pop-up que contém uma linha de texto que descreve a finalidade de uma ferramenta, representada como um objeto gráfico, em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="05c6e-107">A tooltip control displays a small pop-up window that contains a line of text that describes the purpose of a tool, represented as a graphical object, in an application.</span></span>

<span data-ttu-id="05c6e-108">O nome da classe da janela para uma dica de ferramenta é a classe TOOLTIPs \_ , que é definida como "classe tooltips \_ " em commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="05c6e-108">The window class name for a tooltip is TOOLTIPS\_CLASS, which is defined as "tooltips\_class" in Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="05c6e-109">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="05c6e-109">IAccessible Methods</span></span>

<span data-ttu-id="05c6e-110">Um controle ToolTip dá suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="05c6e-110">A tooltip control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="05c6e-111">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="05c6e-111">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="05c6e-112">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="05c6e-112">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="05c6e-113">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="05c6e-113">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="05c6e-114">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="05c6e-114">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="05c6e-115">Propriedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="05c6e-115">IAccessible Properties</span></span>

<span data-ttu-id="05c6e-116">Um controle ToolTip dá suporte às seguintes propriedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="05c6e-116">A tooltip control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="05c6e-117">Propriedade</span><span class="sxs-lookup"><span data-stu-id="05c6e-117">Property</span></span>                                                                 | <span data-ttu-id="05c6e-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="05c6e-118">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="05c6e-119">**obter \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="05c6e-119">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="05c6e-120">A propriedade **ChildCount** é zero.</span><span class="sxs-lookup"><span data-stu-id="05c6e-120">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="05c6e-121">**obter \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="05c6e-121">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="05c6e-122">**obter \_ accName**</span><span class="sxs-lookup"><span data-stu-id="05c6e-122">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="05c6e-123">A propriedade **Name** é o texto contido no controle ToolTip.</span><span class="sxs-lookup"><span data-stu-id="05c6e-123">The **Name** property is the text contained in the tooltip control.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="05c6e-124">**obter \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="05c6e-124">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="05c6e-125">A propriedade **Parent** é uma janela ( [**\_ \_ janela do sistema de funções**](object-roles.md) ) que circunda o controle e tem a mesma propriedade **Name** e o nome da classe Window que o controle.</span><span class="sxs-lookup"><span data-stu-id="05c6e-125">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="05c6e-126">**obter \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="05c6e-126">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="05c6e-127">A propriedade **role** é [**\_ \_ TOOLTIP do sistema de função**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="05c6e-127">The **Role** property is [**ROLE\_SYSTEM\_TOOLTIP**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="05c6e-128">**obter \_ accState**</span><span class="sxs-lookup"><span data-stu-id="05c6e-128">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="05c6e-129">A propriedade de **estado** é uma combinação de um ou mais dos seguintes [valores](object-state-constants.md): [**estado \_ sistema \_ invisível**](object-state-constants.md) \| [**estado \_ sistema \_ indisponível**](object-state-constants.md) sistema de estado \| [**\_ \_ focalizado**](object-state-constants.md) sistema estado \| [**\_ \_ foco**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="05c6e-129">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="05c6e-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="05c6e-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05c6e-131">Interface IAccessible</span><span class="sxs-lookup"><span data-stu-id="05c6e-131">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





