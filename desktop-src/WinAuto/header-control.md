---
title: Controle de cabeçalho (referência de elemento de interface do usuário do MSAA)
description: Um controle de cabeçalho exibe os títulos na parte superior das colunas de informações e permite que o usuário classifique as informações clicando nos títulos. O Windows Explorer usa um controle de cabeçalho quando a exibição detalhes é selecionada.
ms.assetid: 669d6bb8-7bc4-4e6f-bf4f-207887f44b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6d069770b14ad3ba58022af28ad07fc78cb8c5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292549"
---
# <a name="header-control-msaa-ui-element-reference"></a><span data-ttu-id="1605c-104">Controle de cabeçalho (referência de elemento de interface do usuário do MSAA)</span><span class="sxs-lookup"><span data-stu-id="1605c-104">Header Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="1605c-105">Este tópico descreve objetos de **controle de cabeçalho** para fins de referência de elemento da interface do usuário do MSAA.</span><span class="sxs-lookup"><span data-stu-id="1605c-105">This topic describes **Header Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="1605c-106">Como criar objetos de **controle de cabeçalho** em várias estruturas de interface do usuário não é descrito aqui.</span><span class="sxs-lookup"><span data-stu-id="1605c-106">How to create **Header Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="1605c-107">Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.</span><span class="sxs-lookup"><span data-stu-id="1605c-107">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="1605c-108">Um controle de cabeçalho exibe os títulos na parte superior das colunas de informações e permite que o usuário classifique as informações clicando nos títulos.</span><span class="sxs-lookup"><span data-stu-id="1605c-108">A header control displays headings at the top of columns of information and lets the user sort the information by clicking the headings.</span></span> <span data-ttu-id="1605c-109">O Windows Explorer usa um controle de cabeçalho quando a exibição detalhes é selecionada.</span><span class="sxs-lookup"><span data-stu-id="1605c-109">Windows Explorer uses a header control when the Details view is selected.</span></span>

<span data-ttu-id="1605c-110">O nome de classe da janela para um controle de cabeçalho é WC \_ header, que é definido como "SysHeader32" em commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="1605c-110">The window class name for a header control is WC\_HEADER, which is defined as "SysHeader32" in Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="1605c-111">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="1605c-111">IAccessible Methods</span></span>

<span data-ttu-id="1605c-112">Um controle de cabeçalho dá suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="1605c-112">A header control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>



| <span data-ttu-id="1605c-113">Método</span><span class="sxs-lookup"><span data-stu-id="1605c-113">Method</span></span>                                                                    | <span data-ttu-id="1605c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1605c-114">Comments</span></span>                                                        |
|---------------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="1605c-115">**accDoDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="1605c-115">**accDoDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | <span data-ttu-id="1605c-116">Esse método executa a ação padrão clicando no cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="1605c-116">This method performs the default action by clicking the header.</span></span> |
| [<span data-ttu-id="1605c-117">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="1605c-117">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                 |
| [<span data-ttu-id="1605c-118">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="1605c-118">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                 |
| [<span data-ttu-id="1605c-119">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="1605c-119">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                 |
| [<span data-ttu-id="1605c-120">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="1605c-120">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                 |



 

## <a name="iaccessible-properties"></a><span data-ttu-id="1605c-121">Propriedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="1605c-121">IAccessible Properties</span></span>

<span data-ttu-id="1605c-122">Um controle de cabeçalho dá suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="1605c-122">A header control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="1605c-123">Propriedade</span><span class="sxs-lookup"><span data-stu-id="1605c-123">Property</span></span>                                                                       | <span data-ttu-id="1605c-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="1605c-124">Comments</span></span>                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1605c-125">**obter \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="1605c-125">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | <span data-ttu-id="1605c-126">A propriedade **ChildCount** é zero.</span><span class="sxs-lookup"><span data-stu-id="1605c-126">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                                   |
| [<span data-ttu-id="1605c-127">**obter \_ accDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="1605c-127">**get\_accDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | <span data-ttu-id="1605c-128">A propriedade **DefaultAction** é "click".</span><span class="sxs-lookup"><span data-stu-id="1605c-128">The **DefaultAction** property is "Click".</span></span>                                                                                                                                                                                             |
| [<span data-ttu-id="1605c-129">**obter \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="1605c-129">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 |                                                                                                                                                                                                                                        |
| [<span data-ttu-id="1605c-130">**obter \_ accName**</span><span class="sxs-lookup"><span data-stu-id="1605c-130">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | <span data-ttu-id="1605c-131">A propriedade **Name** é igual ao nome do cabeçalho da coluna.</span><span class="sxs-lookup"><span data-stu-id="1605c-131">The **Name** property is the same as the name of the column header.</span></span>                                                                                                                                                                    |
| [<span data-ttu-id="1605c-132">**obter \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="1605c-132">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)               | <span data-ttu-id="1605c-133">A propriedade **Parent** é uma janela ( [**\_ \_ lista de sistema de funções**](object-roles.md) ) que circunda o controle e tem o mesmo nome de classe de janela que o controle.</span><span class="sxs-lookup"><span data-stu-id="1605c-133">The **Parent** property is a window ( [**ROLE\_SYSTEM\_LIST**](object-roles.md) ) that surrounds the control and has the same window class name as the control.</span></span>                                                      |
| [<span data-ttu-id="1605c-134">**obter \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="1605c-134">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | <span data-ttu-id="1605c-135">A propriedade **role** é o [**sistema de função \_ \_ COLUMNHEADER**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1605c-135">The **Role** property is [**ROLE\_SYSTEM\_COLUMNHEADER**](object-roles.md).</span></span>                                                                                                                                  |
| [<span data-ttu-id="1605c-136">**obter \_ accState**</span><span class="sxs-lookup"><span data-stu-id="1605c-136">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | <span data-ttu-id="1605c-137">O valor da propriedade **estado** é sempre [**estado \_ sistema \_ ReadOnly**](object-state-constants.md) e também pode incluir o [**estado do \_ sistema \_ invisível**](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="1605c-137">The value for the **State** property is always [**STATE\_SYSTEM\_READONLY**](object-state-constants.md) and can also include [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="1605c-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1605c-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1605c-139">Interface IAccessible</span><span class="sxs-lookup"><span data-stu-id="1605c-139">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




