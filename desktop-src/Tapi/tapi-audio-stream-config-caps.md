---
description: A \_ estrutura de \_ Caps config do fluxo de áudio TAPI \_ \_ está contida na \_ estrutura Caps de configuração do fluxo TAPI \_ \_ quando o membro capstype é definido como o membro AudioCap da União StreamConfigCapsType.
ms.assetid: 61575839-4604-4c8b-ae4d-fe796c3c5314
title: Estrutura de TAPI_AUDIO_STREAM_CONFIG_CAPS (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: daec587a8e760bedd3ab9c6b3469ef8f70b72383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780588"
---
# <a name="tapi_audio_stream_config_caps-structure"></a><span data-ttu-id="3113b-103">\_Estrutura de \_ Caps de configuração de fluxo de áudio TAPI \_ \_</span><span class="sxs-lookup"><span data-stu-id="3113b-103">TAPI\_AUDIO\_STREAM\_CONFIG\_CAPS structure</span></span>

<span data-ttu-id="3113b-104">\[ Essa estrutura não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="3113b-104">\[ This structure is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3113b-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="3113b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="3113b-106">A estrutura de **\_ \_ \_ \_ Caps config do fluxo de áudio TAPI** está contida na estrutura [**\_ \_ \_ Caps de configuração do fluxo TAPI**](tapi-stream-config-caps.md) quando o membro **capstype** é definido como o membro **AudioCap** da União [**StreamConfigCapsType**](streamconfigcapstype.md) .</span><span class="sxs-lookup"><span data-stu-id="3113b-106">The **TAPI\_AUDIO\_STREAM\_CONFIG\_CAPS** structure is contained by the [**TAPI\_STREAM\_CONFIG\_CAPS**](tapi-stream-config-caps.md) structure when the **CapsType** member is set to the **AudioCap** member of the [**StreamConfigCapsType**](streamconfigcapstype.md) union.</span></span>

## <a name="syntax"></a><span data-ttu-id="3113b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3113b-107">Syntax</span></span>


```C++
} TAPI_AUDIO_STREAM_CONFIG_CAPS;
```



## <a name="members"></a><span data-ttu-id="3113b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="3113b-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3113b-109">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3113b-109">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="3113b-110">Uma descrição amigável do tipo de configuração de fluxo de áudio para exibição para usuários do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3113b-110">A friendly description of the audio stream configuration type for display to application users.</span></span>

</dd> <dt>

<span data-ttu-id="3113b-111">**MinimumChannels**</span><span class="sxs-lookup"><span data-stu-id="3113b-111">**MinimumChannels**</span></span>
</dt> <dd>

<span data-ttu-id="3113b-112">O número mínimo de canais associados ao fluxo.</span><span class="sxs-lookup"><span data-stu-id="3113b-112">The minimum number of channels associated with the stream.</span></span>

</dd> <dt>

<span data-ttu-id="3113b-113">**MaximumChannels**</span><span class="sxs-lookup"><span data-stu-id="3113b-113">**MaximumChannels**</span></span>
</dt> <dd>

<span data-ttu-id="3113b-114">O número máximo de canais associados ao fluxo.</span><span class="sxs-lookup"><span data-stu-id="3113b-114">The maximum number of channels associated with the stream.</span></span>

</dd> <dt>

<span data-ttu-id="3113b-115">**ChannelsGranularity**</span><span class="sxs-lookup"><span data-stu-id="3113b-115">**ChannelsGranularity**</span></span>
</dt> <dd>

<span data-ttu-id="3113b-116">A granularidade da contagem de canais.</span><span class="sxs-lookup"><span data-stu-id="3113b-116">The granularity of the channel count.</span></span>

</dd> <dt>

<span data-ttu-id="3113b-117">**MinimumBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="3113b-117">**MinimumBitsPerSample**</span></span>
</dt> <dd>

<span data-ttu-id="3113b-118">O número mínimo de bits por amostra.</span><span class="sxs-lookup"><span data-stu-id="3113b-118">The minimum number of bits per sample.</span></span>

</dd> <dt>

<span data-ttu-id="3113b-119">**MaximumBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="3113b-119">**MaximumBitsPerSample**</span></span>
</dt> <dd>

<span data-ttu-id="3113b-120">O número máximo de bits por amostra.</span><span class="sxs-lookup"><span data-stu-id="3113b-120">The maximum number of bits per sample.</span></span>

</dd> <dt>

<span data-ttu-id="3113b-121">**BitsPerSampleGranularity**</span><span class="sxs-lookup"><span data-stu-id="3113b-121">**BitsPerSampleGranularity**</span></span>
</dt> <dd>

<span data-ttu-id="3113b-122">A granularidade dos bits por valores de exemplo.</span><span class="sxs-lookup"><span data-stu-id="3113b-122">The granularity of the bits per sample values.</span></span>

</dd> <dt>

<span data-ttu-id="3113b-123">**MinimumSampleFrequency**</span><span class="sxs-lookup"><span data-stu-id="3113b-123">**MinimumSampleFrequency**</span></span>
</dt> <dd>

<span data-ttu-id="3113b-124">A frequência de amostragem mínima.</span><span class="sxs-lookup"><span data-stu-id="3113b-124">The minimum sampling frequency.</span></span>

</dd> <dt>

<span data-ttu-id="3113b-125">**MaximumSampleFrequency**</span><span class="sxs-lookup"><span data-stu-id="3113b-125">**MaximumSampleFrequency**</span></span>
</dt> <dd>

<span data-ttu-id="3113b-126">A frequência de amostragem máxima.</span><span class="sxs-lookup"><span data-stu-id="3113b-126">The maximum sampling frequency.</span></span>

</dd> <dt>

<span data-ttu-id="3113b-127">**SampleFrequencyGranularity**</span><span class="sxs-lookup"><span data-stu-id="3113b-127">**SampleFrequencyGranularity**</span></span>
</dt> <dd>

<span data-ttu-id="3113b-128">A granularidade dos valores de frequência de amostragem.</span><span class="sxs-lookup"><span data-stu-id="3113b-128">The granularity of the sampling frequency values.</span></span>

</dd> <dt>

<span data-ttu-id="3113b-129">**MinimumAvgBytesPerSec**</span><span class="sxs-lookup"><span data-stu-id="3113b-129">**MinimumAvgBytesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="3113b-130">A média mínima de bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="3113b-130">The minimum average bytes per second.</span></span>

</dd> <dt>

<span data-ttu-id="3113b-131">**MaximumAvgBytesPerSec**</span><span class="sxs-lookup"><span data-stu-id="3113b-131">**MaximumAvgBytesPerSec**</span></span>
</dt> <dd>

<span data-ttu-id="3113b-132">A média máxima de bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="3113b-132">The maximum average bytes per second.</span></span>

</dd> <dt>

<span data-ttu-id="3113b-133">**AvgBytesPerSecGranularity**</span><span class="sxs-lookup"><span data-stu-id="3113b-133">**AvgBytesPerSecGranularity**</span></span>
</dt> <dd>

<span data-ttu-id="3113b-134">A granularidade dos valores de bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="3113b-134">The granularity of the bytes per second values.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3113b-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3113b-135">Requirements</span></span>



| <span data-ttu-id="3113b-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="3113b-136">Requirement</span></span> | <span data-ttu-id="3113b-137">Valor</span><span class="sxs-lookup"><span data-stu-id="3113b-137">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3113b-138">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="3113b-138">TAPI version</span></span><br/> | <span data-ttu-id="3113b-139">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="3113b-139">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="3113b-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3113b-140">Header</span></span><br/>       | <dl> <span data-ttu-id="3113b-141"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3113b-141"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3113b-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="3113b-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3113b-143">**\_limites de \_ configuração de fluxo TAPI \_**</span><span class="sxs-lookup"><span data-stu-id="3113b-143">**TAPI\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-stream-config-caps.md)
</dt> </dl>

 

 




