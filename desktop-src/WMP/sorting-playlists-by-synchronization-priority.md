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
# <a name="sorting-playlists-by-synchronization-priority"></a><span data-ttu-id="b3533-116">Classificando listas de reprodução por prioridade de sincronização</span><span class="sxs-lookup"><span data-stu-id="b3533-116">Sorting Playlists by Synchronization Priority</span></span>

<span data-ttu-id="b3533-117">O código a seguir executa uma classificação simples de listas de reprodução.</span><span class="sxs-lookup"><span data-stu-id="b3533-117">The following code performs a simple sort of playlists.</span></span> <span data-ttu-id="b3533-118">Você pode ver como essa função é usada no código de exemplo na [enumeração de listas de reprodução de sincronização](enumerating-synchronization-playlists.md).</span><span class="sxs-lookup"><span data-stu-id="b3533-118">You can see how this function is used in the example code in [Enumerating Synchronization Playlists](enumerating-synchronization-playlists.md).</span></span> <span data-ttu-id="b3533-119">A função usa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="b3533-119">The function takes the following parameters:</span></span>

-   <span data-ttu-id="b3533-120">*pPlaylist*.</span><span class="sxs-lookup"><span data-stu-id="b3533-120">*pPlaylist*.</span></span> <span data-ttu-id="b3533-121">O ponteiro para a lista de reprodução do Windows Media Player a ser classificado.</span><span class="sxs-lookup"><span data-stu-id="b3533-121">The pointer to the Windows Media Player playlist to sort.</span></span> <span data-ttu-id="b3533-122">Os itens de mídia na lista de reprodução devem apontar para outras listas de reprodução, não para arquivos de mídia digital individuais.</span><span class="sxs-lookup"><span data-stu-id="b3533-122">The media items in the playlist must point to other playlists, not individual digital media files.</span></span>
-   <span data-ttu-id="b3533-123">*bstrSyncAttribute*.</span><span class="sxs-lookup"><span data-stu-id="b3533-123">*bstrSyncAttribute*.</span></span> <span data-ttu-id="b3533-124">Um BSTR que contém o nome do atributo de parceria de sincronização para o dispositivo atual ("Sync01", "Sync02" e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="b3533-124">A BSTR containing the name of the synchronization partnership attribute for the current device ("Sync01", "Sync02", and so on).</span></span>
-   <span data-ttu-id="b3533-125">*plSelected*.</span><span class="sxs-lookup"><span data-stu-id="b3533-125">*plSelected*.</span></span> <span data-ttu-id="b3533-126">Ponteiro para uma variável **longa** que recebe a contagem de listas de reprodução de sincronização.</span><span class="sxs-lookup"><span data-stu-id="b3533-126">Pointer to a **long** variable that receives the count of synchronization playlists.</span></span>

<span data-ttu-id="b3533-127">A função inspeciona o atributo de parceria de sincronização para cada item de mídia (representando uma lista de reprodução) na lista de reprodução especificada por *pPlaylist*.</span><span class="sxs-lookup"><span data-stu-id="b3533-127">The function inspects the synchronization partnership attribute for each media item (representing a playlist) in the playlist specified by *pPlaylist*.</span></span> <span data-ttu-id="b3533-128">Se o atributo tiver um valor diferente de zero, o código moverá o item de mídia para o início da lista de reprodução e o inserirá em ordem de prioridade.</span><span class="sxs-lookup"><span data-stu-id="b3533-128">If the attribute has a nonzero value, the code moves the media item to the beginning of the playlist and inserts it in priority order.</span></span>

<span data-ttu-id="b3533-129">Quando terminar, a função retorna a contagem de itens de mídia (playlists de sincronização) que tinham um valor diferente de zero para o atributo de parceria de sincronização.</span><span class="sxs-lookup"><span data-stu-id="b3533-129">When finished, the function returns the count of media items (synchronization playlists) that had a nonzero value for the synchronization partnership attribute.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="b3533-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b3533-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3533-131">**IWMPMedia:: getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="b3533-131">**IWMPMedia::getItemInfo**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo)
</dt> <dt>

[<span data-ttu-id="b3533-132">**IWMPPlaylist:: obter \_ Item**</span><span class="sxs-lookup"><span data-stu-id="b3533-132">**IWMPPlaylist::get\_item**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-get_item)
</dt> <dt>

[<span data-ttu-id="b3533-133">**IWMPPlaylist::moveItem**</span><span class="sxs-lookup"><span data-stu-id="b3533-133">**IWMPPlaylist::moveItem**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-moveitem)
</dt> <dt>

[<span data-ttu-id="b3533-134">**Gerenciando listas de reprodução de sincronização**</span><span class="sxs-lookup"><span data-stu-id="b3533-134">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> <dt>

[<span data-ttu-id="b3533-135">**Atributos de sincronização**</span><span class="sxs-lookup"><span data-stu-id="b3533-135">**Sync Attributes**</span></span>](sync-attributes.md)
</dt> </dl>

 

 




