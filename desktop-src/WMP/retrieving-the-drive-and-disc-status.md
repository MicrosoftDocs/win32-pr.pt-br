---
title: Recuperando o status da unidade e do disco
description: Recuperando o status da unidade e do disco
ms.assetid: 5e3e6107-d2bc-450c-a86e-5d3ef7b3092a
keywords:
- Windows Media Player, gravação de CD
- Windows Media Player modelo de objeto, gravação de CD
- modelo de objeto, gravação de CD
- Windows Media Player ActiveX controle, gravação de CD
- ActiveX controle, gravação de CD
- Windows Media Player Controle de ActiveX móvel, gravação de CD
- Windows Media Player Móvel, gravação de CD
- Gravação de CD, recuperação do status da unidade e do disco
- CDs de gravação, recuperando o status da unidade e do disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664315972158b4cf68e7f766f98be095a27d7fa8496f983305cc6baaafe784d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746268"
---
# <a name="retrieving-the-drive-and-disc-status"></a>Recuperando o status da unidade e do disco

Antes de iniciar uma operação de gravação de CD, você deve garantir que a unidade CD-ROM selecionada seja compatível com a operação que você deseja executar. Por exemplo, você deve verificar se um CD é capaz de ser apagado antes de chamar [IWMPCdrom Ltd::erase](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-erase). O código a seguir mostra um exemplo de como [usar IWMPCdrom Gates::isAvailable](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-isavailable) para determinar se há suporte para uma operação:


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

[**Gravar um CD**](burning-a-cd.md)
</dt> <dt>

[**Recuperar a interface de gravação de CD**](retrieving-the-cd-burning-interface.md)
</dt> <dt>

[**Iniciando o processo de burn**](starting-the-burn-process.md)
</dt> <dt>

[**Apagando um CD reeritável**](erasing-a-rewritable-cd.md)
</dt> <dt>

[**Recuperando o status de burn**](retrieving-the-burn-status.md)
</dt> </dl>

 

 




