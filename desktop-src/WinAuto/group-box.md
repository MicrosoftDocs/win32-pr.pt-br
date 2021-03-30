---
title: Caixa de grupo (referência de elemento de interface do usuário do MSAA)
description: Uma caixa de grupo é um retângulo que circunda um conjunto de controles, como caixas de seleção ou botões de opção, e contém um texto definido pelo aplicativo (rótulo).
ms.assetid: c6cd81a1-76c0-41c5-bb7f-4796ea7e3114
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a105242aabd49d87241a2a49bdaca5c19edd350b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636592"
---
# <a name="group-box-msaa-ui-element-reference"></a><span data-ttu-id="1d385-103">Caixa de grupo (referência de elemento de interface do usuário do MSAA)</span><span class="sxs-lookup"><span data-stu-id="1d385-103">Group Box (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="1d385-104">Este tópico descreve os objetos da **caixa de grupo** para fins de referência de elemento da interface do usuário do MSAA.</span><span class="sxs-lookup"><span data-stu-id="1d385-104">This topic describes **Group Box** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="1d385-105">A criação de objetos de **caixa de grupo** em várias estruturas de interface do usuário não é descrita aqui.</span><span class="sxs-lookup"><span data-stu-id="1d385-105">How to create **Group Box** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="1d385-106">Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.</span><span class="sxs-lookup"><span data-stu-id="1d385-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="1d385-107">Uma caixa de grupo é um retângulo que circunda um conjunto de controles, como caixas de seleção ou botões de opção, e contém um texto definido pelo aplicativo (rótulo).</span><span class="sxs-lookup"><span data-stu-id="1d385-107">A group box is a rectangle that surrounds a set of controls, such as check boxes or radio buttons, and contains an application-defined text (label).</span></span>

<span data-ttu-id="1d385-108">A única finalidade de uma caixa de grupo é organizar os controles relacionados por uma finalidade comum, indicada pelo rótulo.</span><span class="sxs-lookup"><span data-stu-id="1d385-108">The sole purpose of a group box is to organize controls related by a common purpose, indicated by the label.</span></span>

<span data-ttu-id="1d385-109">O nome da classe de janela para uma caixa de grupo é "BUTTON".</span><span class="sxs-lookup"><span data-stu-id="1d385-109">The window class name for a group box is "BUTTON".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="1d385-110">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="1d385-110">IAccessible Methods</span></span>

<span data-ttu-id="1d385-111">Uma caixa de grupo dá suporte aos seguintes métodos de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="1d385-111">A group box supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="1d385-112">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="1d385-112">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="1d385-113">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="1d385-113">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="1d385-114">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="1d385-114">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a><span data-ttu-id="1d385-115">Propriedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="1d385-115">IAccessible Properties</span></span>

<span data-ttu-id="1d385-116">Uma caixa de grupo dá suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="1d385-116">A group box supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="1d385-117">Propriedade</span><span class="sxs-lookup"><span data-stu-id="1d385-117">Property</span></span>                                                                             | <span data-ttu-id="1d385-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d385-118">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1d385-119">**obter \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="1d385-119">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | <span data-ttu-id="1d385-120">A propriedade **ChildCount** é sempre zero.</span><span class="sxs-lookup"><span data-stu-id="1d385-120">The **ChildCount** property is always zero.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="1d385-121">**obter \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="1d385-121">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="1d385-122">**obter \_ accKeyboardShortcut**</span><span class="sxs-lookup"><span data-stu-id="1d385-122">**get\_accKeyboardShortcut**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | <span data-ttu-id="1d385-123">As caixas de grupo não têm atalhos de teclado.</span><span class="sxs-lookup"><span data-stu-id="1d385-123">Group boxes do not have keyboard shortcuts.</span></span> <span data-ttu-id="1d385-124">No entanto, se o texto da janela da caixa de grupo contiver um caractere de e comercial (&), o Microsoft Acessibilidade Ativa retornará uma cadeia de caracteres não nula como a propriedade **KeyboardShortcut** .</span><span class="sxs-lookup"><span data-stu-id="1d385-124">However, if the window text for the group box contains an ampersand (&) character, Microsoft Active Accessibility returns a non-Null string as the **KeyboardShortcut** property.</span></span>                                                                                                                                                                                                                                            |
| [<span data-ttu-id="1d385-125">**obter \_ accName**</span><span class="sxs-lookup"><span data-stu-id="1d385-125">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | <span data-ttu-id="1d385-126">A propriedade **Name** é obtida no texto da janela do controle (ou legenda), que é exibido com a caixa de grupo.</span><span class="sxs-lookup"><span data-stu-id="1d385-126">The **Name** property is obtained from the control's window text (or caption), which is displayed with the group box.</span></span>                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="1d385-127">**obter \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="1d385-127">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | <span data-ttu-id="1d385-128">A propriedade **Parent** é uma janela ( [**\_ \_ janela do sistema de funções**](object-roles.md) ) que circunda o controle e tem a mesma propriedade **Name** e o nome da classe Window que o controle.</span><span class="sxs-lookup"><span data-stu-id="1d385-128">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span>                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="1d385-129">**obter \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="1d385-129">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | <span data-ttu-id="1d385-130">A propriedade **role** é [**\_ \_ agrupamento do sistema de funções**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="1d385-130">The **Role** property is [**ROLE\_SYSTEM\_GROUPING**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="1d385-131">**obter \_ accState**</span><span class="sxs-lookup"><span data-stu-id="1d385-131">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | <span data-ttu-id="1d385-132">A propriedade de **estado** é uma combinação de um ou mais dos seguintes [valores](object-state-constants.md):[**estado \_ sistema \_ invisível**](object-state-constants.md) \| [**estado \_ sistema \_ indisponível**](object-state-constants.md) sistema de estado \| [**\_ \_ focalizado**](object-state-constants.md) sistema estado \| [**\_ \_ foco**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="1d385-132">The **State** property is a combination of one or more of the following [values](object-state-constants.md):[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="1d385-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1d385-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d385-134">Interface IAccessible</span><span class="sxs-lookup"><span data-stu-id="1d385-134">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





