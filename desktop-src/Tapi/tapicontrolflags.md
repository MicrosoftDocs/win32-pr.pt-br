---
description: A enumeração TAPIControlFlags é usada por vários métodos para indicar se uma determinada propriedade é controlada automaticamente ou manualmente.
ms.assetid: 48259444-bf7b-4f0e-9068-2bdf89dde694
title: Enumeração TAPIControlFlags (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07cc3e931c69a408d996fa28e6002b6c53c9df87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788043"
---
# <a name="tapicontrolflags-enumeration"></a><span data-ttu-id="23ebf-103">Enumeração TAPIControlFlags</span><span class="sxs-lookup"><span data-stu-id="23ebf-103">TAPIControlFlags enumeration</span></span>

<span data-ttu-id="23ebf-104">\[ Essa enumeração não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="23ebf-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="23ebf-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="23ebf-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="23ebf-106">A enumeração **TAPIControlFlags** é usada por vários métodos para indicar se uma determinada propriedade é controlada automaticamente ou manualmente.</span><span class="sxs-lookup"><span data-stu-id="23ebf-106">The **TAPIControlFlags** enum is used by a number of methods to indicate whether a given property is controlled automatically or manually.</span></span>

## <a name="syntax"></a><span data-ttu-id="23ebf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="23ebf-107">Syntax</span></span>


```C++
} TAPIControlFlags;
```



## <a name="constants"></a><span data-ttu-id="23ebf-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="23ebf-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="23ebf-109"><span id="TAPIControl_Flags_None"></span><span id="tapicontrol_flags_none"></span><span id="TAPICONTROL_FLAGS_NONE"></span>**TAPIControl \_ flags \_ None**</span><span class="sxs-lookup"><span data-stu-id="23ebf-109"><span id="TAPIControl_Flags_None"></span><span id="tapicontrol_flags_none"></span><span id="TAPICONTROL_FLAGS_NONE"></span>**TAPIControl\_Flags\_None**</span></span>
</dt> <dd>

<span data-ttu-id="23ebf-110">A TAPI não tem sinalizadores de controle para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="23ebf-110">TAPI has no control flags for the property.</span></span>

</dd> <dt>

<span data-ttu-id="23ebf-111"><span id="TAPIControl_Flags_Auto"></span><span id="tapicontrol_flags_auto"></span><span id="TAPICONTROL_FLAGS_AUTO"></span>**TAPIControl \_ sinalizadores \_ automáticos**</span><span class="sxs-lookup"><span data-stu-id="23ebf-111"><span id="TAPIControl_Flags_Auto"></span><span id="tapicontrol_flags_auto"></span><span id="TAPICONTROL_FLAGS_AUTO"></span>**TAPIControl\_Flags\_Auto**</span></span>
</dt> <dd>

<span data-ttu-id="23ebf-112">A propriedade é controlada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="23ebf-112">The property is controlled automatically.</span></span>

</dd> <dt>

<span data-ttu-id="23ebf-113"><span id="TAPIControl_Flags_Manual"></span><span id="tapicontrol_flags_manual"></span><span id="TAPICONTROL_FLAGS_MANUAL"></span>**\_Manual de sinalizadores TAPIControl \_**</span><span class="sxs-lookup"><span data-stu-id="23ebf-113"><span id="TAPIControl_Flags_Manual"></span><span id="tapicontrol_flags_manual"></span><span id="TAPICONTROL_FLAGS_MANUAL"></span>**TAPIControl\_Flags\_Manual**</span></span>
</dt> <dd>

<span data-ttu-id="23ebf-114">A propriedade é controlada manualmente.</span><span class="sxs-lookup"><span data-stu-id="23ebf-114">The property is controlled manually.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="23ebf-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23ebf-115">Requirements</span></span>



| <span data-ttu-id="23ebf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="23ebf-116">Requirement</span></span> | <span data-ttu-id="23ebf-117">Valor</span><span class="sxs-lookup"><span data-stu-id="23ebf-117">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="23ebf-118">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="23ebf-118">TAPI version</span></span><br/> | <span data-ttu-id="23ebf-119">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="23ebf-119">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="23ebf-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="23ebf-120">Header</span></span><br/>       | <dl> <span data-ttu-id="23ebf-121"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="23ebf-121"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23ebf-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="23ebf-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23ebf-123">**ITAudioDeviceControl:: GetRange**</span><span class="sxs-lookup"><span data-stu-id="23ebf-123">**ITAudioDeviceControl::GetRange**</span></span>](itaudiodevicecontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="23ebf-124">**ITAudioDeviceControl:: Get**</span><span class="sxs-lookup"><span data-stu-id="23ebf-124">**ITAudioDeviceControl::Get**</span></span>](itaudiodevicecontrol-get.md)
</dt> <dt>

[<span data-ttu-id="23ebf-125">**ITAudioDeviceControl:: Set**</span><span class="sxs-lookup"><span data-stu-id="23ebf-125">**ITAudioDeviceControl::Set**</span></span>](itaudiodevicecontrol-set.md)
</dt> <dt>

[<span data-ttu-id="23ebf-126">**ITAudioSettings:: GetRange**</span><span class="sxs-lookup"><span data-stu-id="23ebf-126">**ITAudioSettings::GetRange**</span></span>](itaudiosettings-getrange.md)
</dt> <dt>

[<span data-ttu-id="23ebf-127">**ITAudioSettings:: Get**</span><span class="sxs-lookup"><span data-stu-id="23ebf-127">**ITAudioSettings::Get**</span></span>](itaudiosettings-get.md)
</dt> <dt>

[<span data-ttu-id="23ebf-128">**ITAudioSettings:: Set**</span><span class="sxs-lookup"><span data-stu-id="23ebf-128">**ITAudioSettings::Set**</span></span>](itaudiosettings-set.md)
</dt> <dt>

[<span data-ttu-id="23ebf-129">**ITCallQualityControl:: GetRange**</span><span class="sxs-lookup"><span data-stu-id="23ebf-129">**ITCallQualityControl::GetRange**</span></span>](itcallqualitycontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="23ebf-130">**ITCallQualityControl:: Get**</span><span class="sxs-lookup"><span data-stu-id="23ebf-130">**ITCallQualityControl::Get**</span></span>](itcallqualitycontrol-get.md)
</dt> <dt>

[<span data-ttu-id="23ebf-131">**ITCallQualityControl:: Set**</span><span class="sxs-lookup"><span data-stu-id="23ebf-131">**ITCallQualityControl::Set**</span></span>](itcallqualitycontrol-set.md)
</dt> <dt>

[<span data-ttu-id="23ebf-132">**ITStreamQualityControl:: GetRange**</span><span class="sxs-lookup"><span data-stu-id="23ebf-132">**ITStreamQualityControl::GetRange**</span></span>](itstreamqualitycontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="23ebf-133">**ITStreamQualityControl:: Get**</span><span class="sxs-lookup"><span data-stu-id="23ebf-133">**ITStreamQualityControl::Get**</span></span>](itstreamqualitycontrol-get.md)
</dt> <dt>

[<span data-ttu-id="23ebf-134">**ITStreamQualityControl:: Set**</span><span class="sxs-lookup"><span data-stu-id="23ebf-134">**ITStreamQualityControl::Set**</span></span>](itstreamqualitycontrol-set.md)
</dt> </dl>

 

 




