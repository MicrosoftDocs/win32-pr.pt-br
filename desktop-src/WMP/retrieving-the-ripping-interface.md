---
title: Recuperar a interface de extração
description: Recuperar a interface de extração
ms.assetid: 760610eb-e356-4b50-b865-53557ba9b815
keywords:
- Windows Media Player, CD de cds
- modelo de objeto Windows Media Player, cópia de CD
- modelo de objeto, cópia de CD
- controle de ActiveX de Windows Media Player, CD de cds
- controle de ActiveX, CD de cds
- Windows Media Player controle de ActiveX móvel, CD de cds
- Windows Media Player Dispositivos móveis e de CDs
- CD de CDs, interface IWMPCdromRip
- copiando CDs, interface IWMPCdromRip
- Interface IWMPCdromRip
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2179e4f38eee121d7b8fefc028adf232eb724264362396c8cacedfcc55b162d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002546"
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

 

 




