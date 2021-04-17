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
# <a name="managing-synchronization-playlists"></a><span data-ttu-id="ea6b4-124">Gerenciando listas de reprodução de sincronização</span><span class="sxs-lookup"><span data-stu-id="ea6b4-124">Managing Synchronization Playlists</span></span>

<span data-ttu-id="ea6b4-125">O Windows Media Player 10 ou posterior usa listas de reprodução para sincronizar arquivos de mídia digital com dispositivos portáteis.</span><span class="sxs-lookup"><span data-stu-id="ea6b4-125">Windows Media Player 10 or later uses playlists to synchronize digital media files with portable devices.</span></span> <span data-ttu-id="ea6b4-126">Esta seção explica como trabalhar com listas de reprodução de sincronização.</span><span class="sxs-lookup"><span data-stu-id="ea6b4-126">This section explains how to work with synchronization playlists.</span></span>

<span data-ttu-id="ea6b4-127">O código de exemplo nesta seção usa dois controles ListView para exibir informações.</span><span class="sxs-lookup"><span data-stu-id="ea6b4-127">The example code in this section uses two ListView controls to display information.</span></span> <span data-ttu-id="ea6b4-128">O primeiro controle ListView (IDC \_ PLVIEW) exibe todas as listas de reprodução na biblioteca do Windows Media Player, com as playlists de sincronização exibidas primeiro.</span><span class="sxs-lookup"><span data-stu-id="ea6b4-128">The first ListView control (IDC\_PLVIEW) displays all of the playlists in the Windows Media Player library, with synchronization playlists appearing first.</span></span> <span data-ttu-id="ea6b4-129">As playlists de sincronização para o dispositivo selecionado no momento são marcadas com uma marca de seleção e são classificadas em ordem de prioridade de sincronização.</span><span class="sxs-lookup"><span data-stu-id="ea6b4-129">Synchronization playlists for the currently selected device are marked with a check mark and are sorted in synchronization priority order.</span></span> <span data-ttu-id="ea6b4-130">Todas as outras listas de reprodução estão desmarcadas.</span><span class="sxs-lookup"><span data-stu-id="ea6b4-130">All other playlists are unchecked.</span></span> <span data-ttu-id="ea6b4-131">O controle ListView foi configurado para seleção única.</span><span class="sxs-lookup"><span data-stu-id="ea6b4-131">The ListView control was configured for single selection.</span></span> <span data-ttu-id="ea6b4-132">A ordem das listas de reprodução no controle ListView determina sua prioridade de sincronização.</span><span class="sxs-lookup"><span data-stu-id="ea6b4-132">The order of playlists in the ListView control determines their synchronization priority.</span></span> <span data-ttu-id="ea6b4-133">O estado de verificação de uma lista de reprodução individual determina se é uma lista de reprodução de sincronização para o dispositivo selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="ea6b4-133">The checked state of an individual playlist determines whether it is a synchronization playlist for the currently selected device.</span></span>

<span data-ttu-id="ea6b4-134">O segundo controle ListView (IDC \_ MEDIAVIEW) exibe os itens de mídia na lista de reprodução selecionada.</span><span class="sxs-lookup"><span data-stu-id="ea6b4-134">The second ListView control (IDC\_MEDIAVIEW) displays the media items in the selected playlist.</span></span> <span data-ttu-id="ea6b4-135">Duas colunas adicionais exibem texto indicando se o arquivo de mídia digital foi copiado para o dispositivo e, em caso de falha, se a cópia falhou porque o arquivo de mídia digital não se ajustou.</span><span class="sxs-lookup"><span data-stu-id="ea6b4-135">Two additional columns display text indicating whether the digital media file was copied to the device and, in the case of a failure, whether the copy failed because the digital media file did not fit.</span></span>

<span data-ttu-id="ea6b4-136">O código de exemplo a seguir mostra como os controles ListView são inicializados:</span><span class="sxs-lookup"><span data-stu-id="ea6b4-136">The following example code shows how the ListView controls are initialized:</span></span>


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



<span data-ttu-id="ea6b4-137">A matriz de cadeias de caracteres a seguir contém os nomes dos atributos de sincronização usados nos exemplos:</span><span class="sxs-lookup"><span data-stu-id="ea6b4-137">The following array of strings contains the names of the synchronization attributes used in the examples:</span></span>


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



<span data-ttu-id="ea6b4-138">A variável de membro a seguir contém uma lista de reprodução que contém todas as listas de reprodução na biblioteca do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="ea6b4-138">The following member variable contains a playlist containing all playlists in the Windows Media Player library.</span></span> <span data-ttu-id="ea6b4-139">Cada playlist é representada como um item de mídia.</span><span class="sxs-lookup"><span data-stu-id="ea6b4-139">Each playlist is represented as a media item.</span></span>


```C++
CComPtr<IWMPPlaylist> m_spPlaylist;
```



<span data-ttu-id="ea6b4-140">As seções a seguir fornecem código de exemplo:</span><span class="sxs-lookup"><span data-stu-id="ea6b4-140">The following sections provide example code:</span></span>

-   [<span data-ttu-id="ea6b4-141">Enumerando listas de reprodução de sincronização</span><span class="sxs-lookup"><span data-stu-id="ea6b4-141">Enumerating Synchronization Playlists</span></span>](enumerating-synchronization-playlists.md)
-   [<span data-ttu-id="ea6b4-142">Classificando listas de reprodução por prioridade de sincronização</span><span class="sxs-lookup"><span data-stu-id="ea6b4-142">Sorting Playlists by Synchronization Priority</span></span>](sorting-playlists-by-synchronization-priority.md)
-   [<span data-ttu-id="ea6b4-143">Enumerando os itens de mídia</span><span class="sxs-lookup"><span data-stu-id="ea6b4-143">Enumerating the Media Items</span></span>](enumerating-the-media-items.md)
-   [<span data-ttu-id="ea6b4-144">Determinando o estado de sincronização da playlist</span><span class="sxs-lookup"><span data-stu-id="ea6b4-144">Determining Playlist Synchronization State</span></span>](determining-playlist-synchronization-state.md)
-   [<span data-ttu-id="ea6b4-145">Alterando a prioridade de sincronização</span><span class="sxs-lookup"><span data-stu-id="ea6b4-145">Changing Synchronization Priority</span></span>](changing-synchronization-priority.md)

## <a name="related-topics"></a><span data-ttu-id="ea6b4-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ea6b4-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ea6b4-147">**Trabalhando com dispositivos portáteis**</span><span class="sxs-lookup"><span data-stu-id="ea6b4-147">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




