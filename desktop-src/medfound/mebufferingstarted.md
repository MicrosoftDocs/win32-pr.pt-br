---
description: Sinaliza que uma fonte de mídia começou a armazenar em buffer os dados.
ms.assetid: 8637dfcd-2e0c-4cf4-a216-4089c201bfc6
title: Evento MEBufferingStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eb3baf8e66d44eb67ee4c1bbc54ae2e197db081
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798300"
---
# <a name="mebufferingstarted-event"></a>Evento MEBufferingStarted

Sinaliza que uma fonte de mídia começou a armazenar em buffer os dados.

Uma fonte de mídia pode enviar esse evento se a origem armazenar dados em buffer enquanto a sessão de mídia estiver em execução. Quando a sessão de mídia recebe esse evento, ele pausa o relógio de apresentação até que a origem de mídia envie o evento [MEBufferingStopped](mebufferingstopped.md) . A sessão de mídia também encaminha o evento MEBufferingStarted para o aplicativo.

Os fluxos de bytes que implementam a interface [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) também enviam esse evento.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE              | Descrição                           |
|----------------------|---------------------------------------|
| VT \_ vazio<br/> | Nenhum dado do evento.<br/> <br/> |



## <a name="remarks"></a>Comentários

Se uma origem de mídia enviar o evento MEBufferingStarted, ela deverá enviar o evento [MEBufferingStopped](mebufferingstopped.md) quando parar de armazenar em buffer os dados. A origem da mídia deve enviar um evento MEBufferingStopped correspondente para cada evento MEBufferingStarted. A origem da mídia não deve encaminhar esses eventos antes que o método [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) da fonte seja chamado ou depois que o método [**IMFMediaSource:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) da fonte for chamado.

Se você estiver transmitindo da fonte de rede Media Foundation, poderá obter o progresso do buffer consultando a estatística **de \_ \_ ID MFNETSOURCE BUFFERPROGRESS** . Para obter mais informações, [**consulte \_ \_ IDs de estatísticas do MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




