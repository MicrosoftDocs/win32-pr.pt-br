---
title: Alterando a prioridade de sincronização
description: Alterando a prioridade de sincronização
ms.assetid: 992781cb-5018-4b88-aa93-2f8a86468a42
keywords:
- Windows Media Player, playlists de sincronização
- modelo de objeto Windows Media Player, playlists de sincronização
- modelo de objeto, playlists de sincronização
- Windows Media Player Listas de reprodução móveis e de sincronização
- controle de ActiveX de Windows Media Player, listas de reprodução de sincronização
- Windows Media Player controle de ActiveX móvel, playlists de sincronização
- controle de ActiveX, listas de reprodução de sincronização
- listas de reprodução, sincronização
- listas de reprodução de metarquivo, sincronização
- Windows Listas de reprodução de metarquivo de mídia, sincronização
- dispositivos portáteis, alterando as prioridades da lista de reprodução de sincronização
- listas de reprodução de sincronização, prioridades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1513679bcde31893cd7c4f456bc0e99404bb5dc66de37976f2053ae1559a4cdf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997656"
---
# <a name="changing-synchronization-priority"></a>Alterando a prioridade de sincronização

O código de exemplo a seguir especifica um valor de prioridade para cada item no controle ListView identificado pelo IDC \_ PLVIEW. Os itens marcados com uma marca de seleção recebem um valor de prioridade com base em sua ordem na lista. Os itens que não são verificados recebem um valor de prioridade zero.


```C++
void CSyncSettings::SetPriorities()
{
    ATLASSERT(m_spPlaylist.p);
    
    long lCount = 0;
    CComBSTR bstrAttribute(g_szSyncAttributeNames[m_lCurrentPSIndex]); 
    long lPriorityCount = 0; // Tracks the next priority value to be assigned.
    long lNewPriority = 0; // Contains the new priority value for the playlist.

    HRESULT hr = m_spPlaylist->get_count(&lCount);

    if(SUCCEEDED(hr) && lCount > 0)
    {
        HCURSOR hCursor = LoadCursor(NULL, IDC_WAIT);
        HCURSOR hCursorOld = SetCursor(hCursor);

        // Walk the list.
        for(long i = 0; i < lCount; i++)
        {
            CComPtr<IWMPMedia> spMedia;
            BOOL bChecked = ListView_GetCheckState(m_hPlView, i);

            if(TRUE == bChecked)
            {
                // Assign a priority value.
                lNewPriority = ++lPriorityCount;
            }
            else
            {
                // Not a sync playlist.
                lNewPriority = 0;
            }

            // Set the attribute on the playlist.
            hr = m_spPlaylist->get_item(i, &spMedia);

            if(SUCCEEDED(hr))
            {     
                WCHAR buffer[30];
                _ltow(lNewPriority, buffer, 10);
                CComBSTR bstrPriority(buffer);
                hr = spMedia->setItemInfo(bstrAttribute, bstrPriority);
            }
        }
        SetCursor(hCursorOld);
    }       
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**Interface IWMPPlaylist**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[**Gerenciando listas de reprodução de sincronização**](managing-synchronization-playlists.md)
</dt> </dl>

 

 




