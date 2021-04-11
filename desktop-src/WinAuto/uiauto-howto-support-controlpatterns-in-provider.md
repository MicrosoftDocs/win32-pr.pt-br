---
title: Padrões de controle de suporte em um provedor de automação da interface do usuário
description: Este tópico mostra como um provedor de automação de interface do usuário da Microsoft implementa padrões de controle para um controle. Os padrões de controle permitem que os aplicativos cliente manipulem o controle e obtenham informações sobre ele.
ms.assetid: 504d0ed8-32c1-43ed-9f71-328a013ab350
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54e75fa12dba891bc4eded5fd9763f7825eb7f88
ms.sourcegitcommit: 2e9db3c7d9a3dbea15196b03c883846fad6f32be
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/12/2019
ms.locfileid: "104293539"
---
# <a name="support-control-patterns-in-a-ui-automation-provider"></a><span data-ttu-id="25503-104">Padrões de controle de suporte em um provedor de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="25503-104">Support Control Patterns in a UI Automation Provider</span></span>

<span data-ttu-id="25503-105">Este tópico mostra como um provedor de automação de interface do usuário da Microsoft implementa padrões de controle para um controle.</span><span class="sxs-lookup"><span data-stu-id="25503-105">This topic shows how a Microsoft UI Automation provider implements control patterns for a control.</span></span> <span data-ttu-id="25503-106">Os padrões de controle permitem que os aplicativos cliente manipulem o controle e obtenham informações sobre ele.</span><span class="sxs-lookup"><span data-stu-id="25503-106">Control patterns enable client applications to manipulate the control and get information about it.</span></span>

<span data-ttu-id="25503-107">Um provedor implementa um padrão de controle seguindo estas etapas principais:</span><span class="sxs-lookup"><span data-stu-id="25503-107">A provider implements a control pattern by following these main steps:</span></span>

1.  <span data-ttu-id="25503-108">Implemente a interface do provedor que dá suporte ao padrão de controle.</span><span class="sxs-lookup"><span data-stu-id="25503-108">Implement the provider interface that supports the control pattern.</span></span> <span data-ttu-id="25503-109">Por exemplo, para dar suporte ao padrão de controle [Selection](uiauto-implementingselection.md) , um provedor para um controle de lista personalizado implementaria a interface [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) .</span><span class="sxs-lookup"><span data-stu-id="25503-109">For example, to support the [Selection](uiauto-implementingselection.md) control pattern, a provider for a custom list control would implement the [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) interface.</span></span>
2.  <span data-ttu-id="25503-110">Retornar um objeto que contém a interface do provedor de padrão de controle quando a automação da interface do usuário chama o método [**IRawElementProviderSimple:: GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) do provedor.</span><span class="sxs-lookup"><span data-stu-id="25503-110">Return an object that contains the control pattern provider interface when UI Automation calls the provider's [**IRawElementProviderSimple::GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) method.</span></span>

<span data-ttu-id="25503-111">O exemplo a seguir mostra a implementação da interface [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) para um controle de lista de seleção única personalizado.</span><span class="sxs-lookup"><span data-stu-id="25503-111">The following example shows the [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) interface implementation for a custom, single-selection list control.</span></span> <span data-ttu-id="25503-112">A implementação inclui métodos de recuperação de propriedade para as propriedades IsSelectionRequired e CanSelectMultiple, e um método para recuperar o provedor para o item de lista selecionado.</span><span class="sxs-lookup"><span data-stu-id="25503-112">The implementation includes property-retrieval methods for the IsSelectionRequired and CanSelectMultiple properties, and a method for retrieving the provider for the selected list item.</span></span>


```C++
// Specifies whether the list control supports the selection of
// multiple items at the same time.
IFACEMETHODIMP ListProvider::get_CanSelectMultiple(BOOL *pRetVal)
{
    *pRetVal = FALSE;
    return S_OK;
} 

// Specifies whether the list must have an item selected at all times.
IFACEMETHODIMP ListProvider::get_IsSelectionRequired(BOOL *pRetVal)
{
   *pRetVal = TRUE;
   return S_OK;
}

// Retrieves the provider of the selected item in a custom list control. 
//
// m_pControl - pointer to an application-defined object for managing
//   the custom list control. 
//
// ListItemProvider - application-defined class that inherits the 
//   IRawElementProviderSimple interface.
//
// GetItemProviderByIndex - application-defined method that retrieves the 
//   IRawElementProviderSimple interface of the selected item.
IFACEMETHODIMP ListProvider::GetSelection(SAFEARRAY** pRetVal)
{
    // Create a safe array to store the IRawElementProviderSimple pointer.
    SAFEARRAY *psa = SafeArrayCreateVector(VT_UNKNOWN, 0, 1);

    // Retrieve the index of the selected list item. 
    int index = m_pControl->GetSelectedIndex(); 

    // Retrieve the IRawElementProviderSimple pointer of the selected list
    // item. ListItemProvider is an application-defined class that 
    // inherits the IRawElementProviderSimple interface. 
    ListItemProvider* pItem = GetItemProviderByIndex(index); 
    if (pItem != NULL)
    {
        LONG i = 0;
        SafeArrayPutElement(psa, &i, pItem);
    }
    *pRetVal = psa;
    return S_OK;
}
```



<span data-ttu-id="25503-113">O exemplo a seguir mostra uma implementação de [**IRawElementProviderSimple:: GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) que retorna um objeto que implementa [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span><span class="sxs-lookup"><span data-stu-id="25503-113">The following example shows an implementation of [**IRawElementProviderSimple::GetPatternProvider**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementprovidersimple-getpatternprovider) that returns an object that implements [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span></span> <span data-ttu-id="25503-114">A maioria dos controles List também ofereceria suporte a outros padrões, mas este exemplo retorna uma referência nula para todos os outros identificadores de padrão de controle.</span><span class="sxs-lookup"><span data-stu-id="25503-114">Most list controls would support other patterns as well, but this example returns a null reference for all other control pattern identifiers.</span></span>


```C++
// Retrieves an object that supports the control pattern provider interface 
// for the specified control pattern. 
IFACEMETHODIMP ListProvider::GetPatternProvider(PATTERNID patternId, IUnknown** pRetVal)
{
    *pRetVal = NULL;
    if (patternId == UIA_SelectionPatternId) 
    {
        // Return the object that implements ISelectionProvider. In this example, 
        // ISelectionProvider is implemented in the current object (this).
        *pRetVal = static_cast<IRawElementProviderSimple*>(this);
        AddRef();  
    }
    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="25503-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="25503-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="25503-116">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="25503-116">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="25503-117">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="25503-117">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="25503-118">Tópicos de instruções para provedores de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="25503-118">How-To Topics for UI Automation Providers</span></span>](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




