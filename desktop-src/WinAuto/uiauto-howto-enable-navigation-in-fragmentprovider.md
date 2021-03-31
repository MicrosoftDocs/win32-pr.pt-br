---
title: Como habilitar a navegação em um provedor de fragmento de automação de interface do usuário
description: Este tópico contém um código de exemplo que mostra como habilitar a navegação em um provedor de automação da interface do usuário da Microsoft para um elemento em um fragmento.
ms.assetid: 8c390e19-3c17-4e02-ade8-cd5c1ed9E938
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58495c48f6f355e7cc2a42b58ac0e32f88958361
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004993"
---
# <a name="how-to-enable-navigation-in-a-ui-automation-fragment-provider"></a>Como habilitar a navegação em um provedor de fragmento de automação de interface do usuário

Este tópico contém um código de exemplo que mostra como habilitar a navegação em um provedor de automação da interface do usuário da Microsoft para um elemento em um fragmento.

O código de exemplo a seguir implementa o método [**IRawElementProviderFragment:: Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) para um item de lista em um controle de lista personalizado. O elemento pai é o controle de lista personalizado e os elementos irmãos são outros itens na lista. O método define o parâmetro *pRetVal* como **NULL** se não houver nenhum elemento na direção especificada.


```C++
// Implementation of IRawElementProviderFragment::Navigate.
// Enables UI Automation to locate the element in the tree.
HRESULT STDMETHODCALLTYPE ListItemProvider::Navigate(NavigateDirection direction, IRawElementProviderFragment ** pRetVal)
{
    if (pRetVal == NULL) 
    {
        return E_INVALIDARG;
    }

    IRawElementProviderFragment* pFrag = NULL;
    switch(direction)
    {
        case NavigateDirection_Parent:
            pFrag = (IRawElementProviderFragment*) m_parentProvider;       
            break;

        case NavigateDirection_NextSibling:
            pFrag = (IRawElementProviderFragment*) m_nextSiblingProvider;
            break;

        case NavigateDirection_PreviousSibling:  
            pFrag = (IRawElementProviderFragment*) m_previousSiblingProvider;
            break;
    }
    *pRetVal = pFrag;
    if (pFrag != NULL) 
    {
        pFrag->AddRef();
    }
    return S_OK;
}              
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Implementando um provedor de automação de interface do usuário Server-Side](uiauto-serversideprovider.md)
</dt> <dt>

[Tópicos de instruções para provedores de automação de interface do usuário](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




