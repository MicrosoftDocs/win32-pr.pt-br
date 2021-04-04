---
title: Recuperando o status do RIP
description: Recuperando o status do RIP
ms.assetid: 9907bfdd-eae7-4ca2-b488-5a6ad11416f5
keywords:
- Windows Media Player, CD de CDs
- Modelo de objeto do Windows Media Player, cópia de CD
- modelo de objeto, cópia de CD
- Controle ActiveX do Windows Media Player, cópia de CD
- Controle ActiveX, cópia de CD
- Controle ActiveX móvel do Windows Media Player, cópia de CD
- Windows Media Player Mobile, CD-CDs
- CD de CDs, recuperando o status do RIP
- copiando CDs, recuperando o status do RIP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be1fce1a46f9cc2d8477cabcc12a3a1b5bd159d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007152"
---
# <a name="retrieving-the-rip-status"></a><span data-ttu-id="31995-112">Recuperando o status do RIP</span><span class="sxs-lookup"><span data-stu-id="31995-112">Retrieving the Rip Status</span></span>

<span data-ttu-id="31995-113">Você pode monitorar o progresso da operação de cópia de CDs chamando periodicamente [IWMPCdromRip:: get \_ ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress).</span><span class="sxs-lookup"><span data-stu-id="31995-113">You can monitor the progress of the ripping operation by periodically calling [IWMPCdromRip::get\_ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress).</span></span> <span data-ttu-id="31995-114">Esse método recupera um valor de progresso para toda a operação de cópia de CDs.</span><span class="sxs-lookup"><span data-stu-id="31995-114">This method retrieves a progress value for the entire ripping operation.</span></span> <span data-ttu-id="31995-115">O valor recuperado é um número que representa a porcentagem de cópia concluída, de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="31995-115">The value retrieved is a number that represents the percentage of ripping completed, from 0 to 100.</span></span>

<span data-ttu-id="31995-116">O valor de progresso representa a porcentagem completa de todo o processo de cópia de CDs.</span><span class="sxs-lookup"><span data-stu-id="31995-116">The progress value represents the completed percentage of the entire ripping process.</span></span> <span data-ttu-id="31995-117">Para determinar o progresso de uma faixa específica, use [IWMPMedia:: getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo) com "RipProgress" como o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="31995-117">To determine the progress of a specific track, use [IWMPMedia::getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia-getiteminfo) with "RipProgress" as the attribute name.</span></span> <span data-ttu-id="31995-118">Para determinar o índice da faixa que está sendo copiada no momento, chame **IWMPPlaylist:: getItemInfo** com "CurrentRipTrackIndex" como o nome do atributo.</span><span class="sxs-lookup"><span data-stu-id="31995-118">To determine the index of the track currently being ripped, call **IWMPPlaylist::getItemInfo** with "CurrentRipTrackIndex" as the attribute name.</span></span>

<span data-ttu-id="31995-119">Você pode monitorar o estado da operação de cópia de CDs chamando periodicamente [IWMPCdromRip:: get \_ ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate).</span><span class="sxs-lookup"><span data-stu-id="31995-119">You can monitor the state of the ripping operation by periodically calling [IWMPCdromRip::get\_ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate).</span></span> <span data-ttu-id="31995-120">Esse método recupera um valor de enumeração [WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) que indica se a operação está em andamento ou foi interrompida.</span><span class="sxs-lookup"><span data-stu-id="31995-120">This method retrieves a [WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) enumeration value that indicates whether the operation is in progress or stopped.</span></span> <span data-ttu-id="31995-121">Você também pode monitorar o estado da operação de cópia de CDs manipulando o evento [IWMPEvents3:: CdromRipStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) .</span><span class="sxs-lookup"><span data-stu-id="31995-121">You can also monitor the state of the ripping operation by handling the [IWMPEvents3::CdromRipStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) event.</span></span> <span data-ttu-id="31995-122">(Consulte [manipulação de eventos em C++](handling-events-in-c.md).) Tenha cuidado para comparar o ponteiro **IWMPCdromRip** (fornecido pelo evento) com o ponteiro que representa a operação de cópia, a fim de garantir que o evento foi gerado pela operação.</span><span class="sxs-lookup"><span data-stu-id="31995-122">(See [Handling Events in C++](handling-events-in-c.md).) Be careful to compare the **IWMPCdromRip** pointer (provided by the event) to the pointer that represents your ripping operation, to ensure that the event was raised by your operation.</span></span>

<span data-ttu-id="31995-123">O código de exemplo a seguir mostra como usar essas funções para recuperar o status de uma operação de cópia de CDs.</span><span class="sxs-lookup"><span data-stu-id="31995-123">The following example code shows how to use these functions to retrieve the status of a ripping operation.</span></span>

<span data-ttu-id="31995-124">Os seguintes controles de diálogo são definidos para o exemplo de código.</span><span class="sxs-lookup"><span data-stu-id="31995-124">The following dialog controls are defined for the code example.</span></span>



| <span data-ttu-id="31995-125">ID do controle</span><span class="sxs-lookup"><span data-stu-id="31995-125">Control ID</span></span>                   | <span data-ttu-id="31995-126">Description</span><span class="sxs-lookup"><span data-stu-id="31995-126">Description</span></span>                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31995-127">\_faixa atual do IDC \_</span><span class="sxs-lookup"><span data-stu-id="31995-127">IDC\_CURRENT\_TRACK</span></span>          | <span data-ttu-id="31995-128">Texto estático que representa o índice da faixa que está sendo copiada no momento.</span><span class="sxs-lookup"><span data-stu-id="31995-128">Static text that represents the index of the track currently being ripped.</span></span>                                         |
| <span data-ttu-id="31995-129">texto de progresso da IDC \_ Track \_ \_</span><span class="sxs-lookup"><span data-stu-id="31995-129">IDC\_TRACK\_PROGRESS\_TEXT</span></span>   | <span data-ttu-id="31995-130">Texto estático que representa o progresso da faixa atualmente sendo copiada como uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="31995-130">Static text that represents the progress of the track currently being ripped as a percentage.</span></span>                      |
| <span data-ttu-id="31995-131">\_faixa de progresso da IDC \_</span><span class="sxs-lookup"><span data-stu-id="31995-131">IDC\_PROGRESS\_TRACK</span></span>         | <span data-ttu-id="31995-132">Barra de progresso com intervalo de 0 a 100 que representa o progresso da faixa que está sendo copiada no momento como uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="31995-132">Progress bar with range 0 to 100 that represents the progress of the track currently being ripped as a percentage.</span></span> |
| <span data-ttu-id="31995-133">\_texto de \_ progresso \_ geral da IDC</span><span class="sxs-lookup"><span data-stu-id="31995-133">IDC\_OVERALL\_PROGRESS\_TEXT</span></span> | <span data-ttu-id="31995-134">Texto estático que representa o progresso do processo total de cópia de música como uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="31995-134">Static text that represents the progress of the total ripping process as a percentage.</span></span>                             |
| <span data-ttu-id="31995-135">\_progresso \_ geral da IDC</span><span class="sxs-lookup"><span data-stu-id="31995-135">IDC\_PROGRESS\_OVERALL</span></span>       | <span data-ttu-id="31995-136">Barra de progresso com intervalo de 0 a 100 que representa o progresso do processo total de cópia de música como uma porcentagem.</span><span class="sxs-lookup"><span data-stu-id="31995-136">Progress bar with range 0 to 100 that represents the progress of the total ripping process as a percentage.</span></span>        |
| <span data-ttu-id="31995-137">Estado do IDC \_ RIP \_</span><span class="sxs-lookup"><span data-stu-id="31995-137">IDC\_RIP\_STATE</span></span>              | <span data-ttu-id="31995-138">Texto estático que exibe a operação que está sendo executada no momento ("copiando", "parado" ou "desconhecido")</span><span class="sxs-lookup"><span data-stu-id="31995-138">Static text that displays the operation currently being performed ("Ripping", "Stopped", or "Unknown")</span></span>             |



 


```C++
HRESULT CMainDlg::UpdateStatus (void)
{
    // bstrItemName and bstrVal are used for getItemInfo.
    CComBSTR bstrItemName;
    CComBSTR bstrVal;

    // Get the current track index.
    HRESULT hr = bstrItemName.Append("CurrentRipTrackIndex");
    if (SUCCEEDED(hr))
    {
        hr = m_spPlaylist->getItemInfo(bstrItemName, &bstrVal);
    }

    // Update the dialog text with the track number.
    if (SUCCEEDED(hr))
    {
        SetDlgItemTextW(IDC_CURRENT_TRACK, bstrVal.m_str);
    }

    // Get an IWMPMedia interface from the Playlist.
    CComPtr<IWMPMedia> spMedia;
    if (SUCCEEDED(hr))
    {
        long lIndex = _wtol(bstrVal.m_str);
        hr = m_spPlaylist->get_item(lIndex, &spMedia);
    }

    // Update the current track progress bar and progress text.
    if (SUCCEEDED(hr))
    {
        bstrItemName.Empty();
        hr = bstrItemName.Append("RipProgress");
    }
    if (SUCCEEDED(hr))
    {
        hr = spMedia->getItemInfo(bstrItemName, &bstrVal);
    }

    if (SUCCEEDED(hr))
    {
        // Update the text corresponding to the percentage.
        SetDlgItemTextW(IDC_TRACK_PROGRESS_TEXT, bstrVal.m_str);

        // Obtain a numerical value from the progress string.
        long lTrackPosition = _wtol(bstrVal.m_str);

        // Update the progress bar showing the percentage.
        SendMessage(GetDlgItem(IDC_PROGRESS_TRACK),
            PBM_SETPOS, lTrackPosition, 0);
    }

    // Update the total progress bar and progress text.
    long lTotalPosition = 0;
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromRip->get_ripProgress(&lTotalPosition);
    }
    if (SUCCEEDED(hr))
    {
        // Update the text corresponding to the percentage.
        SetDlgItemInt(IDC_OVERALL_PROGRESS_TEXT, lTotalPosition);

        // Update the progress bar showing the percentage.
        SendMessage(GetDlgItem(IDC_PROGRESS_OVERALL),
            PBM_SETPOS, lTotalPosition, 0);
    }

    // Update the ripping state.
    CComBSTR bstrState;
    WMPRipState wmprs = wmprsUnknown;
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromRip->get_ripState(&wmprs);
    }
    if (SUCCEEDED(hr))
    {
        switch (wmprs)
        {
            case wmprsUnknown:
            default:
                hr = bstrState.Append("Unknown");
                break;
            case wmprsRipping:
                hr = bstrState.Append("Ripping");
                break;
            case wmprsStopped:
                hr = bstrState.Append("Stopped");
                break;
        }
    }
    if (SUCCEEDED(hr))
    {
        SetDlgItemTextW(IDC_RIP_STATE, bstrState.m_str);
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="31995-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="31995-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31995-140">**Copiando um CD**</span><span class="sxs-lookup"><span data-stu-id="31995-140">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> <dt>

[<span data-ttu-id="31995-141">**Recuperar a interface de extração**</span><span class="sxs-lookup"><span data-stu-id="31995-141">**Retrieving the Ripping Interface**</span></span>](retrieving-the-ripping-interface.md)
</dt> <dt>

[<span data-ttu-id="31995-142">**Iniciando o processo de RIP**</span><span class="sxs-lookup"><span data-stu-id="31995-142">**Starting the Rip Process**</span></span>](starting-the-rip-process.md)
</dt> <dt>

[<span data-ttu-id="31995-143">**Selecionando itens para copiar**</span><span class="sxs-lookup"><span data-stu-id="31995-143">**Selecting Items for Ripping**</span></span>](selecting-items-for-ripping.md)
</dt> </dl>

 

 




