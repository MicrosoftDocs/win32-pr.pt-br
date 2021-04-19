---
description: A \_ estrutura Caps de configuração de fluxo de vídeo TAPI \_ \_ \_ está contida \_ na \_ estrutura Caps de configuração de fluxo TAPI \_ quando o membro capstype é definido como o membro VideoCap da União StreamConfigCapsType.
ms.assetid: 8812755a-50e8-4d8e-ab67-7a3a4b2a4a67
title: Estrutura de TAPI_VIDEO_STREAM_CONFIG_CAPS (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 525a35cb7c7332aa4e80fe8d5e2436e75e2d5c08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768563"
---
# <a name="tapi_video_stream_config_caps-structure"></a><span data-ttu-id="c2000-103">\_Estrutura de \_ Caps de configuração de fluxo de vídeo TAPI \_ \_</span><span class="sxs-lookup"><span data-stu-id="c2000-103">TAPI\_VIDEO\_STREAM\_CONFIG\_CAPS structure</span></span>

<span data-ttu-id="c2000-104">\[ Essa estrutura não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c2000-104">\[ This structure is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c2000-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="c2000-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c2000-106">A **estrutura \_ \_ Caps de \_ configuração \_ de fluxo de vídeo TAPI** está contida na estrutura [**\_ \_ \_ Caps de configuração de fluxo TAPI**](tapi-stream-config-caps.md) quando o membro **capstype** é definido como o membro **VideoCap** da União [**StreamConfigCapsType**](streamconfigcapstype.md) .</span><span class="sxs-lookup"><span data-stu-id="c2000-106">The **TAPI\_VIDEO\_STREAM\_CONFIG\_CAPS** structure is contained by the [**TAPI\_STREAM\_CONFIG\_CAPS**](tapi-stream-config-caps.md) structure when the **CapsType** member is set to the **VideoCap** member of the [**StreamConfigCapsType**](streamconfigcapstype.md) union.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2000-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c2000-107">Syntax</span></span>


```C++
} TAPI_VIDEO_STREAM_CONFIG_CAPS;
```



## <a name="members"></a><span data-ttu-id="c2000-108">Membros</span><span class="sxs-lookup"><span data-stu-id="c2000-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c2000-109">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c2000-109">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c2000-110">Uma descrição amigável do tipo de configuração de fluxo de áudio para exibição para usuários do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c2000-110">A friendly description of the audio stream configuration type for display to application users.</span></span>

</dd> <dt>

<span data-ttu-id="c2000-111">**VideoStandard**</span><span class="sxs-lookup"><span data-stu-id="c2000-111">**VideoStandard**</span></span>
</dt> <dd>

<span data-ttu-id="c2000-112">Padrão de vídeo sendo usado.</span><span class="sxs-lookup"><span data-stu-id="c2000-112">Video standard being used.</span></span>

</dd> <dt>

<span data-ttu-id="c2000-113">**Incolocar**</span><span class="sxs-lookup"><span data-stu-id="c2000-113">**InputSize**</span></span>
</dt> <dd>

<span data-ttu-id="c2000-114">Tamanho de entrada do quadro.</span><span class="sxs-lookup"><span data-stu-id="c2000-114">Input size of frame.</span></span>

</dd> <dt>

<span data-ttu-id="c2000-115">**MinCroppingSize**</span><span class="sxs-lookup"><span data-stu-id="c2000-115">**MinCroppingSize**</span></span>
</dt> <dd>

<span data-ttu-id="c2000-116">Tamanho mínimo de corte.</span><span class="sxs-lookup"><span data-stu-id="c2000-116">Minimum cropping size.</span></span>

</dd> <dt>

<span data-ttu-id="c2000-117">**MaxCroppingSize**</span><span class="sxs-lookup"><span data-stu-id="c2000-117">**MaxCroppingSize**</span></span>
</dt> <dd>

<span data-ttu-id="c2000-118">Tamanho máximo de corte.</span><span class="sxs-lookup"><span data-stu-id="c2000-118">Maximum cropping size.</span></span>

</dd> <dt>

<span data-ttu-id="c2000-119">**CropGranularityX**</span><span class="sxs-lookup"><span data-stu-id="c2000-119">**CropGranularityX**</span></span>
</dt> <dd>

<span data-ttu-id="c2000-120">Granularidade do corte permitido ao longo do eixo x.</span><span class="sxs-lookup"><span data-stu-id="c2000-120">Granularity of cropping allowed along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="c2000-121">**CropGranularityY**</span><span class="sxs-lookup"><span data-stu-id="c2000-121">**CropGranularityY**</span></span>
</dt> <dd>

<span data-ttu-id="c2000-122">Granularidade do corte permitido ao longo do eixo y.</span><span class="sxs-lookup"><span data-stu-id="c2000-122">Granularity of cropping allowed along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="c2000-123">**CropAlignX**</span><span class="sxs-lookup"><span data-stu-id="c2000-123">**CropAlignX**</span></span>
</dt> <dd>

<span data-ttu-id="c2000-124">Alinhamento do corte do eixo x.</span><span class="sxs-lookup"><span data-stu-id="c2000-124">Alignment of x-axis cropping.</span></span>

</dd> <dt>

<span data-ttu-id="c2000-125">**CropAlignY**</span><span class="sxs-lookup"><span data-stu-id="c2000-125">**CropAlignY**</span></span>
</dt> <dd>

<span data-ttu-id="c2000-126">Alinhamento do corte do eixo y.</span><span class="sxs-lookup"><span data-stu-id="c2000-126">Alignment of y-axis cropping.</span></span>

</dd> <dt>

<span data-ttu-id="c2000-127">**MinOutputSize**</span><span class="sxs-lookup"><span data-stu-id="c2000-127">**MinOutputSize**</span></span>
</dt> <dd>

<span data-ttu-id="c2000-128">Tamanho mínimo resultante da janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c2000-128">Minimum resultant size of video window.</span></span>

</dd> <dt>

<span data-ttu-id="c2000-129">**MaxOutputSize**</span><span class="sxs-lookup"><span data-stu-id="c2000-129">**MaxOutputSize**</span></span>
</dt> <dd>

<span data-ttu-id="c2000-130">Tamanho máximo resultante da janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c2000-130">Maximum resultant size of video window.</span></span>

</dd> <dt>

<span data-ttu-id="c2000-131">**OutputGranularityX**</span><span class="sxs-lookup"><span data-stu-id="c2000-131">**OutputGranularityX**</span></span>
</dt> <dd>

<span data-ttu-id="c2000-132">Granularidade do tamanho de saída ao longo do eixo x.</span><span class="sxs-lookup"><span data-stu-id="c2000-132">Granularity of output size along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="c2000-133">**OutputGranularityY**</span><span class="sxs-lookup"><span data-stu-id="c2000-133">**OutputGranularityY**</span></span>
</dt> <dd>

<span data-ttu-id="c2000-134">Granularidade do tamanho de saída ao longo do eixo y.</span><span class="sxs-lookup"><span data-stu-id="c2000-134">Granularity of output size along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="c2000-135">**StretchTapsX**</span><span class="sxs-lookup"><span data-stu-id="c2000-135">**StretchTapsX**</span></span>
</dt> <dd>

<span data-ttu-id="c2000-136">Stretch ao longo do eixo x.</span><span class="sxs-lookup"><span data-stu-id="c2000-136">Stretch along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="c2000-137">**StretchTapsY**</span><span class="sxs-lookup"><span data-stu-id="c2000-137">**StretchTapsY**</span></span>
</dt> <dd>

<span data-ttu-id="c2000-138">Stretch ao longo do eixo y.</span><span class="sxs-lookup"><span data-stu-id="c2000-138">Stretch along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="c2000-139">**ShrinkTapsX**</span><span class="sxs-lookup"><span data-stu-id="c2000-139">**ShrinkTapsX**</span></span>
</dt> <dd>

<span data-ttu-id="c2000-140">Reduzir ao longo do eixo x.</span><span class="sxs-lookup"><span data-stu-id="c2000-140">Shrink along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="c2000-141">**ShrinkTapsY**</span><span class="sxs-lookup"><span data-stu-id="c2000-141">**ShrinkTapsY**</span></span>
</dt> <dd>

<span data-ttu-id="c2000-142">Reduzir ao longo do eixo y.</span><span class="sxs-lookup"><span data-stu-id="c2000-142">Shrink along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="c2000-143">**MinFrameInterval**</span><span class="sxs-lookup"><span data-stu-id="c2000-143">**MinFrameInterval**</span></span>
</dt> <dd>

<span data-ttu-id="c2000-144">Intervalo mínimo de quadros de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c2000-144">Minimum video frame interval.</span></span>

</dd> <dt>

<span data-ttu-id="c2000-145">**MaxFrameInterval**</span><span class="sxs-lookup"><span data-stu-id="c2000-145">**MaxFrameInterval**</span></span>
</dt> <dd>

<span data-ttu-id="c2000-146">Intervalo máximo de quadros de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c2000-146">Maximum video frame interval.</span></span>

</dd> <dt>

<span data-ttu-id="c2000-147">**MinBitsPerSecond**</span><span class="sxs-lookup"><span data-stu-id="c2000-147">**MinBitsPerSecond**</span></span>
</dt> <dd>

<span data-ttu-id="c2000-148">Mínimo de bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="c2000-148">Minimum bits per second.</span></span>

</dd> <dt>

<span data-ttu-id="c2000-149">**MaxBitsPerSecond**</span><span class="sxs-lookup"><span data-stu-id="c2000-149">**MaxBitsPerSecond**</span></span>
</dt> <dd>

<span data-ttu-id="c2000-150">Máximo de bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="c2000-150">Maximum bits per second.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c2000-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c2000-151">Requirements</span></span>



| <span data-ttu-id="c2000-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2000-152">Requirement</span></span> | <span data-ttu-id="c2000-153">Valor</span><span class="sxs-lookup"><span data-stu-id="c2000-153">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c2000-154">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="c2000-154">TAPI version</span></span><br/> | <span data-ttu-id="c2000-155">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="c2000-155">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="c2000-156">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c2000-156">Header</span></span><br/>       | <dl> <span data-ttu-id="c2000-157"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2000-157"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2000-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2000-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2000-159">**\_limites de \_ configuração de fluxo TAPI \_**</span><span class="sxs-lookup"><span data-stu-id="c2000-159">**TAPI\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-stream-config-caps.md)
</dt> </dl>

 

 




