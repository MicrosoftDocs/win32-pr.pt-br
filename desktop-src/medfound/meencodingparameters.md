---
description: Enviado pelo pipeline para o codificador MFTs em série com exemplos de mídia por meio de IMFTransform::P rocessEvent.
ms.assetid: D5D4544B-CD8D-4C94-B050-7BA1944800CC
title: Evento MEEncodingParameters (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e193044b25eb1d333182a2593fcf2248fba2366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165047"
---
# <a name="meencodingparameters-event"></a><span data-ttu-id="9bd57-103">Evento MEEncodingParameters</span><span class="sxs-lookup"><span data-stu-id="9bd57-103">MEEncodingParameters event</span></span>

<span data-ttu-id="9bd57-104">Enviado pelo pipeline para o codificador MFTs em série com exemplos de mídia por meio de [**IMFTransform::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).</span><span class="sxs-lookup"><span data-stu-id="9bd57-104">Sent by the pipeline to encoder MFTs serially with media samples via [**IMFTransform::ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).</span></span>

## <a name="event-values"></a><span data-ttu-id="9bd57-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="9bd57-105">Event values</span></span>

<span data-ttu-id="9bd57-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="9bd57-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="9bd57-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="9bd57-107">VARTYPE</span></span>              | <span data-ttu-id="9bd57-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="9bd57-108">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="9bd57-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="9bd57-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="9bd57-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="9bd57-110">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="9bd57-111">Atributos</span><span class="sxs-lookup"><span data-stu-id="9bd57-111">Attributes</span></span>

<span data-ttu-id="9bd57-112">Os atributos a seguir são definidos para este evento.</span><span class="sxs-lookup"><span data-stu-id="9bd57-112">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="9bd57-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="9bd57-113">Attribute</span></span>                                         | <span data-ttu-id="9bd57-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="9bd57-114">Description</span></span>                                                                                                                    |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9bd57-115">**IMFAttributes**</span><span class="sxs-lookup"><span data-stu-id="9bd57-115">**IMFAttributes**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)<br/> | <span data-ttu-id="9bd57-116">Contém as novas configurações baseadas em ICodecAPI que o codificador deve aplicar em exemplos de entrada subsequentes.</span><span class="sxs-lookup"><span data-stu-id="9bd57-116">Contains the new ICodecAPI-based settings that the encoder should apply on subsequent incoming samples.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="9bd57-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="9bd57-117">Remarks</span></span>

<span data-ttu-id="9bd57-118">A carga do evento é um repositório de atributos (ponteiro IMFAttributes) que contém as novas configurações baseadas em ICodecAPI///que o codificador deve aplicar nos exemplos de entrada subsequentes.</span><span class="sxs-lookup"><span data-stu-id="9bd57-118">Event payload is an attribute store (IMFAttributes pointer) that contains the new ICodecAPI-based /// settings that the encoder should apply on subsequent incoming samples.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bd57-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9bd57-119">Requirements</span></span>



| <span data-ttu-id="9bd57-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bd57-120">Requirement</span></span> | <span data-ttu-id="9bd57-121">Valor</span><span class="sxs-lookup"><span data-stu-id="9bd57-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9bd57-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9bd57-122">Minimum supported client</span></span><br/> | <span data-ttu-id="9bd57-123">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9bd57-123">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="9bd57-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9bd57-124">Minimum supported server</span></span><br/> | <span data-ttu-id="9bd57-125">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="9bd57-125">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="9bd57-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9bd57-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bd57-127"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9bd57-127"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9bd57-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="9bd57-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9bd57-129">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9bd57-129">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




