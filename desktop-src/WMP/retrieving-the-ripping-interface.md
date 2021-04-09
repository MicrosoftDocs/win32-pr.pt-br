---
title: Recuperar a interface de extração
description: Recuperar a interface de extração
ms.assetid: 760610eb-e356-4b50-b865-53557ba9b815
keywords:
- Windows Media Player, CD de CDs
- Modelo de objeto do Windows Media Player, cópia de CD
- modelo de objeto, cópia de CD
- Controle ActiveX do Windows Media Player, cópia de CD
- Controle ActiveX, cópia de CD
- Controle ActiveX móvel do Windows Media Player, cópia de CD
- Windows Media Player Mobile, CD-CDs
- CD de CDs, interface IWMPCdromRip
- copiando CDs, interface IWMPCdromRip
- Interface IWMPCdromRip
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 903fa285404700e35363a94239c79706e7af0e34
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103823599"
---
# <a name="retrieving-the-ripping-interface"></a>Recuperar a interface de extração

Para enumerar as unidades de CD no computador do usuário, use a interface **IWMPCdromCollection** . Recupere um ponteiro para essa interface chamando [IWMPCore:: get \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).

Usando os métodos [de \_ contagem](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-get_count) e [Item](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromcollection-item) de Get, você pode iterar a coleção para recuperar uma interface [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) para cada unidade de CD no computador do usuário.

A interface **IWMPCdrom** representa uma unidade de CD individual. Antes de começar a copiar um CD, você deve primeiro chamar **QueryInterface** por meio de um ponteiro **IWMPCdrom** para recuperar a interface [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip) .

O exemplo de código a seguir demonstra como recuperar uma interface para copiar um CD de uma unidade específica:


```C++
HRESULT CMainDlg::GetCdromDriveCount (long &lDriveCount)
{
    HRESULT hr = m_spPlayer->get_cdromCollection(&m_spCdromCollection);

    // Get the number of CDROM drives.
    if (SUCCEEDED(hr))
    {
        hr = m_spCdromCollection->get_count(&lDriveCount);
    }

    return hr;
}

// lIndex refers to the index of the current drive,
// which must be less than the value retrieved by
// GetCdromDriveCount above.
HRESULT CMainDlg::GetCdromRipInterface (long lIndex)
{
    // Get the IWMPCdrom interface.
    m_spCdrom.Release();
    HRESULT hr = m_spCdromCollection->item(lIndex, &m_spCdrom);
    if (SUCCEEDED(hr))
    {
        // Get the IWMPCdromRip interface.
        m_spCdromRip.Release();
        hr = m_spCdrom->QueryInterface(&m_spCdromRip);
    }

    return hr;
}

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Copiando um CD**](ripping-a-cd.md)
</dt> <dt>

[**Iniciando o processo de RIP**](starting-the-rip-process.md)
</dt> <dt>

[**Recuperando o status do RIP**](retrieving-the-rip-status.md)
</dt> <dt>

[**Selecionando itens para copiar**](selecting-items-for-ripping.md)
</dt> <dt>

[**Interface IWMPCdromCollection**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




