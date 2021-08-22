---
title: Como encontrar elementos da interface do usuário
description: Este tópico contém um código de exemplo que mostra como encontrar elementos de interface do usuário na árvore Automação da Interface do Usuário dados.
ms.assetid: b613eb18-e14d-468e-833d-072bad29ba06
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52998ad92fe1912a5159443642d95bbc14a28da595ddd2b2a255ebecaed8c74d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119505266"
---
# <a name="how-to-find-ui-elements"></a>Como encontrar elementos da interface do usuário

Este tópico contém um código de exemplo que mostra como encontrar elementos de interface do usuário na árvore Automação da Interface do Usuário dados.

-   [Encontrando um elemento por nome](#finding-an-element-by-name)
-   [Localizar elementos relacionados](#finding-related-elements)
-   [Tópicos relacionados](#related-topics)

## <a name="finding-an-element-by-name"></a>Encontrando um elemento por nome

O exemplo a seguir localiza o elemento microsoft Automação da Interface do Usuário que tem o nome especificado e é um filho da janela da área de trabalho.


```C++
IUIAutomationElement* GetTopLevelWindowByName(LPWSTR windowName)
{
    if (windowName == NULL)
    {
        return NULL;
    }

    VARIANT varProp;
    varProp.vt = VT_BSTR;
    varProp.bstrVal = SysAllocString(windowName);
    if (varProp.bstrVal == NULL)
    {
        return NULL;
    }

    IUIAutomationElement* pRoot = NULL;
    IUIAutomationElement* pFound = NULL;

    // Get the desktop element. 
    HRESULT hr = g_pAutomation->GetRootElement(&pRoot);
    if (FAILED(hr) || pRoot == NULL)
        goto cleanup;

    // Get a top-level element by name, such as "Program Manager"
    IUIAutomationCondition* pCondition;
    hr = g_pAutomation->CreatePropertyCondition(UIA_NamePropertyId, varProp, &pCondition);
    if (FAILED(hr))
        goto cleanup;

    pRoot->FindFirst(TreeScope_Children, pCondition, &pFound);

cleanup:
    if (pRoot != NULL)
        pRoot->Release();

    if (pCondition != NULL)
        pCondition->Release();

    VariantClear(&varProp);
    return pFound;
}
```



## <a name="finding-related-elements"></a>Localizar elementos relacionados

A função de exemplo a seguir retorna uma coleção de todos os botões habilitados que são filhos do elemento especificado.


```C++
IUIAutomationElementArray* GetEnabledButtons(IUIAutomationElement* pParent)
{
    if (pParent == NULL)
    {
        return NULL;
    }
    IUIAutomationCondition* pButtonCondition = NULL;
    IUIAutomationCondition* pEnabledCondition = NULL;
    IUIAutomationCondition* pCombinedCondition = NULL;
    IUIAutomationElementArray* pFound = NULL;

    // Create a property condition for the button control type.
    VARIANT varProp;
    varProp.vt = VT_I4;
    varProp.lVal = UIA_ButtonControlTypeId;
    g_pAutomation->CreatePropertyCondition(UIA_ControlTypePropertyId, varProp, &pButtonCondition);
    if (pButtonCondition == NULL)
        goto cleanup;

    // Create a property condition for the enabled property.
    varProp.vt = VT_BOOL;
    varProp.boolVal = VARIANT_TRUE;
    g_pAutomation->CreatePropertyCondition(UIA_IsEnabledPropertyId, varProp, &pEnabledCondition);
    if (pEnabledCondition == NULL)
        goto cleanup;

    // Combine the conditions.
    g_pAutomation->CreateAndCondition(pButtonCondition, pEnabledCondition, &pCombinedCondition);
    if (pCombinedCondition == NULL)
        goto cleanup;

    // Find the matching elements. Note that if the scope is changed to TreeScope_Descendants, 
    // system buttons on the caption bar will be found as well.
    pParent->FindAll(TreeScope_Children, pCombinedCondition, &pFound);

cleanup:
    if (pButtonCondition != NULL)
        pButtonCondition->Release();

    if (pEnabledCondition != NULL) 
        pEnabledCondition->Release();
    
    if (pCombinedCondition != NULL)
        pCombinedCondition->Release();

    return pFound;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Obtendo elementos da automação interface do usuário](uiauto-obtainingelements.md)
</dt> <dt>

[Tópicos de ida e Automação da Interface do Usuário clientes](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




