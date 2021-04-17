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
# <a name="mebufferingstarted-event"></a><span data-ttu-id="baab5-103">Evento MEBufferingStarted</span><span class="sxs-lookup"><span data-stu-id="baab5-103">MEBufferingStarted event</span></span>

<span data-ttu-id="baab5-104">Sinaliza que uma fonte de mídia começou a armazenar em buffer os dados.</span><span class="sxs-lookup"><span data-stu-id="baab5-104">Signals that a media source has started to buffer data.</span></span>

<span data-ttu-id="baab5-105">Uma fonte de mídia pode enviar esse evento se a origem armazenar dados em buffer enquanto a sessão de mídia estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="baab5-105">A media source can send this event if the source buffers data while the Media Session is running.</span></span> <span data-ttu-id="baab5-106">Quando a sessão de mídia recebe esse evento, ele pausa o relógio de apresentação até que a origem de mídia envie o evento [MEBufferingStopped](mebufferingstopped.md) .</span><span class="sxs-lookup"><span data-stu-id="baab5-106">When the Media Session receives this event, it pauses the presentation clock until the media source sends the [MEBufferingStopped](mebufferingstopped.md) event.</span></span> <span data-ttu-id="baab5-107">A sessão de mídia também encaminha o evento MEBufferingStarted para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="baab5-107">The Media Session also forwards the MEBufferingStarted event to the application.</span></span>

<span data-ttu-id="baab5-108">Os fluxos de bytes que implementam a interface [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) também enviam esse evento.</span><span class="sxs-lookup"><span data-stu-id="baab5-108">Byte streams that implement the [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) interface also send this event.</span></span>

## <a name="event-values"></a><span data-ttu-id="baab5-109">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="baab5-109">Event values</span></span>

<span data-ttu-id="baab5-110">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="baab5-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="baab5-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="baab5-111">VARTYPE</span></span>              | <span data-ttu-id="baab5-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="baab5-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="baab5-113">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="baab5-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="baab5-114">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="baab5-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="baab5-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="baab5-115">Remarks</span></span>

<span data-ttu-id="baab5-116">Se uma origem de mídia enviar o evento MEBufferingStarted, ela deverá enviar o evento [MEBufferingStopped](mebufferingstopped.md) quando parar de armazenar em buffer os dados.</span><span class="sxs-lookup"><span data-stu-id="baab5-116">If a media source sends the MEBufferingStarted event, it must send the [MEBufferingStopped](mebufferingstopped.md) event when it stops buffering data.</span></span> <span data-ttu-id="baab5-117">A origem da mídia deve enviar um evento MEBufferingStopped correspondente para cada evento MEBufferingStarted.</span><span class="sxs-lookup"><span data-stu-id="baab5-117">The media source must send a matching MEBufferingStopped event for every MEBufferingStarted event.</span></span> <span data-ttu-id="baab5-118">A origem da mídia não deve encaminhar esses eventos antes que o método [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) da fonte seja chamado ou depois que o método [**IMFMediaSource:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) da fonte for chamado.</span><span class="sxs-lookup"><span data-stu-id="baab5-118">The media source should not forward these events before the source's [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method is called, or after the source's [**IMFMediaSource::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) method is called.</span></span>

<span data-ttu-id="baab5-119">Se você estiver transmitindo da fonte de rede Media Foundation, poderá obter o progresso do buffer consultando a estatística **de \_ \_ ID MFNETSOURCE BUFFERPROGRESS** .</span><span class="sxs-lookup"><span data-stu-id="baab5-119">If you are streaming from the Media Foundation network source, you can get the buffering progress by querying the **MFNETSOURCE\_BUFFERPROGRESS\_ID** statistic.</span></span> <span data-ttu-id="baab5-120">Para obter mais informações, [**consulte \_ \_ IDs de estatísticas do MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span><span class="sxs-lookup"><span data-stu-id="baab5-120">For more information, see [**MFNETSOURCE\_STATISTICS\_IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span></span>

## <a name="examples"></a><span data-ttu-id="baab5-121">Exemplos</span><span class="sxs-lookup"><span data-stu-id="baab5-121">Examples</span></span>


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



## <a name="requirements"></a><span data-ttu-id="baab5-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="baab5-122">Requirements</span></span>



| <span data-ttu-id="baab5-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="baab5-123">Requirement</span></span> | <span data-ttu-id="baab5-124">Valor</span><span class="sxs-lookup"><span data-stu-id="baab5-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="baab5-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="baab5-125">Minimum supported client</span></span><br/> | <span data-ttu-id="baab5-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="baab5-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="baab5-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="baab5-127">Minimum supported server</span></span><br/> | <span data-ttu-id="baab5-128">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="baab5-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="baab5-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="baab5-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="baab5-130"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="baab5-130"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baab5-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="baab5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baab5-132">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="baab5-132">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="baab5-133">Rede em Media Foundation</span><span class="sxs-lookup"><span data-stu-id="baab5-133">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




