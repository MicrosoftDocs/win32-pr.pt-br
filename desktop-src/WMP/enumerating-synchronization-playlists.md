---
title: Enumerando listas de reprodução de sincronização
description: Enumerando listas de reprodução de sincronização
ms.assetid: 830c3ea5-2937-48b5-b89f-ef68a6649ca3
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
- listas de reprodução de sincronização, enumerando
- dispositivos portáteis, enumerando
- enumerações, listas de reprodução de sincronização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29679380cec1844e9a790ac4ff047bfa4bf05288
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105788171"
---
# <a name="enumerating-synchronization-playlists"></a>Enumerando listas de reprodução de sincronização

O código de exemplo a seguir cria uma função que preenche um controle ListView com listas de reprodução. As playlists de sincronização aparecem primeiro. As playlists de sincronização para o dispositivo selecionado no momento são marcadas com uma marca de seleção e são classificadas em ordem de prioridade de sincronização. Todas as outras listas de reprodução estão desmarcadas.

O controle ListView foi configurado para seleção única. A ordem das listas de reprodução no controle ListView determina sua prioridade de sincronização. O estado de verificação de uma lista de reprodução individual determina se é uma lista de reprodução de sincronização para o dispositivo selecionado no momento.

O parâmetro *lPSIndex* especifica o índice de parceria para o dispositivo portátil selecionado no momento.


```C++
STDMETHODIMP CSyncSettings::ShowPlaylists(long lPSIndex)
{ 
    HRESULT hr = S_OK; 
    ATLASSERT(m_pMainDlg);
   
    CComPtr<IWMPMediaCollection> spMediaCollection;
    CComPtr<IWMPPlaylist> spPlaylist; // Contains a playlist of all playlists.
    long lSyncItemCount= 0; // Count of items selected for synchronization. 

    ListView_DeleteAllItems(m_hPlView);

    m_spPlaylist.Release();
   
    if(lPSIndex == 0)
    {
        return S_OK;
    } 

    HCURSOR hCursor = LoadCursor(NULL, IDC_WAIT);
    HCURSOR hCursorOld = SetCursor(hCursor);

    if(SUCCEEDED(hr))
    {
        // Retrieve a pointer to IWMPMediaCollection.
        hr = m_spPlayer->get_mediaCollection(&spMediaCollection);
    }

    if(SUCCEEDED(hr) && spMediaCollection)
    {
        // Retrieve a playlist filled with IWMPMedia items.
        // Each IWMPMedia represents an individual playlist 
        // in the library.
        hr = spMediaCollection->getByAttribute(CComBSTR("MediaType"), CComBSTR("playlist"), &spPlaylist);
    }
 
    if(SUCCEEDED(hr) && spPlaylist)
    {  
        // Get the sync attribute name for the current device.
        CComBSTR bstrAttribute(g_szSyncAttributeNames[lPSIndex]);

        // Sort the playlist.
        // lSyncItemCount is the count of synchronization playlists.
        hr = SortPlaylist(spPlaylist, bstrAttribute, &lSyncItemCount);
     
        if(SUCCEEDED(hr))
        {
            m_spPlaylist = spPlaylist;  // Cache the playlist.

            long lCount = 0;
            spPlaylist->get_count(&lCount);
             
            // Fill the ListView control.
            for(long i = 0; i < lCount; i++)
            {
                CComPtr<IWMPMedia> spMedia;
                CComBSTR bstrPlaylistName;
                CComBSTR bstrVal; // Value of the SyncXX attribute.

                // Retrieve a playlist.
                hr = spPlaylist->get_item(i, &spMedia);

                if(SUCCEEDED(hr) && spMedia)
                {
                    // Get the name.
                    hr = spMedia->get_name(&bstrPlaylistName);
                }  
                if(SUCCEEDED(hr) && spMedia)
                {      
                    // Get the SyncXX attribute value.
                    hr = spMedia->getItemInfo(bstrAttribute, &bstrVal);
                }

                if(SUCCEEDED(hr) && bstrPlaylistName.Length())
                {
                    // Insert the item in the ListView control.
                    LVITEM lvI;
                    ZeroMemory(&lvI, sizeof(LVITEM));
                    lvI.mask = LVIF_TEXT; 
                    lvI.lParam = _wtol(bstrVal);
                    lvI.iItem = ListView_GetItemCount(m_hPlView);
                    lvI.pszText = "";
                    ListView_InsertItem(m_hPlView, &lvI);

                    // If this is a sync playlist, mark the check box.
                    if(i < lSyncItemCount)
                    {
                        ListView_SetCheckState(m_hPlView, i, TRUE);
                    }

                    // Display the playlist name.
                    lvI.iSubItem = 1;
                    lvI.pszText = COLE2T(bstrPlaylistName);
                    ListView_SetItem(m_hPlView, &lvI);
                }
            }
        }        
    }

    SetCursor(hCursorOld);
    return hr;
}
```



Para a implementação da função SortPlaylist, consulte [classificando listas de reprodução por prioridade de sincronização](sorting-playlists-by-synchronization-priority.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWMPMedia:: getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo)
</dt> <dt>

[**IWMPMediaCollection::getByAttribute**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyattribute)
</dt> <dt>

[**Gerenciando listas de reprodução de sincronização**](managing-synchronization-playlists.md)
</dt> <dt>

[**Atributos de sincronização**](sync-attributes.md)
</dt> </dl>

 

 




