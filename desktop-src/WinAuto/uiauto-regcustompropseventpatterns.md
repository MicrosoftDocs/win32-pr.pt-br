---
title: Registrar Propriedades personalizadas, eventos e padrões de controle
description: Antes que um padrão de propriedade, evento ou controle personalizado possa ser usado, o provedor e o cliente devem registrar a propriedade, o evento ou o padrão de controle em tempo de execução.
ms.assetid: ae36e404-8432-46ed-930e-b86dd5a88d6d
keywords:
- Automação da interface do usuário, propriedades personalizadas
- Automação da interface do usuário, visão geral de eventos
- Visão geral da automação da interface do usuário, padrões de controle
- Automação da interface do usuário, registrando Propriedades personalizadas
- Automação da interface do usuário, registro de eventos
- Automação da interface do usuário, registro de padrões de controle
- Propriedades personalizadas, registrando
- eventos, registrando
- padrões de controle, registro
- registrando, propriedades personalizadas
- registrando, eventos
- registrando, padrões de controle
- padrões de controle, personalizado
- padrões de controle, implementando personalizados
- Implementando padrões de controle personalizados
- padrões de controle personalizados
- wrappers de cliente
- manipuladores de padrões
- Implementando manipuladores de padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b6b157e8f08a2c0be74af6b9f53d3578d1e4d03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007988"
---
# <a name="register-custom-properties-events-and-control-patterns"></a><span data-ttu-id="30ce6-122">Registrar Propriedades personalizadas, eventos e padrões de controle</span><span class="sxs-lookup"><span data-stu-id="30ce6-122">Register custom properties, events, and control patterns</span></span>

<span data-ttu-id="30ce6-123">Antes que um padrão de propriedade, evento ou controle personalizado possa ser usado, o provedor e o cliente devem registrar a propriedade, o evento ou o padrão de controle em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="30ce6-123">Before a custom property, event, or control pattern can be used, both the provider and the client must register the property, event, or control pattern at run time.</span></span> <span data-ttu-id="30ce6-124">O registro é efetivo globalmente dentro de um processo de aplicativo e permanece em vigor até que o processo seja fechado ou o último objeto de elemento de automação da interface do usuário da Microsoft ([**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) ou [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)) seja liberado dentro do processo.</span><span class="sxs-lookup"><span data-stu-id="30ce6-124">The registration is effective globally within an application process, and remains effective until the process closes or the last Microsoft UI Automation element object ([**IUIAutomation**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomation) or [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple)) is released within the process.</span></span>

<span data-ttu-id="30ce6-125">O registro envolve a passagem de um GUID para a automação da interface do usuário, juntamente com informações detalhadas sobre a propriedade personalizada, evento ou padrão de controle.</span><span class="sxs-lookup"><span data-stu-id="30ce6-125">Registation involves passing a GUID to UI Automation, along with detailed information about the custom property, event, or control pattern.</span></span> <span data-ttu-id="30ce6-126">A tentativa de registrar o mesmo GUID uma segunda vez com as mesmas informações terá êxito, mas tentar registrar o mesmo GUID uma segunda vez, mas com informações diferentes (por exemplo, uma propriedade personalizada de um tipo diferente) falhará.</span><span class="sxs-lookup"><span data-stu-id="30ce6-126">Attempting to register the same GUID a second time with the same information will succeed, but attempting to register the same GUID a second time but with different information (for example, a custom property of a different type) will fail.</span></span> <span data-ttu-id="30ce6-127">No futuro, se a especificação personalizada for aceita e integrada ao núcleo de automação da interface do usuário, a automação da interface do usuário validará as informações de registro personalizadas e usará o código já registrado em vez da implementação da estrutura "oficial", minimizando assim os problemas de compatibilidade do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="30ce6-127">In the future, if the custom specification is accepted and integrated into the UI Automation core, UI Automation will validate the custom registration information and use the already registered code instead of the "official" framework implementation, thereby minimizing application compatibility issues.</span></span> <span data-ttu-id="30ce6-128">Você não pode remover propriedades, eventos ou padrões de controle que já estão registrados.</span><span class="sxs-lookup"><span data-stu-id="30ce6-128">You cannot remove properties, events, or control patterns that are already registered.</span></span>

<span data-ttu-id="30ce6-129">Este tópico contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="30ce6-129">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="30ce6-130">Registrando Propriedades e eventos personalizados</span><span class="sxs-lookup"><span data-stu-id="30ce6-130">Registering Custom Properties and Events</span></span>](#registering-custom-properties-and-events)
-   [<span data-ttu-id="30ce6-131">Implementando padrões de controle personalizados</span><span class="sxs-lookup"><span data-stu-id="30ce6-131">Implementing Custom Control Patterns</span></span>](#implementing-custom-control-patterns)
    -   [<span data-ttu-id="30ce6-132">O wrapper do cliente e o manipulador de padrão</span><span class="sxs-lookup"><span data-stu-id="30ce6-132">The Client Wrapper and the Pattern Handler</span></span>](#the-client-wrapper-and-the-pattern-handler)
    -   [<span data-ttu-id="30ce6-133">Implementando o wrapper do cliente</span><span class="sxs-lookup"><span data-stu-id="30ce6-133">Implementing the Client Wrapper</span></span>](#implementing-the-client-wrapper)
    -   [<span data-ttu-id="30ce6-134">Implementando o manipulador de padrões</span><span class="sxs-lookup"><span data-stu-id="30ce6-134">Implementing the Pattern Handler</span></span>](#implementing-the-pattern-handler)
    -   [<span data-ttu-id="30ce6-135">Registrando um padrão de controle personalizado</span><span class="sxs-lookup"><span data-stu-id="30ce6-135">Registering a Custom Control Pattern</span></span>](#registering-a-custom-control-pattern)
    -   [<span data-ttu-id="30ce6-136">Exemplo de implementação de um padrão de controle personalizado</span><span class="sxs-lookup"><span data-stu-id="30ce6-136">Example Implementation of a Custom Control Pattern</span></span>](#example-implementation-of-a-custom-control-pattern)
-   [<span data-ttu-id="30ce6-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="30ce6-137">Related topics</span></span>](#related-topics)

## <a name="registering-custom-properties-and-events"></a><span data-ttu-id="30ce6-138">Registrando Propriedades e eventos personalizados</span><span class="sxs-lookup"><span data-stu-id="30ce6-138">Registering Custom Properties and Events</span></span>

<span data-ttu-id="30ce6-139">O registro de uma propriedade ou evento personalizado permite que o provedor e o cliente obtenham uma ID para a propriedade ou evento, que pode ser passada para vários métodos de API que usam IDs como parâmetros.</span><span class="sxs-lookup"><span data-stu-id="30ce6-139">Registering a custom property or event enables the provider and client to obtain an ID for the property or event, which can then be passed to various API methods that take IDs as parameters.</span></span>

<span data-ttu-id="30ce6-140">Para registrar uma propriedade ou evento:</span><span class="sxs-lookup"><span data-stu-id="30ce6-140">To register a property or event:</span></span>

1.  <span data-ttu-id="30ce6-141">Defina um GUID para a propriedade ou evento personalizado.</span><span class="sxs-lookup"><span data-stu-id="30ce6-141">Define a GUID for the custom property or event.</span></span>
2.  <span data-ttu-id="30ce6-142">Preencha uma estrutura [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) ou [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) com informações sobre a propriedade ou o evento, incluindo o GUID e uma cadeia de caracteres não localizável que contém o nome da propriedade ou do evento personalizado.</span><span class="sxs-lookup"><span data-stu-id="30ce6-142">Fill a [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) or a [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) structure with information about the property or event, including the GUID and a nonlocalizable string that contains the name of the custom property or event.</span></span> <span data-ttu-id="30ce6-143">As propriedades personalizadas também exigem que o tipo de dados da propriedade seja especificado, por exemplo, se a propriedade contém um inteiro ou uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="30ce6-143">Custom properties also require the data type of the property to be specified, for example, whether the property holds an integer or a string.</span></span> <span data-ttu-id="30ce6-144">O tipo de dados deve ser um dos tipos a seguir especificados pela enumeração [**UIAutomationType**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) .</span><span class="sxs-lookup"><span data-stu-id="30ce6-144">The data type must be one of the following types specified by the [**UIAutomationType**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-uiautomationtype) enumeration.</span></span> <span data-ttu-id="30ce6-145">Nenhum outro tipo de dados tem suporte para propriedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="30ce6-145">No other data types are supported for custom properties.</span></span>
    -   <span data-ttu-id="30ce6-146">**\_Bool UIAutomationType**</span><span class="sxs-lookup"><span data-stu-id="30ce6-146">**UIAutomationType\_Bool**</span></span>
    -   <span data-ttu-id="30ce6-147">**UIAutomationType \_ duplo**</span><span class="sxs-lookup"><span data-stu-id="30ce6-147">**UIAutomationType\_Double**</span></span>
    -   <span data-ttu-id="30ce6-148">**\_Elemento UIAutomationType**</span><span class="sxs-lookup"><span data-stu-id="30ce6-148">**UIAutomationType\_Element**</span></span>
    -   <span data-ttu-id="30ce6-149">**UIAutomationType \_ int**</span><span class="sxs-lookup"><span data-stu-id="30ce6-149">**UIAutomationType\_Int**</span></span>
    -   <span data-ttu-id="30ce6-150">**Ponto de UIAutomationType \_**</span><span class="sxs-lookup"><span data-stu-id="30ce6-150">**UIAutomationType\_Point**</span></span>
    -   <span data-ttu-id="30ce6-151">**\_Cadeia de caracteres UIAutomationType**</span><span class="sxs-lookup"><span data-stu-id="30ce6-151">**UIAutomationType\_String**</span></span>
3.  <span data-ttu-id="30ce6-152">Use a função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para criar uma instância do objeto [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) e recuperar um ponteiro para a interface [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) do objeto.</span><span class="sxs-lookup"><span data-stu-id="30ce6-152">Use the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an instance of the [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) object and retrieve a pointer to the object's [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) interface.</span></span>
4.  <span data-ttu-id="30ce6-153">Chame o método [**IUIAutomationRegistrar:: RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) ou [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) e passe o endereço da estrutura [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) ou da estrutura [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) .</span><span class="sxs-lookup"><span data-stu-id="30ce6-153">Call the [**IUIAutomationRegistrar::RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) or [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) method and pass the address of the [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) structure or the [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) structure.</span></span>

<span data-ttu-id="30ce6-154">O método [**IUIAutomationRegistrar:: RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) ou [**REGISTEREVENT**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) retorna uma ID de propriedade ou ID de evento que um aplicativo pode passar para qualquer método de automação de interface do usuário que usa um identificador como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="30ce6-154">The [**IUIAutomationRegistrar::RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) or [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) method returns a property ID or event ID that an application can pass to any UI Automation method that takes such an identifier as a parameter.</span></span> <span data-ttu-id="30ce6-155">Por exemplo, você pode passar uma ID de propriedade registrada para o método [**IUIAutomationElement:: GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) ou para o método [**IUIAutomation:: CreatePropertyCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition) .</span><span class="sxs-lookup"><span data-stu-id="30ce6-155">For example, you can pass a registered property ID to the [**IUIAutomationElement::GetCurrentPropertyValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpropertyvalue) method or to the [**IUIAutomation::CreatePropertyCondition**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-createpropertycondition) method.</span></span>

<span data-ttu-id="30ce6-156">O exemplo a seguir demonstra como registrar uma propriedade personalizada.</span><span class="sxs-lookup"><span data-stu-id="30ce6-156">The following example demonstrates how to register a custom property.</span></span>


```C++
// Declare a variable for holding the custom property ID.
PATTERNID g_MyCustomPropertyID;
// Define a GUID for the custom property.
GUID GUID_MyCustomProperty = { 0x82f383ff, 0x4b4d, 0x40d3, 
    { 0x8e, 0xd2, 0x90, 0xb5, 0x25, 0x8e, 0xaa, 0x19 } };

HRESULT RegisterProperty()
{
    // Fill the structure with the GUID, name, and data type.
    UIAutomationPropertyInfo MyCustomPropertyInfo = 
    {
        GUID_MyCustomProperty,
        L"MyCustomProp",
        UIAutomationType_String
    };

    // Create the registrar object and get the IUIAutomationRegistrar 
    // interface pointer. 
    IUIAutomationRegistrar * pUIARegistrar = NULL;
    CoCreateInstance(CLSID_CUIAutomationRegistrar, NULL, CLSCTX_INPROC_SERVER, 
            IID_IUIAutomationRegistrar, (void **)&pUIARegistrar);

    if (pUIARegistrar == NULL)
        return E_NOINTERFACE;

    // Register the property and retrieve the property ID. 
    HRESULT hr = pUIARegistrar->RegisterProperty(&MyCustomPropertyInfo, &g_MyCustomPropertyID);
    pUIARegistrar->Release();

    return hr;
}
```



<span data-ttu-id="30ce6-157">Os identificadores de propriedade e evento recuperados pelos métodos [**IUIAutomationRegistrar:: RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) e [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) são válidos somente no contexto do aplicativo que os recupera e apenas durante o tempo de vida do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="30ce6-157">The property and event identifiers retrieved by the [**IUIAutomationRegistrar::RegisterProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerproperty) and [**RegisterEvent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerevent) methods are valid only in the context of the application that retrieves them, and only for the duration of the application's lifetime.</span></span> <span data-ttu-id="30ce6-158">Os métodos de registro podem retornar valores inteiros diferentes para o mesmo GUID quando ele é chamado em instâncias de tempo de execução diferentes do mesmo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="30ce6-158">The registration methods can return different integer values for the same GUID when it is called over different runtime instances of the same application.</span></span>

<span data-ttu-id="30ce6-159">Não há nenhum método que cancele o registro de uma propriedade ou evento personalizado.</span><span class="sxs-lookup"><span data-stu-id="30ce6-159">There is no method that unregisters a custom property or event.</span></span> <span data-ttu-id="30ce6-160">Em vez disso, eles são implicitamente cancelados no registro quando o último objeto de automação da interface do usuário é liberado.</span><span class="sxs-lookup"><span data-stu-id="30ce6-160">Instead, they are implicitly unregistered when the last UI Automation object is released.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="30ce6-161">Se o seu código for um cliente Microsoft Acessibilidade Ativa (MSAA), você deverá chamar a função [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) quando alterar o valor de uma propriedade personalizada.</span><span class="sxs-lookup"><span data-stu-id="30ce6-161">If your code is a Microsoft Active Accessibility (MSAA) client, you must call the [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) function when you change the value of a custom property.</span></span>

 

## <a name="implementing-custom-control-patterns"></a><span data-ttu-id="30ce6-162">Implementando padrões de controle personalizados</span><span class="sxs-lookup"><span data-stu-id="30ce6-162">Implementing Custom Control Patterns</span></span>

<span data-ttu-id="30ce6-163">Um padrão de controle personalizado não está incluído na API de automação da interface do usuário, mas é fornecido por terceiros em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="30ce6-163">A custom control pattern is not included in the UI Automation API, but is provided by a third party at run time.</span></span> <span data-ttu-id="30ce6-164">Os desenvolvedores de aplicativos cliente e provedor devem trabalhar juntos para definir um padrão de controle personalizado, incluindo os métodos, as propriedades e os eventos que o padrão de controle dará suporte.</span><span class="sxs-lookup"><span data-stu-id="30ce6-164">Developers of client and provider applications must work together to define a custom control pattern, including the methods, properties, and events that the control pattern will support.</span></span> <span data-ttu-id="30ce6-165">Depois de definir o padrão de controle, o cliente e o provedor devem implementar o suporte a objetos Component Object Model (COM), juntamente com o código para registrar o padrão de controle em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="30ce6-165">After defining the control pattern, both the client and the provider must implement supporting Component Object Model (COM) objects, along with code to register the control pattern at run time.</span></span> <span data-ttu-id="30ce6-166">Um padrão de controle personalizado requer a implementação de dois objetos COM: um wrapper de cliente e um manipulador de padrão.</span><span class="sxs-lookup"><span data-stu-id="30ce6-166">A custom control pattern requires the implementation of two COM objects: a client wrapper and a pattern handler.</span></span>

> [!Note]  
> <span data-ttu-id="30ce6-167">Os exemplos nos tópicos a seguir ilustram como implementar um padrão de controle personalizado que duplica a funcionalidade do padrão de controle de [valor](uiauto-implementingvalue.md) existente.</span><span class="sxs-lookup"><span data-stu-id="30ce6-167">The examples in the following topics illustrate how to implement a custom control pattern that duplicates the functionality of the existing [Value](uiauto-implementingvalue.md) control pattern.</span></span> <span data-ttu-id="30ce6-168">Esses exemplos são apenas para fins de instrução.</span><span class="sxs-lookup"><span data-stu-id="30ce6-168">These examples are for instructional purposes only.</span></span> <span data-ttu-id="30ce6-169">Um padrão de controle personalizado real deve fornecer funcionalidade que não está disponível nos padrões de controle de automação da interface do usuário padrão.</span><span class="sxs-lookup"><span data-stu-id="30ce6-169">An actual custom control pattern should provide functionality that is not available from the standard UI Automation control patterns.</span></span>

 

### <a name="the-client-wrapper-and-the-pattern-handler"></a><span data-ttu-id="30ce6-170">O wrapper do cliente e o manipulador de padrão</span><span class="sxs-lookup"><span data-stu-id="30ce6-170">The Client Wrapper and the Pattern Handler</span></span>

<span data-ttu-id="30ce6-171">O wrapper do cliente implementa a API que é usada pelo cliente para recuperar propriedades e métodos de chamada expostos pelo padrão de controle personalizado.</span><span class="sxs-lookup"><span data-stu-id="30ce6-171">The client wrapper implements the API that is used by the client to retrieve properties and call methods exposed by the custom control pattern.</span></span> <span data-ttu-id="30ce6-172">A API é implementada como uma interface COM que passa todas as solicitações de propriedade e chamadas de método para o núcleo de automação da interface do usuário, que realiza marshaling das solicitações e chamadas para o provedor.</span><span class="sxs-lookup"><span data-stu-id="30ce6-172">The API is implemented as a COM interface that passes all property requests and method calls to the UI Automation core, which then marshals the requests and calls to the provider.</span></span>

<span data-ttu-id="30ce6-173">O código que registra um padrão de controle personalizado deve fornecer uma fábrica de classes que a automação da interface do usuário pode usar para criar instâncias do objeto de wrapper do cliente.</span><span class="sxs-lookup"><span data-stu-id="30ce6-173">The code that registers a custom control pattern must supply a class factory that UI Automation can use to create instances of the client wrapper object.</span></span> <span data-ttu-id="30ce6-174">Quando um padrão de controle personalizado é registrado com êxito, a automação da interface do usuário retorna um ponteiro de interface [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) que é usado pelo cliente para encaminhar solicitações de propriedade e chamadas de métodos para o núcleo de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="30ce6-174">When a custom control pattern is successfully registered, UI Automation returns an [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) interface pointer that is used by the client to forward property requests and methods calls to the UI Automation core.</span></span>

<span data-ttu-id="30ce6-175">No lado do provedor, o núcleo de automação da interface do usuário usa as solicitações de propriedade e chamadas de método do cliente e as passa para o objeto de manipulador de padrão.</span><span class="sxs-lookup"><span data-stu-id="30ce6-175">On the provider side, the UI Automation core takes the property requests and method calls from the client and passes them to the pattern handler object.</span></span> <span data-ttu-id="30ce6-176">Em seguida, o manipulador de padrões chama os métodos apropriados na interface do provedor para o padrão de controle personalizado.</span><span class="sxs-lookup"><span data-stu-id="30ce6-176">The pattern handler then calls the appropriate methods on the provider interface for the custom control pattern.</span></span>

<span data-ttu-id="30ce6-177">O código que registra um padrão de controle personalizado cria o objeto de manipulador de padrão e, ao registrar o padrão de controle, fornece automação de interface do usuário com um ponteiro para a interface [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) do objeto.</span><span class="sxs-lookup"><span data-stu-id="30ce6-177">The code that registers a custom control pattern creates the pattern handler object and, when registering the control pattern, provides UI Automation with a pointer to the object's [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) interface.</span></span>

<span data-ttu-id="30ce6-178">O diagrama a seguir mostra como uma solicitação de propriedade de cliente ou uma chamada de método flui do wrapper do cliente, por meio dos componentes principais de automação da interface do usuário para o manipulador de padrões e, em seguida, para a interface do provedor.</span><span class="sxs-lookup"><span data-stu-id="30ce6-178">The following diagram shows how a client property request or method call flows from the client wrapper, through the UI Automation core components to the pattern handler, and then to the provider interface.</span></span>

![diagrama mostrando o fluxo do wrapper do cliente para o manipulador de padrões e o provedor](images/custompatternsupport.jpg)

<span data-ttu-id="30ce6-180">Os objetos que implementam as interfaces do manipulador de padrões e do wrapper do cliente devem ser de thread livre.</span><span class="sxs-lookup"><span data-stu-id="30ce6-180">The objects that implement the client wrapper and pattern handler interfaces must be free-threaded.</span></span> <span data-ttu-id="30ce6-181">Além disso, o núcleo de automação da interface do usuário deve ser capaz de chamar os objetos diretamente sem qualquer código de marshaling intermediário.</span><span class="sxs-lookup"><span data-stu-id="30ce6-181">Also, the UI Automation core must be able to call the objects directly without any intermediate marshaling code.</span></span>

### <a name="implementing-the-client-wrapper"></a><span data-ttu-id="30ce6-182">Implementando o wrapper do cliente</span><span class="sxs-lookup"><span data-stu-id="30ce6-182">Implementing the Client Wrapper</span></span>

<span data-ttu-id="30ce6-183">O wrapper do cliente é um objeto que expõe uma interface IXxxPattern que o cliente usa para solicitar Propriedades e chamar métodos com suporte pelo padrão de controle personalizado.</span><span class="sxs-lookup"><span data-stu-id="30ce6-183">The client wrapper is an object that exposes an IXxxPattern interface that the client uses to request properties and call methods supported by the custom control pattern.</span></span> <span data-ttu-id="30ce6-184">A interface consiste em um par de métodos "getter" para cada propriedade com suporte (get \_ CurrentXxx e get \_ CachedXxx Method) e um método "Caller" para cada método com suporte.</span><span class="sxs-lookup"><span data-stu-id="30ce6-184">The interface consists of a pair of "getter" methods for each supported property (get\_CurrentXxx and get\_CachedXxx method), and a "caller" method for each supported method.</span></span> <span data-ttu-id="30ce6-185">Quando o objeto é instanciado, o construtor de objeto recebe um ponteiro para a interface [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) , que é implementada pelo núcleo de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="30ce6-185">When the object is instantiated, the object constructor receives a pointer to the [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) interface, which is implemented by the UI Automation core.</span></span> <span data-ttu-id="30ce6-186">Os métodos da interface IXxxPattern usam os métodos [**IUIAutomationPatternInstance:: GetProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-getproperty) e [**CallMethod**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-callmethod) para encaminhar solicitações de propriedade e chamadas de método para o núcleo de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="30ce6-186">The methods of the IXxxPattern interface use the [**IUIAutomationPatternInstance::GetProperty**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-getproperty) and [**CallMethod**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatterninstance-callmethod) methods to forward property requests and method calls to the UI Automation core.</span></span>

<span data-ttu-id="30ce6-187">O exemplo a seguir mostra como implementar um objeto de wrapper de cliente para um padrão de controle personalizado simples que dá suporte a uma única propriedade.</span><span class="sxs-lookup"><span data-stu-id="30ce6-187">The following example shows how to implement a client wrapper object for a simple custom control pattern that supports a single property.</span></span> <span data-ttu-id="30ce6-188">Para obter um exemplo mais complexo, consulte [exemplo de implementação de um padrão de controle personalizado](#example-implementation-of-a-custom-control-pattern).</span><span class="sxs-lookup"><span data-stu-id="30ce6-188">For a more complex example, see [Example Implementation of a Custom Control Pattern](#example-implementation-of-a-custom-control-pattern).</span></span>


```C++
// Define the client interface.
interface __declspec(uuid("c78b266d-b2c0-4e9d-863b-e3f74a721d47"))
IMyCustomPattern : public IUnknown
{
    STDMETHOD (get_CurrentIsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (get_CachedIsReadOnly)(BOOL * pIsReadOnly) = 0;
};

// Implement the client wrapper class.
class CMyValuePatternClientWrapper :
    public IMyCustomPattern
{
    IUIAutomationPatternInstance * _pInstance;
    
public:
    // Get IUIAutomationPatternInstance interface pointer from the
    // UI Automation core.
    CMyValuePatternClientWrapper(IUIAutomationPatternInstance * pInstance)
        : _pInstance(pInstance)
    {
        _pInstance->AddRef();
    }
    
    ~CMyValuePatternClientWrapper()
    {
        _pInstance->Release();
    }

    // Note: Put standard IUnknown implementation here.

    STDMETHODIMP get_CurrentIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(0, FALSE, UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP get_CachedIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(0, TRUE, UIAutomationType_Bool, pIsReadOnly);
    }
};
```



### <a name="implementing-the-pattern-handler"></a><span data-ttu-id="30ce6-189">Implementando o manipulador de padrões</span><span class="sxs-lookup"><span data-stu-id="30ce6-189">Implementing the Pattern Handler</span></span>

<span data-ttu-id="30ce6-190">O manipulador de padrões é um objeto que implementa a interface [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) .</span><span class="sxs-lookup"><span data-stu-id="30ce6-190">The pattern handler is an object that implements the [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) interface.</span></span> <span data-ttu-id="30ce6-191">Essa interface tem dois métodos: [**IUIAutomationPatternHandler:: CreateClientWrapper**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-createclientwrapper) e [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch).</span><span class="sxs-lookup"><span data-stu-id="30ce6-191">This interface has two methods: [**IUIAutomationPatternHandler::CreateClientWrapper**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-createclientwrapper) and [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch).</span></span> <span data-ttu-id="30ce6-192">O método **CreateClientWrapper** é chamado pelo núcleo de automação da interface do usuário e recebe um ponteiro para a interface [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) .</span><span class="sxs-lookup"><span data-stu-id="30ce6-192">The **CreateClientWrapper** method is called by the UI Automation core and receives a pointer to the [**IUIAutomationPatternInstance**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatterninstance) interface.</span></span> <span data-ttu-id="30ce6-193">**CreateClientWrapper** responde instanciando o objeto wrapper do cliente e passando o ponteiro de interface **IUIAutomationPatternInstance** para o construtor do wrapper do cliente.</span><span class="sxs-lookup"><span data-stu-id="30ce6-193">**CreateClientWrapper** responds by instantiating the client wrapper object and passing the **IUIAutomationPatternInstance** interface pointer to the client wrapper constructor.</span></span>

<span data-ttu-id="30ce6-194">O método de [**expedição**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch) é usado pelo núcleo de automação da interface do usuário para passar solicitações de propriedade e chamadas de método para a interface do provedor para o padrão de controle personalizado.</span><span class="sxs-lookup"><span data-stu-id="30ce6-194">The [**Dispatch**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationpatternhandler-dispatch) method is used by the UI Automation core to pass property requests and method calls to the provider interface for the custom control pattern.</span></span> <span data-ttu-id="30ce6-195">Os parâmetros incluem um ponteiro para a interface do provedor, o índice de base zero do getter de propriedade ou o método que está sendo chamado e uma matriz de estruturas [**UIAutomationParameter**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationparameter) que contêm os parâmetros a serem passados para o provedor.</span><span class="sxs-lookup"><span data-stu-id="30ce6-195">Parameters include a pointer to the provider interface, the zero-based index of the property getter or method being called, and an array of [**UIAutomationParameter**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationparameter) structures that contain the parameters to pass to the provider.</span></span> <span data-ttu-id="30ce6-196">O manipulador de padrões responde verificando o parâmetro de índice para determinar qual método de provedor deve ser chamado e, em seguida, chama essa interface de provedor, passando os parâmetros contidos nas estruturas **UIAutomationParameter** .</span><span class="sxs-lookup"><span data-stu-id="30ce6-196">The pattern handler responds by checking the index parameter to determine which provider method to call, and then calls that provider interface, passing the parameters contained in the **UIAutomationParameter** structures.</span></span>

<span data-ttu-id="30ce6-197">O objeto de manipulador de padrão é instanciado pelo mesmo código que registra o padrão de controle personalizado, antes de o padrão de controle ser registrado.</span><span class="sxs-lookup"><span data-stu-id="30ce6-197">The pattern handler object is instantiated by the same code that registers the custom control pattern, before the control pattern is registered.</span></span> <span data-ttu-id="30ce6-198">O código deve passar o ponteiro de interface [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) do objeto de manipulador padrão para o núcleo de automação da interface do usuário no momento do registro.</span><span class="sxs-lookup"><span data-stu-id="30ce6-198">The code must pass the pattern handler object's [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) interface pointer to the UI Automation core at registration time.</span></span>

<span data-ttu-id="30ce6-199">O exemplo a seguir mostra como implementar um objeto de manipulador de padrão para um padrão de controle personalizado simples que dá suporte a uma única propriedade.</span><span class="sxs-lookup"><span data-stu-id="30ce6-199">The following example shows how to implement a pattern handler object for a simple custom control pattern that supports a single property.</span></span> <span data-ttu-id="30ce6-200">Para obter um exemplo mais complexo, consulte [exemplo de implementação de um padrão de controle personalizado](#example-implementation-of-a-custom-control-pattern).</span><span class="sxs-lookup"><span data-stu-id="30ce6-200">For a more complex example, see [Example Implementation of a Custom Control Pattern](#example-implementation-of-a-custom-control-pattern).</span></span>


```C++
// Define the provider interface.
interface __declspec(uuid("9f5266dd-f0ab-4562-8175-c383abb2569e"))
IMyValueProvider : public IUnknown
{
    STDMETHOD (get_IsReadOnly)(BOOL * pIsReadOnly) = 0;
};            

// Index used by IUIAutomationPatternHandler::Dispatch.
const int MyValue_GetIsReadOnly = 0; 
            
// Define the pattern handler class.        
class CMyValuePatternHandler : public IUIAutomationPatternHandler
{
public:
    
    // Put standard IUnknown implementation here.

    STDMETHODIMP CreateClientWrapper(
            IUIAutomationPatternInstance * pPatternInstance, 
            IUnknown ** pClientWrapper)
    {
        *pClientWrapper = new CMyValuePatternClientWrapper(pPatternInstance);
        if (*pClientWrapper == NULL)
            return E_INVALIDARG;
        return S_OK;
    }
    
    STDMETHODIMP Dispatch (IUnknown * pTarget, UINT index, 
            const struct UIAutomationParameter *pParams, UINT cParams)
    {
        switch(index)
        {
        case MyValue_GetIsReadOnly:
            return ((IMyValueProvider*)pTarget)->get_IsReadOnly((BOOL*)pParams[0].pData);
        }
        return E_INVALIDARG;
    }
};
```



### <a name="registering-a-custom-control-pattern"></a><span data-ttu-id="30ce6-201">Registrando um padrão de controle personalizado</span><span class="sxs-lookup"><span data-stu-id="30ce6-201">Registering a Custom Control Pattern</span></span>

<span data-ttu-id="30ce6-202">Antes que possa ser usado, um padrão de controle personalizado deve ser registrado pelo provedor e pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="30ce6-202">Before it can be used, a custom control pattern must be registered by both the provider and the client.</span></span> <span data-ttu-id="30ce6-203">O registro fornece o núcleo de automação da interface do usuário com informações detalhadas sobre o padrão de controle e fornece o provedor ou o cliente com a ID do padrão de controle e as IDs para as propriedades e eventos que são suportados pelo padrão de controle.</span><span class="sxs-lookup"><span data-stu-id="30ce6-203">Registering provides the UI Automation core with detailed information about the control pattern, and supplies the provider or client with the control pattern ID, and IDs for the properties and events that are supported by the control pattern.</span></span> <span data-ttu-id="30ce6-204">No lado do provedor, o padrão de controle personalizado deve ser registrado antes que o controle associado manipule a mensagem do [**WM \_ GetObject**](wm-getobject.md) ou ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="30ce6-204">On the provider side, the custom control pattern must be registered before the associated control handles the [**WM\_GETOBJECT**](wm-getobject.md) message, or at the same time.</span></span>

<span data-ttu-id="30ce6-205">Ao registrar um padrão de controle personalizado, o provedor ou o cliente fornece as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="30ce6-205">When registering a custom control pattern, the provider or client supplies the following information:</span></span>

-   <span data-ttu-id="30ce6-206">O GUID do padrão de controle personalizado.</span><span class="sxs-lookup"><span data-stu-id="30ce6-206">The GUID of the custom control pattern.</span></span>
-   <span data-ttu-id="30ce6-207">Uma cadeia de caracteres não localizável que contém o nome do padrão de controle personalizado.</span><span class="sxs-lookup"><span data-stu-id="30ce6-207">A nonlocalizable string containing the name of the custom control pattern.</span></span>
-   <span data-ttu-id="30ce6-208">O GUID da interface do provedor que dá suporte ao padrão de controle personalizado.</span><span class="sxs-lookup"><span data-stu-id="30ce6-208">The GUID of the provider interface that supports the custom control pattern.</span></span>
-   <span data-ttu-id="30ce6-209">O GUID da interface do cliente que dá suporte ao padrão de controle personalizado.</span><span class="sxs-lookup"><span data-stu-id="30ce6-209">The GUID of the client interface that supports the custom control pattern.</span></span>
-   <span data-ttu-id="30ce6-210">Uma matriz de estruturas [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) que descrevem as propriedades com suporte pelo padrão de controle personalizado.</span><span class="sxs-lookup"><span data-stu-id="30ce6-210">An array of [**UIAutomationPropertyInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo) structures that describe the properties supported by the custom control pattern.</span></span> <span data-ttu-id="30ce6-211">Para cada propriedade, o GUID, o nome da propriedade e o tipo de dados devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="30ce6-211">For each property, the GUID, property name, and data type must be specified.</span></span>
-   <span data-ttu-id="30ce6-212">Uma matriz de estruturas [**UIAutomationMethodInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationmethodinfo) que descreve os métodos com suporte pelo padrão de controle personalizado.</span><span class="sxs-lookup"><span data-stu-id="30ce6-212">An array of [**UIAutomationMethodInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationmethodinfo) structures that describe the methods supported by the custom control pattern.</span></span> <span data-ttu-id="30ce6-213">Para cada método, a estrutura inclui as seguintes informações: o nome do método, uma contagem de parâmetros, uma lista de tipos de dados de parâmetro e uma lista de nomes de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="30ce6-213">For each method, the structure includes the following information: the method name, a count of parameters, a list of parameter data types, and a list of the parameter names.</span></span>
-   <span data-ttu-id="30ce6-214">Uma matriz de estruturas [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) que descreve os eventos gerados pelo padrão de controle personalizado.</span><span class="sxs-lookup"><span data-stu-id="30ce6-214">An array of [**UIAutomationEventInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo) structures that describe the events raised by the custom control pattern.</span></span> <span data-ttu-id="30ce6-215">Para cada evento, o GUID e o nome do evento devem ser especificados.</span><span class="sxs-lookup"><span data-stu-id="30ce6-215">For each event, the GUID and event name must be specified.</span></span>
-   <span data-ttu-id="30ce6-216">O endereço da interface [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) do objeto de manipulador de padrão que torna o padrão de controle personalizado disponível para os clientes.</span><span class="sxs-lookup"><span data-stu-id="30ce6-216">The address of the [**IUIAutomationPatternHandler**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationpatternhandler) interface of the pattern handler object that makes the custom control pattern available to clients.</span></span>

<span data-ttu-id="30ce6-217">Para registrar o padrão de controle personalizado, o provedor ou o código do cliente deve executar as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="30ce6-217">To register the custom control pattern, the provider or client code must perform the following steps:</span></span>

1.  <span data-ttu-id="30ce6-218">Preencha uma estrutura [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) com as informações anteriores.</span><span class="sxs-lookup"><span data-stu-id="30ce6-218">Fill a [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) structure with the preceding information.</span></span>
2.  <span data-ttu-id="30ce6-219">Use a função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para criar uma instância do objeto [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) e recuperar um ponteiro para a interface [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) do objeto.</span><span class="sxs-lookup"><span data-stu-id="30ce6-219">Use the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) function to create an instance of the [**CUIAutomationRegistrar**](/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)) object and retrieve a pointer to the object's [**IUIAutomationRegistrar**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iuiautomationregistrar) interface.</span></span>
3.  <span data-ttu-id="30ce6-220">Chame o método [**IUIAutomationRegistrar:: RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) , passando o endereço da estrutura [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) .</span><span class="sxs-lookup"><span data-stu-id="30ce6-220">Call the [**IUIAutomationRegistrar::RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) method, passing the address of the [**UIAutomationPatternInfo**](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo) structure.</span></span>

<span data-ttu-id="30ce6-221">O método [**RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) retorna uma ID de padrão de controle, juntamente com uma lista de IDs de propriedade e IDs de evento.</span><span class="sxs-lookup"><span data-stu-id="30ce6-221">The [**RegisterPattern**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iuiautomationregistrar-registerpattern) method returns a control pattern ID, along with a list of property IDs and event IDs.</span></span> <span data-ttu-id="30ce6-222">Um aplicativo pode passar essas IDs para qualquer método de automação de interface do usuário que usa um identificador como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="30ce6-222">An application can pass these IDs to any UI Automation method that takes such an identifier as a parameter.</span></span> <span data-ttu-id="30ce6-223">Por exemplo, você pode passar uma ID de padrão registrado para o método [**IUIAutomationElement:: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) para recuperar um ponteiro para a interface do provedor para o padrão de controle.</span><span class="sxs-lookup"><span data-stu-id="30ce6-223">For example, you can pass a registered pattern ID to the [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) method to retrieve a pointer to the provider interface for the control pattern.</span></span>

<span data-ttu-id="30ce6-224">Não há nenhum método que cancele o registro de um padrão de controle personalizado.</span><span class="sxs-lookup"><span data-stu-id="30ce6-224">There is no method that unregisters a custom control pattern.</span></span> <span data-ttu-id="30ce6-225">Em vez disso, ele é implicitamente cancelado quando o último objeto de automação da interface do usuário é liberado.</span><span class="sxs-lookup"><span data-stu-id="30ce6-225">Instead, it is implicitly unregistered when the last UI Automation object is released.</span></span>

<span data-ttu-id="30ce6-226">Para obter um exemplo que mostra como registrar um padrão de controle personalizado, consulte a seção a seguir.</span><span class="sxs-lookup"><span data-stu-id="30ce6-226">For an example that shows how to register a custom control pattern, see the following section.</span></span>

### <a name="example-implementation-of-a-custom-control-pattern"></a><span data-ttu-id="30ce6-227">Exemplo de implementação de um padrão de controle personalizado</span><span class="sxs-lookup"><span data-stu-id="30ce6-227">Example Implementation of a Custom Control Pattern</span></span>

<span data-ttu-id="30ce6-228">Esta seção contém um código de exemplo que demonstra como implementar o wrapper do cliente e objetos de manipulador de padrão para um padrão de controle personalizado.</span><span class="sxs-lookup"><span data-stu-id="30ce6-228">This section contains example code that demonstrates how to implement the client wrapper and pattern handler objects for a custom control pattern.</span></span> <span data-ttu-id="30ce6-229">O exemplo implementa um padrão de controle personalizado baseado no padrão de controle de [valor](uiauto-implementingvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="30ce6-229">The example implements a custom control pattern that is based on the [Value](uiauto-implementingvalue.md) control pattern.</span></span>


```C++
// Step 1: Define the public provider and client interfaces using IDL. Interface 
// definitions are in C here to simplify the example.

// Define the provider interface.
interface __declspec(uuid("9f5266dd-f0ab-4562-8175-c383abb2569e"))
IMyValueProvider : public IUnknown
{
    STDMETHOD (get_Value)(BSTR * pValue) = 0;
    STDMETHOD (get_IsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (SetValue)(LPCWSTR pNewValue) = 0;
    STDMETHOD (Reset)() = 0;
};

// Define the client interface.
interface __declspec(uuid("103b8323-b04a-4180-9140-8c1e437713a3"))
IUIAutomationMyValuePattern : public IUnknown
{
    STDMETHOD (get_CurrentValue)(BSTR * pValue) = 0;
    STDMETHOD (get_CachedValue)(BSTR * pValue) = 0;

    STDMETHOD (get_CurrentIsReadOnly)(BOOL * pIsReadOnly) = 0;
    STDMETHOD (get_CachedIsReadOnly)(BOOL * pIsReadOnly) = 0;

    STDMETHOD (SetValue)(LPCWSTR pNewValue) = 0;
    STDMETHOD (Reset)() = 0;
};

// Enumerate the properties and methods starting from 0, and placing the 
// properties first. 
enum
{
    MyValue_GetValue = 0,
    MyValue_GetIsReadOnly = 1,
    MyValue_SetValue = 2,
    MyValue_Reset = 3,
};

// Step 2: Implement the client wrapper class.
class CMyValuePatternClientWrapper :
    public IUIAutomationMyValuePattern
{
    IUIAutomationPatternInstance * _pInstance;

public:
    // Get IUIAutomationPatternInstance interface pointer.
    CMyValuePatternClientWrapper(IUIAutomationPatternInstance * pInstance)
    {
        _pInstance = pInstance;
        _pInstance->AddRef();
    }

    // Put standard IUnknown implementation here.

    STDMETHODIMP get_CurrentValue(BSTR * pValue)
    {
        return _pInstance->GetProperty(MyValue_GetValue, FALSE, 
                UIAutomationType_String, pValue);
    }

    STDMETHODIMP get_CachedValue(BSTR * pValue)
    {
        return _pInstance->GetProperty(MyValue_GetValue, TRUE, 
                UIAutomationType_String, pValue);
    }

    STDMETHODIMP get_CurrentIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(MyValue_GetIsReadOnly, FALSE, 
                UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP get_CachedIsReadOnly(BOOL * pIsReadOnly)
    {
        return _pInstance->GetProperty(MyValue_GetIsReadOnly, TRUE, 
                UIAutomationType_Bool, pIsReadOnly);
    }

    STDMETHODIMP SetValue(LPCWSTR pValue)
    {
        UIAutomationParameter SetValueParams[] = 
                { UIAutomationType_String, &pValue };
        return _pInstance->CallMethod(MyValue_SetValue,  SetValueParams, 
                ARRAYSIZE(SetValueParams));
    }

    STDMETHODIMP Reset()
    {
        return _pInstance->CallMethod(MyValue_Reset, NULL, 0);
    }
};

// Step 3: Implement the pattern handler class.
class CMyValuePatternHandler : public IUIAutomationPatternHandler
{
public:

    // Put standard IUnknown implementation here.
    
    STDMETHODIMP CreateClientWrapper(
            IUIAutomationPatternInstance * pPatternInstance, 
            IUnknown ** pClientWrapper)
    {
        *pClientWrapper = new CMyValuePatternClientWrapper(pPatternInstance);
        if (*pClientWrapper == NULL)
            return E_INVALIDARG;
        return S_OK;
    }
    
    STDMETHODIMP Dispatch (IUnknown * pTarget, UINT index, 
            const struct UIAutomationParameter *pParams, 
            UINT cParams)
    {
        switch(index)
        {
        case MyValue_GetValue:
            return ((IMyValueProvider*)pTarget)->get_Value((BSTR*)pParams[0].pData);

        case MyValue_GetIsReadOnly:
            return ((IMyValueProvider*)pTarget)->get_IsReadOnly((BOOL*)pParams[0].pData);

        case MyValue_SetValue:
            return ((IMyValueProvider*)pTarget)->SetValue(*(LPCWSTR*)pParams[0].pData);

        case MyValue_Reset:
            return ((IMyValueProvider*)pTarget)->Reset();
        }
        return E_INVALIDARG;
    }
};

CMyValuePatternHandler g_MyValuePatternHandler;

// Step 4: Declare information about the properties and methods supported
// by the custom control pattern.

// Define GUIDs for the custom control pattern and each of its properties 
// and events.
static const GUID MyValue_Pattern_Guid = { 0xa49aa3c0, 0xe413, 0x4ecf, 
        { 0xa1, 0xc3, 0x37, 0x42, 0xa7, 0x86, 0x67, 0x3f } };
static const GUID MyValue_Value_Property_Guid = { 0xe58f3f67, 0x22c7, 0x44f0, 
        { 0x83, 0x55, 0xd8, 0x76, 0x14, 0xa1, 0x10, 0x81 } };
static const GUID MyValue_IsReadOnly_Property_Guid = { 0x480540f2, 0x9829, 0x4acd, 
        { 0xb8, 0xea, 0x6e, 0x2a, 0xdc, 0xe5, 0x3a, 0xfb } };
static const GUID MyValue_Reset_Event_Guid = { 0x5b80edd3, 0x67f, 0x4a70, 
        { 0xb0, 0x7, 0x4, 0x12, 0x85, 0x11, 0x1, 0x7a } };

// Declare information about the properties, in the same order as the
// previously defined "MyValue_" enumerated type.
UIAutomationPropertyInfo g_MyValueProperties[] = 
{
    // GUID, name, data type.
    { MyValue_Value_Property_Guid, L"MyValuePattern.Value", 
                                                    UIAutomationType_String },
    { MyValue_IsReadOnly_Property_Guid, L"MyValuePattern.IsReadOnly", 
                                                    UIAutomationType_Bool },
};

// Declare information about the event.
UIAutomationEventInfo g_MyValueEvents [] =
{
    { MyValue_Reset_Event_Guid,  L"MyValuePattern.Reset" },
};

// Declare the data type and name of the SetValue method parameter. 
UIAutomationType g_SetValueParamTypes[] = { UIAutomationType_String };
LPCWSTR g_SetValueParamNames[] = {L"pNewValue"};

// Declare information about the methods.
UIAutomationMethodInfo g_MyValueMethods[] =
{
    // Name, focus flag, count of in parameters, count of out parameters, types, parameter names.
    { L"MyValuePattern.SetValue", TRUE, 1, 0, g_SetValueParamTypes, g_SetValueParamNames },
    { L"MyValuePattern.Reset", TRUE, 0, 0, NULL, NULL },
};

// Declare the custom control pattern using the previously defined information.
UIAutomationPatternInfo g_ValuePatternInfo =
{
    MyValue_Pattern_Guid,
    L"MyValuePattern",
    __uuidof(IMyValueProvider),
    __uuidof(IUIAutomationMyValuePattern),
    ARRAYSIZE(g_MyValueProperties), g_MyValueProperties, // properties
    ARRAYSIZE(g_MyValueMethods), g_MyValueMethods,       // methods
    ARRAYSIZE(g_MyValueEvents), g_MyValueEvents,         // events 
    &g_MyValuePatternHandler
};

// Step 5: Register the custom control pattern and retrieve the control pattern and property 
// identifiers.

// Control pattern, property, and event IDs.
PATTERNID  g_MyValue_PatternID;
PROPERTYID g_MyValue_Value_PropertyID;
PROPERTYID g_MyValue_IsReadOnly_PropertyID;
EVENTID    g_MyValueReset_EventID;

// ID used by the client to determine whether the custom control pattern is available.
PROPERTYID g_IsMyValuePatternAvailable_PropertyID;

HRESULT RegisterPattern()
{
    // Create the registrar object and get the IUIAutomationRegistrar interface pointer. 
    IUIAutomationRegistrar * pUIARegistrar;
    CoCreateInstance(CLSID_CUIAutomationRegistrar, NULL, CLSCTX_INPROC_SERVER, 
            IID_IUIAutomationRegistrar, (void **)&pUIARegistrar);

    if (pUIARegistrar == NULL)
        return E_NOINTERFACE;

    PROPERTYID propIDs[2]; // Array for property IDs.

    // Register the control pattern.
    HRESULT hr = pUIARegistrar->RegisterPattern(
        &g_ValuePatternInfo,
        &g_MyValue_PatternID,
        &g_IsMyValuePatternAvailable_PropertyID,
        ARRAYSIZE(propIDs), 
        propIDs,
        1,
        &g_MyValueReset_EventID);
            
    if (hr == S_OK)
    {
        // Copy the property IDs.
        g_MyValue_Value_PropertyID = propIDs[0];
        g_MyValue_IsReadOnly_PropertyID = propIDs[1];
    }

    pUIARegistrar->Release();
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="30ce6-230">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="30ce6-230">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="30ce6-231">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="30ce6-231">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="30ce6-232">Criando Propriedades personalizadas, eventos e padrões de controle</span><span class="sxs-lookup"><span data-stu-id="30ce6-232">Designing Custom Properties, Events, and Control Patterns</span></span>](uiauto-designingcustompropseventpatterns.md)
</dt> <dt>

[<span data-ttu-id="30ce6-233">Visão geral das propriedades de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="30ce6-233">UI Automation Properties Overview</span></span>](uiauto-propertiesoverview.md)
</dt> <dt>

[<span data-ttu-id="30ce6-234">Visão geral sobre eventos de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="30ce6-234">UI Automation Events Overview</span></span>](uiauto-eventsoverview.md)
</dt> <dt>

[<span data-ttu-id="30ce6-235">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="30ce6-235">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 