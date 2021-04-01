---
title: Visão geral das propriedades de automação da interface do usuário
description: Os provedores de automação da interface do usuário da Microsoft expõem propriedades em elementos de automação de interface As propriedades permitem que os aplicativos cliente recuperem informações sobre controles.
ms.assetid: 35f017cb-f50a-4680-9f01-5079aa59da73
keywords:
- Automação da interface do usuário, visão geral das propriedades
- Automação da interface do usuário, Propriedades vs. eventos
- Automação da interface do usuário, eventos vs. Propriedades
- Propriedades, sobre
- Propriedades, identificadores
- Propriedades, valores
- Propriedades, eventos
- eventos, propriedades
- Propriedades, dinâmicas
- propriedades dinâmicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f4e5e1b29ae516059a531b17d50d0631282f82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159246"
---
# <a name="ui-automation-properties-overview"></a><span data-ttu-id="28ed5-114">Visão geral das propriedades de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="28ed5-114">UI Automation Properties Overview</span></span>

<span data-ttu-id="28ed5-115">Os provedores de automação da interface do usuário da Microsoft expõem propriedades em elementos de automação de interface</span><span class="sxs-lookup"><span data-stu-id="28ed5-115">Microsoft UI Automation providers expose properties on UI Automation elements.</span></span> <span data-ttu-id="28ed5-116">As propriedades permitem que os aplicativos cliente recuperem informações sobre controles.</span><span class="sxs-lookup"><span data-stu-id="28ed5-116">Properties enable client applications to retrieve information about controls.</span></span>

<span data-ttu-id="28ed5-117">A automação da interface do usuário expõe dois tipos diferentes de propriedades: *Propriedades do elemento Automation* e *padrões de controle*.</span><span class="sxs-lookup"><span data-stu-id="28ed5-117">UI Automation exposes two different kinds of properties: *automation element properties*, and *control pattern propertes*.</span></span> <span data-ttu-id="28ed5-118">As propriedades do elemento Automation consistem em um conjunto comum de propriedades, como Name, AcceleratorKey e ClassName, que são expostas por todos os elementos de automação da interface do usuário, independentemente do tipo de controle.</span><span class="sxs-lookup"><span data-stu-id="28ed5-118">The automation element properties consist of a common set of properties, such as Name, AcceleratorKey, and ClassName, that are exposed by all UI Automation elements, regardless of the control type.</span></span> <span data-ttu-id="28ed5-119">A maioria das propriedades de elementos de automação são valores estáticos.</span><span class="sxs-lookup"><span data-stu-id="28ed5-119">Most automation element properties are static values.</span></span>

<span data-ttu-id="28ed5-120">As propriedades de padrão de controle são aquelas que são expostas por um controle que dá suporte a um padrão de controle específico.</span><span class="sxs-lookup"><span data-stu-id="28ed5-120">Control pattern properties are those that are exposed by a control that supports a particular control pattern.</span></span> <span data-ttu-id="28ed5-121">Cada padrão de controle tem um conjunto correspondente de propriedades de padrão de controle que o controle deve expor.</span><span class="sxs-lookup"><span data-stu-id="28ed5-121">Each control pattern has a corresponding set of control pattern properties that the control must expose.</span></span> <span data-ttu-id="28ed5-122">Por exemplo, um controle que dá suporte ao padrão de controle de [grade](uiauto-implementinggrid.md) expõe as propriedades ColumnCount e RowCount.</span><span class="sxs-lookup"><span data-stu-id="28ed5-122">For example, a control that supports the [Grid](uiauto-implementinggrid.md) control pattern exposes the ColumnCount and RowCount properties.</span></span> <span data-ttu-id="28ed5-123">A maioria das propriedades de padrão de controle são valores dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="28ed5-123">Most control pattern properties are dynamic values.</span></span>

<span data-ttu-id="28ed5-124">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="28ed5-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="28ed5-125">Identificadores de propriedade</span><span class="sxs-lookup"><span data-stu-id="28ed5-125">Property Identifiers</span></span>](#property-identifiers)
-   [<span data-ttu-id="28ed5-126">Valores de propriedade</span><span class="sxs-lookup"><span data-stu-id="28ed5-126">Property Values</span></span>](#property-values)
-   [<span data-ttu-id="28ed5-127">Propriedades e eventos</span><span class="sxs-lookup"><span data-stu-id="28ed5-127">Properties and Events</span></span>](#properties-and-events)
-   [<span data-ttu-id="28ed5-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="28ed5-128">Related topics</span></span>](#related-topics)

## <a name="property-identifiers"></a><span data-ttu-id="28ed5-129">Identificadores de propriedade</span><span class="sxs-lookup"><span data-stu-id="28ed5-129">Property Identifiers</span></span>

<span data-ttu-id="28ed5-130">Cada propriedade é identificada por um valor numérico **PropertyId** chamado de *identificador de propriedade* (ID).</span><span class="sxs-lookup"><span data-stu-id="28ed5-130">Every property is identified by a **PROPERTYID** numeric value called a *property identifier* (ID).</span></span> <span data-ttu-id="28ed5-131">Provedores e clientes usam as IDs numéricas em chamadas de método, como [**IRawElementProviderAdviseEvents:: AdviseEventAdded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) e [**IUIAutomationElement:: GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue) para identificar solicitações de propriedade.</span><span class="sxs-lookup"><span data-stu-id="28ed5-131">Providers and clients use the numeric IDs in method calls such as [**IRawElementProviderAdviseEvents::AdviseEventAdded**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded) and [**IUIAutomationElement::GetCachedPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue) to identify property requests.</span></span> <span data-ttu-id="28ed5-132">Para obter uma descrição detalhada de cada identificador de propriedade de automação de interface do usuário, incluindo o tipo de dados e o valor padrão de cada propriedade, consulte [identificadores de propriedade](uiauto-entry-propids.md).</span><span class="sxs-lookup"><span data-stu-id="28ed5-132">For a detailed description of each UI Automation property identifier, including the data type and default value of each property, see [Property Identifiers](uiauto-entry-propids.md).</span></span>

## <a name="property-values"></a><span data-ttu-id="28ed5-133">Valores da propriedade</span><span class="sxs-lookup"><span data-stu-id="28ed5-133">Property Values</span></span>

<span data-ttu-id="28ed5-134">Todas as propriedades são somente leitura, embora algumas possam ser alteradas usando métodos que atuam no controle, como [**IDockProvider:: SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) (Provider) ou [**IUIAutomationDockPattern:: SetDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-setdockposition) (Client).</span><span class="sxs-lookup"><span data-stu-id="28ed5-134">All properties are read-only, although some can be changed by using methods that act on the control, such as [**IDockProvider::SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) (provider) or [**IUIAutomationDockPattern::SetDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-setdockposition) (client).</span></span>

<span data-ttu-id="28ed5-135">Para obter informações sobre como recuperar valores de propriedade, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="28ed5-135">For information about retrieving property values, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>

## <a name="properties-and-events"></a><span data-ttu-id="28ed5-136">Propriedades e eventos</span><span class="sxs-lookup"><span data-stu-id="28ed5-136">Properties and Events</span></span>

<span data-ttu-id="28ed5-137">Fortemente associado às propriedades na automação da interface do usuário é o conceito de *eventos de alteração de propriedade*.</span><span class="sxs-lookup"><span data-stu-id="28ed5-137">Closely associated with the properties in UI Automation is the concept of *property-changed events*.</span></span> <span data-ttu-id="28ed5-138">Para propriedades dinâmicas, um aplicativo cliente precisa de uma maneira de saber que um valor de propriedade foi alterado, para que ele possa atualizar seu cache de informações ou reagir às novas informações de alguma outra maneira.</span><span class="sxs-lookup"><span data-stu-id="28ed5-138">For dynamic properties, a client application needs a way to know that a property value has changed, so that it can update its cache of information or react to the new information in some other way.</span></span> <span data-ttu-id="28ed5-139">Os clientes podem se registrar para escutar eventos de propriedade alterada em qualquer propriedade.</span><span class="sxs-lookup"><span data-stu-id="28ed5-139">Clients can register to listen for property-changed events on any property.</span></span>

<span data-ttu-id="28ed5-140">Os provedores geram eventos quando algo na interface do usuário é alterado.</span><span class="sxs-lookup"><span data-stu-id="28ed5-140">Providers raise events when something in the UI changes.</span></span> <span data-ttu-id="28ed5-141">Por exemplo, se uma caixa de seleção for marcada ou desmarcada, um evento de alteração de propriedade será gerado pela implementação do provedor do padrão de controle de [alternância](uiauto-implementingtoggle.md) .</span><span class="sxs-lookup"><span data-stu-id="28ed5-141">For example, if a check box is selected or cleared, a property-changed event is raised by the provider implementation of the [Toggle](uiauto-implementingtoggle.md) control pattern.</span></span> <span data-ttu-id="28ed5-142">Os provedores podem gerar eventos seletivamente, dependendo se algum cliente está ouvindo eventos ou escutando eventos específicos.</span><span class="sxs-lookup"><span data-stu-id="28ed5-142">Providers can raise events selectively, depending on whether any clients are listening for events, or listening for specific events.</span></span>

<span data-ttu-id="28ed5-143">Nem todas as alterações de propriedade geram eventos; Isso é inteiramente a implementação do provedor de automação da interface do usuário para o elemento.</span><span class="sxs-lookup"><span data-stu-id="28ed5-143">Not all property changes raise events; that is entirely up to the implementation of the UI Automation provider for the element.</span></span> <span data-ttu-id="28ed5-144">Por exemplo, os provedores de proxy padrão para caixas de listagem não geram um evento de alteração de propriedade quando a propriedade Selection é alterada.</span><span class="sxs-lookup"><span data-stu-id="28ed5-144">For example, the standard proxy providers for list boxes do not raise a property-changed event when the Selection property changes.</span></span> <span data-ttu-id="28ed5-145">Nesse caso, o aplicativo deve escutar o evento gerado quando a seleção é alterada ([**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="28ed5-145">In this case, the application must listen for the event raised when the selection changes ([**UIA\_SelectionItem\_ElementSelectedEventId**](uiauto-event-ids.md)).</span></span>

<span data-ttu-id="28ed5-146">Os clientes escutam eventos assinando-os, conforme descrito em [inscrever-se em eventos de automação da interface do usuário](uiauto-eventsforclients.md).</span><span class="sxs-lookup"><span data-stu-id="28ed5-146">Clients listen for events by subscribing to them, as described at [Subscribing to UI Automation Events](uiauto-eventsforclients.md).</span></span> <span data-ttu-id="28ed5-147">Para eventos de propriedade alterada em particular, os clientes devem implementar [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) e passar a interface para [**IUIAutomation:: AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) ou [**IUIAutomation:: AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray).</span><span class="sxs-lookup"><span data-stu-id="28ed5-147">For property-changed events in particular, clients must implement [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) and pass the interface to [**IUIAutomation::AddPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandler) or [**IUIAutomation::AddPropertyChangedEventHandlerNativeArray**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-addpropertychangedeventhandlernativearray).</span></span>

## <a name="related-topics"></a><span data-ttu-id="28ed5-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="28ed5-148">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="28ed5-149">**Referência**</span><span class="sxs-lookup"><span data-stu-id="28ed5-149">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="28ed5-150">**GetCurrentPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="28ed5-150">**GetCurrentPropertyValue**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
</dt> <dt>

[<span data-ttu-id="28ed5-151">**GetCurrentPropertyValueEx**</span><span class="sxs-lookup"><span data-stu-id="28ed5-151">**GetCurrentPropertyValueEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
</dt> <dt>

[<span data-ttu-id="28ed5-152">**GetCachedPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="28ed5-152">**GetCachedPropertyValue**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
</dt> <dt>

[<span data-ttu-id="28ed5-153">**GetCachedPropertyValueEx**</span><span class="sxs-lookup"><span data-stu-id="28ed5-153">**GetCachedPropertyValueEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)
</dt> <dt>

<span data-ttu-id="28ed5-154">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="28ed5-154">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="28ed5-155">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="28ed5-155">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="28ed5-156">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="28ed5-156">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="28ed5-157">Visão geral sobre eventos de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="28ed5-157">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> </dl>

 

 




