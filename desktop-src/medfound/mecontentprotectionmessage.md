---
description: Gerado por um componente de pipeline quando a configuração é alterada para um dos esquemas de proteção de saída. Esse evento se aplica somente ao conteúdo protegido.
ms.assetid: 0a13fc08-2bbe-46d8-a076-6165cca6ea36
title: Evento MEContentProtectionMessage (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f96ac75711559881232ced4cec6bfca2bc030c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647570"
---
# <a name="mecontentprotectionmessage-event"></a><span data-ttu-id="ac949-104">Evento MEContentProtectionMessage</span><span class="sxs-lookup"><span data-stu-id="ac949-104">MEContentProtectionMessage event</span></span>

<span data-ttu-id="ac949-105">Gerado por um componente de pipeline quando a configuração é alterada para um dos esquemas de proteção de saída.</span><span class="sxs-lookup"><span data-stu-id="ac949-105">Raised by a pipeline component when the configuration changes for one of the output protection schemes.</span></span> <span data-ttu-id="ac949-106">Esse evento se aplica somente ao conteúdo protegido.</span><span class="sxs-lookup"><span data-stu-id="ac949-106">This event applies only to protected content.</span></span>

## <a name="event-values"></a><span data-ttu-id="ac949-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="ac949-107">Event values</span></span>

<span data-ttu-id="ac949-108">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="ac949-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="ac949-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="ac949-109">VARTYPE</span></span>              | <span data-ttu-id="ac949-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="ac949-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="ac949-111">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="ac949-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="ac949-112">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="ac949-112">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="ac949-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ac949-113">Remarks</span></span>

<span data-ttu-id="ac949-114">Todas as saídas confiáveis devem lidar com esse evento.</span><span class="sxs-lookup"><span data-stu-id="ac949-114">All trusted outputs must handle this event.</span></span> <span data-ttu-id="ac949-115">Media Foundation transformações (MFTs) recebem esse evento por meio do método [**IMFTransform::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) .</span><span class="sxs-lookup"><span data-stu-id="ac949-115">Media Foundation transforms (MFTs) receive this event through the [**IMFTransform::ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) method.</span></span> <span data-ttu-id="ac949-116">Os coletores de mídia recebem esse evento por meio do método [**IMFStreamSink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) .</span><span class="sxs-lookup"><span data-stu-id="ac949-116">Media sinks receive this event through the [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) method.</span></span>

<span data-ttu-id="ac949-117">A saída confiável deve aplicar as alterações de política ou retornar o código de erro MF \_ E \_ política \_ sem suporte.</span><span class="sxs-lookup"><span data-stu-id="ac949-117">The trusted output must apply the policy changes or return the error code MF\_E\_POLICY\_UNSUPPORTED.</span></span>

<span data-ttu-id="ac949-118">Os dados e atributos do evento dependem do sistema de proteção de conteúdo em uso.</span><span class="sxs-lookup"><span data-stu-id="ac949-118">The event data and attributes depend on the content protection system in use.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac949-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac949-119">Requirements</span></span>



| <span data-ttu-id="ac949-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ac949-120">Requirement</span></span> | <span data-ttu-id="ac949-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ac949-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ac949-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac949-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ac949-123">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="ac949-123">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="ac949-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ac949-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ac949-125">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ac949-125">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="ac949-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ac949-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ac949-127"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ac949-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac949-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac949-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac949-129">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ac949-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




