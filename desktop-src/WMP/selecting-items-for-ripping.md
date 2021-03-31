---
title: Selecionando itens para copiar
description: Selecionando itens para copiar
ms.assetid: 94bc765a-8318-4715-82e0-e7a9b93e99e0
keywords:
- Windows Media Player, CD de CDs
- Modelo de objeto do Windows Media Player, cópia de CD
- modelo de objeto, cópia de CD
- Controle ActiveX do Windows Media Player, cópia de CD
- Controle ActiveX, cópia de CD
- Controle ActiveX móvel do Windows Media Player, cópia de CD
- Windows Media Player Mobile, CD-CDs
- CDs, selecionando itens
- copiando CDs, selecionando itens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc18ded43b609be6c7ac1f16833b0c8a33505ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916405"
---
# <a name="selecting-items-for-ripping"></a><span data-ttu-id="185df-112">Selecionando itens para copiar</span><span class="sxs-lookup"><span data-stu-id="185df-112">Selecting Items for Ripping</span></span>

<span data-ttu-id="185df-113">Às vezes, um usuário não deseja copiar todas as trilhas em um CD.</span><span class="sxs-lookup"><span data-stu-id="185df-113">Sometimes a user does not want to rip every track on a CD.</span></span> <span data-ttu-id="185df-114">O Windows Media Player fornece uma interface para especificar quais faixas estão selecionadas para cópia.</span><span class="sxs-lookup"><span data-stu-id="185df-114">Windows Media Player provides an interface for specifying which tracks are selected for ripping.</span></span> <span data-ttu-id="185df-115">Normalmente, em um aplicativo de cópia de CD, há uma interface do usuário que permite ao usuário selecionar caixas de seleção em uma lista de faixas no CD.</span><span class="sxs-lookup"><span data-stu-id="185df-115">Typically in a CD ripping application there is a user interface that lets the user select check boxes in a list of tracks on the CD.</span></span>

<span data-ttu-id="185df-116">Alguns controles podem não ser selecionados para copiar por padrão.</span><span class="sxs-lookup"><span data-stu-id="185df-116">Some tracks might not be selected for ripping by default.</span></span> <span data-ttu-id="185df-117">Se uma faixa já estiver na biblioteca do Windows Media Player, ela não será selecionada automaticamente para cópia.</span><span class="sxs-lookup"><span data-stu-id="185df-117">If a track is already in the Windows Media Player library, it will not be automatically selected for ripping.</span></span> <span data-ttu-id="185df-118">O segundo exemplo de código nesta seção demonstra como ignorar o valor padrão e selecionar manualmente uma faixa para copiar se já tiver sido copiada.</span><span class="sxs-lookup"><span data-stu-id="185df-118">The second code example in this section demonstrates how to bypass the default value and manually select a track for ripping if it has already been ripped.</span></span>

<span data-ttu-id="185df-119">O exemplo de código a seguir demonstra como determinar se uma faixa está selecionada para cópia:</span><span class="sxs-lookup"><span data-stu-id="185df-119">The following code example demonstrates how to determine whether a track is selected for ripping:</span></span>


```C++
HRESULT CMainDlg::IsTrackSelected(long lIndex, bool &bSelected)
{
    // The track is selected unless the
    // "SelectedForRip" attribute is true.
    bSelected = true;

    // bstrItemName and bstrVal are used for getItemInfo.
    CComBSTR bstrItemName;
    CComBSTR bstrVal;

    // Get an IWMPMedia from the Playlist.
    CComPtr<IWMPMedia> spMedia;
    HRESULT hr = m_spPlaylist->get_item(lIndex, &spMedia);

    // Check whether it is selected for ripping.
    if (SUCCEEDED(hr))
    {
        hr = bstrItemName.Append("SelectedForRip");
    }
    if (SUCCEEDED(hr))
    {
        hr = spMedia->getItemInfo(
            bstrItemName,
            &bstrVal);
    }
    if (SUCCEEDED(hr))
    {
        // If getItemInfo("SelectedForRip") is not "True"
        // then the track is not selected.
        if (wcscmp(bstrVal.m_str, L"True"))
            bSelected = false;
    }

    return hr;
}

```



<span data-ttu-id="185df-120">O exemplo de código a seguir demonstra como especificar se uma faixa está selecionada para cópia.</span><span class="sxs-lookup"><span data-stu-id="185df-120">The following code example demonstrates how to specify whether a track is selected for ripping.</span></span>


```C++
HRESULT CMainDlg::SelectTrack (long lIndex, bool bSelected)
{
    // bstrItemName and bstrVal are used for setItemInfo.
    CComBSTR bstrItemName;
    CComBSTR bstrVal;

    // Get an IWMPMedia from the Playlist.
    CComPtr<IWMPMedia> spMedia;
    HRESULT hr = m_spPlaylist->get_item(lIndex, &spMedia);

    // Select the track for ripping.
    if (SUCCEEDED(hr))
    {
        hr = bstrItemName.Append("SelectedForRip");
    }
    if (SUCCEEDED(hr))
    {
        if (bSelected)
        {
            hr = bstrVal.Append("True");
        }
        else
        {
            hr = bstrVal.Append("False");
        }
    }
    if (SUCCEEDED(hr))
    {
        hr = spMedia->setItemInfo(
            bstrItemName,
            bstrVal);
    }

    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="185df-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="185df-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="185df-122">**Copiando um CD**</span><span class="sxs-lookup"><span data-stu-id="185df-122">**Ripping a CD**</span></span>](ripping-a-cd.md)
</dt> <dt>

[<span data-ttu-id="185df-123">**Recuperar a interface de extração**</span><span class="sxs-lookup"><span data-stu-id="185df-123">**Retrieving the Ripping Interface**</span></span>](retrieving-the-ripping-interface.md)
</dt> <dt>

[<span data-ttu-id="185df-124">**Iniciando o processo de RIP**</span><span class="sxs-lookup"><span data-stu-id="185df-124">**Starting the Rip Process**</span></span>](starting-the-rip-process.md)
</dt> <dt>

[<span data-ttu-id="185df-125">**Recuperando o status do RIP**</span><span class="sxs-lookup"><span data-stu-id="185df-125">**Retrieving the Rip Status**</span></span>](retrieving-the-rip-status.md)
</dt> </dl>

 

 




