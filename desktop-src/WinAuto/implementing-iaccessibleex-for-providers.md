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
# <a name="implementing-iaccessibleex-for-providers"></a>Implementando IAccessibleEx para provedores

Esta seção explica como adicionar recursos do provedor de automação de interface do usuário da Microsoft a um Microsoft Acessibilidade Ativa Server implementando a interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .

Antes de implementar o [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex), considere os seguintes requisitos:

-   A hierarquia de objetos de linha de base do Microsoft Acessibilidade Ativa acessível deve ser limpa. [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) não pode corrigir problemas com hierarquias de objeto acessíveis existentes. Todos os problemas com a estrutura do modelo de objeto devem ser corrigidos na implementação do Microsoft Acessibilidade Ativa antes de implementar o **IAccessibleEx**.
-   A implementação de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) deve estar em conformidade com a especificação do Microsoft acessibilidade ativa e a especificação de automação da interface do usuário. As ferramentas estão disponíveis para validar a conformidade em ambas as especificações. Para obter mais informações, consulte [ferramentas de teste](testing-tools.md) e [verificação de automação da interface do usuário (UIA verificar) estrutura de automação de teste](https://www.codeplex.com/UIAutomationVerify/).

A implementação de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) requer estas etapas principais:

-   Implemente **IServiceProvider** no objeto acessível para que a interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) possa ser encontrada neste ou em um objeto separado.
-   Implemente [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) no objeto acessível.
-   Crie objetos acessíveis para os itens filho da Microsoft Acessibilidade Ativa, que no Microsoft Acessibilidade Ativa são representados pela interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) no objeto pai (por exemplo, itens de lista). Implemente [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) nesses objetos.
-   Implemente [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) em todos os objetos acessíveis.
-   Implemente as interfaces de padrão de controle apropriadas nos objetos acessíveis.

### <a name="implementing-the-iserviceprovider-interface"></a>Implementando a interface IServiceProvider

Como a implementação de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) para um controle pode residir em um objeto separado, os aplicativos cliente não podem confiar em [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obter essa interface. Em vez disso, os clientes devem chamar **IServiceProvider:: QueryService**. Na implementação de exemplo a seguir desse método, supõe-se que **IAccessibleEx** não está implementado em um objeto separado; Portanto, o método simplesmente chama para **QueryInterface**.


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



### <a name="implementing-the-iaccessibleex-interface"></a>Implementando a interface IAccessibleEx

No Microsoft Acessibilidade Ativa, um elemento de interface do usuário sempre é identificado por uma interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e uma ID filho. Uma única instância do **IAccessible** pode representar vários elementos da interface do usuário.

Como cada instância de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) representa apenas um único elemento de interface do usuário, cada ID do [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e de identificação filho deve ser mapeada para uma única instância de **IAccessibleEx** . O **IAccessibleEx** inclui dois métodos para lidar com esse mapeamento:

-   [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild)– recupera a interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) para o filho especificado. Esse método retornará **NULL** se a implementação de **IAccessibleEx** não reconhecer a ID filho especificada, não tiver um **IAccessibleEx** para o filho especificado ou representar um elemento filho.
-   [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair)— recupera a interface [**IACCESSIBLE**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e a ID filho para o elemento [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) . Para implementações do **IAccessible** que não usam uma ID filho, esse método recupera o objeto **IAccessible** correspondente e o childID \_ próprio.

O exemplo a seguir mostra a implementação dos métodos [**GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) e [**GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) para um item em uma exibição de lista personalizada. Os métodos habilitam a automação da interface do usuário para mapear o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e o par de ID filho para uma instância [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) correspondente.


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



Se uma implementação de objeto acessível não usar uma ID filho, os métodos ainda poderão ser implementados conforme mostrado no trecho de código a seguir.


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



### <a name="implement-the-irawelementprovidersimple-interface"></a>Implementar a interface IRawElementProviderSimple

Os servidores usam [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) para expor informações sobre propriedades de automação da interface do usuário e padrões de controle. **IRawElementProviderSimple** inclui os seguintes métodos:

-   [**GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider)— esse método é usado para expor interfaces de padrão de controle. Ele retorna um objeto que dá suporte ao padrão de controle especificado, ou **NULL** se não houver suporte para o padrão de controle.
-   [**GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue)— esse método é usado para expor valores de propriedade de automação da interface do usuário.
-   [**HostRawElementProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider)– esse método não é usado com implementações de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .
-   [**ProviderOptions**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-get_provideroptions)— esse método não é usado com implementações de [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) .

Um servidor [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) expõe padrões de controle implementando [**IRawElementProviderSimple:: GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider). Esse método usa um parâmetro inteiro que especifica o padrão de controle. O servidor retornará **nulo** se não houver suporte para o padrão. Se a interface de padrão de controle tiver suporte, os servidores retornarão um [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) e o cliente chamará [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para obter o padrão de controle apropriado.

Um servidor [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) pode dar suporte a propriedades de automação da interface do usuário (como LabeledBy e IsRequiredForForm) implementando [**IRawElementProviderSimple:: GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) e fornecendo uma PropertyId de número inteiro que identifica a propriedade como um parâmetro. Essa técnica se aplica somente às propriedades de automação da interface do usuário que não estão incluídas em uma interface de padrão de controle. As propriedades associadas a uma interface de padrão de controle são expostas por meio do método de interface de padrão de controle. Por exemplo, a propriedade IsSelected do padrão de controle [SelectionItem](uiauto-implementingselectionitem.md) seria exposta com [**ISelectionItemProvider:: get \_ IsSelected**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected).

 

 