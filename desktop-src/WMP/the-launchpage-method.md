---
title: O método LaunchPage
description: O método LaunchPage
ms.assetid: f0f93535-5afc-4777-9188-5bbac63ddc6b
keywords:
- plug-ins Windows Media Player, método LaunchPage
- plug-ins, método LaunchPage
- plug-ins de interface do usuário, método LaunchPage
- Plug-ins de interface do usuário, método LaunchPage
- Método LaunchPage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11a22e1f4b136711a6f4336fbe54d6d90e4bb18b24a88645587311a0b4046f6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762716"
---
# <a name="the-launchpage-method"></a>O método LaunchPage

O método LaunchPage fornece a principal funcionalidade do plug-in, que é para iniciar uma página de pesquisa que contém informações sobre o artista do item de mídia passado para o método.

Esse método é chamado pelo método onsearch usando o objeto de **mídia** atual.

O código a seguir é usado para implementar esse método:


```C++
void LaunchPage(IWMPMedia *pMedia)
{
    USES_CONVERSION;

    HRESULT hr;
    CComBSTR bstrType;
    CComBSTR bstrArtist;

    // Get the name of the artist.
    bstrType = _T("artist");
    hr = pMedia->getItemInfo(bstrType, &bstrArtist);
    if (SUCCEEDED(hr)) 
    {
        // Create the search URL.
        TCHAR szSearch[MAX_PATH];
        _stprintf_s(szSearch, MAX_PATH, _T("https://search.msn.com/results.asp?q=%s"), OLE2T(bstrArtist));
        CComBSTR bstrURL = szSearch;

        // Launch the search page.
        m_pPlugin->m_spCore->launchURL(bstrURL);
    }
    else
    {
        MessageBox(_T("Failed to get artist information from media."), _T("Warn"), MB_OK | MB_ICONWARNING);
    }
}

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




