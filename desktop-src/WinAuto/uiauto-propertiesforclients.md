---
title: Recuperando propriedades de elementos de automação da interface do usuário
description: Propriedades em objetos IUIAutomationElement contêm informações sobre elementos de interface do usuário, geralmente controles.
ms.assetid: e358fd67-22d0-4e43-a138-8afcc45f130e
keywords:
- clientes, obtendo elementos de automação da interface do usuário
- clientes, elementos de automação da interface do usuário
- clientes, propriedades
- clientes, recuperando Propriedades
- clientes, propriedades de automação da interface do usuário
- Automação da interface do usuário, obtendo elementos
- Automação da interface do usuário, elementos
- Automação da interface do usuário, propriedades
- Automação da interface do usuário, recuperando Propriedades
- Recuperando propriedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e199522dbefaa2f722a67b0ede57fe910b8ed63b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105797597"
---
# <a name="retrieving-properties-from-ui-automation-elements"></a><span data-ttu-id="8d274-113">Recuperando propriedades de elementos de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="8d274-113">Retrieving Properties from UI Automation Elements</span></span>

<span data-ttu-id="8d274-114">Propriedades em objetos [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) contêm informações sobre elementos de interface do usuário, geralmente controles.</span><span class="sxs-lookup"><span data-stu-id="8d274-114">Properties on [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) objects contain information about UI elements, usually controls.</span></span> <span data-ttu-id="8d274-115">As propriedades de um elemento são genéricas; ou seja, não é específico para um tipo de controle.</span><span class="sxs-lookup"><span data-stu-id="8d274-115">The properties of an element are generic; that is, not specific to a control type.</span></span> <span data-ttu-id="8d274-116">As propriedades específicas de controle de um elemento são expostas por suas interfaces de padrão de controle.</span><span class="sxs-lookup"><span data-stu-id="8d274-116">Control-specific properties of an element are exposed by its control pattern interfaces.</span></span>

<span data-ttu-id="8d274-117">As propriedades de automação da interface do usuário da Microsoft são somente leitura.</span><span class="sxs-lookup"><span data-stu-id="8d274-117">Microsoft UI Automation properties are read-only.</span></span> <span data-ttu-id="8d274-118">Para definir as propriedades de um controle, você deve usar os métodos do padrão de controle apropriado.</span><span class="sxs-lookup"><span data-stu-id="8d274-118">To set properties of a control, you must use the methods of the appropriate control pattern.</span></span> <span data-ttu-id="8d274-119">Por exemplo, use [**IUIAutomationScrollPattern:: Scroll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollpattern-scroll) para alterar os valores de posição de uma janela de rolagem.</span><span class="sxs-lookup"><span data-stu-id="8d274-119">For example, use [**IUIAutomationScrollPattern::Scroll**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationscrollpattern-scroll) to change the position values of a scrolling window.</span></span>

<span data-ttu-id="8d274-120">Para melhorar o desempenho, os valores de propriedade de controles e padrões de controle podem ser armazenados em cache quando os elementos são recuperados.</span><span class="sxs-lookup"><span data-stu-id="8d274-120">To improve performance, property values of controls and control patterns can be cached when elements are retrieved.</span></span> <span data-ttu-id="8d274-121">Para obter mais informações, consulte [Caching interface de usuário Propriedades de automação e padrões de controle](uiauto-cachingforclients.md).</span><span class="sxs-lookup"><span data-stu-id="8d274-121">For more information, see [Caching UI Automation Properties and Control Patterns](uiauto-cachingforclients.md).</span></span>

<span data-ttu-id="8d274-122">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="8d274-122">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="8d274-123">IDs de propriedade</span><span class="sxs-lookup"><span data-stu-id="8d274-123">Property IDs</span></span>](#property-ids)
-   [<span data-ttu-id="8d274-124">Condições de propriedade</span><span class="sxs-lookup"><span data-stu-id="8d274-124">Property Conditions</span></span>](#property-conditions)
-   [<span data-ttu-id="8d274-125">Recuperando propriedades</span><span class="sxs-lookup"><span data-stu-id="8d274-125">Retrieving Properties</span></span>](#retrieving-properties)
-   [<span data-ttu-id="8d274-126">Valores de propriedade padrão</span><span class="sxs-lookup"><span data-stu-id="8d274-126">Default Property Values</span></span>](#default-property-values)
-   [<span data-ttu-id="8d274-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8d274-127">Related topics</span></span>](#related-topics)

## <a name="property-ids"></a><span data-ttu-id="8d274-128">IDs de propriedade</span><span class="sxs-lookup"><span data-stu-id="8d274-128">Property IDs</span></span>

<span data-ttu-id="8d274-129">Os identificadores de propriedade são definidos em UIAutomationClient. h.</span><span class="sxs-lookup"><span data-stu-id="8d274-129">Property identifiers are defined in Uiautomationclient.h.</span></span> <span data-ttu-id="8d274-130">Eles são usados para especificar propriedades quando você se inscreve em eventos de propriedade alterada, recupera valores de propriedade e cria condições de propriedade.</span><span class="sxs-lookup"><span data-stu-id="8d274-130">They are used to specify properties when you subscribe to property-changed events, retrieve property values, and construct property conditions.</span></span> <span data-ttu-id="8d274-131">Os identificadores de propriedade também identificam a propriedade que foi alterada quando [**IUIAutomationPropertyChangedEventHandler:: HandlePropertyChangedEvent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationpropertychangedeventhandler-handlepropertychangedevent) é chamado.</span><span class="sxs-lookup"><span data-stu-id="8d274-131">Property identifiers also identify the property that has changed when [**IUIAutomationPropertyChangedEventHandler::HandlePropertyChangedEvent**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationpropertychangedeventhandler-handlepropertychangedevent) is called.</span></span>

<span data-ttu-id="8d274-132">Para obter uma lista de identificadores de propriedade de automação da interface do usuário, consulte [identificadores de propriedade](uiauto-entry-propids.md).</span><span class="sxs-lookup"><span data-stu-id="8d274-132">For a list of UI Automation property identifiers, see [Property Identifiers](uiauto-entry-propids.md).</span></span>

## <a name="property-conditions"></a><span data-ttu-id="8d274-133">Condições de propriedade</span><span class="sxs-lookup"><span data-stu-id="8d274-133">Property Conditions</span></span>

<span data-ttu-id="8d274-134">As IDs de propriedade são usadas na construção de objetos [**IUIAutomationPropertyCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition) que são usados para localizar elementos de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="8d274-134">The property IDs are used in constructing [**IUIAutomationPropertyCondition**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertycondition) objects that are used to find UI Automation elements.</span></span> <span data-ttu-id="8d274-135">Por exemplo, você pode querer encontrar um elemento que tenha um determinado nome ou todos os controles que estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="8d274-135">For example, you might want to find an element that has a certain name, or all controls that are enabled.</span></span> <span data-ttu-id="8d274-136">Cada condição de propriedade especifica um identificador de propriedade e o valor que a propriedade deve corresponder.</span><span class="sxs-lookup"><span data-stu-id="8d274-136">Each property condition specifies a property identifier and the value that the property must match.</span></span>

<span data-ttu-id="8d274-137">Para obter mais informações, consulte os seguintes tópicos de referência:</span><span class="sxs-lookup"><span data-stu-id="8d274-137">For more information, see the following reference topics:</span></span>

-   [<span data-ttu-id="8d274-138">**IUIAutomation::CreatePropertyCondition**</span><span class="sxs-lookup"><span data-stu-id="8d274-138">**IUIAutomation::CreatePropertyCondition**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition)
-   [<span data-ttu-id="8d274-139">**IUIAutomation::CreatePropertyConditionEx**</span><span class="sxs-lookup"><span data-stu-id="8d274-139">**IUIAutomation::CreatePropertyConditionEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertyconditionex)
-   [<span data-ttu-id="8d274-140">**IUIAutomationElement:: FindFirst**</span><span class="sxs-lookup"><span data-stu-id="8d274-140">**IUIAutomationElement::FindFirst**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findfirst)
-   [<span data-ttu-id="8d274-141">**IUIAutomationElement:: FindAll**</span><span class="sxs-lookup"><span data-stu-id="8d274-141">**IUIAutomationElement::FindAll**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-findall)

## <a name="retrieving-properties"></a><span data-ttu-id="8d274-142">Recuperando propriedades</span><span class="sxs-lookup"><span data-stu-id="8d274-142">Retrieving Properties</span></span>

<span data-ttu-id="8d274-143">Algumas propriedades genéricas e todas as propriedades de padrão de controle estão disponíveis como propriedades na interface de padrão de [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) ou de controle e podem ser recuperadas usando um acessador, como [**IUIAutomationElement:: CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) ou [**CachedDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-get_cacheddockposition).</span><span class="sxs-lookup"><span data-stu-id="8d274-143">Some generic properties, and all control pattern properties, are available as properties on the [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) or control pattern interface and can be retrieved by using an accessor, such as [**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) or [**CachedDockPosition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationdockpattern-get_cacheddockposition).</span></span>

<span data-ttu-id="8d274-144">Além disso, qualquer propriedade atual ou armazenada em cache (diferente das propriedades de padrão de controle) pode ser recuperada usando um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="8d274-144">In addition, any current or cached property (other than control pattern properties) can be retrieved by using one of the following methods:</span></span>

-   [<span data-ttu-id="8d274-145">**GetCurrentPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="8d274-145">**GetCurrentPropertyValue**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue)
-   [<span data-ttu-id="8d274-146">**GetCurrentPropertyValueEx**</span><span class="sxs-lookup"><span data-stu-id="8d274-146">**GetCurrentPropertyValueEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex)
-   [<span data-ttu-id="8d274-147">**GetCachedPropertyValue**</span><span class="sxs-lookup"><span data-stu-id="8d274-147">**GetCachedPropertyValue**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalue)
-   [<span data-ttu-id="8d274-148">**GetCachedPropertyValueEx**</span><span class="sxs-lookup"><span data-stu-id="8d274-148">**GetCachedPropertyValueEx**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedpropertyvalueex)

<span data-ttu-id="8d274-149">Esses métodos oferecem um desempenho ligeiramente melhor e o acesso à gama completa de propriedades.</span><span class="sxs-lookup"><span data-stu-id="8d274-149">These methods offer slightly better performance and access to the full range of properties.</span></span> <span data-ttu-id="8d274-150">No entanto, os valores são retornados em estruturas [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) , enquanto os acessadores de propriedade individuais convertem o valor para o tipo apropriado.</span><span class="sxs-lookup"><span data-stu-id="8d274-150">However, values are returned in [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) structures, whereas the individual property accessors cast the value to the appropriate type.</span></span>

## <a name="default-property-values"></a><span data-ttu-id="8d274-151">Valores de propriedade padrão</span><span class="sxs-lookup"><span data-stu-id="8d274-151">Default Property Values</span></span>

<span data-ttu-id="8d274-152">Se um provedor de automação de interface do usuário não implementar uma propriedade, a automação da interface do usuário poderá fornecer um valor padrão.</span><span class="sxs-lookup"><span data-stu-id="8d274-152">If a UI Automation provider does not implement a property, UI Automation can supply a default value.</span></span> <span data-ttu-id="8d274-153">Por exemplo, se o provedor de um controle não oferecer suporte à propriedade identificada por [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md), a automação da interface do usuário retornará uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="8d274-153">For example, if the provider for a control does not support the property identified by [**UIA\_HelpTextPropertyId**](uiauto-automation-element-propids.md), UI Automation returns an empty string.</span></span> <span data-ttu-id="8d274-154">Da mesma forma, se o provedor não oferecer suporte à propriedade identificada por [**UIA \_ IsDockPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md), a automação da interface do usuário retornará **false**.</span><span class="sxs-lookup"><span data-stu-id="8d274-154">Similarly, if the provider does not support the property identified by [**UIA\_IsDockPatternAvailablePropertyId**](uiauto-control-pattern-availability-propids.md), UI Automation returns **FALSE**.</span></span>

<span data-ttu-id="8d274-155">A diferença entre [**IUIAutomationElement:: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) e [**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex) (e entre pares semelhantes de métodos) é que o método "ex" pode especificar que nenhum valor padrão seja retornado.</span><span class="sxs-lookup"><span data-stu-id="8d274-155">The difference between [**IUIAutomationElement::GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) and [**GetCurrentPropertyValueEx**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalueex) (and between similar pairs of methods) is that the "Ex" method can specify that no default value is to be returned.</span></span> <span data-ttu-id="8d274-156">Nesse caso, o valor de retorno é uma constante exclusiva especial, indicando que não há suporte para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="8d274-156">In this case, the return value is a special unique constant, indicating that the property is not supported.</span></span> <span data-ttu-id="8d274-157">Ao receber esse valor, o aplicativo pode fornecer seu próprio valor ou simplesmente ignorar a propriedade.</span><span class="sxs-lookup"><span data-stu-id="8d274-157">On receiving this value, the application can supply its own value or simply ignore the property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d274-158">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8d274-158">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8d274-159">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="8d274-159">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8d274-160">Visão geral das propriedades de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="8d274-160">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
</dt> <dt>

[<span data-ttu-id="8d274-161">Identificadores de propriedade</span><span class="sxs-lookup"><span data-stu-id="8d274-161">Property Identifiers</span></span>](uiauto-entry-propids.md)
</dt> </dl>

 

 