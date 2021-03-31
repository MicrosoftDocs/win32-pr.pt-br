---
title: Adicionando a funcionalidade de automação da interface do usuário a servidores Acessibilidade Ativa
description: Controles que não têm um provedor de automação da interface do usuário da Microsoft, mas que implementam o IAccessible, podem ser facilmente atualizados para fornecer algumas funcionalidades de automação da interface do usuário, implementando a interface IAccessibleEx.
ms.assetid: 7ceab704-3e02-4550-b236-748e4f0a092a
keywords:
- Automação da interface do usuário, servidores de Acessibilidade Ativa
- Automação da interface do usuário, Microsoft Acessibilidade Ativa Servers
- Automação da interface do usuário, IAccessible
- Automação da interface do usuário, IAccessibleEx
- Automação da interface do usuário, expondo IAccessibleEx
- Automação da interface do usuário, implementando IAccessibleEx
- IAccessible
- IAccessibleEx
- Acessibilidade Ativa da Microsoft
- Acessibilidade Ativa
- expondo IAccessibleEx
- Implementando IAccessibleEx
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f45311deb8d3ec20fb8102285cddea1339373f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917360"
---
# <a name="adding-ui-automation-functionality-to-active-accessibility-servers"></a><span data-ttu-id="c18f7-115">Adicionando a funcionalidade de automação da interface do usuário a servidores Acessibilidade Ativa</span><span class="sxs-lookup"><span data-stu-id="c18f7-115">Adding UI Automation Functionality to Active Accessibility Servers</span></span>

<span data-ttu-id="c18f7-116">Controles que não têm um provedor de automação da interface do usuário da Microsoft, mas que implementam o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , podem ser facilmente atualizados para fornecer algumas funcionalidades de automação da interface do usuário, implementando a interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="c18f7-116">Controls that do not have a Microsoft UI Automation provider but that implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) can easily be upgraded to provide some UI Automation functionality, by implementing the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface.</span></span> <span data-ttu-id="c18f7-117">Essa interface permite que o controle exponha Propriedades de automação da interface do usuário e padrões de controle, sem a necessidade de uma implementação completa das interfaces do provedor de automação da interface do usuário, como [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment).</span><span class="sxs-lookup"><span data-stu-id="c18f7-117">This interface enables the control to expose UI Automation properties and control patterns, without the need for a full implementation of UI Automation provider interfaces such as [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment).</span></span> <span data-ttu-id="c18f7-118">Para implementar **IAccessibleEx**, a hierarquia de objetos de linha de base do Microsoft acessibilidade ativa não deve conter erros ou inconsistências (como um objeto filho cujo objeto pai não o lista como um filho) e não deve entrar em conflito com as especificações de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="c18f7-118">To implement **IAccessibleEx**, the baseline Microsoft Active Accessibility object hierarchy must contain no errors or inconsistencies (such as a child object whose parent object does not list it as a child), and must not conflict with UI Automation specifications.</span></span> <span data-ttu-id="c18f7-119">Se a hierarquia de objetos do Microsoft Acessibilidade Ativa atender a esses requisitos, será um bom candidato para adicionar funcionalidades usando o **IAccessibleEx**; caso contrário, você deve implementar a automação da interface do usuário sozinha ou junto com a implementação do Microsoft Acessibilidade Ativa.</span><span class="sxs-lookup"><span data-stu-id="c18f7-119">If the Microsoft Active Accessibility object hierarchy meets these requirements, it is a good candidate for adding functionality by using **IAccessibleEx**; otherwise, you must implement UI Automation alone or alongside the Microsoft Active Accessibility implementation.</span></span>

<span data-ttu-id="c18f7-120">Use o caso de um controle personalizado que tenha um valor de intervalo.</span><span class="sxs-lookup"><span data-stu-id="c18f7-120">Take the case of a custom control that has a range value.</span></span> <span data-ttu-id="c18f7-121">O Microsoft Acessibilidade Ativa Server para o controle define sua função e é capaz de retornar seu valor atual, mas não tem o meio de retornar os valores mínimo e máximo do controle, pois essas propriedades não são definidas no Microsoft Acessibilidade Ativa.</span><span class="sxs-lookup"><span data-stu-id="c18f7-121">The Microsoft Active Accessibility server for the control defines its role, and is able to return its current value, but lacks the means to return the minimum and maximum values of the control, because these properties are not defined in Microsoft Active Accessibility.</span></span> <span data-ttu-id="c18f7-122">Um cliente de automação de interface do usuário é capaz de recuperar a função do controle, o valor atual e outras propriedades do Microsoft Acessibilidade Ativa, porque o núcleo de automação da interface do usuário pode obtê-los por meio do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="c18f7-122">A UI Automation client is able to retrieve the control's role, current value, and other Microsoft Active Accessibility properties, because the UI Automation core can obtain these through [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="c18f7-123">No entanto, sem acesso a uma interface [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) no objeto, a automação da interface do usuário também não consegue recuperar os valores mínimo e máximo.</span><span class="sxs-lookup"><span data-stu-id="c18f7-123">However, without access to an [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) interface on the object, UI Automation is also unable to retrieve the maximum and minimum values.</span></span>

<span data-ttu-id="c18f7-124">O desenvolvedor de controle poderia fornecer um provedor de automação de interface do usuário completo para o controle, mas isso significaria duplicar grande parte da funcionalidade existente da implementação do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) : por exemplo, navegação e propriedades comuns.</span><span class="sxs-lookup"><span data-stu-id="c18f7-124">The control developer could supply a complete UI Automation provider for the control, but this would mean duplicating much of the existing functionality of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation: for example, navigation and common properties.</span></span> <span data-ttu-id="c18f7-125">Em vez disso, o desenvolvedor pode continuar a confiar no **IAccessible** para fornecer essa funcionalidade, ao mesmo tempo em que adiciona suporte para propriedades específicas de controle por meio de [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).</span><span class="sxs-lookup"><span data-stu-id="c18f7-125">Instead, the developer can continue to rely on **IAccessible** to supply this functionality, while adding support for control-specific properties through [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider).</span></span>

<span data-ttu-id="c18f7-126">A atualização do controle personalizado requer estas etapas principais:</span><span class="sxs-lookup"><span data-stu-id="c18f7-126">Updating the custom control requires these main steps:</span></span>

-   <span data-ttu-id="c18f7-127">Implemente [IServiceProvider](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678965(v=vs.85)) no objeto acessível para que a interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) possa ser encontrada neste ou em um objeto separado.</span><span class="sxs-lookup"><span data-stu-id="c18f7-127">Implement [IServiceProvider](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678965(v=vs.85)) on the accessible object so that the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface can be found on this or a separate object.</span></span>
-   <span data-ttu-id="c18f7-128">Implemente [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) no objeto acessível.</span><span class="sxs-lookup"><span data-stu-id="c18f7-128">Implement [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) on the accessible object.</span></span>
-   <span data-ttu-id="c18f7-129">Crie objetos distintos acessíveis para qualquer item filho da Microsoft Acessibilidade Ativa, que no Microsoft Acessibilidade Ativa pode ter sido representado pela interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) no objeto pai (por exemplo, itens de lista).</span><span class="sxs-lookup"><span data-stu-id="c18f7-129">Create distinct accessible objects for any Microsoft Active Accessibility child items, which in Microsoft Active Accessibility might have been represented by the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface on the parent object (for example, list items).</span></span> <span data-ttu-id="c18f7-130">Implemente [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) nesses objetos.</span><span class="sxs-lookup"><span data-stu-id="c18f7-130">Implement [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) on these objects.</span></span>
-   <span data-ttu-id="c18f7-131">Implemente [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) em todos os objetos acessíveis.</span><span class="sxs-lookup"><span data-stu-id="c18f7-131">Implement [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) on all the accessible objects.</span></span>
-   <span data-ttu-id="c18f7-132">Implemente as interfaces de padrão de controle apropriadas nos objetos acessíveis.</span><span class="sxs-lookup"><span data-stu-id="c18f7-132">Implement the appropriate control pattern interfaces on the accessible objects.</span></span>

<span data-ttu-id="c18f7-133">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="c18f7-133">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c18f7-134">Expondo IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="c18f7-134">Exposing IAccessibleEx</span></span>](#exposing-iaccessibleex)
-   [<span data-ttu-id="c18f7-135">Implementando IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="c18f7-135">Implementing IAccessibleEx</span></span>](#implementing-iaccessibleex)
-   [<span data-ttu-id="c18f7-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c18f7-136">Related topics</span></span>](#related-topics)

## <a name="exposing-iaccessibleex"></a><span data-ttu-id="c18f7-137">Expondo IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="c18f7-137">Exposing IAccessibleEx</span></span>

<span data-ttu-id="c18f7-138">Como a implementação de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) para um controle pode residir em um objeto separado, os aplicativos cliente não podem confiar em [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obter essa interface.</span><span class="sxs-lookup"><span data-stu-id="c18f7-138">Because the implementation of [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) for a control may reside in a separate object, client applications cannot rely on [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to obtain this interface.</span></span> <span data-ttu-id="c18f7-139">Em vez disso, os clientes devem chamar [**IServiceProvider:: QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="c18f7-139">Instead, clients are expected to call [**IServiceProvider::QueryService**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)).</span></span> <span data-ttu-id="c18f7-140">Na implementação de exemplo a seguir desse método, supõe-se que **IAccessibleEx** não está implementado em um objeto separado; Portanto, o método simplesmente chama para **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="c18f7-140">In the following example implementation of this method, it is assumed that **IAccessibleEx** is not implemented on a separate object; therefore the method simply calls through to **QueryInterface**.</span></span>


```C++
HRESULT CListboxAccessibleObject::QueryService(REFGUID guidService, REFIID riid, LPVOID *ppvObject)
{
    if (!ppvObject)
    {
        return E_INVALIDARG;
    }
    *ppvObject = NULL;
    if (guidService == __uuidof(IAccessibleEx))
    {
        return QueryInterface(riid, ppvObject);
    }
    else 
    {
        return E_INVALIDARG;
    }
};
```



## <a name="implementing-iaccessibleex"></a><span data-ttu-id="c18f7-141">Implementando IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="c18f7-141">Implementing IAccessibleEx</span></span>

<span data-ttu-id="c18f7-142">O método de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) que é da maior parte do seu interesse é [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild).</span><span class="sxs-lookup"><span data-stu-id="c18f7-142">The method of [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) that is of most interest is [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild).</span></span> <span data-ttu-id="c18f7-143">Esse método dá ao Microsoft Acessibilidade Ativa Server uma oportunidade de criar um objeto acessível (um que expõe, no mínimo, **IAccessibleEx**) para um item filho.</span><span class="sxs-lookup"><span data-stu-id="c18f7-143">This method gives the Microsoft Active Accessibility server an opportunity to create an accessible object (one that exposes, at a minimum, **IAccessibleEx**) for a child item.</span></span> <span data-ttu-id="c18f7-144">No Microsoft Acessibilidade Ativa, os itens filho normalmente não são representados como objetos acessíveis, mas como filhos de um objeto acessível.</span><span class="sxs-lookup"><span data-stu-id="c18f7-144">In Microsoft Active Accessibility, child items typically are not represented as accessible objects but as children of an accessible object.</span></span> <span data-ttu-id="c18f7-145">No entanto, como a automação da interface do usuário requer que cada elemento seja representado por um objeto acessível separado, **GetObjectForChild** deve criar um objeto separado para cada filho sob demanda.</span><span class="sxs-lookup"><span data-stu-id="c18f7-145">However, because UI Automation requires that each element be represented by a separate accessible object, **GetObjectForChild** must create a separate object for each child on demand.</span></span>

<span data-ttu-id="c18f7-146">A implementação de exemplo a seguir retorna um objeto acessível para um item em uma exibição de lista personalizada.</span><span class="sxs-lookup"><span data-stu-id="c18f7-146">The following example implementation returns an accessible object for an item in a custom list view.</span></span>


```C++
HRESULT CListboxAccessibleObject::GetObjectForChild(long idChild, IAccessibleEx **pRetVal)
{ 
    *pRetVal = NULL;
    VARIANT vChild;
    vChild.vt = VT_I4;
    vChild.lVal = idChild;

    // ValidateChildId is an application-defined function that checks whether
    // the child ID is valid. This is similar to code that validates the varChild
    // parameter in IAccessible methods.
    //
    // Additionally, if this idChild corresponds to a child that has its own
    // IAccessible, we should also return E_INVALIDARG here. (The caller
    // should instead be using the IAccessibleEx from that child's own
    // IAccessible in that case.)
    if (idChild == CHILDID_SELF || FAILED(ValidateChildId(vChild)))
    {
        return E_INVALIDARG;
    }

    // Return a suitable provider for this specific child.
    // This implementation returns a new instance each time; an implementation
    // can cache these if desired.

    // _pListboxControl is a member variable pointer to the owning control.
    IAccessibleEx* pAccEx  = new CListItemAccessibleObject(idChild, _pListboxControl);
    if (pAccEx == NULL)
    {
        return E_OUTOFMEMORY;
    }
    *pRetVal = pAccEx;
    return S_OK; 
}
```



<span data-ttu-id="c18f7-147">Para obter uma implementação de exemplo completa, consulte [tornando os controles personalizados acessíveis, parte 5: usando IAccessibleEx para adicionar suporte à automação da interface do usuário a um controle personalizado](/previous-versions/msdn10/cc307850(v=msdn.10)) no msdn.</span><span class="sxs-lookup"><span data-stu-id="c18f7-147">For a complete sample implementation, see [Making Custom Controls Accessible, Part 5: Using IAccessibleEx to Add UI Automation Support to a Custom Control](/previous-versions/msdn10/cc307850(v=msdn.10)) on MSDN.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c18f7-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c18f7-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c18f7-149">Guia do programador do provedor de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="c18f7-149">UI Automation Provider Programmer's Guide</span></span>](uiauto-providerportal.md)
</dt> </dl>

 

 