---
title: Recuperando a unidade e o status do disco
description: Recuperando a unidade e o status do disco
ms.assetid: 5e3e6107-d2bc-450c-a86e-5d3ef7b3092a
keywords:
- Windows Media Player, gravação de CD
- Modelo de objeto do Windows Media Player, gravação de CD
- modelo de objeto, gravação de CD
- Controle ActiveX do Windows Media Player, gravação de CD
- Controle ActiveX, gravação de CD
- Controle ActiveX móvel do Windows Media Player, gravação de CD
- Windows Media Player Mobile, gravação de CD
- Gravação de CD, recuperando a unidade e o status do disco
- gravando CDs, recuperando a unidade e o status do disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eab66581c336f642fd53b22f81949847d0a1c89
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103823573"
---
# <a name="retrieving-the-drive-and-disc-status"></a>Recuperando a unidade e o status do disco

Antes de iniciar uma operação de gravação de CD, você deve garantir que a unidade de CD-ROM selecionada dê suporte à operação que você deseja executar. Por exemplo, você deve verificar se um CD pode ser apagado antes de chamar [IWMPCdromBurn:: Erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase). O código a seguir mostra um exemplo de como usar [IWMPCdromBurn:: IsAvailable](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-isavailable) para determinar se há suporte para uma operação:


```C++
VARIANT_BOOL vbResult;
    
// Check whether this drive can burn CDs.
CComBSTR bstrItem;
HRESULT hr = bstrItem.Append("Burn");
if (SUCCEEDED(hr))
{
    hr = m_spCdromBurn->isAvailable(bstrItem, &vbResult);
}
if (SUCCEEDED(hr))
{
    if (VARIANT_TRUE == vbResult)
    {
        // The current drive can burn CDs.
    }
}

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Gravando um CD**](burning-a-cd.md)
</dt> <dt>

[**Recuperar a interface de gravação de CD**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**Iniciando o processo de gravação**](starting-the-burn-process.md)
</dt> <dt>

[**Apagando um CD regravável**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Recuperando o status da gravação**](retrieving-the-burn-status.md)
</dt> </dl>

 

 




