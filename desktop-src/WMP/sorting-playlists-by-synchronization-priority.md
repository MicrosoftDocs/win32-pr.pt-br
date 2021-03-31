---
title: Classificando listas de reprodução por prioridade de sincronização
description: Classificando listas de reprodução por prioridade de sincronização
ms.assetid: 0f7f1ed3-0639-47bf-bf8e-52ae0a1d7ab2
keywords:
- Windows Media Player, listas de reprodução de sincronização
- Modelo de objeto do Windows Media Player, listas de reprodução de sincronização
- modelo de objeto, playlists de sincronização
- Windows Media Player Mobile, listas de reprodução de sincronização
- Controle ActiveX do Windows Media Player, listas de reprodução de sincronização
- Controle ActiveX móvel do Windows Media Player, listas de reprodução de sincronização
- Controle ActiveX, listas de reprodução de sincronização
- listas de reprodução, sincronização
- listas de reprodução de metarquivo, sincronização
- Listas de reprodução do metarquivo do Windows Media, sincronização
- dispositivos portáteis, classificando listas de reprodução de sincronização
- listas de reprodução de sincronização, classificação
- listas de reprodução de sincronização, prioridades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90624e8e1cab715e8a26e33f40a444d53ab35def
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103823570"
---
# <a name="sorting-playlists-by-synchronization-priority"></a>Classificando listas de reprodução por prioridade de sincronização

O código a seguir executa uma classificação simples de listas de reprodução. Você pode ver como essa função é usada no código de exemplo na [enumeração de listas de reprodução de sincronização](enumerating-synchronization-playlists.md). A função usa os seguintes parâmetros:

-   *pPlaylist*. O ponteiro para a lista de reprodução do Windows Media Player a ser classificado. Os itens de mídia na lista de reprodução devem apontar para outras listas de reprodução, não para arquivos de mídia digital individuais.
-   *bstrSyncAttribute*. Um BSTR que contém o nome do atributo de parceria de sincronização para o dispositivo atual ("Sync01", "Sync02" e assim por diante).
-   *plSelected*. Ponteiro para uma variável **longa** que recebe a contagem de listas de reprodução de sincronização.

A função inspeciona o atributo de parceria de sincronização para cada item de mídia (representando uma lista de reprodução) na lista de reprodução especificada por *pPlaylist*. Se o atributo tiver um valor diferente de zero, o código moverá o item de mídia para o início da lista de reprodução e o inserirá em ordem de prioridade.

Quando terminar, a função retorna a contagem de itens de mídia (playlists de sincronização) que tinham um valor diferente de zero para o atributo de parceria de sincronização.


```C++
STDMETHODIMP CSyncSettings::SortPlaylist(IWMPPlaylist *pPlaylist, BSTR bstrSyncAttribute, long *plSelected)
{
    HRESULT hr = S_OK;
    long lSyncItemCount = 0;

    ATLASSERT (pPlaylist);
    ATLASSERT (plSelected);

    // Local copies of the parameters.
    CComPtr<IWMPPlaylist> spPlaylist(pPlaylist);
    CComBSTR bstrAttribute(bstrSyncAttribute);

    ATLASSERT (bstrAttribute.Length());

    // Get the count of playlist media items.
    long lCount = 0;
    spPlaylist->get_count(&lCount);

    // Walk the playlist.
    for(long i = 0; i < lCount; i++)
    {
        CComPtr<IWMPMedia> spMedia;                 
        CComBSTR bstrVal;            
        long lPriority = 0;
        
        hr = spPlaylist->get_item(i, &spMedia);

        if(SUCCEEDED(hr) && spMedia)
        {      
            // Get the sync priority value as a string.
            hr = spMedia->getItemInfo(bstrAttribute, &bstrVal);
        }

        if(SUCCEEDED(hr) && spMedia)
        {
            // Convert sync priority to a long number.
            lPriority = _wtol(bstrVal);
        }

        // Sort the playlist.
        // Only move the current item if it has a
        // sync priority value.
        if(lPriority > 0)
        {
            lSyncItemCount++;

            // Walk down the list and insert the item
            // in ascending order.
            for(long j = 0; j < lCount; j++)
            {
                CComPtr<IWMPMedia> spMediaCompare;
                CComBSTR bstrValCompare;
                long lPriorityTest = 0;

                hr = spPlaylist->get_item(j, &spMediaCompare);

                if(SUCCEEDED(hr) && spMediaCompare.p)
                {
                    hr = spMediaCompare->getItemInfo(bstrAttribute, &bstrValCompare);
                }
                if(SUCCEEDED(hr) && spMediaCompare.p)
                {
                    lPriorityTest = _wtol(bstrValCompare);
                    
                    if(lPriority <= lPriorityTest || 
                        0 == lPriorityTest)
                    {
                        hr = spPlaylist->moveItem(i, j);
                        break;                            
                    }                        
                } 
            } // for j                       
        } // if(lPriority > 0)          
    } // for i  
  
    // Return the sync item count.
    *plSelected = lSyncItemCount;

    return hr;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMPMedia:: getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo)
</dt> <dt>

[**IWMPPlaylist:: obter \_ Item**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-get_item)
</dt> <dt>

[**IWMPPlaylist::moveItem**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-moveitem)
</dt> <dt>

[**Gerenciando listas de reprodução de sincronização**](managing-synchronization-playlists.md)
</dt> <dt>

[**Atributos de sincronização**](sync-attributes.md)
</dt> </dl>

 

 




