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
# <a name="medevicestreamcreated-event"></a><span data-ttu-id="f27e1-103">Evento MEDeviceStreamCreated</span><span class="sxs-lookup"><span data-stu-id="f27e1-103">MEDeviceStreamCreated event</span></span>

<span data-ttu-id="f27e1-104">MEDeviceStreamCreated é um tipo de evento de mídia estendido gerado com um evento de mídia MEUnknown pelo MFT do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f27e1-104">MEDeviceStreamCreated is an extended media event type generated with an MEUnknown media event by the Device MFT.</span></span>

<span data-ttu-id="f27e1-105">Este tipo de evento de mídia estendida não tem carga.</span><span class="sxs-lookup"><span data-stu-id="f27e1-105">This extended media event type has no payload.</span></span>  <span data-ttu-id="f27e1-106">HRESULT apropriado deve ser fornecido por meio do método [**IMFMediaEvent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) .</span><span class="sxs-lookup"><span data-stu-id="f27e1-106">Appropriate HRESULT should be provided via the [**IMFMediaEvent::GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) method.</span></span>




## <a name="remarks"></a><span data-ttu-id="f27e1-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="f27e1-107">Remarks</span></span>

<span data-ttu-id="f27e1-108">Esse evento de mídia estendido deve ser enviado pelo MFT do dispositivo como parte da seleção do tipo de mídia no fluxo de saída do DMFT.</span><span class="sxs-lookup"><span data-stu-id="f27e1-108">This extended media event must be sent by the Device MFT as a part of the media type selection on the output stream of the DMFT.</span></span>  <span data-ttu-id="f27e1-109">Quando o SetOutputStreamState é invocado na interface IMFDeviceTransform, o DMFT é responsável por sinalizar a alteração nos Estados de fluxo de entrada necessários com o evento [METransformInputStreamStateChanged](/windows-hardware/drivers/stream/metransforminputstreamstatechanged) Media.</span><span class="sxs-lookup"><span data-stu-id="f27e1-109">When the SetOutputStreamState is invoked on the IMFDeviceTransform interface, the DMFT is responsible for signaling the change in the required input stream states with the [METransformInputStreamStateChanged](/windows-hardware/drivers/stream/metransforminputstreamstatechanged) media event.</span></span> <span data-ttu-id="f27e1-110">Quando a alteração de estado do fluxo de entrada tiver sido reconhecida pelo pipeline com a chamada em SetInputStreamState do DMFT, o DMFT será responsável por concluir sua configuração de estado interno e gerar o tipo de evento de mídia estendida **MEDeviceStreamCreated** .</span><span class="sxs-lookup"><span data-stu-id="f27e1-110">When the input stream state change has been acknowledged by the pipeline with the call into SetInputStreamState of the DMFT, the DMFT is responsible for completing its internal state configuration and raising the **MEDeviceStreamCreated** extended media event type.</span></span>

<span data-ttu-id="f27e1-111">Se esse tipo de evento de mídia estendido não for gerado, o Gerenciador de transformação de dispositivo não fornecerá nenhum quadro de entrada para o DMFT.</span><span class="sxs-lookup"><span data-stu-id="f27e1-111">If this extended media event type is not raised, the Device Transform Manager will not deliver any input frames to the DMFT.</span></span>
<span data-ttu-id="f27e1-112">O tipo de evento de mídia estendido também deve ser definido como um atributo de IMFMediaEvent, a ID do fluxo de saída usando o atributo **MF_EVENT_MFT_INPUT_STREAM_ID** .</span><span class="sxs-lookup"><span data-stu-id="f27e1-112">The extended media event type must also set as an attribute of the IMFMediaEvent, the output stream ID using the **MF_EVENT_MFT_INPUT_STREAM_ID** attribute.</span></span>

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

## <a name="requirements"></a><span data-ttu-id="f27e1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f27e1-113">Requirements</span></span>



| <span data-ttu-id="f27e1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f27e1-114">Requirement</span></span> | <span data-ttu-id="f27e1-115">Valor</span><span class="sxs-lookup"><span data-stu-id="f27e1-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f27e1-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f27e1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f27e1-117">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="f27e1-117">Windows 10 \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f27e1-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f27e1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f27e1-119">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="f27e1-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f27e1-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f27e1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f27e1-121"><dt>mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="f27e1-121"><dt>mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f27e1-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="f27e1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f27e1-123">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f27e1-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="f27e1-124">Processador de streaming de áudio</span><span class="sxs-lookup"><span data-stu-id="f27e1-124">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
