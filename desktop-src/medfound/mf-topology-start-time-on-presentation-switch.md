---
description: Especifica a hora de início para as apresentações que são enfileiradas após a primeira apresentação.
ms.assetid: 087f5d61-b3e6-4fdf-98e6-b018de7b237f
title: Atributo MF_TOPOLOGY_START_TIME_ON_PRESENTATION_SWITCH (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5f4c50271ad2da9682be9d259ad855352e844af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783726"
---
# <a name="mf_topology_start_time_on_presentation_switch-attribute"></a><span data-ttu-id="21468-103">\_ \_ \_ Hora de início da topologia MF \_ no \_ atributo do \_ comutador de apresentação</span><span class="sxs-lookup"><span data-stu-id="21468-103">MF\_TOPOLOGY\_START\_TIME\_ON\_PRESENTATION\_SWITCH attribute</span></span>

<span data-ttu-id="21468-104">Especifica a hora de início para as apresentações que são enfileiradas após a primeira apresentação.</span><span class="sxs-lookup"><span data-stu-id="21468-104">Specifies the start time for presentations that are queued after the first presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="21468-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="21468-105">Data type</span></span>

<span data-ttu-id="21468-106">**Int64** armazenado como **UINT64**</span><span class="sxs-lookup"><span data-stu-id="21468-106">**INT64** stored as **UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="21468-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="21468-107">Get/set</span></span>

<span data-ttu-id="21468-108">Para obter esse atributo, chame [**IMFAttributes:: getuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="21468-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="21468-109">Para definir esse atributo, chame [**IMFAttributes:: setuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="21468-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="21468-110">Aplica-se A</span><span class="sxs-lookup"><span data-stu-id="21468-110">Applies To</span></span>

[<span data-ttu-id="21468-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="21468-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="21468-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="21468-112">Remarks</span></span>

<span data-ttu-id="21468-113">Quando o aplicativo enfileira a primeira apresentação na sessão de mídia, o aplicativo especifica a hora de início no parâmetro *pvarStartPosition* do método [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) .</span><span class="sxs-lookup"><span data-stu-id="21468-113">When the application queues the first presentation on the Media Session, the application specifies the start time in the *pvarStartPosition* parameter of the [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method.</span></span> <span data-ttu-id="21468-114">No entanto, para todas as apresentações subsequentes, a hora de início é fornecida pela \_ hora de início da topologia MF \_ \_ \_ no \_ \_ atributo switch de apresentação na topologia.</span><span class="sxs-lookup"><span data-stu-id="21468-114">For any subsequent presentations, however, the start time is given by the MF\_TOPOLOGY\_START\_TIME\_ON\_PRESENTATION\_SWITCH attribute on the topology.</span></span> <span data-ttu-id="21468-115">A hora de início é especificada em unidades de 100 a nanossegundos, em relação ao início da apresentação.</span><span class="sxs-lookup"><span data-stu-id="21468-115">The start time is specified in 100-nanosecond units, relative to the beginning of the presentation.</span></span> <span data-ttu-id="21468-116">Por exemplo, se o valor for 50 milhões, a reprodução iniciará 5 segundos na apresentação.</span><span class="sxs-lookup"><span data-stu-id="21468-116">For example, if the value is 50000000, playback starts 5 seconds into the presentation.</span></span> <span data-ttu-id="21468-117">Se esse atributo não for definido, a hora de início padrão será zero.</span><span class="sxs-lookup"><span data-stu-id="21468-117">If this attribute is not set, the default start time is zero.</span></span>

<span data-ttu-id="21468-118">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="21468-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="21468-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21468-119">Requirements</span></span>



| <span data-ttu-id="21468-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="21468-120">Requirement</span></span> | <span data-ttu-id="21468-121">Valor</span><span class="sxs-lookup"><span data-stu-id="21468-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="21468-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21468-122">Minimum supported client</span></span><br/> | <span data-ttu-id="21468-123">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="21468-123">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="21468-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="21468-124">Minimum supported server</span></span><br/> | <span data-ttu-id="21468-125">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="21468-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="21468-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="21468-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="21468-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="21468-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21468-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="21468-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21468-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="21468-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="21468-130">Atributos de topologia</span><span class="sxs-lookup"><span data-stu-id="21468-130">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




