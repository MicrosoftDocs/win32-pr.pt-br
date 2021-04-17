---
description: A estrutura de Caps de configuração de \_ fluxo TAPI \_ \_ contém informações de configuração de fluxo de áudio ou vídeo.
ms.assetid: 83b39751-b00f-4762-830b-13cafbcb1cfd
title: Estrutura de TAPI_STREAM_CONFIG_CAPS (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379ca481d3bebaf8ceb11bfc2dbdab6642ca20b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789843"
---
# <a name="tapi_stream_config_caps-structure"></a><span data-ttu-id="cd4de-103">\_Estrutura de \_ Caps de configuração de fluxo TAPI \_</span><span class="sxs-lookup"><span data-stu-id="cd4de-103">TAPI\_STREAM\_CONFIG\_CAPS structure</span></span>

<span data-ttu-id="cd4de-104">\[ Essa estrutura não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="cd4de-104">\[ This structure is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cd4de-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="cd4de-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="cd4de-106">A estrutura de **\_ \_ \_ Caps** de configuração de fluxo TAPI contém informações de configuração de fluxo de áudio ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="cd4de-106">The **TAPI\_STREAM\_CONFIG\_CAPS** structure contains either video or audio stream configuration information.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd4de-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd4de-107">Syntax</span></span>


```C++
} TAPI_STREAM_CONFIG_CAPS, *PTAPI_STREAM_CONFIG_CAPS;
```



## <a name="members"></a><span data-ttu-id="cd4de-108">Membros</span><span class="sxs-lookup"><span data-stu-id="cd4de-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="cd4de-109">**Capstype**</span><span class="sxs-lookup"><span data-stu-id="cd4de-109">**CapsType**</span></span>
</dt> <dd>

<span data-ttu-id="cd4de-110">Define se o membro de União contém informações de vídeo ou áudio.</span><span class="sxs-lookup"><span data-stu-id="cd4de-110">Defines whether the union member contains video or audio information.</span></span>

</dd> <dt>

<span data-ttu-id="cd4de-111">**VideoCap**</span><span class="sxs-lookup"><span data-stu-id="cd4de-111">**VideoCap**</span></span>
</dt> <dd>

<span data-ttu-id="cd4de-112">Uma [**estrutura \_ \_ Caps de \_ configuração \_ de fluxo de vídeo TAPI**](tapi-video-stream-config-caps.md) que contém os recursos de fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="cd4de-112">A [**TAPI\_VIDEO\_STREAM\_CONFIG\_CAPS**](tapi-video-stream-config-caps.md) structure containing the video stream capabilities.</span></span>

</dd> <dt>

<span data-ttu-id="cd4de-113">**AudioCap**</span><span class="sxs-lookup"><span data-stu-id="cd4de-113">**AudioCap**</span></span>
</dt> <dd>

<span data-ttu-id="cd4de-114">Uma estrutura de [**limites de configuração de \_ fluxo de áudio \_ \_ \_ TAPI**](tapi-audio-stream-config-caps.md) que contém os recursos de fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="cd4de-114">A [**TAPI\_AUDIO\_STREAM\_CONFIG\_CAPS**](tapi-audio-stream-config-caps.md) structure containing the audio stream capabilities.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cd4de-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd4de-115">Requirements</span></span>



| <span data-ttu-id="cd4de-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd4de-116">Requirement</span></span> | <span data-ttu-id="cd4de-117">Valor</span><span class="sxs-lookup"><span data-stu-id="cd4de-117">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cd4de-118">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="cd4de-118">TAPI version</span></span><br/> | <span data-ttu-id="cd4de-119">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="cd4de-119">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="cd4de-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cd4de-120">Header</span></span><br/>       | <dl> <span data-ttu-id="cd4de-121"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd4de-121"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd4de-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd4de-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd4de-123">**ITFormatControl::GetStreamCaps**</span><span class="sxs-lookup"><span data-stu-id="cd4de-123">**ITFormatControl::GetStreamCaps**</span></span>](itformatcontrol-getstreamcaps.md)
</dt> <dt>

[<span data-ttu-id="cd4de-124">**StreamConfigCapsType**</span><span class="sxs-lookup"><span data-stu-id="cd4de-124">**StreamConfigCapsType**</span></span>](streamconfigcapstype.md)
</dt> <dt>

[<span data-ttu-id="cd4de-125">**\_limites de \_ configuração de fluxo de vídeo TAPI \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cd4de-125">**TAPI\_VIDEO\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-video-stream-config-caps.md)
</dt> <dt>

[<span data-ttu-id="cd4de-126">**\_limites de \_ configuração do fluxo de áudio TAPI \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cd4de-126">**TAPI\_AUDIO\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-audio-stream-config-caps.md)
</dt> </dl>

 

 




