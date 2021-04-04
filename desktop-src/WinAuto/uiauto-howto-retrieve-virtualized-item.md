---
title: Como recuperar um item virtualizado
description: Este tópico contém um código de exemplo que mostra como localizar e recuperar informações da interface do usuário sobre itens virtualizados em um controle.
ms.assetid: 1882b8a9-0d03-4388-a1d0-1bff0ab9fc66
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae878ce25dd4d279211948ddaa6f9d0965ce9b40
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104008607"
---
# <a name="how-to-retrieve-a-virtualized-item"></a><span data-ttu-id="46fd1-103">Como recuperar um item virtualizado</span><span class="sxs-lookup"><span data-stu-id="46fd1-103">How to Retrieve a Virtualized Item</span></span>

<span data-ttu-id="46fd1-104">Este tópico contém um código de exemplo que mostra como localizar e recuperar informações da interface do usuário sobre itens virtualizados em um controle.</span><span class="sxs-lookup"><span data-stu-id="46fd1-104">This topic contains example code that shows how to find and retrieve UI information about virtualized items in a control.</span></span>


<span data-ttu-id="46fd1-105">O exemplo a seguir pesquisa um contêiner de um item que tem o nome especificado e recupera a interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para o item.</span><span class="sxs-lookup"><span data-stu-id="46fd1-105">The following example searches a container for an item that has the specified name and retrieves the [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface for the item.</span></span> <span data-ttu-id="46fd1-106">O exemplo procura primeiro na subárvore de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="46fd1-106">The example looks in the UI Automation subtree first.</span></span> <span data-ttu-id="46fd1-107">Se o item não estiver lá, o exemplo usará a interface [**IUIAutomationItemContainerPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationitemcontainerpattern) do contêiner para localizar o item e, em seguida, usará a interface [**IUIAutomationVirtualizedItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) do item para perceber o item.</span><span class="sxs-lookup"><span data-stu-id="46fd1-107">If the item is not there, the example uses the container [**IUIAutomationItemContainerPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationitemcontainerpattern) interface to find the item, and then uses the item [**IUIAutomationVirtualizedItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationvirtualizeditempattern) interface to realize the item.</span></span>


```C++
HRESULT GetContainerItem (BSTR bstrItemName, IUIAutomationElement *pContainerElement, 
                          IUIAutomationElement **ppItemElement)                                  
{
    HRESULT hr;
    VARIANT varNameStr;
    IUIAutomationCondition *pNamePropertyCond = NULL;
    IUIAutomationElement *pFoundElement = NULL;
    IUIAutomationItemContainerPattern *pItemContainer = NULL;

    // Make sure the pointers are valid.
    if (ppItemElement == NULL || pContainerElement == NULL || bstrItemName == NULL)
        return E_INVALIDARG;
    
    *ppItemElement = NULL;

    // Try to find the item in the UI Automation tree. This attempt will fail if the
    // item is virtualized. Note: g_pAutomation is a global pointer to the IUIAutomation interface.
    varNameStr.vt = VT_BSTR;
    varNameStr.bstrVal = SysAllocString(bstrItemName);
    hr = g_pAutomation->CreatePropertyCondition(UIA_NamePropertyId, varNameStr, &pNamePropertyCond);
    if (pNamePropertyCond == NULL)
        goto cleanup;

    hr = pContainerElement->FindFirst(TreeScope_Subtree, pNamePropertyCond, &pFoundElement);
    if (pFoundElement == NULL) { 

        // The item is not in the UI Automation tree, so it may be virtualized. Try
        // using the ItemContainer control pattern to find the item.
        hr = pContainerElement->GetCurrentPatternAs(UIA_ItemContainerPatternId, 
                                                    __uuidof(IUIAutomationItemContainerPattern), 
                                                    (void**)&pItemContainer);
        if (pItemContainer == NULL)
            goto cleanup;

        hr = pItemContainer->FindItemByProperty(NULL, UIA_NamePropertyId, varNameStr, &pFoundElement);
        if (pFoundElement == NULL) // container has no item with the specified name
            goto cleanup;
    }

    // Attempt to get the name property. The attempt will fail with 
    // UIA_E_ELEMENTNOTAVAILABLE if the item is virtualized. 
    BSTR bstrName; 
    hr = pFoundElement->get_CurrentName(&bstrName);
    if (hr == UIA_E_ELEMENTNOTAVAILABLE) 
    {
        // The item might be virtualized. Use the VirtualizedItem control pattern to 
        // realize the item. 
        IUIAutomationVirtualizedItemPattern *pVirtualizedItem;
        hr = pFoundElement->GetCurrentPatternAs(UIA_VirtualizedItemPatternId, 
                    __uuidof(IUIAutomationVirtualizedItemPattern), (void**)&pVirtualizedItem);
        if (pVirtualizedItem == NULL)
            goto cleanup;

        hr = pVirtualizedItem->Realize();
        pVirtualizedItem->Release();

        if (hr != S_OK)
            goto cleanup;

        // Try to get the name again. 
        hr = pFoundElement->get_CurrentName(&bstrName);
    }    

    if (SUCCEEDED(hr))
    {
        // Make sure the item is the one we're looking for.
        if (wcscmp(bstrName, bstrItemName) == 0)
        {
            *ppItemElement = pFoundElement;
            pFoundElement = NULL;
        }
    }


cleanup:
        VariantClear(&varNameStr);

        if (pNamePropertyCond != NULL) pNamePropertyCond->Release();
        if (pFoundElement != NULL) pFoundElement->Release();
        if (pItemContainer != NULL) pItemContainer->Release();

        return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="46fd1-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="46fd1-108">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="46fd1-109">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="46fd1-109">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="46fd1-110">Trabalhando com itens virtualizados</span><span class="sxs-lookup"><span data-stu-id="46fd1-110">Working with Virtualized Items</span></span>](uiauto-workingwithvirtualizeditems.md)
</dt> <dt>

[<span data-ttu-id="46fd1-111">Tópicos de instruções para clientes de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="46fd1-111">How-To Topics for UI Automation Clients</span></span>](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




