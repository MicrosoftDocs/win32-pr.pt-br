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
# <a name="selecting-items-for-ripping"></a>Selecionando itens para copiar

Às vezes, um usuário não deseja copiar todas as trilhas em um CD. O Windows Media Player fornece uma interface para especificar quais faixas estão selecionadas para cópia. Normalmente, em um aplicativo de cópia de CD, há uma interface do usuário que permite ao usuário selecionar caixas de seleção em uma lista de faixas no CD.

Alguns controles podem não ser selecionados para copiar por padrão. Se uma faixa já estiver na biblioteca do Windows Media Player, ela não será selecionada automaticamente para cópia. O segundo exemplo de código nesta seção demonstra como ignorar o valor padrão e selecionar manualmente uma faixa para copiar se já tiver sido copiada.

O exemplo de código a seguir demonstra como determinar se uma faixa está selecionada para cópia:


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



O exemplo de código a seguir demonstra como especificar se uma faixa está selecionada para cópia.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Copiando um CD**](ripping-a-cd.md)
</dt> <dt>

[**Recuperar a interface de extração**](retrieving-the-ripping-interface.md)
</dt> <dt>

[**Iniciando o processo de RIP**](starting-the-rip-process.md)
</dt> <dt>

[**Recuperando o status do RIP**](retrieving-the-rip-status.md)
</dt> </dl>

 

 




