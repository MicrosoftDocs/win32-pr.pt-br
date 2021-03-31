---
title: O método onsearch
description: O método onsearch
ms.assetid: 709bb428-1a5e-4b8d-8622-5fcc816f0a1a
keywords:
- Plug-ins do Windows Media Player, método onsearch
- plug-ins, método onsearch
- plug-ins de interface do usuário, método onsearch
- Plug-ins de interface do usuário, método onsearch
- Método onsearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de5c33af434028e6ee72c757c8d71def0d4109fd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005627"
---
# <a name="the-onsearch-method"></a><span data-ttu-id="e54e9-108">O método onsearch</span><span class="sxs-lookup"><span data-stu-id="e54e9-108">The OnSearch Method</span></span>

<span data-ttu-id="e54e9-109">O método onsearch é chamado pelo Windows Media Player quando o botão **Pesquisar** é clicado.</span><span class="sxs-lookup"><span data-stu-id="e54e9-109">The OnSearch method is called by Windows Media Player when the **Search** button is clicked.</span></span> <span data-ttu-id="e54e9-110">Esse método recupera o objeto de **mídia** atual e o passa para o método LaunchPage.</span><span class="sxs-lookup"><span data-stu-id="e54e9-110">This method retrieves the current **Media** object and passes it to the LaunchPage method.</span></span>

<span data-ttu-id="e54e9-111">O código a seguir é usado para implementar esse método:</span><span class="sxs-lookup"><span data-stu-id="e54e9-111">The following code is used to implement this method:</span></span>


```C++
LRESULT OnSearch(WORD wNotifyCode, WORD wID, HWND hwndCtl, BOOL& fHandled)
{
    HRESULT hr;
    CComPtr<IWMPMedia> spMedia;

    if( m_pPlugin && m_pPlugin->m_spCore )
    {
        // Get a pointer to the current media item.
        hr = m_pPlugin->m_spCore->get_currentMedia(&spMedia);
        if (SUCCEEDED(hr) && spMedia)
        {
            LaunchPage(spMedia);
        }
    else
        {
            MessageBox(_T("There is no media loaded."), _T("Warn"), MB_OK | MB_ICONWARNING);
        }
    }
    return 0;
}

```



## <a name="related-topics"></a><span data-ttu-id="e54e9-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e54e9-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e54e9-113">**Implementando CPluginWindow**</span><span class="sxs-lookup"><span data-stu-id="e54e9-113">**Implementing CPluginWindow**</span></span>](implementing-cpluginwindow.md)
</dt> </dl>

 

 




