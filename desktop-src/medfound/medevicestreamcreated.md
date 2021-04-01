---
description: MEDeviceStreamCreated é um tipo de evento de mídia estendido gerado com um evento de mídia MEUnknown pelo MFT do dispositivo.
ms.assetid: 8aaa6908-0f2e-4a73-9362-69f42b74f495
title: Evento MEDeviceStreamCreated (mftransform. h)
ms.topic: article
ms.date: 08/31/2018
ms.openlocfilehash: 632ebc305473cd596656a21f562be25d53c2bace
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164765"
---
# <a name="medevicestreamcreated-event"></a>Evento MEDeviceStreamCreated

MEDeviceStreamCreated é um tipo de evento de mídia estendido gerado com um evento de mídia MEUnknown pelo MFT do dispositivo.

Este tipo de evento de mídia estendida não tem carga.  HRESULT apropriado deve ser fornecido por meio do método [**IMFMediaEvent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) .




## <a name="remarks"></a>Comentários

Esse evento de mídia estendido deve ser enviado pelo MFT do dispositivo como parte da seleção do tipo de mídia no fluxo de saída do DMFT.  Quando o SetOutputStreamState é invocado na interface IMFDeviceTransform, o DMFT é responsável por sinalizar a alteração nos Estados de fluxo de entrada necessários com o evento [METransformInputStreamStateChanged](/windows-hardware/drivers/stream/metransforminputstreamstatechanged) Media. Quando a alteração de estado do fluxo de entrada tiver sido reconhecida pelo pipeline com a chamada em SetInputStreamState do DMFT, o DMFT será responsável por concluir sua configuração de estado interno e gerar o tipo de evento de mídia estendida **MEDeviceStreamCreated** .

Se esse tipo de evento de mídia estendido não for gerado, o Gerenciador de transformação de dispositivo não fornecerá nenhum quadro de entrada para o DMFT.
O tipo de evento de mídia estendido também deve ser definido como um atributo de IMFMediaEvent, a ID do fluxo de saída usando o atributo **MF_EVENT_MFT_INPUT_STREAM_ID** .

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>mftransform. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> <dt>

[Processador de streaming de áudio](streaming-audio-renderer.md)
</dt> </dl>

 

 
