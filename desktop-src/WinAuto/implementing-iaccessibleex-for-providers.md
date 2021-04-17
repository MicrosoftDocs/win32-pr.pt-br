---
title: Implementando IAccessibleEx para provedores
description: Esta seção explica como adicionar recursos do provedor de automação de interface do usuário da Microsoft a um Microsoft Acessibilidade Ativa Server implementando a interface IAccessibleEx.
ms.assetid: c03dc552-7919-4a35-8ff2-4cdd822bc0b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9460ccbd243aef390b7ade0deb41626173c927a0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105790264"
---
# <a name="implementing-iaccessibleex-for-providers"></a><span data-ttu-id="c6de9-103">Implementando IAccessibleEx para provedores</span><span class="sxs-lookup"><span data-stu-id="c6de9-103">Implementing IAccessibleEx for Providers</span></span>

<span data-ttu-id="c6de9-104">Esta seção explica como adicionar recursos do provedor de automação de interface do usuário da Microsoft a um Microsoft Acessibilidade Ativa Server implementando a interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="c6de9-104">This section explains how to add Microsoft UI Automation provider capabilities to a Microsoft Active Accessibility server by implementing the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface.</span></span>

<span data-ttu-id="c6de9-105">Antes de implementar o [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex), considere os seguintes requisitos:</span><span class="sxs-lookup"><span data-stu-id="c6de9-105">Before implementing [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex), consider the following requirements:</span></span>

-   <span data-ttu-id="c6de9-106">A hierarquia de objetos de linha de base do Microsoft Acessibilidade Ativa acessível deve ser limpa.</span><span class="sxs-lookup"><span data-stu-id="c6de9-106">The baseline Microsoft Active Accessibility accessible object hierarchy must be clean.</span></span> <span data-ttu-id="c6de9-107">[**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) não pode corrigir problemas com hierarquias de objeto acessíveis existentes.</span><span class="sxs-lookup"><span data-stu-id="c6de9-107">[**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) cannot correct problems with existing accessible object hierarchies.</span></span> <span data-ttu-id="c6de9-108">Todos os problemas com a estrutura do modelo de objeto devem ser corrigidos na implementação do Microsoft Acessibilidade Ativa antes de implementar o **IAccessibleEx**.</span><span class="sxs-lookup"><span data-stu-id="c6de9-108">Any problems with the object model structure must be corrected in the Microsoft Active Accessibility implementation before implementing **IAccessibleEx**.</span></span>
-   <span data-ttu-id="c6de9-109">A implementação de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) deve estar em conformidade com a especificação do Microsoft acessibilidade ativa e a especificação de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="c6de9-109">The [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) implementation must comply with both the Microsoft Active Accessibility specification and the UI Automation specification.</span></span> <span data-ttu-id="c6de9-110">As ferramentas estão disponíveis para validar a conformidade em ambas as especificações.</span><span class="sxs-lookup"><span data-stu-id="c6de9-110">Tools are available to validate compliance under both specifications.</span></span> <span data-ttu-id="c6de9-111">Para obter mais informações, consulte [ferramentas de teste](testing-tools.md) e [verificação de automação da interface do usuário (UIA verificar) estrutura de automação de teste](https://www.codeplex.com/UIAutomationVerify/).</span><span class="sxs-lookup"><span data-stu-id="c6de9-111">For more information, see [Testing Tools](testing-tools.md) and [UI Automation Verify (UIA Verify) Test Automation Framework](https://www.codeplex.com/UIAutomationVerify/).</span></span>

<span data-ttu-id="c6de9-112">A implementação de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) requer estas etapas principais:</span><span class="sxs-lookup"><span data-stu-id="c6de9-112">Implementing [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) requires these main steps:</span></span>

-   <span data-ttu-id="c6de9-113">Implemente **IServiceProvider** no objeto acessível para que a interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) possa ser encontrada neste ou em um objeto separado.</span><span class="sxs-lookup"><span data-stu-id="c6de9-113">Implement **IServiceProvider** on the accessible object so that the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface can be found on this or a separate object.</span></span>
-   <span data-ttu-id="c6de9-114">Implemente [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) no objeto acessível.</span><span class="sxs-lookup"><span data-stu-id="c6de9-114">Implement [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) on the accessible object.</span></span>
-   <span data-ttu-id="c6de9-115">Crie objetos acessíveis para os itens filho da Microsoft Acessibilidade Ativa, que no Microsoft Acessibilidade Ativa são representados pela interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) no objeto pai (por exemplo, itens de lista).</span><span class="sxs-lookup"><span data-stu-id="c6de9-115">Create accessible objects for any Microsoft Active Accessibility child items, which in Microsoft Active Accessibility are represented by the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface on the parent object (for example, list items).</span></span> <span data-ttu-id="c6de9-116">Implemente [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) nesses objetos.</span><span class="sxs-lookup"><span data-stu-id="c6de9-116">Implement [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) on these objects.</span></span>
-   <span data-ttu-id="c6de9-117">Implemente [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) em todos os objetos acessíveis.</span><span class="sxs-lookup"><span data-stu-id="c6de9-117">Implement [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) on all the accessible objects.</span></span>
-   <span data-ttu-id="c6de9-118">Implemente as interfaces de padrão de controle apropriadas nos objetos acessíveis.</span><span class="sxs-lookup"><span data-stu-id="c6de9-118">Implement the appropriate control pattern interfaces on the accessible objects.</span></span>

### <a name="implementing-the-iserviceprovider-interface"></a><span data-ttu-id="c6de9-119">Implementando a interface IServiceProvider</span><span class="sxs-lookup"><span data-stu-id="c6de9-119">Implementing the IServiceProvider Interface</span></span>

<span data-ttu-id="c6de9-120">Como a implementação de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) para um controle pode residir em um objeto separado, os aplicativos cliente não podem confiar em [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obter essa interface.</span><span class="sxs-lookup"><span data-stu-id="c6de9-120">Because the implementation of [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) for a control may reside in a separate object, client applications cannot rely on [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to obtain this interface.</span></span> <span data-ttu-id="c6de9-121">Em vez disso, os clientes devem chamar **IServiceProvider:: QueryService**.</span><span class="sxs-lookup"><span data-stu-id="c6de9-121">Instead, clients are expected to call **IServiceProvider::QueryService**.</span></span> <span data-ttu-id="c6de9-122">Na implementação de exemplo a seguir desse método, supõe-se que **IAccessibleEx** não está implementado em um objeto separado; Portanto, o método simplesmente chama para **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="c6de9-122">In the following example implementation of this method, it is assumed that **IAccessibleEx** is not implemented on a separate object; therefore the method simply calls through to **QueryInterface**.</span></span>


```C++
           
HRESULT CListboxAccessibleObject::QueryService(REFGUID guidService, REFIID riid, LPVOID *ppvObject)
{
    if (ppvObject == NULL)
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
        return E_NOINTERFACE;
    }
};      
```



### <a name="implementing-the-iaccessibleex-interface"></a><span data-ttu-id="c6de9-123">Implementando a interface IAccessibleEx</span><span class="sxs-lookup"><span data-stu-id="c6de9-123">Implementing the IAccessibleEx Interface</span></span>

<span data-ttu-id="c6de9-124">No Microsoft Acessibilidade Ativa, um elemento de interface do usuário sempre é identificado por uma interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e uma ID filho.</span><span class="sxs-lookup"><span data-stu-id="c6de9-124">In Microsoft Active Accessibility, a UI element is always identified by an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface and a child ID.</span></span> <span data-ttu-id="c6de9-125">Uma única instância do **IAccessible** pode representar vários elementos da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="c6de9-125">A single instance of **IAccessible** can represent multiple UI elements.</span></span>

<span data-ttu-id="c6de9-126">Como cada instância de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) representa apenas um único elemento de interface do usuário, cada ID do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e de identificação filho deve ser mapeada para uma única instância de **IAccessibleEx** .</span><span class="sxs-lookup"><span data-stu-id="c6de9-126">Because each [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) instance represents only a single UI element, each [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) and child ID pair must be mapped to a single **IAccessibleEx** instance.</span></span> <span data-ttu-id="c6de9-127">O **IAccessibleEx** inclui dois métodos para lidar com esse mapeamento:</span><span class="sxs-lookup"><span data-stu-id="c6de9-127">**IAccessibleEx** includes two methods to handle this mapping:</span></span>

-   <span data-ttu-id="c6de9-128">[**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild)– recupera a interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) para o filho especificado.</span><span class="sxs-lookup"><span data-stu-id="c6de9-128">[**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild)—Retrieves the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) interface for the specified child.</span></span> <span data-ttu-id="c6de9-129">Esse método retornará **NULL** se a implementação de **IAccessibleEx** não reconhecer a ID filho especificada, não tiver um **IAccessibleEx** para o filho especificado ou representar um elemento filho.</span><span class="sxs-lookup"><span data-stu-id="c6de9-129">This method returns **NULL** if the **IAccessibleEx** implementation does not recognize the specified child ID, does not have an **IAccessibleEx** for the specified child, or represents a child element.</span></span>
-   <span data-ttu-id="c6de9-130">[**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair)— recupera a interface [**IACCESSIBLE**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e a ID filho para o elemento [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="c6de9-130">[**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair)—Retrieves the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface and child ID for the [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) element.</span></span> <span data-ttu-id="c6de9-131">Para implementações do **IAccessible** que não usam uma ID filho, esse método recupera o objeto **IAccessible** correspondente e o childID \_ próprio.</span><span class="sxs-lookup"><span data-stu-id="c6de9-131">For **IAccessible** implementations that do not use a child ID, this method retrieves the corresponding **IAccessible** object and CHILDID\_SELF.</span></span>

<span data-ttu-id="c6de9-132">O exemplo a seguir mostra a implementação dos métodos [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) e [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) para um item em uma exibição de lista personalizada.</span><span class="sxs-lookup"><span data-stu-id="c6de9-132">The following example shows the implementation of the [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) and [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) methods for an item in a custom list view.</span></span> <span data-ttu-id="c6de9-133">Os métodos habilitam a automação da interface do usuário para mapear o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e o par de ID filho para uma instância [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) correspondente.</span><span class="sxs-lookup"><span data-stu-id="c6de9-133">The methods enable UI Automation to map the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) and child ID pair to a corresponding [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) instance.</span></span>


```C++
           
HRESULT CListboxAccessibleObject::GetObjectForChild(
    long idChild, IAccessibleEx **ppRetVal)
{ 
    VARIANT vChild;
    vChild.vt = VT_I4;
    vChild.lVal = idChild;
    HRESULT hr = ValidateChildId(vChild);
    if (FAILED(hr))
    {
        return E_INVALIDARG;
    }
    // List item accessible objects are stored as an array of
    // pointers; for the purpose of this example it is assumed that 
    // the list contents will not change. Accessible objects are
    // created only when needed.
    if (itemProviders[idChild - 1] == NULL)
    {
        // Create an object that supports UI Automation and
        // IAccessibleEx for the item.
        itemProviders[idChild - 1] = 
          new CListItemAccessibleObject(idChild, 
          g_pListboxControl);
        if (itemProviders[idChild - 1] == NULL)
        {
            return E_OUTOFMEMORY;
        }
    }
    IAccessibleEx* pAccEx = static_cast<IAccessibleEx*>
      (itemProviders[idChild - 1]);
    if (pAccEx != NULL)
    {
      pAccEx->AddRef();
    }
    *ppRetVal = pAccEx;
    return S_OK; 
}

HRESULT CListItemAccessibleObject::GetIAccessiblePair(
    IAccessible **ppAcc, long *pidChild)
{ 
    if (ppAcc == NULL || pidChild == NULL)
    {
        return E_INVALIDARG;   
    }

                CListboxAccessibleObject* pParent = 
        m_control->GetAccessibleObject();

    HRESULT hr = pParent->QueryInterface( 
        __uuidof(IAccessible), (void**)ppAcc);
    if (FAILED(hr))
    {
        *pidChild = 0;
        return E_NOINTERFACE;
    }
    *pidChild = m_childID; 
    return S_OK; 
}
}
```



<span data-ttu-id="c6de9-134">Se uma implementação de objeto acessível não usar uma ID filho, os métodos ainda poderão ser implementados conforme mostrado no trecho de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="c6de9-134">If an accessible object implementation does not use a child ID, the methods can still be implemented as shown in the following code snippet.</span></span>


```C++
           

    // This sample implements IAccessibleEx on the same object; it could use a tear-off
    // or inner object instead.
    class MyAccessibleImpl: public IAccessible,
                        public IAccessibleEx,
                        public IRawElementProviderSimple
    {
    public:
    ...
   HRESULT STDMETHODCALLTYPE GetObjectForChild( long idChild, IAccessibleEx **ppRetVal )
    {
        // This implementation does not support child IDs.
        *ppRetVal = NULL;
        return S_OK;
    }

    HRESULT STDMETHODCALLTYPE GetIAccessiblePair( IAccessible ** ppAcc, long * pidChild )
    {
        // This implementation assumes that IAccessibleEx is implemented on same object as
        // IAccessible.
        *ppAcc = static_cast<IAccessible *>(this);
        (*ppAcc)->AddRef();
        *pidChild = CHILDID_SELF;
        return S_OK;
    }
```



### <a name="implement-the-irawelementprovidersimple-interface"></a><span data-ttu-id="c6de9-135">Implementar a interface IRawElementProviderSimple</span><span class="sxs-lookup"><span data-stu-id="c6de9-135">Implement the IRawElementProviderSimple Interface</span></span>

<span data-ttu-id="c6de9-136">Os servidores usam [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) para expor informações sobre propriedades de automação da interface do usuário e padrões de controle.</span><span class="sxs-lookup"><span data-stu-id="c6de9-136">Servers use [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) to expose information about UI Automation properties and control patterns.</span></span> <span data-ttu-id="c6de9-137">**IRawElementProviderSimple** inclui os seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="c6de9-137">**IRawElementProviderSimple** includes the following methods:</span></span>

-   <span data-ttu-id="c6de9-138">[**GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider)— esse método é usado para expor interfaces de padrão de controle.</span><span class="sxs-lookup"><span data-stu-id="c6de9-138">[**GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider)—This method is used to expose control pattern interfaces.</span></span> <span data-ttu-id="c6de9-139">Ele retorna um objeto que dá suporte ao padrão de controle especificado, ou **NULL** se não houver suporte para o padrão de controle.</span><span class="sxs-lookup"><span data-stu-id="c6de9-139">It returns an object that supports the specified control pattern, or **NULL** if the control pattern is not supported.</span></span>
-   <span data-ttu-id="c6de9-140">[**GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue)— esse método é usado para expor valores de propriedade de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="c6de9-140">[**GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue)—This method is used to expose UI Automation property values.</span></span>
-   <span data-ttu-id="c6de9-141">[**HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider)– esse método não é usado com implementações de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="c6de9-141">[**HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider)—This method is not used with [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) implementations.</span></span>
-   <span data-ttu-id="c6de9-142">[**ProviderOptions**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_provideroptions)— esse método não é usado com implementações de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .</span><span class="sxs-lookup"><span data-stu-id="c6de9-142">[**ProviderOptions**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_provideroptions)—This method is not used with [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) implementations.</span></span>

<span data-ttu-id="c6de9-143">Um servidor [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) expõe padrões de controle implementando [**IRawElementProviderSimple:: GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider).</span><span class="sxs-lookup"><span data-stu-id="c6de9-143">An [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) server exposes control patterns by implementing [**IRawElementProviderSimple::GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider).</span></span> <span data-ttu-id="c6de9-144">Esse método usa um parâmetro inteiro que especifica o padrão de controle.</span><span class="sxs-lookup"><span data-stu-id="c6de9-144">This method takes an integer parameter that specifies the control pattern.</span></span> <span data-ttu-id="c6de9-145">O servidor retornará **nulo** se não houver suporte para o padrão.</span><span class="sxs-lookup"><span data-stu-id="c6de9-145">The server returns **NULL** if the pattern is not supported.</span></span> <span data-ttu-id="c6de9-146">Se a interface de padrão de controle tiver suporte, os servidores retornarão um [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) e o cliente chamará [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obter o padrão de controle apropriado.</span><span class="sxs-lookup"><span data-stu-id="c6de9-146">If the control pattern interface is supported, servers return an [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) and the client then calls [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to get the appropriate control pattern.</span></span>

<span data-ttu-id="c6de9-147">Um servidor [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) pode dar suporte a propriedades de automação da interface do usuário (como LabeledBy e IsRequiredForForm) implementando [**IRawElementProviderSimple:: GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) e fornecendo uma PropertyId de número inteiro que identifica a propriedade como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="c6de9-147">An [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) server can support UI Automation properties (such as LabeledBy, and IsRequiredForForm) by implementing [**IRawElementProviderSimple::GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) and supplying an integer PROPERTYID identifying the property as a parameter.</span></span> <span data-ttu-id="c6de9-148">Essa técnica se aplica somente às propriedades de automação da interface do usuário que não estão incluídas em uma interface de padrão de controle.</span><span class="sxs-lookup"><span data-stu-id="c6de9-148">This technique applies only to UI Automation properties that are not included in a control pattern interface.</span></span> <span data-ttu-id="c6de9-149">As propriedades associadas a uma interface de padrão de controle são expostas por meio do método de interface de padrão de controle.</span><span class="sxs-lookup"><span data-stu-id="c6de9-149">Properties associated with a control pattern interface are exposed through the control pattern interface method.</span></span> <span data-ttu-id="c6de9-150">Por exemplo, a propriedade IsSelected do padrão de controle [SelectionItem](uiauto-implementingselectionitem.md) seria exposta com [**ISelectionItemProvider:: get \_ IsSelected**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected).</span><span class="sxs-lookup"><span data-stu-id="c6de9-150">For example, the IsSelected property from the [SelectionItem](uiauto-implementingselectionitem.md) control pattern would be exposed with [**ISelectionItemProvider::get\_IsSelected**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected).</span></span>

 

 