---
description: 'A enumeração StreamQualityProperty usada pelos métodos ITStreamQualityControl:: GetRange, ITStreamQualityControl:: Get e ITStreamQualityControl:: set para indicar a propriedade de qualidade de fluxo que está sendo endereçada.'
ms.assetid: 28c9257f-6fbb-440f-9b84-c15a74229b5b
title: Enumeração StreamQualityProperty (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f552641cd0847bb3ff8eec9d528a03171a78c2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760327"
---
# <a name="streamqualityproperty-enumeration"></a><span data-ttu-id="005f1-103">Enumeração StreamQualityProperty</span><span class="sxs-lookup"><span data-stu-id="005f1-103">StreamQualityProperty enumeration</span></span>

<span data-ttu-id="005f1-104">\[ Essa enumeração não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="005f1-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="005f1-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="005f1-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="005f1-106">A enumeração **StreamQualityProperty** usada pelos métodos [**ITStreamQualityControl:: GetRange**](itstreamqualitycontrol-getrange.md), [**ITStreamQualityControl:: Get**](itstreamqualitycontrol-get.md)e [**ITStreamQualityControl:: Set**](itstreamqualitycontrol-set.md) para indicar a propriedade de qualidade de fluxo que está sendo endereçada.</span><span class="sxs-lookup"><span data-stu-id="005f1-106">The **StreamQualityProperty** enum used by the [**ITStreamQualityControl::GetRange**](itstreamqualitycontrol-getrange.md), [**ITStreamQualityControl::Get**](itstreamqualitycontrol-get.md), and [**ITStreamQualityControl::Set**](itstreamqualitycontrol-set.md) methods to indicate the stream quality property being addressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="005f1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="005f1-107">Syntax</span></span>


```C++
} StreamQualityProperty;
```



## <a name="constants"></a><span data-ttu-id="005f1-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="005f1-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="005f1-109"><span id="StreamQuality_MaxBitrate"></span><span id="streamquality_maxbitrate"></span><span id="STREAMQUALITY_MAXBITRATE"></span>**StreamQuality \_ MaxBitrate**</span><span class="sxs-lookup"><span data-stu-id="005f1-109"><span id="StreamQuality_MaxBitrate"></span><span id="streamquality_maxbitrate"></span><span id="STREAMQUALITY_MAXBITRATE"></span>**StreamQuality\_MaxBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="005f1-110">Taxa máxima de bits.</span><span class="sxs-lookup"><span data-stu-id="005f1-110">Maximum bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="005f1-111"><span id="StreamQuality_CurrBitrate"></span><span id="streamquality_currbitrate"></span><span id="STREAMQUALITY_CURRBITRATE"></span>**StreamQuality \_ CurrBitrate**</span><span class="sxs-lookup"><span data-stu-id="005f1-111"><span id="StreamQuality_CurrBitrate"></span><span id="streamquality_currbitrate"></span><span id="STREAMQUALITY_CURRBITRATE"></span>**StreamQuality\_CurrBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="005f1-112">Taxa mínima de bits.</span><span class="sxs-lookup"><span data-stu-id="005f1-112">Minimum bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="005f1-113"><span id="StreamQuality_MinFrameInterval"></span><span id="streamquality_minframeinterval"></span><span id="STREAMQUALITY_MINFRAMEINTERVAL"></span>**StreamQuality \_ MinFrameInterval**</span><span class="sxs-lookup"><span data-stu-id="005f1-113"><span id="StreamQuality_MinFrameInterval"></span><span id="streamquality_minframeinterval"></span><span id="STREAMQUALITY_MINFRAMEINTERVAL"></span>**StreamQuality\_MinFrameInterval**</span></span>
</dt> <dd>

<span data-ttu-id="005f1-114">Intervalo máximo de quadros.</span><span class="sxs-lookup"><span data-stu-id="005f1-114">Maximum frame interval.</span></span>

</dd> <dt>

<span data-ttu-id="005f1-115"><span id="StreamQuality_AvgFrameInterval"></span><span id="streamquality_avgframeinterval"></span><span id="STREAMQUALITY_AVGFRAMEINTERVAL"></span>**StreamQuality \_ AvgFrameInterval**</span><span class="sxs-lookup"><span data-stu-id="005f1-115"><span id="StreamQuality_AvgFrameInterval"></span><span id="streamquality_avgframeinterval"></span><span id="STREAMQUALITY_AVGFRAMEINTERVAL"></span>**StreamQuality\_AvgFrameInterval**</span></span>
</dt> <dd>

<span data-ttu-id="005f1-116">Intervalo mínimo de quadros.</span><span class="sxs-lookup"><span data-stu-id="005f1-116">Minimum frame interval.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="005f1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="005f1-117">Requirements</span></span>



| <span data-ttu-id="005f1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="005f1-118">Requirement</span></span> | <span data-ttu-id="005f1-119">Valor</span><span class="sxs-lookup"><span data-stu-id="005f1-119">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="005f1-120">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="005f1-120">TAPI version</span></span><br/> | <span data-ttu-id="005f1-121">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="005f1-121">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="005f1-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="005f1-122">Header</span></span><br/>       | <dl> <span data-ttu-id="005f1-123"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="005f1-123"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="005f1-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="005f1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="005f1-125">**ITStreamQualityControl:: GetRange**</span><span class="sxs-lookup"><span data-stu-id="005f1-125">**ITStreamQualityControl::GetRange**</span></span>](itstreamqualitycontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="005f1-126">**ITStreamQualityControl:: Get**</span><span class="sxs-lookup"><span data-stu-id="005f1-126">**ITStreamQualityControl::Get**</span></span>](itstreamqualitycontrol-get.md)
</dt> <dt>

[<span data-ttu-id="005f1-127">**ITStreamQualityControl:: Set**</span><span class="sxs-lookup"><span data-stu-id="005f1-127">**ITStreamQualityControl::Set**</span></span>](itstreamqualitycontrol-set.md)
</dt> </dl>

 

 




