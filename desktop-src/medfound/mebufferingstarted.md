---
description: Sinaliza que uma fonte de mídia começou a buffer de dados.
ms.assetid: 8637dfcd-2e0c-4cf4-a216-4089c201bfc6
title: Evento MEBufferingStarted (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e55a691b723fc2e09487752ee8f5226e32504d60a6d68a4652bbb2b5b3e5aa7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724266"
---
# <a name="mebufferingstarted-event"></a>Evento MEBufferingStarted

Sinaliza que uma fonte de mídia começou a buffer de dados.

Uma fonte de mídia pode enviar esse evento se a origem em buffer de dados enquanto a Sessão de Mídia está em execução. Quando a Sessão de Mídia recebe esse evento, ela pausa o relógio de apresentação até que a fonte de mídia envie o [evento MEBufferingStopped.](mebufferingstopped.md) A Sessão de Mídia também encaminha o evento MEBufferingStarted para o aplicativo.

Fluxos de byte que implementam a interface [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) também enviam esse evento.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| Vartype              | Descrição                           |
|----------------------|---------------------------------------|
| VT \_ VAZIO<br/> | Nenhum dado do evento.<br/> <br/> |



## <a name="remarks"></a>Comentários

Se uma fonte de mídia enviar o evento MEBufferingStarted, ela deverá enviar o [evento MEBufferingStopped](mebufferingstopped.md) quando parar de buffer de dados. A fonte de mídia deve enviar um evento MEBufferingStopped correspondente para cada evento MEBufferingStarted. A fonte de mídia não deve encaminhar esses eventos antes que o método [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) da origem seja chamado ou depois que o método [**IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) da origem for chamado.

Se você estiver transmitindo da fonte Media Foundation rede, poderá obter o progresso do buffer consultando a estatística de **\_ \_ ID BUFFERPROGRESS do MFNETSOURCE.** Para obter mais informações, [**consulte MFNETSOURCE \_ STATISTICS \_ IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).

## <a name="examples"></a>Exemplos


```C++
HRESULT GetBufferProgress(IMFMediaSession *pSession, DWORD *pProgress)
{
    IPropertyStore *pProp = NULL;
    PROPVARIANT var;

    // Get the property store from the media session.
    HRESULT hr = MFGetService(
        pSession, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_PPV_ARGS(&pProp)
        );

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_BUFFERPROGRESS_ID;

        hr = pProp->GetValue(key, &var);
    }

    if (SUCCEEDED(hr))
    {
        *pProgress = var.lVal;
    }

    PropVariantClear(&var);
    SafeRelease(&pProp);
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
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




