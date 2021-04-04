---
title: Como percorrer a árvore de automação da interface do usuário
description: Este tópico contém um código de exemplo que mostra como usar a interface IUIAutomationTreeWalker para percorrer e examinar os elementos na árvore de automação da interface do usuário da Microsoft.
ms.assetid: 41ca783d-56d1-4ad5-8f07-c265ff2e07bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed5c6c1bec961d4f0df83687cd19eecba6ed179
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822556"
---
# <a name="how-to-walk-the-ui-automation-tree"></a><span data-ttu-id="baa30-103">Como percorrer a árvore de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="baa30-103">How to Walk the UI Automation Tree</span></span>

<span data-ttu-id="baa30-104">Este tópico contém um código de exemplo que mostra como usar a interface [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) para percorrer e examinar os elementos na árvore de automação da interface do usuário da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="baa30-104">This topic contains example code that shows how to use the [**IUIAutomationTreeWalker**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker) interface to walk through and examine the elements in the Microsoft UI Automation tree.</span></span> <span data-ttu-id="baa30-105">Ele aborda os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="baa30-105">It discusses the following topics:</span></span>

-   [<span data-ttu-id="baa30-106">Percorrendo os descendentes de um elemento</span><span class="sxs-lookup"><span data-stu-id="baa30-106">Walking through Descendants of an Element</span></span>](#walking-through-descendants-of-an-element)
-   [<span data-ttu-id="baa30-107">Percorrendo elementos ancestrais</span><span class="sxs-lookup"><span data-stu-id="baa30-107">Walking through Ancestor Elements</span></span>](#walking-through-ancestor-elements)
-   [<span data-ttu-id="baa30-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="baa30-108">Related topics</span></span>](#related-topics)

## <a name="walking-through-descendants-of-an-element"></a><span data-ttu-id="baa30-109">Percorrendo os descendentes de um elemento</span><span class="sxs-lookup"><span data-stu-id="baa30-109">Walking through Descendants of an Element</span></span>

<span data-ttu-id="baa30-110">O exemplo de código a seguir é uma função recursiva que percorre todos os descendentes de um elemento de interface do usuário e exibe seus tipos de controle em uma lista hierárquica.</span><span class="sxs-lookup"><span data-stu-id="baa30-110">The following code example is a recursive function that walks through all the descendants of a UI element and displays their control types in a hierarchical list.</span></span>


```C++
// CAUTION: Do not pass in the root (desktop) element. Traversing the entire subtree
// of the desktop could take a very long time and even lead to a stack overflow.
void ListDescendants(IUIAutomationElement* pParent, int indent)
{
    if (pParent == NULL)
        return;

    IUIAutomationTreeWalker* pControlWalker = NULL;
    IUIAutomationElement* pNode = NULL;

    g_pAutomation->get_ControlViewWalker(&pControlWalker);
    if (pControlWalker == NULL)
        goto cleanup;

    pControlWalker->GetFirstChildElement(pParent, &pNode);
    if (pNode == NULL)
        goto cleanup;

    while (pNode)
    {
        BSTR desc;
        pNode->get_CurrentLocalizedControlType(&desc);
        for (int x = 0; x <= indent; x++)
        {
            std::wcout << L"   ";
        }
        std::wcout << desc << L"\n";
        SysFreeString(desc);

        ListDescendants(pNode, indent+1);
        IUIAutomationElement* pNext;
        pControlWalker->GetNextSiblingElement(pNode, &pNext);
        pNode->Release();
        pNode = pNext;
    }

cleanup:
    if (pControlWalker != NULL)
        pControlWalker->Release();

    if (pNode != NULL)
        pNode->Release();

    return;
}
```



## <a name="walking-through-ancestor-elements"></a><span data-ttu-id="baa30-111">Percorrendo elementos ancestrais</span><span class="sxs-lookup"><span data-stu-id="baa30-111">Walking through Ancestor Elements</span></span>

<span data-ttu-id="baa30-112">O exemplo de código a seguir é uma função que percorre os ancestrais de um elemento para identificar o elemento pai.</span><span class="sxs-lookup"><span data-stu-id="baa30-112">The following code example is a function that walks through the ancestors of a element to identify the parent element.</span></span> <span data-ttu-id="baa30-113">Isso é útil quando você precisa identificar a janela pai de um controle.</span><span class="sxs-lookup"><span data-stu-id="baa30-113">This is useful when you need to identify the parent window of a control.</span></span> <span data-ttu-id="baa30-114">A função retorna **NULL** para elementos de nível superior; ou seja, elementos cujo pai é a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="baa30-114">The function returns **NULL** for top-level elements; that is, elements whose parent is the desktop.</span></span>


```C++
IUIAutomationElement* GetContainingWindow(IUIAutomationElement* pChild)
{

    if (pChild == NULL)
        return NULL;

    IUIAutomationElement* pDesktop = NULL;
    HRESULT hr = g_pAutomation->GetRootElement(&pDesktop);
    if (FAILED(hr))
        return NULL;

    BOOL same;
    g_pAutomation->CompareElements(pChild, pDesktop, &same);
    if (same)
    {
        pDesktop->Release();
        return NULL; // No parent, so return NULL.
    }

    IUIAutomationElement* pParent = NULL;
    IUIAutomationElement* pNode = pChild;

    // Create the treewalker.
    IUIAutomationTreeWalker* pWalker = NULL;
    g_pAutomation->get_ControlViewWalker(&pWalker);
    if (pWalker == NULL)
        goto cleanup;

    // Walk up the tree.
    while (TRUE)
    {
        hr = pWalker->GetParentElement(pNode, &pParent);
        if (FAILED(hr) || pParent == NULL)
        {
            break;
        }
        g_pAutomation->CompareElements(pParent, pDesktop, &same);
        if (same)
        {
            pDesktop->Release();
            pParent->Release();
            pWalker->Release();
            // Reached desktop, so return next element below it.
            return pNode;
        }
        if (pNode != pChild) // Do not release the in-param.
            pNode->Release();
        pNode = pParent;
    }

cleanup:
    if ((pNode != NULL) && (pNode != pChild)) 
        pNode->Release();

    if (pDesktop != NULL)
        pDesktop->Release();

    if (pWalker != NULL)
        pWalker->Release();

    if (pParent != NULL)
        pParent->Release();

    return NULL;  
}
```



## <a name="related-topics"></a><span data-ttu-id="baa30-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="baa30-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="baa30-116">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="baa30-116">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="baa30-117">Obtendo elementos da automação interface do usuário</span><span class="sxs-lookup"><span data-stu-id="baa30-117">Obtaining UI Automation Elements</span></span>](uiauto-obtainingelements.md)
</dt> <dt>

[<span data-ttu-id="baa30-118">Tópicos de instruções para clientes de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="baa30-118">How-To Topics for UI Automation Clients</span></span>](uiauto-howto-topics-for-uiautomation-clients.md)
</dt> </dl>

 

 




