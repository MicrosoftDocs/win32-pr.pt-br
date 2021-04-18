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
# <a name="how-to-use-caching"></a>Como usar o armazenamento em cache

Este tópico contém um código de exemplo que mostra como usar os recursos de cache (ou busca em massa) da árvore de automação da interface do usuário da Microsoft. Ele aborda os seguintes tópicos:

-   [Buscando Propriedades e padrões de controle no cache](#fetching-properties-and-control-patterns-into-the-cache)
-   [Recuperando propriedades e padrões de controle do cache](#retrieving-properties-and-control-patterns-from-the-cache)
-   [Tópicos relacionados](#related-topics)

## <a name="fetching-properties-and-control-patterns-into-the-cache"></a>Buscando Propriedades e padrões de controle no cache

O exemplo de código a seguir mostra uma função que recupera itens de um controle de lista e armazena em cache o padrão de controle SelectionItem e a propriedade Name para cada item. Por padrão, os itens de lista são retornados com uma referência completa, para que todas as propriedades atuais ainda estejam disponíveis.


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



## <a name="retrieving-properties-and-control-patterns-from-the-cache"></a>Recuperando propriedades e padrões de controle do cache

O código a seguir demonstra como recuperar propriedades e padrões de controle do cache. Ele recupera o padrão de controle SelectionItem e a propriedade Name para um item de lista.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Cache de propriedades de automação da interface do usuário e padrões de controle](uiauto-cachingforclients.md)
</dt> <dt>

[Tópicos de instruções para clientes de automação da interface do usuário](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




