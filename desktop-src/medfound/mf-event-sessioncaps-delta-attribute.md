---
description: Contém sinalizadores que indicam quais funcionalidades foram alteradas na sessão de mídia, com base na apresentação atual.
ms.assetid: aa01d17f-f2ac-4504-b278-3edd90ab8a23
title: Atributo MF_EVENT_SESSIONCAPS_DELTA (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 284a31a8d3fc661c15e7de991972455468efbd40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370657"
---
# <a name="mf_event_sessioncaps_delta-attribute"></a><span data-ttu-id="4c4fb-103">\_Atributo de Delta de evento MF \_ SESSIONCAPS \_</span><span class="sxs-lookup"><span data-stu-id="4c4fb-103">MF\_EVENT\_SESSIONCAPS\_DELTA attribute</span></span>

<span data-ttu-id="4c4fb-104">Contém sinalizadores que indicam quais funcionalidades foram alteradas na sessão de mídia, com base na apresentação atual.</span><span class="sxs-lookup"><span data-stu-id="4c4fb-104">Contains flags that indicate which capabilities have changed in the Media Session, based on the current presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="4c4fb-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="4c4fb-105">Data type</span></span>

<span data-ttu-id="4c4fb-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="4c4fb-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="4c4fb-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c4fb-107">Remarks</span></span>

<span data-ttu-id="4c4fb-108">Esse atributo contém um bitmask que indica quais sinalizadores de funcionalidades foram alterados.</span><span class="sxs-lookup"><span data-stu-id="4c4fb-108">This attribute contains a bitmask indicating which capabilities flags have changed.</span></span> <span data-ttu-id="4c4fb-109">Para obter uma lista de possíveis sinalizadores, consulte [**IMFMediaSession:: GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).</span><span class="sxs-lookup"><span data-stu-id="4c4fb-109">For a list of possible flags, see [**IMFMediaSession::GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).</span></span> <span data-ttu-id="4c4fb-110">Os bits são definidos como 1 no bitmask por qualquer um dos seguintes motivos:</span><span class="sxs-lookup"><span data-stu-id="4c4fb-110">Bits are set to 1 in the bitmask for any of the following reasons:</span></span>

-   <span data-ttu-id="4c4fb-111">O bit de recursos correspondente foi alterado de 0 para 1.</span><span class="sxs-lookup"><span data-stu-id="4c4fb-111">The corresponding capabilities bit changed from 0 to 1.</span></span>
-   <span data-ttu-id="4c4fb-112">O bit de recursos correspondente mudou de 1 para 0.</span><span class="sxs-lookup"><span data-stu-id="4c4fb-112">The corresponding capabilities bit changed from 1 to 0.</span></span>
-   <span data-ttu-id="4c4fb-113">O bit de recursos correspondente permaneceu 1, mas os detalhes do recurso foram alterados.</span><span class="sxs-lookup"><span data-stu-id="4c4fb-113">The corresponding capabilities bit remained 1, but the details of the capability changed.</span></span> <span data-ttu-id="4c4fb-114">Por exemplo, a taxa de reprodução máxima foi alterada.</span><span class="sxs-lookup"><span data-stu-id="4c4fb-114">For example, the maximum playback rate changed.</span></span>

<span data-ttu-id="4c4fb-115">Esse atributo é usado com o evento [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) .</span><span class="sxs-lookup"><span data-stu-id="4c4fb-115">This attribute is used with the [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) event.</span></span>

<span data-ttu-id="4c4fb-116">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="4c4fb-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c4fb-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c4fb-117">Requirements</span></span>



| <span data-ttu-id="4c4fb-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c4fb-118">Requirement</span></span> | <span data-ttu-id="4c4fb-119">Valor</span><span class="sxs-lookup"><span data-stu-id="4c4fb-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4c4fb-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c4fb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="4c4fb-121">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4c4fb-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4c4fb-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4c4fb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="4c4fb-123">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4c4fb-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4c4fb-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4c4fb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c4fb-125"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c4fb-125"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c4fb-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c4fb-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c4fb-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="4c4fb-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="4c4fb-128">Atributos do evento</span><span class="sxs-lookup"><span data-stu-id="4c4fb-128">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="4c4fb-129">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="4c4fb-129">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="4c4fb-130">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="4c4fb-130">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




