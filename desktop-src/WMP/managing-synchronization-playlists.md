---
title: Gerenciando listas de reprodução de sincronização
description: Gerenciando listas de reprodução de sincronização
ms.assetid: 5891ada0-37a6-4256-9885-8aa9dbe98b7c
keywords:
- Windows Media Player, dispositivos portáteis
- Modelo de objeto do Windows Media Player, dispositivos portáteis
- modelo de objeto, dispositivos portáteis
- Controle ActiveX do Windows Media Player, dispositivos portáteis
- Controle ActiveX, dispositivos portáteis
- Controle ActiveX móvel do Windows Media Player, dispositivos portáteis
- Windows Media Player Mobile, dispositivos portáteis
- dispositivos portáteis, Gerenciando listas de reprodução de sincronização
- sincronização de dispositivo, listas de reprodução
- Sincronizando dispositivos, listas de reprodução
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
- listas de reprodução de sincronização, gerenciando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be0fe084918c0b69b827dbb941388246cbd177ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105811562"
---
# <a name="managing-synchronization-playlists"></a>Gerenciando listas de reprodução de sincronização

O Windows Media Player 10 ou posterior usa listas de reprodução para sincronizar arquivos de mídia digital com dispositivos portáteis. Esta seção explica como trabalhar com listas de reprodução de sincronização.

O código de exemplo nesta seção usa dois controles ListView para exibir informações. O primeiro controle ListView (IDC \_ PLVIEW) exibe todas as listas de reprodução na biblioteca do Windows Media Player, com as playlists de sincronização exibidas primeiro. As playlists de sincronização para o dispositivo selecionado no momento são marcadas com uma marca de seleção e são classificadas em ordem de prioridade de sincronização. Todas as outras listas de reprodução estão desmarcadas. O controle ListView foi configurado para seleção única. A ordem das listas de reprodução no controle ListView determina sua prioridade de sincronização. O estado de verificação de uma lista de reprodução individual determina se é uma lista de reprodução de sincronização para o dispositivo selecionado no momento.

O segundo controle ListView (IDC \_ MEDIAVIEW) exibe os itens de mídia na lista de reprodução selecionada. Duas colunas adicionais exibem texto indicando se o arquivo de mídia digital foi copiado para o dispositivo e, em caso de falha, se a cópia falhou porque o arquivo de mídia digital não se ajustou.

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



A matriz de cadeias de caracteres a seguir contém os nomes dos atributos de sincronização usados nos exemplos:


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



A variável de membro a seguir contém uma lista de reprodução que contém todas as listas de reprodução na biblioteca do Windows Media Player. Cada playlist é representada como um item de mídia.


```C++
CComPtr<IWMPPlaylist> m_spPlaylist;
```



As seções a seguir fornecem código de exemplo:

-   [Enumerando listas de reprodução de sincronização](enumerating-synchronization-playlists.md)
-   [Classificando listas de reprodução por prioridade de sincronização](sorting-playlists-by-synchronization-priority.md)
-   [Enumerando os itens de mídia](enumerating-the-media-items.md)
-   [Determinando o estado de sincronização da playlist](determining-playlist-synchronization-state.md)
-   [Alterando a prioridade de sincronização](changing-synchronization-priority.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Trabalhando com dispositivos portáteis**](working-with-portable-devices.md)
</dt> </dl>

 

 




