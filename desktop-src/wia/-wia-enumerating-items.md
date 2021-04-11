---
description: Quando um dispositivo é criado, o WIA (aquisição de imagem do Windows) cria uma árvore hierárquica de itens WIA que representam o dispositivo e as pastas e imagens associadas a esse dispositivo.
ms.assetid: ab7246e8-47bb-4b94-8d91-1c22010ebd9f
title: Enumerando itens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c216e658b7105f6b3d88d01bd55a3200af7e45c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169541"
---
# <a name="enumerating-items"></a><span data-ttu-id="6ff1e-103">Enumerando itens</span><span class="sxs-lookup"><span data-stu-id="6ff1e-103">Enumerating Items</span></span>

<span data-ttu-id="6ff1e-104">Quando um dispositivo é criado, o WIA (aquisição de imagem do Windows) cria uma árvore hierárquica de itens WIA que representam o dispositivo e as pastas e imagens associadas a esse dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ff1e-104">When a device is created, Windows Image Acquisition (WIA) creates a hierarchical tree of WIA items that represent the device and the folders and images associated with that device.</span></span> <span data-ttu-id="6ff1e-105">Use o item raiz (o item na raiz da árvore que representa o dispositivo) [**IWiaItem:: EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) (ou [**IWiaItem2:: EnumChildItems**](-wia-iwiaitem2-enumchilditems.md)) para criar um objeto enumerador e obter um ponteiro para sua interface [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) (ou [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)), que é usada para navegar na árvore de itens e obter acesso às imagens ou aos ambientes de verificação associados ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ff1e-105">Use the root item's (the item at the root of the tree that represents the device) [**IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) (or [**IWiaItem2::EnumChildItems**](-wia-iwiaitem2-enumchilditems.md)) method to create an enumerator object and obtain a pointer to its [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) (or [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)) interface, which is used to navigate the item tree and gain access to the images or scanning beds associated with the device.</span></span>

<span data-ttu-id="6ff1e-106">O exemplo a seguir mostra uma função que enumera recursivamente todos os itens de uma árvore, começando com um item raiz que é passado para a função.</span><span class="sxs-lookup"><span data-stu-id="6ff1e-106">The following example shows a function that recursively enumerates all of the items of a tree, beginning with a root item that is passed to the function.</span></span>


```
    HRESULT EnumerateItems( IWiaItem *pWiaItem ) //XP or earlier
    HRESULT EnumerateItems( IWiaItem2 *pWiaItem ) //Vista or later
    {
        //
        // Validate arguments
        //
        if (NULL == pWiaItem)
        {
            return E_INVALIDARG;
        }

        //
        // Get the item type for this item.
        //
        LONG lItemType = 0;
        HRESULT hr = pWiaItem->GetItemType( &lItemType );
        if (SUCCEEDED(hr))
        {
            //
            // If it is a folder, or it has attachments, enumerate its children.
            //
            if (lItemType & WiaItemTypeFolder || lItemType & WiaItemTypeHasAttachments)
            {
                //
                // Get the child item enumerator for this item.
                //
                IEnumWiaItem *pEnumWiaItem = NULL; //XP or earlier
                IEnumWiaItem2 *pEnumWiaItem = NULL; //Vista or later
                
                hr = pWiaItem->EnumChildItems( &pEnumWiaItem );
                if (SUCCEEDED(hr))
                {
                    //
                    // Loop until you get an error or pEnumWiaItem->Next returns
                    // S_FALSE to signal the end of the list.
                    //
                    while (S_OK == hr)
                    {
                        //
                        // Get the next child item.
                        //
                        IWiaItem *pChildWiaItem = NULL; //XP or earlier
                        IWiaItem2 *pChildWiaItem = NULL; //Vista or later
                        
                        hr = pEnumWiaItem->Next( 1, &pChildWiaItem, NULL );

                        //
                        // pEnumWiaItem->Next will return S_FALSE when the list is
                        // exhausted, so check for S_OK before using the returned
                        // value.
                        //
                        if (S_OK == hr)
                        {
                            //
                            // Recurse into this item.
                            //
                            hr = EnumerateItems( pChildWiaItem );

                            //
                            // Release this item.
                            //
                            pChildWiaItem->Release();
                            pChildWiaItem = NULL;
                        }
                    }

                    //
                    // If the result of the enumeration is S_FALSE (which
                    // is normal), change it to S_OK.
                    //
                    if (S_FALSE == hr)
                    {
                        hr = S_OK;
                    }

                    //
                    // Release the enumerator.
                    //
                    pEnumWiaItem->Release();
                    pEnumWiaItem = NULL;
                }
            }
        }
        return  hr;
    }
```



<span data-ttu-id="6ff1e-107">A função usa o parâmetro **pWiaItem**, um ponteiro para a interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) (ou [**IWiaItem2**](-wia-iwiaitem2.md)) do item raiz da árvore de itens a ser enumerada.</span><span class="sxs-lookup"><span data-stu-id="6ff1e-107">The function takes the parameter **pWiaItem**, a pointer to the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) (or [**IWiaItem2**](-wia-iwiaitem2.md)) interface of the root item of the item tree to enumerate.</span></span>

<span data-ttu-id="6ff1e-108">Primeiro, a função verifica se o item é uma pasta ou se tem anexos.</span><span class="sxs-lookup"><span data-stu-id="6ff1e-108">First, the function checks to see whether the item is a folder or if it has attachments.</span></span> <span data-ttu-id="6ff1e-109">Em seguida, ele chama o método [**IWiaItem:: EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) (ou [**IWiaItem2:: EnumChildItems**](-wia-iwiaitem2-enumchilditems.md)) de **pWiaItem** para criar um objeto enumerador para a árvore de itens.</span><span class="sxs-lookup"><span data-stu-id="6ff1e-109">If it does, it then calls the [**IWiaItem::EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) (or [**IWiaItem2::EnumChildItems**](-wia-iwiaitem2-enumchilditems.md)) method of **pWiaItem** to create an enumerator object for the item tree.</span></span> <span data-ttu-id="6ff1e-110">Se essa chamada for bem sucedido e o enumerador for válido, a função iterará pelos itens filho e chamará recursivamente a si mesmo em cada item, tratando cada um como um item raiz potencial para o próximo nível de itens filho.</span><span class="sxs-lookup"><span data-stu-id="6ff1e-110">If this call succeeds, and the enumerator is valid, the function iterates through the child items, and recursively calls itself on each item, treating each as a potential root item for the next level of child items.</span></span>

<span data-ttu-id="6ff1e-111">Dessa maneira, a função enumera todas as ramificações da árvore de itens abaixo do item raiz passado para **EnumerateItems**.</span><span class="sxs-lookup"><span data-stu-id="6ff1e-111">In this manner, the function enumerates all branches of the item tree below the root item passed to **EnumerateItems**.</span></span>

 

 



