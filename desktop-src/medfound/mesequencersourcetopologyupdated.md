---
description: 'Gerado pela origem do sequenciador quando o método IMFSequencerSource:: UpdateTopology é concluído de forma assíncrona.'
ms.assetid: f573cbd0-689c-4bfe-846b-6fc8008101c8
title: Evento MESequencerSourceTopologyUpdated (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baaf03119832937a584178b9f5958b066046c633
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766506"
---
# <a name="mesequencersourcetopologyupdated-event"></a><span data-ttu-id="29943-103">Evento MESequencerSourceTopologyUpdated</span><span class="sxs-lookup"><span data-stu-id="29943-103">MESequencerSourceTopologyUpdated event</span></span>

<span data-ttu-id="29943-104">Gerado pela origem do sequenciador quando o método [**IMFSequencerSource:: UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) é concluído de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="29943-104">Raised by the sequencer source when the [**IMFSequencerSource::UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) method completes asynchronously.</span></span>

## <a name="event-values"></a><span data-ttu-id="29943-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="29943-105">Event values</span></span>

<span data-ttu-id="29943-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="29943-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="29943-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="29943-107">VARTYPE</span></span>            | <span data-ttu-id="29943-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="29943-108">Description</span></span>                                                                                                                                                                                                                        |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29943-109">\_UI4 VT</span><span class="sxs-lookup"><span data-stu-id="29943-109">VT\_UI4</span></span><br/> | <span data-ttu-id="29943-110">Identificador do elemento Sequencer da topologia que está sendo atualizada.</span><span class="sxs-lookup"><span data-stu-id="29943-110">Sequencer element identifier of the topology that is being updated.</span></span> <span data-ttu-id="29943-111">O aplicativo especifica esse valor no parâmetro *dwID* do método [**UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) .</span><span class="sxs-lookup"><span data-stu-id="29943-111">The application specifies this value in the *dwId* parameter of the [**UpdateTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-updatetopology) method.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="29943-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="29943-112">Remarks</span></span>

<span data-ttu-id="29943-113">Esse evento sinaliza que a origem do sequenciador atualizou a topologia, mas não significa que a topologia está pronta para reprodução.</span><span class="sxs-lookup"><span data-stu-id="29943-113">This event signals that the sequencer source has updated the topology, but does not mean that the topology is ready for playback.</span></span> <span data-ttu-id="29943-114">O aplicativo deve aguardar o evento [MESessionTopologyStatus](mesessiontopologystatus.md) .</span><span class="sxs-lookup"><span data-stu-id="29943-114">The application should wait for the [MESessionTopologyStatus](mesessiontopologystatus.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="29943-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29943-115">Requirements</span></span>



| <span data-ttu-id="29943-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="29943-116">Requirement</span></span> | <span data-ttu-id="29943-117">Valor</span><span class="sxs-lookup"><span data-stu-id="29943-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29943-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29943-118">Minimum supported client</span></span><br/> | <span data-ttu-id="29943-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="29943-119">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="29943-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29943-120">Minimum supported server</span></span><br/> | <span data-ttu-id="29943-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="29943-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="29943-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="29943-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="29943-123"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="29943-123"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29943-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="29943-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29943-125">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="29943-125">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="29943-126">Origem do sequenciador</span><span class="sxs-lookup"><span data-stu-id="29943-126">Sequencer Source</span></span>](sequencer-source.md)
</dt> </dl>

 

 




