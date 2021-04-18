---
description: Especifica se o carregador de topologia habilita o processador de vídeo transcodificar (XVP). para conversões, habilitando a conversão de cores acelerada por hardware.
title: Atributo MF_TOPOLOGY_ENABLE_XVP_FOR_PLAYBACK (Mfidl. h)
ms.topic: reference
ms.date: 02/22/2021
ms.openlocfilehash: e36841db57e8343248ef5e369915d4bc357815bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105764348"
---
# <a name="mf_topology_enable_xvp_for_playback-attribute"></a><span data-ttu-id="c1c3d-104">\_Topologia MF \_ habilitar \_ XVP \_ para \_ atributo de reprodução</span><span class="sxs-lookup"><span data-stu-id="c1c3d-104">MF\_TOPOLOGY\_ENABLE\_XVP\_FOR\_PLAYBACK attribute</span></span>

<span data-ttu-id="c1c3d-105">Especifica se o carregador de topologia habilita o processador de vídeo transcodificar (XVP).</span><span class="sxs-lookup"><span data-stu-id="c1c3d-105">Specifies whether the topology loader enables the Transcode Video Processor (XVP).</span></span> <span data-ttu-id="c1c3d-106">para conversões, habilitando a conversão de cores acelerada por hardware.</span><span class="sxs-lookup"><span data-stu-id="c1c3d-106">for conversions, enabling hardware accelerated color conversion.</span></span>

## <a name="data-type"></a><span data-ttu-id="c1c3d-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c1c3d-107">Data type</span></span>

<span data-ttu-id="c1c3d-108">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="c1c3d-108">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="c1c3d-109">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="c1c3d-109">Get/set</span></span>

<span data-ttu-id="c1c3d-110">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="c1c3d-110">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="c1c3d-111">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="c1c3d-111">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="c1c3d-112">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="c1c3d-112">Applies to</span></span>

[<span data-ttu-id="c1c3d-113">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="c1c3d-113">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="c1c3d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c1c3d-114">Remarks</span></span>

<span data-ttu-id="c1c3d-115">Se esse atributo for definido, o carregador de topologia efetuará o Pull do processador de vídeo, se necessário, durante a resolução da topologia sem transcodificação.</span><span class="sxs-lookup"><span data-stu-id="c1c3d-115">If this attribute is set, the topology loader will pull in the video processor, if necessary, during non-transcode topology resolution.</span></span> <span data-ttu-id="c1c3d-116">Quando você estiver usando a topologia para criar seu próprio [IMFTopology](/windows/win32/api/mfidl/nn-mfidl-imftopology) , esse atributo instruirá o carregador a usar o XVP para conversões em vez do conversor de cores herdado, habilitando, assim, a conversão de cores acelerada por hardware; o conversor de cores herdado é somente para software.</span><span class="sxs-lookup"><span data-stu-id="c1c3d-116">When you are using the topology to build your own [IMFTopology](/windows/win32/api/mfidl/nn-mfidl-imftopology) this attribute tells the loader to use XVP for conversions instead of the legacy color converter, thus enabling hardware accelerated color conversion; the legacy color converter is software-only.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1c3d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c1c3d-117">Requirements</span></span>



| <span data-ttu-id="c1c3d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c1c3d-118">Requirement</span></span> | <span data-ttu-id="c1c3d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="c1c3d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c1c3d-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1c3d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c1c3d-121">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c1c3d-121">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c1c3d-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c1c3d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c1c3d-123">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="c1c3d-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c1c3d-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c1c3d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c1c3d-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c1c3d-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c1c3d-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="c1c3d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1c3d-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c1c3d-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c1c3d-128">Gerenciador de Dispositivos Direct3D</span><span class="sxs-lookup"><span data-stu-id="c1c3d-128">Direct3D Device Manager</span></span>](direct3d-device-manager.md)
</dt> <dt>

[<span data-ttu-id="c1c3d-129">Atributos de topologia</span><span class="sxs-lookup"><span data-stu-id="c1c3d-129">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




