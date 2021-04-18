---
description: O tipo de enumeração StreamConfigCapsType é usado pela \_ estrutura de troca de configuração de fluxo TAPI \_ \_ como uma opção para indicar se o streaming de áudio ou vídeo está envolvido.
ms.assetid: c3eec6b2-ce3b-49b1-a0ba-f450d60a1477
title: Enumeração StreamConfigCapsType (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14649edb7e451cdc7d955f2028a77c247148182b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758398"
---
# <a name="streamconfigcapstype-enumeration"></a><span data-ttu-id="b2b8b-103">Enumeração StreamConfigCapsType</span><span class="sxs-lookup"><span data-stu-id="b2b8b-103">StreamConfigCapsType enumeration</span></span>

<span data-ttu-id="b2b8b-104">\[ Essa enumeração não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b2b8b-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b2b8b-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="b2b8b-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b2b8b-106">O tipo de enumeração **StreamConfigCapsType** é usado pela estrutura de troca de [**\_ \_ configuração \_ de fluxo TAPI**](tapi-stream-config-caps.md) como uma opção para indicar se o streaming de áudio ou vídeo está envolvido.</span><span class="sxs-lookup"><span data-stu-id="b2b8b-106">The **StreamConfigCapsType** enumeration type is used by the [**TAPI\_STREAM\_CONFIG\_CAPS**](tapi-stream-config-caps.md) structure as a switch to indicate whether audio or video streaming is involved.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2b8b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2b8b-107">Syntax</span></span>


```C++
} StreamConfigCapsType;
```



## <a name="constants"></a><span data-ttu-id="b2b8b-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="b2b8b-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b2b8b-109"><span id="AudioStreamConfigCaps"></span><span id="audiostreamconfigcaps"></span><span id="AUDIOSTREAMCONFIGCAPS"></span>**AudioStreamConfigCaps**</span><span class="sxs-lookup"><span data-stu-id="b2b8b-109"><span id="AudioStreamConfigCaps"></span><span id="audiostreamconfigcaps"></span><span id="AUDIOSTREAMCONFIGCAPS"></span>**AudioStreamConfigCaps**</span></span>
</dt> <dd>

<span data-ttu-id="b2b8b-110">Configuração de streaming de áudio.</span><span class="sxs-lookup"><span data-stu-id="b2b8b-110">Audio streaming configuration.</span></span>

</dd> <dt>

<span data-ttu-id="b2b8b-111"><span id="VideoStreamConfigCaps"></span><span id="videostreamconfigcaps"></span><span id="VIDEOSTREAMCONFIGCAPS"></span>**VideoStreamConfigCaps**</span><span class="sxs-lookup"><span data-stu-id="b2b8b-111"><span id="VideoStreamConfigCaps"></span><span id="videostreamconfigcaps"></span><span id="VIDEOSTREAMCONFIGCAPS"></span>**VideoStreamConfigCaps**</span></span>
</dt> <dd>

<span data-ttu-id="b2b8b-112">Configuração de streaming de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b2b8b-112">Video streaming configuration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2b8b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2b8b-113">Requirements</span></span>



| <span data-ttu-id="b2b8b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2b8b-114">Requirement</span></span> | <span data-ttu-id="b2b8b-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b2b8b-115">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b2b8b-116">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="b2b8b-116">TAPI version</span></span><br/> | <span data-ttu-id="b2b8b-117">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="b2b8b-117">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="b2b8b-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b2b8b-118">Header</span></span><br/>       | <dl> <span data-ttu-id="b2b8b-119"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2b8b-119"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2b8b-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2b8b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2b8b-121">**\_limites de \_ configuração de fluxo TAPI \_**</span><span class="sxs-lookup"><span data-stu-id="b2b8b-121">**TAPI\_STREAM\_CONFIG\_CAPS**</span></span>](tapi-stream-config-caps.md)
</dt> </dl>

 

 




