---
description: este tópico descreve como implementar um pin de visualização em um filtro de captura DirectShow.
ms.assetid: 60306702-97d4-4627-8fbe-e7c8750f3902
title: Implementando um PIN de visualização (opcional)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7de47b86df70500c83c794fe1074dc927622d571e78ef6175b944702277da492
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015554"
---
# <a name="implementing-a-preview-pin-optional"></a>Implementando um PIN de visualização (opcional)

este tópico descreve como implementar um pin de visualização em um filtro de captura DirectShow.

Se o filtro tiver um PIN de visualização, o PIN de visualização deverá enviar uma cópia dos dados entregues pelo PIN de captura. Somente envie dados do PIN de visualização ao fazer isso não fará com que o pino de captura descartar os quadros. O PIN de captura sempre tem prioridade sobre o PIN de visualização.

O PIN de captura e o pino de visualização devem enviar dados com o mesmo formato. Portanto, eles devem se conectar usando tipos de mídia idênticos. Se o PIN de captura se conectar primeiro, o PIN de visualização deverá oferecer o mesmo tipo de mídia e rejeitar outros tipos. Se o pino de visualização se conectar primeiro e o PIN de captura se conectar com um tipo de mídia diferente, o PIN de visualização deverá se reconectar usando o novo tipo de mídia. Se o filtro downstream do PIN de visualização rejeitar o novo tipo, o PIN de captura também deverá rejeitar o tipo. Use o método [**IPin:: QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) para consultar o downstream de filtro do PIN de visualização e use o método [**IFilterGraph:: Reconnect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-reconnect) para reconectar o PIN. essas regras também se aplicam se o filtro Graph Manager reconecta o pin de captura.

O exemplo a seguir mostra um contorno desse processo:


```C++
// Override CBasePin::CheckMediaType.
CCapturePin::CheckMediaType(CMediaType *pmt)
{
    if (m_pMyPreviewPin->IsConnected()) 
    {
        // The preview pin is already connected, so query the pin it is
        // connected to. If the other pin rejects it, so do we.
        hr = m_pMyPreviewPin->GetConnected()->QueryAccept(pmt);
        if (hr != S_OK) 
        {
            // The preview pin cannot reconnect with this media type.
            return E_INVALIDARG;
        }
        // The preview pin will reconnect when SetMediaType is called.
    }
    // Decide whether the capture pin accepts the format. 
    BOOL fAcceptThisType = ...  // (Not shown.)
    return (fAcceptThisType? S_OK : E_FAIL);
}

// Override CBasePin::SetMediaType.
CCapturePin::SetMediaType(CMediaType *pmt);
{
    if (m_pMyPreviewPin->IsConnected()) 
    {
        // The preview pin is already connected, so it must reconnect.
        if (m_pMyPreviewPin->GetConnected()->QueryAccept(pmt) == S_OK)
        {
            // The downstream pin will accept the new type, so it's safe
            // to reconnect. 
            m_pFilter->m_pGraph->Reconnect(m_pMyPreviewPin);
        }
        else
        {
            return VFW_E_INVALIDMEDIATYPE;
        }
    }
    // Now do anything that the capture pin needs to set the type.
    hr = MyInternalSetMediaType(pmt);

    // And finally, call the base-class method.
    return CBasePin::SetMediaType(pmt);
}

CPreviewPin::CheckMediaType(CMediaType *pmt)
{
    if (m_pMyCapturePin->IsConnected())
    {
       // The preview pin must connect with the same type.
       CMediaType cmt = m_pMyCapturePin->m_mt;
       return (*pmt == cmt ? S_OK : VFW_E_INVALIDMEDIATYPE);
    }
    // Decide whether the preview pin accepts the format. You can use your 
    // knowledge of which types the capture pin will accept. Regardless,
    // when the capture pin connects, the preview pin will reconnect.
    return (fAcceptThisType? S_OK : E_FAIL);
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[como os filtros Conexão](how-filters-connect.md)
</dt> <dt>

[Gravando filtros de captura](writing-capture-filters.md)
</dt> </dl>

 

 



