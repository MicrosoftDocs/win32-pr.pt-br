---
description: Contém a hora de início em que uma fonte de mídia é reiniciada de sua posição atual.
ms.assetid: b598b4d1-40e1-4282-b312-5aa6ca3a6733
title: Atributo MF_EVENT_SOURCE_ACTUAL_START (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0132fd8fc50f4e71a3b5bb334bc528d86c04e50c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370669"
---
# <a name="mf_event_source_actual_start-attribute"></a><span data-ttu-id="2889c-103">\_Atributo de \_ \_ início real de origem do evento MF \_</span><span class="sxs-lookup"><span data-stu-id="2889c-103">MF\_EVENT\_SOURCE\_ACTUAL\_START attribute</span></span>

<span data-ttu-id="2889c-104">Contém a hora de início em que uma fonte de mídia é reiniciada de sua posição atual.</span><span class="sxs-lookup"><span data-stu-id="2889c-104">Contains the start time at which a media source restarts from its current position.</span></span>

## <a name="data-type"></a><span data-ttu-id="2889c-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="2889c-105">Data type</span></span>

<span data-ttu-id="2889c-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="2889c-106">**UINT64**</span></span>

<span data-ttu-id="2889c-107">Tratar como um valor de **LONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="2889c-107">Treat as a **LONGLONG** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2889c-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="2889c-108">Remarks</span></span>

<span data-ttu-id="2889c-109">Esse atributo é usado com o evento [MESourceStarted](mesourcestarted.md) .</span><span class="sxs-lookup"><span data-stu-id="2889c-109">This attribute is used with the [MESourceStarted](mesourcestarted.md) event.</span></span> <span data-ttu-id="2889c-110">O atributo é relevante quando os dados do evento estão vazios (**VT \_ vazio**), o que indica que a origem da mídia foi iniciada a partir da posição de reprodução atual.</span><span class="sxs-lookup"><span data-stu-id="2889c-110">The attribute is relevant when the event data is empty (**VT\_EMPTY**), which indicates that the media source started from the current playback position.</span></span> <span data-ttu-id="2889c-111">Nesse caso, o atributo **de \_ \_ \_ \_ início real da origem do evento MF** especifica a hora de início real.</span><span class="sxs-lookup"><span data-stu-id="2889c-111">In that case, the **MF\_EVENT\_SOURCE\_ACTUAL\_START** attribute specifies the actual starting time.</span></span> <span data-ttu-id="2889c-112">Se os dados do evento forem **VT \_ vazio** e esse atributo não estiver definido, o tempo de início será considerado como zero.</span><span class="sxs-lookup"><span data-stu-id="2889c-112">If the event data is **VT\_EMPTY** and this attribute is not set, the starting time is assumed to be zero.</span></span>

<span data-ttu-id="2889c-113">Quando os dados de evento [MESourceStarted](mesourcestarted.md) contêm a hora de início (**VT \_ i8**), esse atributo não deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="2889c-113">When the [MESourceStarted](mesourcestarted.md) event data contains the start time (**VT\_I8**), this attribute should not be set.</span></span>

<span data-ttu-id="2889c-114">Esse atributo é um valor assinado, embora seja armazenado como um **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="2889c-114">This attribute is a signed value, although it is stored as a **UINT64**.</span></span>

<span data-ttu-id="2889c-115">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="2889c-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="2889c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2889c-116">Requirements</span></span>



| <span data-ttu-id="2889c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2889c-117">Requirement</span></span> | <span data-ttu-id="2889c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="2889c-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2889c-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2889c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2889c-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2889c-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="2889c-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2889c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2889c-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2889c-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="2889c-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2889c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="2889c-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2889c-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2889c-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="2889c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2889c-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2889c-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="2889c-127">Atributos do evento</span><span class="sxs-lookup"><span data-stu-id="2889c-127">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="2889c-128">**IMFAttributes:: getuint64**</span><span class="sxs-lookup"><span data-stu-id="2889c-128">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="2889c-129">**IMFAttributes:: setuint64**</span><span class="sxs-lookup"><span data-stu-id="2889c-129">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




