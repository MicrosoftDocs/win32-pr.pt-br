---
title: Determinando o estado de sincronização da playlist
description: Determinando o estado de sincronização da playlist
ms.assetid: 634b659b-c3ae-4957-b17e-18fd92e915be
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
- dispositivos portáteis, determinando o estado da playlist de sincronização
- listas de reprodução de sincronização, estado de sincronização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9758cfbb73c698a40d6d4f48e645e57750d8a332
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105758225"
---
# <a name="determining-playlist-synchronization-state"></a><span data-ttu-id="8689b-115">Determinando o estado de sincronização da playlist</span><span class="sxs-lookup"><span data-stu-id="8689b-115">Determining Playlist Synchronization State</span></span>

<span data-ttu-id="8689b-116">O Windows Media Player 10 ou posterior usa o atributo **SyncState** para conter informações sobre se um arquivo de mídia digital específico foi copiado para um dispositivo portátil e, no caso de uma falha, se a cópia falhou porque o dispositivo não tinha memória suficiente.</span><span class="sxs-lookup"><span data-stu-id="8689b-116">Windows Media Player 10 or later uses the **SyncState** attribute to contain information about whether a particular digital media file has been copied to a portable device and, in the case of a failure, whether copying failed because the device did not have enough memory.</span></span>

<span data-ttu-id="8689b-117">O código de exemplo a seguir cria uma função que recupera essas informações de um arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="8689b-117">The following example code creates a function that retrieves this information from a digital media file.</span></span> <span data-ttu-id="8689b-118">A função usa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="8689b-118">The function takes the following parameters:</span></span>

-   <span data-ttu-id="8689b-119">*pMedia*.</span><span class="sxs-lookup"><span data-stu-id="8689b-119">*pMedia*.</span></span> <span data-ttu-id="8689b-120">Ponteiro para uma interface **IWMPMedia** que representa o arquivo de mídia digital a ser inspecionado.</span><span class="sxs-lookup"><span data-stu-id="8689b-120">Pointer to an **IWMPMedia** interface that represents the digital media file to inspect.</span></span>
-   <span data-ttu-id="8689b-121">*lPsIndex*.</span><span class="sxs-lookup"><span data-stu-id="8689b-121">*lPsIndex*.</span></span> <span data-ttu-id="8689b-122">Índice de parceria do dispositivo atual.</span><span class="sxs-lookup"><span data-stu-id="8689b-122">Partnership index of the current device.</span></span>
-   <span data-ttu-id="8689b-123">*pulOnDevice*.</span><span class="sxs-lookup"><span data-stu-id="8689b-123">*pulOnDevice*.</span></span> <span data-ttu-id="8689b-124">Ponteiro para uma variável **longa** que recebe o valor indicando se o arquivo de mídia digital foi copiado para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8689b-124">Pointer to a **long** variable that receives the value indicating whether the digital media file has been copied to the device.</span></span>
-   <span data-ttu-id="8689b-125">*pulDidNotFit*.</span><span class="sxs-lookup"><span data-stu-id="8689b-125">*pulDidNotFit*.</span></span> <span data-ttu-id="8689b-126">Ponteiro para uma variável **longa** que recebe o valor indicando se a operação de cópia falhou porque o dispositivo não tinha memória suficiente.</span><span class="sxs-lookup"><span data-stu-id="8689b-126">Pointer to a **long** variable that receives the value indicating whether the copy operation failed because the device did not have enough memory.</span></span>

<span data-ttu-id="8689b-127">As informações contidas no atributo **SyncState** são codificadas de forma unificada.</span><span class="sxs-lookup"><span data-stu-id="8689b-127">The information contained in the **SyncState** attribute is encoded in a bitwise fashion.</span></span> <span data-ttu-id="8689b-128">Você pode ver como essa função é usada no código de exemplo para [enumerar os itens de mídia](enumerating-the-media-items.md).</span><span class="sxs-lookup"><span data-stu-id="8689b-128">You can see how this function is used in the example code in [Enumerating the Media Items](enumerating-the-media-items.md).</span></span>


```C++
STDMETHODIMP CSyncSettings::GetPartnershipSyncState(IWMPMedia* pMedia, long lPsIndex, ULONG *pulOnDevice, ULONG *pulDidNotFit)
{
    ATLASSERT(pMedia); 
    ATLASSERT(lPsIndex > 0 && 
              lPsIndex < 17);
    ATLASSERT(pulOnDevice);
    ATLASSERT(pulDidNotFit);
  
    CComVariant varSyncStateVal;   
    CComPtr<IWMPMedia> spMedia(pMedia); 
    CComPtr<IWMPMedia3> spMedia3;     
    HRESULT hr = spMedia.QueryInterface(&spMedia3); 
    ULONG ulSyncState = 0; // Stores the ulVal member of varSyncStateVal. 
    ULONG lLSB = 0; // Represents least significant bit: Did the media fail to copy because it would not fit?
    ULONG lMSB = 0; // Represents most significant bit: Is the media on the device?

    // Calculate the bit shift required to isolate the partnership bit 
    // pair from the SyncState attribute.
    const int iRshift = (lPsIndex - 1) * 2;

    if(SUCCEEDED(hr) && spMedia3)
    {       
        hr = spMedia3->getItemInfoByType(CComBSTR("SyncState"), CComBSTR(""), 0, &varSyncStateVal);
    }

    if(SUCCEEDED(hr) && varSyncStateVal.vt == VT_UI4)
    {   
        // Get the value.
        ulSyncState = varSyncStateVal.ulVal;

        // Shift the bit pair to the rightmost position.
        ulSyncState >>= iRshift; 

        // Mask the rightmost bit pair.
        ulSyncState &= 3;

        // Get the LSB         
        lLSB = ulSyncState & ~2; // Sets the 2E1 bit to zero. 

        // Get the MSB
        ulSyncState >>= 1;
        lMSB = ulSyncState;       
    }

    // Return the bits.
    *pulOnDevice = lMSB;
    *pulDidNotFit = lLSB;

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="8689b-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8689b-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8689b-130">**Interface IWMPMedia**</span><span class="sxs-lookup"><span data-stu-id="8689b-130">**IWMPMedia Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[<span data-ttu-id="8689b-131">**IWMPMedia3::getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="8689b-131">**IWMPMedia3::getItemInfoByType**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmedia3-getiteminfobytype)
</dt> <dt>

[<span data-ttu-id="8689b-132">**Gerenciando listas de reprodução de sincronização**</span><span class="sxs-lookup"><span data-stu-id="8689b-132">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> <dt>

[<span data-ttu-id="8689b-133">**Atributo SyncState**</span><span class="sxs-lookup"><span data-stu-id="8689b-133">**SyncState Attribute**</span></span>](syncstate-attribute.md)
</dt> </dl>

 

 




