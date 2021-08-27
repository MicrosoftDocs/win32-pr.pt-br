---
title: Usando IAccessibleEx de um cliente
description: Este tópico explica como os clientes acessam a implementação IAccessibleEx de um servidor e a usam para obter Automação da Interface do Usuário propriedades e padrões de controle para elementos de interface do usuário.
ms.assetid: e057bbe8-5dd7-41fc-a5d5-bcf4c1c6433d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f03bd58ec80a29f13e0428de4655aa7200144122b1a1889259844db078aa9dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098096"
---
# <a name="using-iaccessibleex-from-a-client"></a>Usando IAccessibleEx de um cliente

Este tópico explica como os clientes acessam a implementação [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) de um servidor e a usam para obter Automação da Interface do Usuário propriedades e padrões de controle para elementos de interface do usuário.

Os procedimentos e exemplos nesta seção supõem um [**cliente IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) que já está em processo e um servidor Microsoft Active Accessibility existente. Eles também supõem que o cliente já obteve um objeto **IAccessible** usando uma das funções de estrutura de acessibilidade, como [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent), [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)ou [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).

### <a name="obtaining-an-iaccessibleex-interface-from-the-iaccessible-interface"></a>Obtendo uma interface IAccessibleEx da interface IAccessible

Um cliente que tenha uma interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para um objeto acessível pode usá-lo para obter a interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) correspondente seguindo estas etapas:

-   Chame [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) original com uma IID de \_ \_ uuidof(IServiceProvider).
-   Chame **IServiceProvider::QueryService** para obter [**o IAccessibleEx.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)

### <a name="handling-the-child-id"></a>Manipulando a ID filho

Os clientes devem estar preparados para servidores com uma ID filho diferente de CHILDID \_ SELF. Depois de obter uma interface [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) de [**um IAccessible,**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)os clientes deverão chamar [**IAccessibleEx::GetObjectForChild**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getobjectforchild) se a ID filho não for CHILDID SELF (indicando um objeto \_ pai).

O exemplo a seguir mostra como obter [**um IAccessibleEx para**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) um objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) específico e uma ID filho.


```C++
   
HRESULT GetIAccessibleExFromIAccessible(IAccessible * pAcc, long idChild, 
                                           IAccessibleEx ** ppaex)
{
    *ppaex = NULL;

    // First, get IServiceProvider from the IAccessible.
    IServiceProvider * pSp = NULL;
    HRESULT hr = pAcc->QueryInterface(IID_IServiceProvider, (void **) & pSp);
    if(FAILED(hr))
        return hr;
    if(pSp == NULL)
        return E_NOINTERFACE;

    // Next, get the IAccessibleEx for the parent object.
    IAccessibleEx * paex = NULL;
    hr = pSp->QueryService(__uuidof(IAccessibleEx), __uuidof(IAccessibleEx),
                                                                 (void **)&paex);
    pSp->Release();
    if(FAILED(hr))
        return hr;
    if(paex == NULL)
        return E_NOINTERFACE;

    // If this is for CHILDID_SELF, we're done. Otherwise, we have a child ID and 
    // can request the object for child.
    if(idChild == CHILDID_SELF)
    {
        *ppaex = paex;
        return S_OK;
    }
    else
    {
        // Get the IAccessibleEx for the specified child.
        IAccessibleEx * paexChild = NULL;
        hr = paex->GetObjectForChild(idChild, &paexChild);
        paex->Release();
        if(FAILED(hr))
            return hr;
        if(paexChild == NULL)
            return E_NOINTERFACE;
        *ppaex = paexChild;
        return S_OK;
    }
}
```



### <a name="obtaining-the-irawelementprovidersimple-interface"></a>Obtendo a interface IRawElementProviderSimple

Se um cliente tiver uma interface [**IAccessibleEx,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) ele poderá usar QueryInterface para chegar à interface [**IRawElementProviderSimple,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) como mostra o exemplo a seguir.


```C++
HRESULT GetIRawElementProviderFromIAccessible(IAccessible * pAcc, long idChild,
                                                 IRawElementProviderSimple ** ppEl)
{
    * ppEl = NULL;

    // First, get the IAccessibleEx for the IAccessible and child ID pair.
    IAccessibleEx * paex;
    HRESULT hr = GetIAccessibleExFromIAccessible( pAcc, idChild, &paex );
    if(FAILED(hr))
        return hr;

    // Next, use QueryInterface.
    hr = paex->QueryInterface(__uuidof(IRawElementProviderSimple), (void **)ppEl);
    paex->Release();
    return hr;
}
```



### <a name="retrieving-control-patterns"></a>Recuperando padrões de controle

Se um cliente tiver acesso à interface [**IRawElementProviderSimple,**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) ele poderá recuperar interfaces de padrão de controle que foram implementadas por provedores e, em seguida, pode chamar métodos nessas interfaces. O exemplo a seguir mostra como fazer isso.


```C++
// Helper function to get a pattern interface from an IAccessible and child ID 
// pair. Gets the IAccessibleEx, then calls GetPatternObject and QueryInterface.
HRESULT GetPatternFromIAccessible(IAccessible * pAcc, long idChild,
                                     PATTERNID patternId, REFIID iid, void ** ppv)
{
    // First, get the IAccesibleEx for this IAccessible and child ID pair.
    IRawElementProviderSimple * pel;
    HRESULT hr = GetIRawElementProviderSimpleFromIAccessible(pAcc, idChild, &pel);
    if(FAILED(hr))
        return hr;
    if(pel == NULL)
        return E_NOINTERFACE;

    // Now get the pattern object.
    IUnknown * pPatternObject = NULL;
    hr = pel->GetPatternProvider(patternId, &pPatternObject);
    pel->Release();
    if(FAILED(hr))
        return hr;
    if(pPatternObject == NULL)
        return E_NOINTERFACE;

    // Finally, use QueryInterface to get the correct interface type.
    hr = pPatternObject->QueryInterface(iid, ppv);
    pPatternObject->Release();
    if(*ppv == NULL)
        return E_NOINTERFACE;
    return hr;
}

HRESULT CallInvokePatternMethod(IAccessible * pAcc, long idChild)
{
    IInvokeProvider * pPattern;
    HRESULT hr = GetPatternFromIAccessible(pAcc, varChild,
                                  UIA_InvokePatternId, __uuidof(IInvokeProvider),
                                  (void **)&pPattern);
    if(FAILED(hr))
        return hr;

    hr = pPattern->Invoke();
    pPattern->Release();
    return hr;
}
```



### <a name="retrieving-property-values"></a>Recuperando valores de propriedade

Se um cliente tiver acesso a [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple), ele poderá recuperar valores de propriedade. O exemplo a seguir mostra como obter valores para as propriedades AutomationId e LabeledBy Microsoft Automação da Interface do Usuário.


```C++
#include <initguid.h>
#include <uiautomationcoreapi.h> // Includes the UI Automation property GUID definitions.
#include <uiautomationcoreids.h> // Includes definitions of pattern/property IDs.

// Assume we already have a IRawElementProviderSimple * pEl.

VARIANT varValue;

// Get AutomationId property:
varValue.vt = VT_EMPTY;
HRESULT hr = pEl->GetPropertyValue(UIA_AutomationIdPropertyId, &varValue);
if(SUCCEEDED(hr))
{
    if(varValue.vt == VT_BSTR)
    {
        // AutomationId is varValue.bstrVal.
    }
    VariantClear(&varValue);
}


// Get LabeledBy property:
varValue.vt = VT_EMPTY;
hr = pEl->GetPropertyValue(UIA_LabeledByPropertyId, &varValue);
if(SUCCEEDED(hr))
{
    if(varValue.vt == VT_UNKNOWN || varValue.punkVal != NULL)
    {
        // Use QueryInterface to get IRawElementProviderSimple.
        IRawElementProviderSimple * pElLabel = NULL;
        hr = varValue.punkVal->QueryInterface(__uuidof(IRawElementProviderSimple),
                                              (void**)& pElLabel);
        if (SUCCEEDED(hr))
        {
            if(pElLabel != NULL)
            {
            // Use the pElLabel pointer here.
            pElLabel ->Release();
            }
        }
    }
    VariantClear(&varValue);
}
```



O exemplo anterior se aplica a propriedades que não estão associadas a um padrão de controle. Para acessar propriedades de padrão de controle, um cliente deve obter e usar uma interface de padrão de controle.

### <a name="retrieving-an-iaccessible-interface-from-an-irawelementprovidersimple-interface"></a>Recuperando uma interface IAccessible de uma interface IRawElementProviderSimple

Se um cliente obtiver a interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) para um elemento de interface do usuário, o cliente poderá usar essa interface para obter uma interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) correspondente para o elemento. Isso será útil se o cliente precisar acessar as propriedades Microsoft Active Accessibility para o elemento .

Um cliente pode obter a interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) como um valor da propriedade (por exemplo, chamando [**IRawElementProviderSimple::GetPropertyValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpropertyvalue) com UIA LabeledByPropertyId) ou como um item recuperado por um método \_ (por exemplo, chamando [**ISelectionProvider::GetSelection**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection) para recuperar uma matriz de interfaces **IRawElementProviderSimple** de elementos selecionados). Depois de obter a interface **IRawElementProviderSimple,** um cliente pode usá-la para obter um [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) correspondente seguindo estas etapas:

-   Tente usar QueryInterface para obter a interface [**IAccessibleEx.**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex)
-   Se QueryInterface falhar, chame [**IAccessibleEx::ConvertReturnedElement**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-convertreturnedelement) na instância [**IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) da qual a propriedade foi originalmente obtida.
-   Chame o [**método GetIAccessiblePair**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iaccessibleex-getiaccessiblepair) na nova [**instância IAccessibleEx**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iaccessibleex) para obter uma [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interfae e uma ID filho.

O snippet de código a seguir demonstra como obter a interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) de uma interface [**IRawElementProviderSimple**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementprovidersimple) obtida anteriormente.


```C++
// IRawElementProviderSimple * pVal - an element returned by a property or method
// from another IRawElementProviderSimple.

IAccessible * pAcc = NULL;
long idChild;

// First, try to use QueryInterface to get the IAccessibleEx interface.
IAccessibleEx * pAccEx;
HRESULT hr = pVal->QueryInterface(__uuidof(IAccessibleEx), (void**)&pAccEx);
if (SUCCEEDED(hr)
{
    if (!pAccEx)
    {
        // If QueryInterface fails, and the IRawElementProviderSimple was 
              // obtained as a property or return value from another 
              // IRawElementProviderSimple, pass it to the 
              // IAccessibleEx::ConvertReturnedValue method of the
        // originating element.

        pAccExOrig->ConvertReturnedElement(pVal, &pAccEx);
    }

    if (pAccEx)
    {
        // Call GetIAccessiblePair to get an IAccessible interface and 
              // child ID.
        pAccEx->GetIAccessiblePair(&pAcc, &idChild);
    }

    // Finally, use the IAccessible interface and child ID.
    if (pAcc)
    {
        // Use IAccessible methods to get further information about this UI
              // element, or pass it to existing code that works in terms of 
              // IAccessible.
        ...
    }
}    
```



 

 