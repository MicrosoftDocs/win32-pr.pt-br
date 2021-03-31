---
title: Padrão de controle CustomNavigation
description: Descreve as diretrizes e convenções para implementar a interface ICustomNavigationProvider, incluindo informações sobre propriedades e métodos.
ms.assetid: 428540BB-5CC0-4F49-8384-0FFC130FBB38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97cc6524585f3ddd7ec764a791141fce9daa3c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159760"
---
# <a name="customnavigation-control-pattern"></a><span data-ttu-id="3067b-103">Padrão de controle CustomNavigation</span><span class="sxs-lookup"><span data-stu-id="3067b-103">CustomNavigation Control Pattern</span></span>

<span data-ttu-id="3067b-104">Descreve as diretrizes e convenções para implementar a interface **ICustomNavigationProvider** , incluindo informações sobre propriedades e métodos.</span><span class="sxs-lookup"><span data-stu-id="3067b-104">Describes guidelines and conventions for implementing the **ICustomNavigationProvider** interface, including information about properties and methods.</span></span> <span data-ttu-id="3067b-105">O padrão de controle **CustomNavigation** é usado para habilitar a navegação personalizada entre controles em estruturas do tipo hierarquia, como itens de lista, listas com marcadores, listas numeradas e títulos.</span><span class="sxs-lookup"><span data-stu-id="3067b-105">The **CustomNavigation** control pattern is used to enable custom navigation between controls in hierarchy-like structures such as list items, bulleted lists, numbered lists and headings.</span></span> <span data-ttu-id="3067b-106">Isso permite que os provedores descrevam estruturas ou definam as relações navegáveis usando o elemento sozinho e não apenas o controle recipiente.</span><span class="sxs-lookup"><span data-stu-id="3067b-106">This enables providers to describe structures or define the navigable relationships using the element alone and not just the containing control.</span></span>

<span data-ttu-id="3067b-107">Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="3067b-107">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="3067b-108">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="3067b-108">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3067b-109">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="3067b-109">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="3067b-110">Membros necessários para **ICustomNavigationProvider**</span><span class="sxs-lookup"><span data-stu-id="3067b-110">Required Members for **ICustomNavigationProvider**</span></span>](#required-members-for-icustomnavigationprovider)
-   [<span data-ttu-id="3067b-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3067b-111">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="3067b-112">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="3067b-112">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="3067b-113">Ao implementar o provedor **CustomNavigation** , observe as seguintes diretrizes e convenções:</span><span class="sxs-lookup"><span data-stu-id="3067b-113">When implementing the **CustomNavigation** provider, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="3067b-114">Os valores de propriedade para **PositionInSet**, **sizeofset** e **Level** são valores inteiros baseados em um.</span><span class="sxs-lookup"><span data-stu-id="3067b-114">Property values for **PositionInSet**, **SizeOfSet**, and **Level** are one-based integer values.</span></span>
-   <span data-ttu-id="3067b-115">O **ICustomNavigationProvider** não fornece manipulação ativa do controle, como mover posições, adicionar e remover itens, ou promover e rebaixar níveis.</span><span class="sxs-lookup"><span data-stu-id="3067b-115">**ICustomNavigationProvider** does not provide for active manipulation of the control such as moving positions, adding and removing items, or promoting and demoting levels.</span></span>
-   <span data-ttu-id="3067b-116">Controles que implementam **ICustomNavigationProvider** normalmente têm uma estrutura hierárquica, mas podem ignorar níveis usando o método **Navigate** .</span><span class="sxs-lookup"><span data-stu-id="3067b-116">Controls that implement **ICustomNavigationProvider** typically have a hierarchical structure, but can skip levels by using the **Navigate** method.</span></span> <span data-ttu-id="3067b-117">As propriedades **PositionInSet**, **sizeofset** e **Level** são necessárias no padrão.</span><span class="sxs-lookup"><span data-stu-id="3067b-117">The properties **PositionInSet**, **SizeOfSet**, and **Level** are required on the pattern.</span></span>

## <a name="required-members-for-icustomnavigationprovider"></a><span data-ttu-id="3067b-118">Membros necessários para **ICustomNavigationProvider**</span><span class="sxs-lookup"><span data-stu-id="3067b-118">Required Members for **ICustomNavigationProvider**</span></span>

<span data-ttu-id="3067b-119">As propriedades a seguir são necessárias para implementar a interface **ICustomNavigationProvider** .</span><span class="sxs-lookup"><span data-stu-id="3067b-119">The following properties are required for implementing the **ICustomNavigationProvider** interface.</span></span>



| <span data-ttu-id="3067b-120">Membros necessários</span><span class="sxs-lookup"><span data-stu-id="3067b-120">Required members</span></span>                                                                  | <span data-ttu-id="3067b-121">Tipo de membro</span><span class="sxs-lookup"><span data-stu-id="3067b-121">Member type</span></span> | <span data-ttu-id="3067b-122">Observações</span><span class="sxs-lookup"><span data-stu-id="3067b-122">Notes</span></span>                                                                               |
|-----------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="3067b-123">**CachedLevel**</span><span class="sxs-lookup"><span data-stu-id="3067b-123">**CachedLevel**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedlevel)                   | <span data-ttu-id="3067b-124">Propriedade</span><span class="sxs-lookup"><span data-stu-id="3067b-124">Property</span></span>    | <span data-ttu-id="3067b-125">Localizado na interface [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) .</span><span class="sxs-lookup"><span data-stu-id="3067b-125">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="3067b-126">**CachedPositionInSet**</span><span class="sxs-lookup"><span data-stu-id="3067b-126">**CachedPositionInSet**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedpositioninset)   | <span data-ttu-id="3067b-127">Propriedade</span><span class="sxs-lookup"><span data-stu-id="3067b-127">Property</span></span>    | <span data-ttu-id="3067b-128">Localizado na interface [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) .</span><span class="sxs-lookup"><span data-stu-id="3067b-128">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="3067b-129">**CachedSizeOfSet**</span><span class="sxs-lookup"><span data-stu-id="3067b-129">**CachedSizeOfSet**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_cachedsizeofset)           | <span data-ttu-id="3067b-130">Propriedade</span><span class="sxs-lookup"><span data-stu-id="3067b-130">Property</span></span>    | <span data-ttu-id="3067b-131">Localizado na interface [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) .</span><span class="sxs-lookup"><span data-stu-id="3067b-131">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="3067b-132">**CurrentLevel**</span><span class="sxs-lookup"><span data-stu-id="3067b-132">**CurrentLevel**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentlevel)                 | <span data-ttu-id="3067b-133">Propriedade</span><span class="sxs-lookup"><span data-stu-id="3067b-133">Property</span></span>    | <span data-ttu-id="3067b-134">Localizado na interface [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) .</span><span class="sxs-lookup"><span data-stu-id="3067b-134">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="3067b-135">**CurrentPositionInSet**</span><span class="sxs-lookup"><span data-stu-id="3067b-135">**CurrentPositionInSet**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentpositioninset) | <span data-ttu-id="3067b-136">Propriedade</span><span class="sxs-lookup"><span data-stu-id="3067b-136">Property</span></span>    | <span data-ttu-id="3067b-137">Localizado na interface [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) .</span><span class="sxs-lookup"><span data-stu-id="3067b-137">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="3067b-138">**CurrentSizeOfSet**</span><span class="sxs-lookup"><span data-stu-id="3067b-138">**CurrentSizeOfSet**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement4-get_currentsizeofset)         | <span data-ttu-id="3067b-139">Propriedade</span><span class="sxs-lookup"><span data-stu-id="3067b-139">Property</span></span>    | <span data-ttu-id="3067b-140">Localizado na interface [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) .</span><span class="sxs-lookup"><span data-stu-id="3067b-140">Located on [**IUIAutomationElement4**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement4) interface.</span></span> |
| [<span data-ttu-id="3067b-141">**Navegue até**</span><span class="sxs-lookup"><span data-stu-id="3067b-141">**Navigate**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate)                   | <span data-ttu-id="3067b-142">Método</span><span class="sxs-lookup"><span data-stu-id="3067b-142">Method</span></span>      | <span data-ttu-id="3067b-143">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3067b-143">None</span></span>                                                                                |



 

<span data-ttu-id="3067b-144">Este padrão de controle não tem nenhum método ou evento associado.</span><span class="sxs-lookup"><span data-stu-id="3067b-144">This control pattern has no associated methods or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3067b-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3067b-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3067b-146">Tipos de controle e seus padrões de controle com suporte</span><span class="sxs-lookup"><span data-stu-id="3067b-146">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="3067b-147">Controle de ListItem</span><span class="sxs-lookup"><span data-stu-id="3067b-147">ListItem Control</span></span>](uiauto-supportlistitemcontroltype.md)
</dt> <dt>

[<span data-ttu-id="3067b-148">Controle HeaderItem</span><span class="sxs-lookup"><span data-stu-id="3067b-148">HeaderItem Control</span></span>](uiauto-supportheaderitemcontroltype.md)
</dt> <dt>

[<span data-ttu-id="3067b-149">Controle DataItem</span><span class="sxs-lookup"><span data-stu-id="3067b-149">DataItem Control</span></span>](uiauto-supportdataitemcontroltype.md)
</dt> <dt>

[<span data-ttu-id="3067b-150">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="3067b-150">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




