---
title: Gerenciando listas de reprodução de sincronização
description: Gerenciando listas de reprodução de sincronização
ms.assetid: 5891ada0-37a6-4256-9885-8aa9dbe98b7c
keywords:
- Windows Media Player, dispositivos portáteis
- Windows Media Player de objeto, dispositivos portáteis
- modelo de objeto, dispositivos portáteis
- Windows Media Player ActiveX controle, dispositivos portáteis
- ActiveX controle, dispositivos portáteis
- Windows Media Player Controle ActiveX dispositivos móveis, dispositivos portáteis
- Windows Media Player Dispositivos móveis e portáteis
- dispositivos portáteis, gerenciando listas de reprodução de sincronização
- sincronização de dispositivo, playlists
- sincronizando dispositivos, playlists
- Windows Media Player, playlists de sincronização
- Windows Media Player de objeto, listas de reprodução de sincronização
- modelo de objeto, playlists de sincronização
- Windows Media Player Mobile, synchronization playlists
- Windows Media Player ActiveX controle, listas de reprodução de sincronização
- Windows Media Player Controle de ActiveX móvel, listas de reprodução de sincronização
- ActiveX controle, listas de reprodução de sincronização
- playlists, sincronização
- playlists de metafile, sincronização
- Windows Playlists de metadados de mídia, sincronização
- playlists de sincronização, gerenciando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10253d7f08c618d62079ccc1767fdaf85560861eae68d39cd897e7959eaffcad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996366"
---
# <a name="managing-synchronization-playlists"></a>Gerenciando listas de reprodução de sincronização

Windows Media Player 10 ou posterior usa playlists para sincronizar arquivos de mídia digital com dispositivos portáteis. Esta seção explica como trabalhar com playlists de sincronização.

O código de exemplo nesta seção usa dois controles ListView para exibir informações. O primeiro controle ListView (IDC PLVIEW) exibe todas as playlists na biblioteca Windows Media Player, com listas de reprodução de sincronização \_ aparecendo primeiro. As listas de reprodução de sincronização para o dispositivo selecionado no momento são marcadas com uma marca de seleção e são classificação na ordem de prioridade de sincronização. Todas as outras playlists estão desmarcadas. O controle ListView foi configurado para seleção única. A ordem das listas de reprodução no controle ListView determina sua prioridade de sincronização. O estado verificado de uma playlist individual determina se é uma playlist de sincronização para o dispositivo selecionado no momento.

O segundo controle ListView (IDC \_ MEDIAVIEW) exibe os itens de mídia na playlist selecionada. Duas colunas adicionais exibem texto que indica se o arquivo de mídia digital foi copiado para o dispositivo e, no caso de uma falha, se a cópia falhou porque o arquivo de mídia digital não se encaixava.

O código de exemplo a seguir mostra como os controles ListView são inicializados:


```C++
STDMETHODIMP CSyncSettings::InitListView()
{
    m_hPlView = GetDlgItem(IDC_PLVIEW);
    m_hMediaView = GetDlgItem(IDC_MEDIAVIEW); 

    ATLASSERT(m_hPlView);
    ATLASSERT(m_hMediaView);

    // Sync playlist information.
    // Selection highlights all rows.
    // Show checkboxes.
    ListView_SetExtendedListViewStyleEx(m_hPlView, 0, LVS_EX_CHECKBOXES | LVS_EX_FULLROWSELECT);
   
    // Add headers.
    LVCOLUMN lvc;
    ZeroMemory(&lvc, sizeof(LVCOLUMN));
    lvc.mask = LVCF_WIDTH | LVCF_TEXT | LVCF_SUBITEM; 
    lvc.iSubItem = 0;
    
    lvc.pszText = _T("Sync");
    lvc.cx = 40;
    ListView_InsertColumn(m_hPlView, lvc.iSubItem, &lvc);

    lvc.iSubItem++;
    lvc.pszText = _T("Playlist Name");
    lvc.cx = 300;
    ListView_InsertColumn(m_hPlView, lvc.iSubItem, &lvc); 

    // Media information.
    // Selection highlights all rows.
    ListView_SetExtendedListViewStyleEx(m_hMediaView, 0, LVS_EX_FULLROWSELECT);

    // Add headers
    ZeroMemory(&lvc, sizeof(LVCOLUMN));
    lvc.mask = LVCF_WIDTH | LVCF_TEXT | LVCF_SUBITEM; 
    lvc.iSubItem = 0;
    
    lvc.pszText = _T("Media name");
    lvc.cx = 150;
    ListView_InsertColumn(m_hMediaView, lvc.iSubItem, &lvc);

    lvc.iSubItem++;
    lvc.pszText = _T("On Device");
    lvc.cx = 69;
    ListView_InsertColumn(m_hMediaView, lvc.iSubItem, &lvc);  

    lvc.iSubItem++;
    lvc.pszText = _T("Fit?");
    lvc.cx = 40;
    ListView_InsertColumn(m_hMediaView, lvc.iSubItem, &lvc);  
   
    return S_OK;
}
```



A seguinte matriz de cadeias de caracteres contém os nomes dos atributos de sincronização usados nos exemplos:


```C++
static const TCHAR *g_szSyncAttributeNames[17] = {
        _T("Not used"), // Do not access this one.
        _T("Sync01"),
        _T("Sync02"),
        _T("Sync03"),
        _T("Sync04"),
        _T("Sync05"),
        _T("Sync06"),
        _T("Sync07"),
        _T("Sync08"),
        _T("Sync09"),
        _T("Sync10"),
        _T("Sync11"),
        _T("Sync12"),
        _T("Sync13"),
        _T("Sync14"),
        _T("Sync15"),
        _T("Sync16")};
```



A variável de membro a seguir contém uma playlist que contém todas as playlists na biblioteca Windows Media Player dados. Cada playlist é representada como um item de mídia.


```C++
CComPtr<IWMPPlaylist> m_spPlaylist;
```



As seções a seguir fornecem código de exemplo:

-   [Enumerando listas de reprodução de sincronização](enumerating-synchronization-playlists.md)
-   [Classificação de listas de reprodução por prioridade de sincronização](sorting-playlists-by-synchronization-priority.md)
-   [Enumerando os itens de mídia](enumerating-the-media-items.md)
-   [Determinando o estado de sincronização da playlist](determining-playlist-synchronization-state.md)
-   [Alterando a prioridade de sincronização](changing-synchronization-priority.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Trabalhando com dispositivos portáteis**](working-with-portable-devices.md)
</dt> </dl>

 

 




