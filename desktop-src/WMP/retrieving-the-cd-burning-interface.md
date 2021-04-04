---
title: Recuperar a interface de gravação de CD
description: Recuperar a interface de gravação de CD
ms.assetid: d52f7b27-a327-4656-8dc2-0b075264d295
keywords:
- Windows Media Player, gravação de CD
- Modelo de objeto do Windows Media Player, gravação de CD
- modelo de objeto, gravação de CD
- Controle ActiveX do Windows Media Player, gravação de CD
- Controle ActiveX, gravação de CD
- Controle ActiveX móvel do Windows Media Player, gravação de CD
- Windows Media Player Mobile, gravação de CD
- Gravação de CD, recuperando a interface IWMPCdromCollection
- gravando CDs, recuperando a interface IWMPCdromCollection
- Interface IWMPCdromCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b63763f9dd99bbaf88ae099edb53ba072cd1a25e
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104007229"
---
# <a name="retrieving-the-cd-burning-interface"></a>Recuperar a interface de gravação de CD

Para enumerar as unidades de CD no computador do usuário, use a interface **IWMPCdromCollection** . Você recupera um ponteiro para essa interface chamando [IWMPCore:: get \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection).

Usando os métodos **de \_ contagem** e **Item** de Get, você pode iterar a coleção para recuperar um ponteiro de interface [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom) para cada unidade de CD no computador do usuário.

A interface **IWMPCdrom** representa uma unidade de CD individual. Antes de começar a gravar um CD, você deve primeiro chamar **QueryInterface** por meio de um ponteiro **IWMPCdrom** para recuperar um ponteiro para a interface [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn) .

O exemplo de código a seguir demonstra como recuperar uma interface para gravar um CD em uma unidade específica:


```C++
HRESULT CMainDlg::GetCdromDriveCount (long &lDriveCount)
{
    hr = m_spPlayer->get_cdromCollection(&m_spCdromCollection);

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
HRESULT CMainDlg::GetCdromBurnInterface (long lIndex)
{
    // Get the IWMPCdrom interface.
    m_spCdrom.Release();
    HRESULT hr = m_spCdromCollection->item(lIndex, &m_spCdrom);
    if (SUCCEEDED(hr))
    {
        // Get the IWMPCdromBurn interface.
        m_spCdromBurn.Release();
        hr = m_spCdrom->QueryInterface(&m_spCdromBurn);
    }

    return hr;
}

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Gravando um CD**](burning-a-cd.md)
</dt> <dt>

[**Iniciando o processo de gravação**](starting-the-burn-process.md)
</dt> <dt>

[**Apagando um CD regravável**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Recuperando a unidade e o status do disco**](retrieving-the-drive-and-disc-status.md)
</dt> <dt>

[**Recuperando o status da gravação**](retrieving-the-burn-status.md)
</dt> <dt>

[**Interface IWMPCdromCollection**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> </dl>

 

 




