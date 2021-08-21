---
title: O método OnSearch
description: O método OnSearch
ms.assetid: 709bb428-1a5e-4b8d-8622-5fcc816f0a1a
keywords:
- Windows Media Player plug-ins, método OnSearch
- plug-ins, método OnSearch
- plug-ins de interface do usuário, método OnSearch
- Plug-ins de interface do usuário, método OnSearch
- Método OnSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ab5cb4b26d291a940ed329e2422240e6fc36e5ba980431af169d58f1398fdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117996"
---
# <a name="the-onsearch-method"></a>O método OnSearch

O método OnSearch é chamado por Windows Media Player quando **o botão** Pesquisar é clicado. Esse método recupera o objeto **media atual** e o passa para o método LaunchPage.

O código a seguir é usado para implementar esse método:


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Implementando CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




