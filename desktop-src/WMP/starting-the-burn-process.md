---
title: Iniciando o processo de gravação
description: Iniciando o processo de gravação
ms.assetid: 91442bd2-1a68-465c-b865-63d309f33d55
keywords:
- Windows Media Player, gravação de CD
- Modelo de objeto do Windows Media Player, gravação de CD
- modelo de objeto, gravação de CD
- Controle ActiveX do Windows Media Player, gravação de CD
- Controle ActiveX, gravação de CD
- Controle ActiveX móvel do Windows Media Player, gravação de CD
- Windows Media Player Mobile, gravação de CD
- Gravação de CD, iniciando processo de gravação
- gravando CDs, iniciando o processo de gravação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a35f473eebe35bffd48ac802dcfe79082689de
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103917004"
---
# <a name="starting-the-burn-process"></a>Iniciando o processo de gravação

Antes que a gravação possa começar, você deve atribuir uma lista de reprodução a ser gravada. Use [IWMPCdromBurn::p UT \_ burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) para especificar uma lista de reprodução para gravação.


```C++
HRESULT CMainDlg::PutPlaylist (void)
{
    // Specify the burn playlist.   
    HRESULT hr = m_spCdromBurn->put_burnPlaylist(m_spPlaylist);

    // Update the status information.
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromBurn->refreshStatus();
    }

    return hr;
}

```



Para obter informações sobre como usar listas de reprodução, consulte [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist).

Para iniciar a operação de gravação, chame [IWMPCdromBurn:: startBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn).


```C++
// Start burning.
hr = m_spCdromBurn->startBurn();

```



Você pode interromper a operação de gravação chamando [IWMPCdromBurn:: stopBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn).


```C++
// Stop burning.
hr = m_spCdromBurn->stopBurn();

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Gravando um CD**](burning-a-cd.md)
</dt> <dt>

[**Recuperar a interface de gravação de CD**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**Apagando um CD regravável**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Recuperando a unidade e o status do disco**](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[**Recuperando o status da gravação**](retrieving-the-burn-status.md)
</dt> </dl>

 

 




