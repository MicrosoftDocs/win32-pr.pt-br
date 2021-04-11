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
# <a name="enumerating-items"></a>Enumerando itens

Quando um dispositivo é criado, o WIA (aquisição de imagem do Windows) cria uma árvore hierárquica de itens WIA que representam o dispositivo e as pastas e imagens associadas a esse dispositivo. Use o item raiz (o item na raiz da árvore que representa o dispositivo) [**IWiaItem:: EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) (ou [**IWiaItem2:: EnumChildItems**](-wia-iwiaitem2-enumchilditems.md)) para criar um objeto enumerador e obter um ponteiro para sua interface [**IEnumWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwiaitem) (ou [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)), que é usada para navegar na árvore de itens e obter acesso às imagens ou aos ambientes de verificação associados ao dispositivo.

O exemplo a seguir mostra uma função que enumera recursivamente todos os itens de uma árvore, começando com um item raiz que é passado para a função.


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



A função usa o parâmetro **pWiaItem**, um ponteiro para a interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) (ou [**IWiaItem2**](-wia-iwiaitem2.md)) do item raiz da árvore de itens a ser enumerada.

Primeiro, a função verifica se o item é uma pasta ou se tem anexos. Em seguida, ele chama o método [**IWiaItem:: EnumChildItems**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumchilditems) (ou [**IWiaItem2:: EnumChildItems**](-wia-iwiaitem2-enumchilditems.md)) de **pWiaItem** para criar um objeto enumerador para a árvore de itens. Se essa chamada for bem sucedido e o enumerador for válido, a função iterará pelos itens filho e chamará recursivamente a si mesmo em cada item, tratando cada um como um item raiz potencial para o próximo nível de itens filho.

Dessa maneira, a função enumera todas as ramificações da árvore de itens abaixo do item raiz passado para **EnumerateItems**.

 

 



