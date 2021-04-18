---
description: 'A enumeração CallQualityProperty é usada pelos métodos ITCallQualityControl:: GetRange, ITCallQualityControl:: Get e ITCallQualityControl:: set para indicar a propriedade de qualidade da chamada que está sendo endereçada.'
ms.assetid: d9a04cc4-9b7d-4b01-918f-e4938c172b8e
title: Enumeração CallQualityProperty (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2ca3af31e0b85a443bb34ac1992b3d3b5c89bfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789875"
---
# <a name="callqualityproperty-enumeration"></a><span data-ttu-id="839f8-103">Enumeração CallQualityProperty</span><span class="sxs-lookup"><span data-stu-id="839f8-103">CallQualityProperty enumeration</span></span>

<span data-ttu-id="839f8-104">\[ Essa enumeração não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="839f8-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="839f8-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="839f8-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="839f8-106">A enumeração **CallQualityProperty** é usada pelos métodos [**ITCallQualityControl:: GetRange**](itcallqualitycontrol-getrange.md), [**ITCallQualityControl:: Get**](itcallqualitycontrol-get.md)e [**ITCallQualityControl:: Set**](itcallqualitycontrol-set.md) para indicar a propriedade de qualidade da chamada que está sendo endereçada.</span><span class="sxs-lookup"><span data-stu-id="839f8-106">The **CallQualityProperty** enum is used by the [**ITCallQualityControl::GetRange**](itcallqualitycontrol-getrange.md), [**ITCallQualityControl::Get**](itcallqualitycontrol-get.md), and [**ITCallQualityControl::Set**](itcallqualitycontrol-set.md) methods to indicate the call quality property being addressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="839f8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="839f8-107">Syntax</span></span>


```C++
} CallQualityProperty;
```



## <a name="constants"></a><span data-ttu-id="839f8-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="839f8-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="839f8-109"><span id="CallQuality_ControlInterval"></span><span id="callquality_controlinterval"></span><span id="CALLQUALITY_CONTROLINTERVAL"></span>**CallQuality \_ ControlInterval**</span><span class="sxs-lookup"><span data-stu-id="839f8-109"><span id="CallQuality_ControlInterval"></span><span id="callquality_controlinterval"></span><span id="CALLQUALITY_CONTROLINTERVAL"></span>**CallQuality\_ControlInterval**</span></span>
</dt> <dd>

<span data-ttu-id="839f8-110">Intervalo de controle.</span><span class="sxs-lookup"><span data-stu-id="839f8-110">Control interval.</span></span>

</dd> <dt>

<span data-ttu-id="839f8-111"><span id="CallQuality_ConfBitrate"></span><span id="callquality_confbitrate"></span><span id="CALLQUALITY_CONFBITRATE"></span>**CallQuality \_ ConfBitrate**</span><span class="sxs-lookup"><span data-stu-id="839f8-111"><span id="CallQuality_ConfBitrate"></span><span id="callquality_confbitrate"></span><span id="CALLQUALITY_CONFBITRATE"></span>**CallQuality\_ConfBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="839f8-112">Taxa de bits para a conferência.</span><span class="sxs-lookup"><span data-stu-id="839f8-112">Bit rate for conference.</span></span>

</dd> <dt>

<span data-ttu-id="839f8-113"><span id="CallQuality_MaxInputBitrate"></span><span id="callquality_maxinputbitrate"></span><span id="CALLQUALITY_MAXINPUTBITRATE"></span>**CallQuality \_ MaxInputBitrate**</span><span class="sxs-lookup"><span data-stu-id="839f8-113"><span id="CallQuality_MaxInputBitrate"></span><span id="callquality_maxinputbitrate"></span><span id="CALLQUALITY_MAXINPUTBITRATE"></span>**CallQuality\_MaxInputBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="839f8-114">Taxa máxima de bits de entrada.</span><span class="sxs-lookup"><span data-stu-id="839f8-114">Maximum input bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="839f8-115"><span id="CallQuality_CurrInputBitrate"></span><span id="callquality_currinputbitrate"></span><span id="CALLQUALITY_CURRINPUTBITRATE"></span>**CallQuality \_ CurrInputBitrate**</span><span class="sxs-lookup"><span data-stu-id="839f8-115"><span id="CallQuality_CurrInputBitrate"></span><span id="callquality_currinputbitrate"></span><span id="CALLQUALITY_CURRINPUTBITRATE"></span>**CallQuality\_CurrInputBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="839f8-116">Taxa de bits de entrada atual.</span><span class="sxs-lookup"><span data-stu-id="839f8-116">Current input bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="839f8-117"><span id="CallQuality_MaxOutputBitrate"></span><span id="callquality_maxoutputbitrate"></span><span id="CALLQUALITY_MAXOUTPUTBITRATE"></span>**CallQuality \_ MaxOutputBitrate**</span><span class="sxs-lookup"><span data-stu-id="839f8-117"><span id="CallQuality_MaxOutputBitrate"></span><span id="callquality_maxoutputbitrate"></span><span id="CALLQUALITY_MAXOUTPUTBITRATE"></span>**CallQuality\_MaxOutputBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="839f8-118">Taxa máxima de bits de saída.</span><span class="sxs-lookup"><span data-stu-id="839f8-118">Maximum output bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="839f8-119"><span id="CallQuality_CurrOutputBitrate"></span><span id="callquality_curroutputbitrate"></span><span id="CALLQUALITY_CURROUTPUTBITRATE"></span>**CallQuality \_ CurrOutputBitrate**</span><span class="sxs-lookup"><span data-stu-id="839f8-119"><span id="CallQuality_CurrOutputBitrate"></span><span id="callquality_curroutputbitrate"></span><span id="CALLQUALITY_CURROUTPUTBITRATE"></span>**CallQuality\_CurrOutputBitrate**</span></span>
</dt> <dd>

<span data-ttu-id="839f8-120">Taxa de bits de saída atual.</span><span class="sxs-lookup"><span data-stu-id="839f8-120">Current output bit rate.</span></span>

</dd> <dt>

<span data-ttu-id="839f8-121"><span id="CallQuality_MaxCPULoad"></span><span id="callquality_maxcpuload"></span><span id="CALLQUALITY_MAXCPULOAD"></span>**CallQuality \_ MaxCPULoad**</span><span class="sxs-lookup"><span data-stu-id="839f8-121"><span id="CallQuality_MaxCPULoad"></span><span id="callquality_maxcpuload"></span><span id="CALLQUALITY_MAXCPULOAD"></span>**CallQuality\_MaxCPULoad**</span></span>
</dt> <dd>

<span data-ttu-id="839f8-122">Carga máxima de CPU.</span><span class="sxs-lookup"><span data-stu-id="839f8-122">Maximum CPU load.</span></span>

</dd> <dt>

<span data-ttu-id="839f8-123"><span id="CallQuality_CurrCPULoad"></span><span id="callquality_currcpuload"></span><span id="CALLQUALITY_CURRCPULOAD"></span>**CallQuality \_ CurrCPULoad**</span><span class="sxs-lookup"><span data-stu-id="839f8-123"><span id="CallQuality_CurrCPULoad"></span><span id="callquality_currcpuload"></span><span id="CALLQUALITY_CURRCPULOAD"></span>**CallQuality\_CurrCPULoad**</span></span>
</dt> <dd>

<span data-ttu-id="839f8-124">Carga de CPU atual.</span><span class="sxs-lookup"><span data-stu-id="839f8-124">Current CPU load.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="839f8-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="839f8-125">Requirements</span></span>



| <span data-ttu-id="839f8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="839f8-126">Requirement</span></span> | <span data-ttu-id="839f8-127">Valor</span><span class="sxs-lookup"><span data-stu-id="839f8-127">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="839f8-128">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="839f8-128">TAPI version</span></span><br/> | <span data-ttu-id="839f8-129">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="839f8-129">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="839f8-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="839f8-130">Header</span></span><br/>       | <dl> <span data-ttu-id="839f8-131"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="839f8-131"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="839f8-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="839f8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="839f8-133">**ITCallQualityControl:: GetRange**</span><span class="sxs-lookup"><span data-stu-id="839f8-133">**ITCallQualityControl::GetRange**</span></span>](itcallqualitycontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="839f8-134">**ITCallQualityControl:: Get**</span><span class="sxs-lookup"><span data-stu-id="839f8-134">**ITCallQualityControl::Get**</span></span>](itcallqualitycontrol-get.md)
</dt> <dt>

[<span data-ttu-id="839f8-135">**ITCallQualityControl:: Set**</span><span class="sxs-lookup"><span data-stu-id="839f8-135">**ITCallQualityControl::Set**</span></span>](itcallqualitycontrol-set.md)
</dt> </dl>

 

 




