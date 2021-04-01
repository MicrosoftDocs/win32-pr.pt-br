---
description: Tempo de apresentação para um exemplo que foi renderizado durante a depuração.
ms.assetid: 6ce52cf5-014b-49a2-abf7-2c9cc5340a42
title: Atributo MF_EVENT_SCRUBSAMPLE_TIME (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de7c4fb1a8015367fa3d48edb066cdb135983926
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921273"
---
# <a name="mf_event_scrubsample_time-attribute"></a><span data-ttu-id="4d5fa-103">\_Atributo de \_ tempo SCRUBSAMPLE de evento MF \_</span><span class="sxs-lookup"><span data-stu-id="4d5fa-103">MF\_EVENT\_SCRUBSAMPLE\_TIME attribute</span></span>

<span data-ttu-id="4d5fa-104">Tempo de apresentação para um exemplo que foi renderizado durante a depuração.</span><span class="sxs-lookup"><span data-stu-id="4d5fa-104">Presentation time for a sample that was rendered while scrubbing.</span></span>

## <a name="data-type"></a><span data-ttu-id="4d5fa-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="4d5fa-105">Data type</span></span>

<span data-ttu-id="4d5fa-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="4d5fa-106">**UINT64**</span></span>

<span data-ttu-id="4d5fa-107">Tratar como um valor de **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="4d5fa-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d5fa-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d5fa-108">Remarks</span></span>

<span data-ttu-id="4d5fa-109">Esse atributo é usado com o evento [MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md) .</span><span class="sxs-lookup"><span data-stu-id="4d5fa-109">This attribute is used with the [MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md) event.</span></span>

<span data-ttu-id="4d5fa-110">Esse atributo é um valor assinado, embora seja armazenado como um **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="4d5fa-110">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="4d5fa-111">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="4d5fa-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d5fa-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d5fa-112">Requirements</span></span>



| <span data-ttu-id="4d5fa-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d5fa-113">Requirement</span></span> | <span data-ttu-id="4d5fa-114">Valor</span><span class="sxs-lookup"><span data-stu-id="4d5fa-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4d5fa-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d5fa-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4d5fa-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4d5fa-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4d5fa-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4d5fa-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4d5fa-118">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4d5fa-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4d5fa-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4d5fa-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d5fa-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4d5fa-120"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d5fa-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="4d5fa-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d5fa-122">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4d5fa-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4d5fa-123">Atributos do evento</span><span class="sxs-lookup"><span data-stu-id="4d5fa-123">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="4d5fa-124">**IMFAttributes:: getuint64**</span><span class="sxs-lookup"><span data-stu-id="4d5fa-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="4d5fa-125">**IMFAttributes:: setuint64**</span><span class="sxs-lookup"><span data-stu-id="4d5fa-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




