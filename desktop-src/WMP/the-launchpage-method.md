---
title: O método LaunchPage
description: O método LaunchPage
ms.assetid: f0f93535-5afc-4777-9188-5bbac63ddc6b
keywords:
- Plug-ins do Windows Media Player, método LaunchPage
- plug-ins, método LaunchPage
- plug-ins de interface do usuário, método LaunchPage
- Plug-ins de interface do usuário, método LaunchPage
- Método LaunchPage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f04974eba1ba5c86300de44acd2ba6e2920954f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005729"
---
# <a name="the-launchpage-method"></a><span data-ttu-id="72a65-108">O método LaunchPage</span><span class="sxs-lookup"><span data-stu-id="72a65-108">The LaunchPage Method</span></span>

<span data-ttu-id="72a65-109">O método LaunchPage fornece a principal funcionalidade do plug-in, que é para iniciar uma página de pesquisa que contém informações sobre o artista do item de mídia passado para o método.</span><span class="sxs-lookup"><span data-stu-id="72a65-109">The LaunchPage method provides the primary functionality of the plug-in, which is to launch a search page containing information about the artist of the media item passed to the method.</span></span>

<span data-ttu-id="72a65-110">Esse método é chamado pelo método onsearch usando o objeto de **mídia** atual.</span><span class="sxs-lookup"><span data-stu-id="72a65-110">This method is called by the OnSearch method using the current **Media** object.</span></span>

<span data-ttu-id="72a65-111">O código a seguir é usado para implementar esse método:</span><span class="sxs-lookup"><span data-stu-id="72a65-111">The following code is used to implement this method:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="72a65-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="72a65-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72a65-113">**Implementando CPluginWindow**</span><span class="sxs-lookup"><span data-stu-id="72a65-113">**Implementing CPluginWindow**</span></span>](implementing-cpluginwindow.md)
</dt> </dl>

 

 




