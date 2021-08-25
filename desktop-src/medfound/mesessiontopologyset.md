---
description: Gerado após o método IMFMediaSession::SetTopology ser concluído de forma assíncrona. A Sessão de Mídia acionará esse evento depois de resolver a topologia em uma topologia completa e enfilfilar a topologia para reprodução.
ms.assetid: 22a298b7-d32b-44ed-b0a1-4e0398ecfe04
title: Evento MESessionTopologySet (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba2b5454309855ff472c633388cddabe0c12fab09e2ae462aacd2de49c3c9bba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957396"
---
# <a name="mesessiontopologyset-event"></a>Evento MESessionTopologySet

Gerado após o [**método IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) ser concluído de forma assíncrona. A Sessão de Mídia acionará esse evento depois de resolver a topologia em uma topologia completa e enfilfilar a topologia para reprodução.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| Vartype                | Descrição                                                                                              |
|------------------------|----------------------------------------------------------------------------------------------------------|
| VT \_ VAZIO<br/>   | Nenhum dado do evento.<br/> <br/>                                                                    |
| VT \_ UNKNOWN<br/> | Ponteiro para a interface [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) da topologia completa.<br/> <br/> |



## <a name="examples"></a>Exemplos

O exemplo a seguir recupera o ponteiro [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) de um evento MESessionTopologySet.


```
HRESULT GetTopologyFromEvent(IMFMediaEvent *pEvent, IMFTopology **ppTopology)
{
    HRESULT hr = S_OK;
    PROPVARIANT var;

    PropVariantInit(&var);
    hr = pEvent->GetValue(&var);
    if (SUCCEEDED(hr))
    {
        if (var.vt != VT_UNKNOWN)
        {
            hr = E_UNEXPECTED;
        }
    }
    if (SUCCEEDED(hr))
    {
        hr = var.punkVal->QueryInterface(__uuidof(IMFTopology), (void**)ppTopology);
    }
    PropVariantClear(&var);
    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects.h (inclua Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




