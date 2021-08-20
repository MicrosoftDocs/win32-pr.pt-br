---
description: MEDeviceStreamCreated é um tipo de evento de mídia estendido gerado com um evento de mídia MEUnknown pelo Device MFT.
ms.assetid: 8aaa6908-0f2e-4a73-9362-69f42b74f495
title: Evento MEDeviceStreamCreated (mftransform.h)
ms.topic: article
ms.date: 08/31/2018
ms.openlocfilehash: 99e13dae5db9d680909a435d5520f6b07d7d4b6c11782c340b72fcdd0eddc53a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878063"
---
# <a name="medevicestreamcreated-event"></a>Evento MEDeviceStreamCreated

MEDeviceStreamCreated é um tipo de evento de mídia estendido gerado com um evento de mídia MEUnknown pelo Device MFT.

Esse tipo de evento de mídia estendida não tem nenhum payload.  O HRESULT apropriado deve ser fornecido por meio [**do método IMFMediaEvent::GetStatus.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus)




## <a name="remarks"></a>Comentários

Esse evento de mídia estendida deve ser enviado pelo Dispositivo MFT como parte da seleção de tipo de mídia no fluxo de saída do DMFT.  Quando SetOutputStreamState é invocado na interface IMFDeviceTransform, a DMFT é responsável por sinalizar a alteração nos estados de fluxo de entrada necessários com o evento de mídia [METransformInputStreamStateChanged.](/windows-hardware/drivers/stream/metransforminputstreamstatechanged) Quando a alteração de estado do fluxo de entrada tiver sido confirmada pelo pipeline com a chamada para SetInputStreamState da DMFT, a DMFT será responsável por concluir sua configuração de estado interno e aumentar o tipo de evento de mídia estendida **MEDeviceStreamCreated.**

Se esse tipo de evento de mídia estendida não for gerado, o Gerenciador de Transformação de Dispositivos não entregará quadros de entrada para o DMFT.
O tipo de evento de mídia estendida também deve ser definido como um atributo do IMFMediaEvent, a ID do fluxo de saída usando o **atributo MF_EVENT_MFT_INPUT_STREAM_ID.**

```cpp
IMFMediaEvent* pMediaEvent = nullptr;

hr = MFCreateMediaEvent (MEUnknown,
                         MEDeviceStreamCreated,
                         S_OK,
                         nullptr,
                         &pMediaEvent);
if (SUCCEEDED(hr))
{
    hr = pMediaEvent->SetUINT32(MF_EVENT_MFT_INPUT_STREAM_ID, GetOutputStreamId());
}

if (SUCCEEDED(hr))
{
    hr = m_pEventQueue->QueueEvent(pMediaEvent);
}

if (nullptr != pMediaEvent)
{
    pMediaEvent->Release();
    pMediaEvent = nullptr;
}

return hr;
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Windows Server 2016 somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>mftransform.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> <dt>

[Renderização de áudio de streaming](streaming-audio-renderer.md)
</dt> </dl>

 

 
