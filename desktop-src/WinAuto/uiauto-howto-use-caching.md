---
title: Como usar o armazenamento em cache
description: Este tópico contém um código de exemplo que mostra como usar os recursos de cache (ou busca em massa) da árvore de automação da interface do usuário da Microsoft.
ms.assetid: d72fa637-35ca-4c28-922d-263f469cb1c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8758621a8499202b820a6ffc3459fade57c2a485
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105798065"
---
# <a name="how-to-use-caching"></a><span data-ttu-id="a3432-103">Como usar o armazenamento em cache</span><span class="sxs-lookup"><span data-stu-id="a3432-103">How to Use Caching</span></span>

<span data-ttu-id="a3432-104">Este tópico contém um código de exemplo que mostra como usar os recursos de cache (ou busca em massa) da árvore de automação da interface do usuário da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a3432-104">This topic contains example code that shows how to use the caching (or bulk fetching) capabilities of Microsoft UI Automation tree.</span></span> <span data-ttu-id="a3432-105">Ele aborda os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="a3432-105">It discusses the following topics:</span></span>

-   [<span data-ttu-id="a3432-106">Buscando Propriedades e padrões de controle no cache</span><span class="sxs-lookup"><span data-stu-id="a3432-106">Fetching Properties and Control Patterns into the Cache</span></span>](#fetching-properties-and-control-patterns-into-the-cache)
-   [<span data-ttu-id="a3432-107">Recuperando propriedades e padrões de controle do cache</span><span class="sxs-lookup"><span data-stu-id="a3432-107">Retrieving Properties and Control Patterns from the Cache</span></span>](#retrieving-properties-and-control-patterns-from-the-cache)
-   [<span data-ttu-id="a3432-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a3432-108">Related topics</span></span>](#related-topics)

## <a name="fetching-properties-and-control-patterns-into-the-cache"></a><span data-ttu-id="a3432-109">Buscando Propriedades e padrões de controle no cache</span><span class="sxs-lookup"><span data-stu-id="a3432-109">Fetching Properties and Control Patterns into the Cache</span></span>

<span data-ttu-id="a3432-110">O exemplo de código a seguir mostra uma função que recupera itens de um controle de lista e armazena em cache o padrão de controle SelectionItem e a propriedade Name para cada item.</span><span class="sxs-lookup"><span data-stu-id="a3432-110">The following code example shows a function that retrieves items from a list control and caches the SelectionItem control pattern and Name property for each item.</span></span> <span data-ttu-id="a3432-111">Por padrão, os itens de lista são retornados com uma referência completa, para que todas as propriedades atuais ainda estejam disponíveis.</span><span class="sxs-lookup"><span data-stu-id="a3432-111">By default, the list items are returned with a full reference, so that all current properties are still available.</span></span>


```C++
// Given a list element, caches a control pattern and a property for
// all the list items.
IUIAutomationElementArray* FindAndCacheListItems(IUIAutomationElement* pList)
{
    if (pList == NULL)
        return NULL;
    
    IUIAutomationCondition* pCondition = NULL;
    IUIAutomationCacheRequest* pCacheRequest = NULL;
    IUIAutomationElementArray* pFound = NULL;

    HRESULT hr = g_pAutomation->CreateTrueCondition(&pCondition);
    if (FAILED(hr))
        goto cleanup;

    hr = g_pAutomation->CreateCacheRequest(&pCacheRequest);
    if (FAILED(hr))
        goto cleanup;

    hr = pCacheRequest->AddPattern(UIA_SelectionItemPatternId);
    if (FAILED(hr))
        goto cleanup;

    hr = pCacheRequest->AddProperty(UIA_NamePropertyId);
    if (FAILED(hr))
        goto cleanup;

    pList->FindAllBuildCache(TreeScope_Children, pCondition, pCacheRequest, &pFound);
    
cleanup:
    if (pCondition != NULL)
        pCondition->Release();

    if (pCacheRequest != NULL)
        pCacheRequest->Release();

    return pFound;
}
```



## <a name="retrieving-properties-and-control-patterns-from-the-cache"></a><span data-ttu-id="a3432-112">Recuperando propriedades e padrões de controle do cache</span><span class="sxs-lookup"><span data-stu-id="a3432-112">Retrieving Properties and Control Patterns from the Cache</span></span>

<span data-ttu-id="a3432-113">O código a seguir demonstra como recuperar propriedades e padrões de controle do cache.</span><span class="sxs-lookup"><span data-stu-id="a3432-113">The following code demonstrates how to retrieve properties and control patterns from the cache.</span></span> <span data-ttu-id="a3432-114">Ele recupera o padrão de controle SelectionItem e a propriedade Name para um item de lista.</span><span class="sxs-lookup"><span data-stu-id="a3432-114">It retrieves the SelectionItem control pattern and Name property for a list item.</span></span>


```C++
// Demonstrates retrieval of cached properties from a list item
// obtained in FindAndCacheListItems.
HRESULT GetCachedListItem(IUIAutomationElement* pItem)
{           
    if (pItem == NULL)
    {
        return E_INVALIDARG;
    }

    IUIAutomationSelectionItemPattern* pSelectionItemPattern;
    HRESULT hr = pItem->GetCachedPatternAs(UIA_SelectionItemPatternId, 
        IID_IUIAutomationSelectionItemPattern, (void**)&pSelectionItemPattern);
    if (pSelectionItemPattern != NULL)
    {
        // ... To do: Do something with the pattern.

        pSelectionItemPattern->Release();
    }

    // Retrieve a cached property.
    BSTR bstrName;
    hr = pItem->get_CachedName(&bstrName);
    if (SUCCEEDED(hr))
    {
        // ... To do: Do something with the property.

        // Clean up when done with name.
        SysFreeString(bstrName);
        bstrName = NULL;
    }

    BOOL isControl;

    // The following returns E_INVALIDARG because the property was not cached.
    // hr = pItem->get_CachedIsControlElement(&isControl);

    // The following is valid because we have a full reference to the object, therefore
    // we can get current properties. If the cache request had been made with 
    // AutomationElementMode_None, no current properties would be available from
    // this IUIAutomationElement.
    hr = pItem->get_CurrentIsControlElement(&isControl);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="a3432-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a3432-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a3432-116">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="a3432-116">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a3432-117">Cache de propriedades de automação da interface do usuário e padrões de controle</span><span class="sxs-lookup"><span data-stu-id="a3432-117">Caching UI Automation Properties and Control Patterns</span></span>](uiauto-cachingforclients.md)
</dt> <dt>

[<span data-ttu-id="a3432-118">Tópicos de instruções para clientes de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="a3432-118">How-To Topics for UI Automation Clients</span></span>](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




