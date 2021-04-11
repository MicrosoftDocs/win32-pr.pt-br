---
title: Controle da barra de status (referência de elemento da interface do usuário do MSAA)
description: Barras de status exibem informações de status em uma janela horizontal na parte inferior de uma janela de aplicativo.
ms.assetid: e910a5c6-84d5-4ade-abf5-792ff1915021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81bddf2898b9b7eca5385d86d6dabc6a50d3d4df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292747"
---
# <a name="status-bar-control-msaa-ui-element-reference"></a><span data-ttu-id="281ad-103">Controle da barra de status (referência de elemento da interface do usuário do MSAA)</span><span class="sxs-lookup"><span data-stu-id="281ad-103">Status Bar Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="281ad-104">Este tópico descreve os objetos de **controle da barra de status** para fins de referência de elemento da interface do usuário do MSAA.</span><span class="sxs-lookup"><span data-stu-id="281ad-104">This topic describes **Status Bar Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="281ad-105">Como criar objetos de **controle da barra de status** em várias estruturas de interface do usuário não é descrito aqui.</span><span class="sxs-lookup"><span data-stu-id="281ad-105">How to create **Status Bar Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="281ad-106">Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.</span><span class="sxs-lookup"><span data-stu-id="281ad-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="281ad-107">Barras de status exibem informações de status em uma janela horizontal na parte inferior de uma janela de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="281ad-107">Status bars display status information in a horizontal window at the bottom of an application window.</span></span> <span data-ttu-id="281ad-108">As barras de status geralmente são divididas em partes, chamadas de painéis e cada painel exibe informações de status diferentes.</span><span class="sxs-lookup"><span data-stu-id="281ad-108">Status bars are often divided into parts, called panes, and each pane displays different status information.</span></span> <span data-ttu-id="281ad-109">Além disso, as barras de status podem conter objetos de tipos diferentes, incluindo botões e barras de progresso.</span><span class="sxs-lookup"><span data-stu-id="281ad-109">Additionally, status bars can contain objects of different types, including buttons and progress bars.</span></span> <span data-ttu-id="281ad-110">O nome da classe de janela para um controle de barra de status é STATUSCLASSNAME, que é definido como "msctls \_ statusbar32" em commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="281ad-110">The window class name for a status bar control is STATUSCLASSNAME, which is defined as "msctls\_statusbar32" in Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="281ad-111">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="281ad-111">IAccessible Methods</span></span>

<span data-ttu-id="281ad-112">Barras de status dão suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="281ad-112">Status bars support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="281ad-113">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="281ad-113">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="281ad-114">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="281ad-114">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="281ad-115">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="281ad-115">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="281ad-116">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="281ad-116">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="281ad-117">Propriedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="281ad-117">IAccessible Properties</span></span>

<span data-ttu-id="281ad-118">Barras de status dão suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="281ad-118">Status bars support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="281ad-119">Propriedade</span><span class="sxs-lookup"><span data-stu-id="281ad-119">Property</span></span>                                                                 | <span data-ttu-id="281ad-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="281ad-120">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="281ad-121">**obter \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="281ad-121">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="281ad-122">A propriedade **ChildCount** é o número de painéis na barra de status.</span><span class="sxs-lookup"><span data-stu-id="281ad-122">The **ChildCount** property is the number of panes in the status bar.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="281ad-123">**obter \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="281ad-123">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="281ad-124">**obter \_ accName**</span><span class="sxs-lookup"><span data-stu-id="281ad-124">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="281ad-125">O próprio objeto da barra de status não tem uma propriedade **Name** .</span><span class="sxs-lookup"><span data-stu-id="281ad-125">The status bar object itself does not have a **Name** property.</span></span> <span data-ttu-id="281ad-126">A propriedade **Name** de cada painel na barra de status é igual ao texto exibido.</span><span class="sxs-lookup"><span data-stu-id="281ad-126">The **Name** property of each pane in the status bar is the same as the displayed text.</span></span>                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="281ad-127">**obter \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="281ad-127">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="281ad-128">A propriedade **Parent** do objeto de barra de status é uma janela [**( \_ \_ janela do sistema de funções**](object-roles.md) ) que circunda o controle e tem o mesmo nome de classe de janela que o controle.</span><span class="sxs-lookup"><span data-stu-id="281ad-128">The **Parent** property of the status bar object is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same window class name as the control.</span></span> <span data-ttu-id="281ad-129">A propriedade **Parent** dos painéis na barra de status é o objeto barra de status.</span><span class="sxs-lookup"><span data-stu-id="281ad-129">The **Parent** property of the panes in the status bar is the status bar object.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="281ad-130">**obter \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="281ad-130">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="281ad-131">A propriedade **role** do próprio objeto da barra de status é o [**sistema de funções \_ \_ STATUSBAR**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="281ad-131">The **Role** property for the status bar object itself is [**ROLE\_SYSTEM\_STATUSBAR**](object-roles.md).</span></span> <span data-ttu-id="281ad-132">O texto exibido em uma barra de status tem o [**sistema de função \_ \_ STATICTEXT**](object-roles.md) como sua propriedade de **função** .</span><span class="sxs-lookup"><span data-stu-id="281ad-132">The text displayed in a status bar has [**ROLE\_SYSTEM\_STATICTEXT**](object-roles.md) as its **Role** property.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="281ad-133">**obter \_ accState**</span><span class="sxs-lookup"><span data-stu-id="281ad-133">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="281ad-134">A propriedade de **estado** é uma combinação de um ou mais dos seguintes [valores](object-state-constants.md): [**estado \_ sistema \_ invisível**](object-state-constants.md) \| [**estado \_ sistema \_ indisponível**](object-state-constants.md) sistema de estado \| [**\_ \_ focalizado**](object-state-constants.md) sistema estado \| [**\_ \_ foco**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="281ad-134">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="notes"></a><span data-ttu-id="281ad-135">Observações</span><span class="sxs-lookup"><span data-stu-id="281ad-135">Notes</span></span>

<span data-ttu-id="281ad-136">Como os atalhos de teclado não têm suporte para controles de barra de status ou áreas de texto em barras de status, [**Get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="281ad-136">Because keyboard shortcuts are not supported for status bar controls or text areas on status bars, [**get\_accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) is not supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="281ad-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="281ad-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="281ad-138">Interface IAccessible</span><span class="sxs-lookup"><span data-stu-id="281ad-138">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





