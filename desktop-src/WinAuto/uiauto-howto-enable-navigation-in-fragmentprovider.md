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
# <a name="how-to-enable-navigation-in-a-ui-automation-fragment-provider"></a><span data-ttu-id="59170-103">Como habilitar a navegação em um provedor de fragmento de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="59170-103">How to Enable Navigation in a UI Automation Fragment Provider</span></span>

<span data-ttu-id="59170-104">Este tópico contém um código de exemplo que mostra como habilitar a navegação em um provedor de automação da interface do usuário da Microsoft para um elemento em um fragmento.</span><span class="sxs-lookup"><span data-stu-id="59170-104">This topic contains example code that shows how to enable navigation in a Microsoft UI Automation provider for an element in a fragment.</span></span>

<span data-ttu-id="59170-105">O código de exemplo a seguir implementa o método [**IRawElementProviderFragment:: Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) para um item de lista em um controle de lista personalizado.</span><span class="sxs-lookup"><span data-stu-id="59170-105">The following example code implements the [**IRawElementProviderFragment::Navigate**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irawelementproviderfragment-navigate) method for a list item in a custom list control.</span></span> <span data-ttu-id="59170-106">O elemento pai é o controle de lista personalizado e os elementos irmãos são outros itens na lista.</span><span class="sxs-lookup"><span data-stu-id="59170-106">The parent element is the custom list control, and the sibling elements are other items in the list.</span></span> <span data-ttu-id="59170-107">O método define o parâmetro *pRetVal* como **NULL** se não houver nenhum elemento na direção especificada.</span><span class="sxs-lookup"><span data-stu-id="59170-107">The method sets the *pRetVal* parameter to **NULL** if there is no element in the specified direction.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="59170-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="59170-108">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="59170-109">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="59170-109">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="59170-110">Implementando um provedor de automação de interface do usuário Server-Side</span><span class="sxs-lookup"><span data-stu-id="59170-110">Implementing a Server-Side UI Automation Provider</span></span>](uiauto-serversideprovider.md)
</dt> <dt>

[<span data-ttu-id="59170-111">Tópicos de instruções para provedores de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="59170-111">How-To Topics for UI Automation Providers</span></span>](uiauto-howto-topics-for-uiautomation-providers.md)
</dt> </dl>

 

 




