---
title: Menu pop-up (referência de elemento de interface do usuário do MSAA)
description: Um menu pop-up exibe uma lista de comandos de menu.
ms.assetid: 9dbfa2d7-a086-4348-8b84-7e36d33e2d27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785fe8ac7a70352116b3a77cf30034092de04a23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822808"
---
# <a name="pop-up-menu-msaa-ui-element-reference"></a><span data-ttu-id="4aa74-103">Menu pop-up (referência de elemento de interface do usuário do MSAA)</span><span class="sxs-lookup"><span data-stu-id="4aa74-103">Pop-up Menu (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="4aa74-104">Este tópico descreve os objetos de **menu pop-up** para fins de referência de elemento da interface do usuário do MSAA.</span><span class="sxs-lookup"><span data-stu-id="4aa74-104">This topic describes **Pop-up Menu** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="4aa74-105">Como criar objetos de **menu pop-up** em várias estruturas de interface do usuário não é descrito aqui.</span><span class="sxs-lookup"><span data-stu-id="4aa74-105">How to create **Pop-up Menu** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="4aa74-106">Consulte a documentação de referência da API para a estrutura de interface do usuário que você está usando.</span><span class="sxs-lookup"><span data-stu-id="4aa74-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="4aa74-107">Um menu pop-up exibe uma lista de comandos de menu.</span><span class="sxs-lookup"><span data-stu-id="4aa74-107">A pop-up menu displays a list of menu commands.</span></span> <span data-ttu-id="4aa74-108">O Microsoft Acessibilidade Ativa cria um objeto pop-up de menu quando um item de menu em uma barra de menus é aberto.</span><span class="sxs-lookup"><span data-stu-id="4aa74-108">Microsoft Active Accessibility creates a menu pop-up object when a menu item in a menu bar is opened.</span></span> <span data-ttu-id="4aa74-109">O Microsoft Acessibilidade Ativa também cria objetos pop-up de menu para menus de contexto, que são exibidos quando o usuário clica com o botão direito do mouse em um elemento de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="4aa74-109">Microsoft Active Accessibility also creates menu pop-up objects for context menus, which are displayed when the user right-clicks a user interface element.</span></span>

<span data-ttu-id="4aa74-110">O nome da classe de janela para um menu pop-up é " \# 32768".</span><span class="sxs-lookup"><span data-stu-id="4aa74-110">The window class name for a pop-up menu is "\#32768".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="4aa74-111">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="4aa74-111">IAccessible Methods</span></span>

<span data-ttu-id="4aa74-112">Um menu pop-up dá suporte aos seguintes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="4aa74-112">A pop-up menu supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="4aa74-113">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="4aa74-113">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="4aa74-114">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="4aa74-114">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="4aa74-115">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="4aa74-115">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="4aa74-116">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="4aa74-116">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="4aa74-117">Propriedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="4aa74-117">IAccessible Properties</span></span>

<span data-ttu-id="4aa74-118">Um menu pop-up dá suporte às seguintes propriedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="4aa74-118">A pop-up menu supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="4aa74-119">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4aa74-119">Property</span></span>                                                                 | <span data-ttu-id="4aa74-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="4aa74-120">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4aa74-121">**obter \_ accChild**</span><span class="sxs-lookup"><span data-stu-id="4aa74-121">**get\_accChild**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           | <span data-ttu-id="4aa74-122">Recupera o [**IDispatch**](idispatch-interface.md) para o item de menu especificado.</span><span class="sxs-lookup"><span data-stu-id="4aa74-122">Retrieves the [**IDispatch**](idispatch-interface.md) for the specified menu item.</span></span> <span data-ttu-id="4aa74-123">As IDs filho para os itens de menu são numeradas em sequência, de cima para baixo, começando com uma.</span><span class="sxs-lookup"><span data-stu-id="4aa74-123">The child IDs for the menu items are numbered sequentially from top to bottom starting with one.</span></span>                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="4aa74-124">**obter \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="4aa74-124">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="4aa74-125">A propriedade **ChildCount** é o número de itens de menu no menu, incluindo separadores de menu.</span><span class="sxs-lookup"><span data-stu-id="4aa74-125">The **ChildCount** property is the number of menu items in the menu, including menu separators.</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="4aa74-126">**obter \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="4aa74-126">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="4aa74-127">**obter \_ accName**</span><span class="sxs-lookup"><span data-stu-id="4aa74-127">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="4aa74-128">A propriedade **Name** para um menu pop-up é o mesmo nome que o menu.</span><span class="sxs-lookup"><span data-stu-id="4aa74-128">The **Name** property for a pop-up menu is the same name as the menu.</span></span> <span data-ttu-id="4aa74-129">A propriedade **Name** de um menu de contexto é "Context".</span><span class="sxs-lookup"><span data-stu-id="4aa74-129">The **Name** property for a context menu is "Context".</span></span>                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="4aa74-130">**obter \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="4aa74-130">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="4aa74-131">A propriedade **Parent** é uma janela ( [**\_ \_ janela do sistema de funções**](object-roles.md) ) que envolve o menu pop-up e tem a mesma propriedade de **nome** e nome de classe de janela que o menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="4aa74-131">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the pop-up menu and has the same **Name** property and window class name as the pop-up menu .</span></span>                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="4aa74-132">**obter \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="4aa74-132">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="4aa74-133">A propriedade **role** é [**\_ System role \_ MENUPOPUP**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4aa74-133">The **Role** property is [**ROLE\_SYSTEM\_MENUPOPUP**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="4aa74-134">**obter \_ accState**</span><span class="sxs-lookup"><span data-stu-id="4aa74-134">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="4aa74-135">A propriedade de **estado** é uma combinação de um ou mais dos seguintes [valores](object-state-constants.md): [**estado \_ sistema \_ invisível**](object-state-constants.md) \| [**estado \_ sistema \_ indisponível**](object-state-constants.md) sistema de estado \| [**\_ \_ focalizado**](object-state-constants.md) sistema estado \| [**\_ \_ foco**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="4aa74-135">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="notes"></a><span data-ttu-id="4aa74-136">Observações</span><span class="sxs-lookup"><span data-stu-id="4aa74-136">Notes</span></span>

-   <span data-ttu-id="4aa74-137">Os objetos de menu pop-up não disparam eventos de [**\_ \_ criação de objeto de evento**](event-constants.md) e [**\_ \_ destruição de objeto de evento**](event-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="4aa74-137">Pop-up menu objects do not trigger [**EVENT\_OBJECT\_CREATE**](event-constants.md) and [**EVENT\_OBJECT\_DESTROY**](event-constants.md) events.</span></span>
-   <span data-ttu-id="4aa74-138">Os menus de várias colunas não dão suporte aos sinalizadores [**NAVDIR \_ esquerdo**](navigation-constants.md) ou [**NAVDIR \_ direito**](navigation-constants.md) do método [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) .</span><span class="sxs-lookup"><span data-stu-id="4aa74-138">Multi-column menus do not support the [**NAVDIR\_LEFT**](navigation-constants.md) or [**NAVDIR\_RIGHT**](navigation-constants.md) flags of the [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) method.</span></span>
-   <span data-ttu-id="4aa74-139">O sistema de eventos de eventos [**\_ \_ MENUPOPUPSTART**](event-constants.md) e o [**sistema de eventos \_ \_ MENUPOPUPEND**](event-constants.md) não são enviados de forma consistente.</span><span class="sxs-lookup"><span data-stu-id="4aa74-139">The events [**EVENT\_SYSTEM\_MENUPOPUPSTART**](event-constants.md) and [**EVENT\_SYSTEM\_MENUPOPUPEND**](event-constants.md) are not sent consistently.</span></span> <span data-ttu-id="4aa74-140">Esse é um problema conhecido e está sendo resolvido.</span><span class="sxs-lookup"><span data-stu-id="4aa74-140">This is a known issue and is being addressed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4aa74-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4aa74-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4aa74-142">Interface IAccessible</span><span class="sxs-lookup"><span data-stu-id="4aa74-142">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[<span data-ttu-id="4aa74-143">**Barra de menus**</span><span class="sxs-lookup"><span data-stu-id="4aa74-143">**Menu Bar**</span></span>](menu-bar.md)
</dt> <dt>

[<span data-ttu-id="4aa74-144">**Item de menu**</span><span class="sxs-lookup"><span data-stu-id="4aa74-144">**Menu Item**</span></span>](menu-item.md)
</dt> </dl>

 

 





