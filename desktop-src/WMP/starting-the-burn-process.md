---
title: Iniciando o processo de burn
description: Iniciando o processo de burn
ms.assetid: 91442bd2-1a68-465c-b865-63d309f33d55
keywords:
- Windows Media Player, gravação de CD
- Windows Media Player modelo de objeto, gravação de CD
- modelo de objeto, gravação de CD
- Windows Media Player ActiveX controle, gravação de CD
- ActiveX controle, gravação de CD
- Windows Media Player Controle ActiveX dispositivo móvel, gravação de CD
- Windows Media Player Móvel, gravação de CD
- Gravação de CD, iniciando o processo de gravação
- CDs de gravação, iniciando o processo de gravação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50f5620ba8fa6ab911cf0fd594fd27f139b5061d1383575f861dadfec45dabbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995076"
---
# <a name="starting-the-burn-process"></a>Iniciando o processo de burn

Antes que a gravação possa começar, você deve atribuir uma playlist para ser desarmada. Use [IWMPCdrom Ltd::p ut \_ burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) para especificar uma playlist para gravação.


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



Para obter informações sobre como usar playlists, consulte [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist).

Para iniciar a operação de gravação, chame [IWMPCdrom Ltd::startEar.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn)


```C++
// Start burning.
hr = m_spCdromBurn->startBurn();

```



Você pode interromper a operação de gravação chamando [IWMPCdrom Ltd::stopEar.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn)


```C++
// Stop burning.
hr = m_spCdromBurn->stopBurn();

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Gravar um CD**](burning-a-cd.md)
</dt> <dt>

[**Recuperar a interface de gravação de CD**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**Apagando um CD reeritável**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Recuperando o status da unidade e do disco**](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[**Recuperando o status de burn**](retrieving-the-burn-status.md)
</dt> </dl>

 

 




