---
description: Gerado por um componente de pipeline quando a política de saída para o fluxo é alterada. Esse evento se aplica somente ao conteúdo protegido.
ms.assetid: 9dc78dc6-3fc2-4a81-ad41-45ff3fdbdade
title: Evento MEPolicyChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b6827c44958e2df016365a8caa9a66f1aad9a30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788605"
---
# <a name="mepolicychanged-event"></a><span data-ttu-id="a9223-104">Evento MEPolicyChanged</span><span class="sxs-lookup"><span data-stu-id="a9223-104">MEPolicyChanged event</span></span>

<span data-ttu-id="a9223-105">Gerado por um componente de pipeline quando a política de saída para o fluxo é alterada.</span><span class="sxs-lookup"><span data-stu-id="a9223-105">Raised by a pipeline component when the output policy for the stream changes.</span></span> <span data-ttu-id="a9223-106">Esse evento se aplica somente ao conteúdo protegido.</span><span class="sxs-lookup"><span data-stu-id="a9223-106">This event applies only to protected content.</span></span>

## <a name="event-values"></a><span data-ttu-id="a9223-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="a9223-107">Event values</span></span>

<span data-ttu-id="a9223-108">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="a9223-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="a9223-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="a9223-109">VARTYPE</span></span>                | <span data-ttu-id="a9223-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="a9223-110">Description</span></span>                                                                                                                  |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9223-111">VT \_ desconhecido</span><span class="sxs-lookup"><span data-stu-id="a9223-111">VT\_UNKNOWN</span></span><br/> | <span data-ttu-id="a9223-112">Ponteiro para a interface [**IMFOutputPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy) da nova política para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="a9223-112">Pointer to the [**IMFOutputPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy) interface of the new policy for the stream.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="a9223-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9223-113">Remarks</span></span>

<span data-ttu-id="a9223-114">Todas as saídas confiáveis devem lidar com esse evento.</span><span class="sxs-lookup"><span data-stu-id="a9223-114">All trusted outputs must handle this event.</span></span> <span data-ttu-id="a9223-115">Media Foundation transformações (MFTs) recebem esse evento por meio do método [**IMFTransform::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) .</span><span class="sxs-lookup"><span data-stu-id="a9223-115">Media Foundation transforms (MFTs) receive this event through the [**IMFTransform::ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) method.</span></span> <span data-ttu-id="a9223-116">Os coletores de mídia recebem esse evento por meio do método [**IMFStreamSink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) .</span><span class="sxs-lookup"><span data-stu-id="a9223-116">Media sinks receive this event through the [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) method.</span></span>

<span data-ttu-id="a9223-117">A saída confiável deve aplicar a nova política ou retornar o código de erro MF \_ E \_ política \_ sem suporte.</span><span class="sxs-lookup"><span data-stu-id="a9223-117">The trusted output must apply the new policy or return the error code MF\_E\_POLICY\_UNSUPPORTED.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9223-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9223-118">Requirements</span></span>



| <span data-ttu-id="a9223-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9223-119">Requirement</span></span> | <span data-ttu-id="a9223-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a9223-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9223-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9223-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a9223-122">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="a9223-122">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="a9223-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9223-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a9223-124">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="a9223-124">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="a9223-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a9223-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9223-126"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a9223-126"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9223-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9223-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9223-128">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a9223-128">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




