---
title: Recuperando o status da gravação
description: Recuperando o status da gravação
ms.assetid: 63b6525d-00be-4c68-8473-3bc1a58fde15
keywords:
- Windows Media Player, gravação de CD
- Modelo de objeto do Windows Media Player, gravação de CD
- modelo de objeto, gravação de CD
- Controle ActiveX do Windows Media Player, gravação de CD
- Controle ActiveX, gravação de CD
- Controle ActiveX móvel do Windows Media Player, gravação de CD
- Windows Media Player Mobile, gravação de CD
- Gravação de CD, recuperando status de gravação
- gravando CDs, recuperando o status da gravação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e9b9ab1d865b728c3a23b9b77f45ab022226605
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103917007"
---
# <a name="retrieving-the-burn-status"></a><span data-ttu-id="5bd39-112">Recuperando o status da gravação</span><span class="sxs-lookup"><span data-stu-id="5bd39-112">Retrieving the Burn Status</span></span>

<span data-ttu-id="5bd39-113">No exemplo de código a seguir, os seguintes controles de diálogo são definidos:</span><span class="sxs-lookup"><span data-stu-id="5bd39-113">In the code example that follows, the following dialog controls are defined:</span></span>



| <span data-ttu-id="5bd39-114">ID do controle</span><span class="sxs-lookup"><span data-stu-id="5bd39-114">Control ID</span></span>           | <span data-ttu-id="5bd39-115">Description</span><span class="sxs-lookup"><span data-stu-id="5bd39-115">Description</span></span>                                                                    |
|----------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="5bd39-116">\_estado de gravação do IDC \_</span><span class="sxs-lookup"><span data-stu-id="5bd39-116">IDC\_BURN\_STATE</span></span>     | <span data-ttu-id="5bd39-117">Texto estático que representa o estado da operação de gravação de CD.</span><span class="sxs-lookup"><span data-stu-id="5bd39-117">Static text that represents the state of the CD burning operation.</span></span>             |
| <span data-ttu-id="5bd39-118">progresso da IDC \_</span><span class="sxs-lookup"><span data-stu-id="5bd39-118">IDC\_PROGRESS</span></span>        | <span data-ttu-id="5bd39-119">Barra de progresso com um intervalo de 0 a 100 que representa o progresso total de gravação.</span><span class="sxs-lookup"><span data-stu-id="5bd39-119">Progress bar with a range of 0 to 100 that represents the total burn progress.</span></span> |
| <span data-ttu-id="5bd39-120">\_texto de progresso da IDC \_</span><span class="sxs-lookup"><span data-stu-id="5bd39-120">IDC\_PROGRESS\_TEXT</span></span>  | <span data-ttu-id="5bd39-121">Texto estático que representa o progresso total da gravação como um número de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="5bd39-121">Static text that represents the total burn progress as a number from 0 to 100.</span></span> |
| <span data-ttu-id="5bd39-122">\_hora disponível do IDC \_</span><span class="sxs-lookup"><span data-stu-id="5bd39-122">IDC\_AVAILABLE\_TIME</span></span> | <span data-ttu-id="5bd39-123">Texto estático para exibir o tempo disponível no CD, em segundos.</span><span class="sxs-lookup"><span data-stu-id="5bd39-123">Static text to display the time available on the CD, in seconds.</span></span>               |
| <span data-ttu-id="5bd39-124">\_espaço livre da IDC \_</span><span class="sxs-lookup"><span data-stu-id="5bd39-124">IDC\_FREE\_SPACE</span></span>     | <span data-ttu-id="5bd39-125">Texto estático para exibir o espaço livre no CD, em bytes.</span><span class="sxs-lookup"><span data-stu-id="5bd39-125">Static text to display the free space on the CD, in bytes.</span></span>                     |
| <span data-ttu-id="5bd39-126">\_espaço total da IDC \_</span><span class="sxs-lookup"><span data-stu-id="5bd39-126">IDC\_TOTAL\_SPACE</span></span>    | <span data-ttu-id="5bd39-127">Texto estático para exibir a capacidade total do CD, em bytes.</span><span class="sxs-lookup"><span data-stu-id="5bd39-127">Static text to display the total capacity of the CD, in bytes.</span></span>                 |



 

<span data-ttu-id="5bd39-128">Você pode monitorar o progresso da operação de gravação chamando periodicamente [IWMPCdromBurn:: get \_ burnProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress) enquanto o CD está sendo gravado.</span><span class="sxs-lookup"><span data-stu-id="5bd39-128">You can monitor the progress of the burning operation by periodically calling [IWMPCdromBurn::get\_burnProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress) while the CD is being burned.</span></span> <span data-ttu-id="5bd39-129">Esse método recupera um valor de progresso para toda a operação de gravação.</span><span class="sxs-lookup"><span data-stu-id="5bd39-129">This method retrieves a progress value for the entire burning operation.</span></span> <span data-ttu-id="5bd39-130">O valor recuperado é um número que representa a porcentagem de gravação concluída, de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="5bd39-130">The value retrieved is a number that represents the percentage of burning completed, from 0 to 100.</span></span>


```C++
// Update the progress bar IDC_PROGRESS
// and the corresponding text string IDC_PROGRESS_TEXT.
long lProgress = 0;
hr = m_spCdromBurn->get_burnProgress(&lProgress);
if (SUCCEEDED(hr))
{
    SendMessage(GetDlgItem(IDC_PROGRESS),
        PBM_SETPOS, lProgress, 0);
    SetDlgItemInt(IDC_PROGRESS_TEXT, lProgress);
}

```



<span data-ttu-id="5bd39-131">Você pode obter o estado atual da operação de gravação chamando [IWMPCdromBurn:: get \_ gravástate](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnstate).</span><span class="sxs-lookup"><span data-stu-id="5bd39-131">You can get the current state of the burning operation by calling [IWMPCdromBurn::get\_burnState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnstate).</span></span> <span data-ttu-id="5bd39-132">Esse método recupera uma enumeração que especifica a operação atual que está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="5bd39-132">This method retrieves an enumeration specifying the current operation being performed.</span></span>


```C++
// Retrieve the burn state.
WMPBurnState wmpbs = wmpbsUnknown;
HRESULT hr = m_spCdromBurn->get_burnState(&wmpbs);

if (SUCCEEDED(hr))
{
    // Set the burn state string.
    CComBSTR bstrState;
    switch (wmpbs)
    {
        case wmpbsUnknown:
        default:
            hr = bstrState.Append("Unknown state.");
            break;
        case wmpbsBusy:
            hr = bstrState.Append("Windows Media Player is Busy.");
            break;
        case wmpbsReady:
            hr = bstrState.Append("Ready to begin burning.");
            break;
        case wmpbsWaitingForDisc:
            hr = bstrState.Append("Waiting for disc.");
            break;
        case wmpbsRefreshStatusPending:
            hr = bstrState.Append("The burn playlist has changed.");
            m_spCdromBurn->refreshStatus();
            break;
        case wmpbsPreparingToBurn:
            hr = bstrState.Append("Preparing to burn the CD.");
            break;
        case wmpbsBurning:
            hr = bstrState.Append("The CD is being burned.");
            break;
        case wmpbsStopped:
            hr = bstrState.Append("The burning operation is stopped.");
            break;
        case wmpbsErasing:
            hr = bstrState.Append("Erasing the CD.");
            break;
    }
    if (SUCCEEDED(hr))
    {
        SetDlgItemTextW(IDC_BURN_STATE, bstrState.m_str);
    }
}

```



<span data-ttu-id="5bd39-133">Para recuperar o número de segundos de áudio que o CD pode conter, chame [IWMPCdromBurn:: getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-getiteminfo) com "availabletime" como o primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5bd39-133">To retrieve the number of seconds of audio the CD can hold, call [IWMPCdromBurn::getItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-getiteminfo) with "AvailableTime" as the first parameter.</span></span> <span data-ttu-id="5bd39-134">O valor recuperado por essa função é representado por uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5bd39-134">The value retrieved by this function is represented by a string.</span></span>


```C++
// Set "AvailableTime" string
CComBSTR bstrTime;
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("AvailableTime");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->getItemInfo(bstrItem, &bstrTime);
}
if (SUCCEEDED(hr))
{
    hr = bstrTime.Append(" seconds");
}
if (SUCCEEDED(hr))
{
    SetDlgItemTextW(IDC_AVAILABLE_TIME, bstrTime.m_str);
}

```



<span data-ttu-id="5bd39-135">Para recuperar a quantidade de espaço livre em um disco, chame **IWMPCdromBurn:: getItemInfo** com "Freespace" como o primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5bd39-135">To retrieve the amount of free space on a disc, call **IWMPCdromBurn::getItemInfo** with "FreeSpace" as the first parameter.</span></span> <span data-ttu-id="5bd39-136">O valor recuperado por essa função é uma cadeia de caracteres que representa o número de bytes livres disponíveis no disco.</span><span class="sxs-lookup"><span data-stu-id="5bd39-136">The value retrieved by this function is a string that represents the number of free bytes available on the disc.</span></span>


```C++
// Set "FreeSpace" string
CComBSTR bstrFreeSpace;
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("FreeSpace");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->getItemInfo(bstrItem, &bstrFreeSpace);
}
if (SUCCEEDED(hr))
{
    hr = bstrFreeSpace.Append(" bytes");
}
if (SUCCEEDED(hr))
{
    SetDlgItemTextW(IDC_FREE_SPACE, bstrFreeSpace.m_str);
}

```



<span data-ttu-id="5bd39-137">Para recuperar a capacidade total de um disco, chame **IWMPCdromBurn:: getItemInfo** com "TotalSpace" como o primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5bd39-137">To retrieve the total capacity of a disc, call **IWMPCdromBurn::getItemInfo** with "TotalSpace" as the first parameter.</span></span> <span data-ttu-id="5bd39-138">O valor recuperado por essa função é uma cadeia de caracteres que corresponde ao número total de bytes no disco.</span><span class="sxs-lookup"><span data-stu-id="5bd39-138">The value retrieved by this function is a string that corresponds to the total number of bytes on the disc.</span></span>


```C++
// Set "TotalSpace" string.
CComBSTR bstrTotalSpace;
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("TotalSpace");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->getItemInfo(bstrItem, &bstrTotalSpace);
}
if (SUCCEEDED(hr))
{
    hr = bstrTotalSpace.Append(" bytes");
}
if (SUCCEEDED(hr))
{
    SetDlgItemTextW(IDC_TOTAL_SPACE, bstrTotalSpace.m_str);
}

```



## <a name="related-topics"></a><span data-ttu-id="5bd39-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5bd39-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bd39-140">**Gravando um CD**</span><span class="sxs-lookup"><span data-stu-id="5bd39-140">**Burning a CD**</span></span>](burning-a-cd.md)
</dt> <dt>

[<span data-ttu-id="5bd39-141">**Recuperar a interface de gravação de CD**</span><span class="sxs-lookup"><span data-stu-id="5bd39-141">**Retrieving the CD Burning Interface**</span></span>](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[<span data-ttu-id="5bd39-142">**Iniciando o processo de gravação**</span><span class="sxs-lookup"><span data-stu-id="5bd39-142">**Starting the Burn Process**</span></span>](starting-the-burn-process.md)
</dt> <dt>

[<span data-ttu-id="5bd39-143">**Apagando um CD regravável**</span><span class="sxs-lookup"><span data-stu-id="5bd39-143">**Erasing a Rewritable CD**</span></span>](erasing-a-rewritable-cd.md)
</dt> <dt>

[<span data-ttu-id="5bd39-144">**Recuperando a unidade e o status do disco**</span><span class="sxs-lookup"><span data-stu-id="5bd39-144">**Retrieving the Drive and Disc Status**</span></span>](retrieving-the-drive-and-disc-status.md)
</dt> </dl>

 

 




