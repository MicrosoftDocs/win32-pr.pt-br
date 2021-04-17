---
description: 'A enumeração AudioSettingsProperty é usada pelos métodos ITAudioSettings:: GetRange, ITAudioSettings:: Get e ITAudioSettings:: set para indicar a propriedade de configuração de áudio que está sendo endereçada.'
ms.assetid: b91c8213-f102-4ebb-ad8a-e43709b3daad
title: Enumeração AudioSettingsProperty (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759e3ca9d9559c35c64c117b9b84b1cee4a1fad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759975"
---
# <a name="audiosettingsproperty-enumeration"></a><span data-ttu-id="18d7e-103">Enumeração AudioSettingsProperty</span><span class="sxs-lookup"><span data-stu-id="18d7e-103">AudioSettingsProperty enumeration</span></span>

<span data-ttu-id="18d7e-104">\[ Essa enumeração não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="18d7e-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="18d7e-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="18d7e-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="18d7e-106">A enumeração **AudioSettingsProperty** é usada pelos métodos [**ITAudioSettings:: GetRange**](itaudiosettings-getrange.md), [**ITAudioSettings:: Get**](itaudiosettings-get.md)e [**ITAudioSettings:: Set**](itaudiosettings-set.md) para indicar a propriedade de configuração de áudio que está sendo endereçada.</span><span class="sxs-lookup"><span data-stu-id="18d7e-106">The **AudioSettingsProperty** enum is used by the [**ITAudioSettings::GetRange**](itaudiosettings-getrange.md), [**ITAudioSettings::Get**](itaudiosettings-get.md), and [**ITAudioSettings::Set**](itaudiosettings-set.md) methods to indicate the audio setting property being addressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="18d7e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="18d7e-107">Syntax</span></span>


```C++
} AudioSettingsProperty;
```



## <a name="constants"></a><span data-ttu-id="18d7e-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="18d7e-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="18d7e-109"><span id="AudioSettings_SignalLevel"></span><span id="audiosettings_signallevel"></span><span id="AUDIOSETTINGS_SIGNALLEVEL"></span>**AudioSettings \_ SignalLevel**</span><span class="sxs-lookup"><span data-stu-id="18d7e-109"><span id="AudioSettings_SignalLevel"></span><span id="audiosettings_signallevel"></span><span id="AUDIOSETTINGS_SIGNALLEVEL"></span>**AudioSettings\_SignalLevel**</span></span>
</dt> <dd>

<span data-ttu-id="18d7e-110">Propriedade de configurações de sinal.</span><span class="sxs-lookup"><span data-stu-id="18d7e-110">Signal settings property.</span></span>

</dd> <dt>

<span data-ttu-id="18d7e-111"><span id="AudioSettings_SilenceThreshold"></span><span id="audiosettings_silencethreshold"></span><span id="AUDIOSETTINGS_SILENCETHRESHOLD"></span>**AudioSettings \_ SilenceThreshold**</span><span class="sxs-lookup"><span data-stu-id="18d7e-111"><span id="AudioSettings_SilenceThreshold"></span><span id="audiosettings_silencethreshold"></span><span id="AUDIOSETTINGS_SILENCETHRESHOLD"></span>**AudioSettings\_SilenceThreshold**</span></span>
</dt> <dd>

<span data-ttu-id="18d7e-112">Propriedade de limite de silêncio.</span><span class="sxs-lookup"><span data-stu-id="18d7e-112">Silence threshold property.</span></span>

</dd> <dt>

<span data-ttu-id="18d7e-113"><span id="AudioSettings_Volume"></span><span id="audiosettings_volume"></span><span id="AUDIOSETTINGS_VOLUME"></span>**\_Volume AudioSettings**</span><span class="sxs-lookup"><span data-stu-id="18d7e-113"><span id="AudioSettings_Volume"></span><span id="audiosettings_volume"></span><span id="AUDIOSETTINGS_VOLUME"></span>**AudioSettings\_Volume**</span></span>
</dt> <dd>

<span data-ttu-id="18d7e-114">Propriedade de volume.</span><span class="sxs-lookup"><span data-stu-id="18d7e-114">Volume property.</span></span>

</dd> <dt>

<span data-ttu-id="18d7e-115"><span id="AudioSettings_Balance"></span><span id="audiosettings_balance"></span><span id="AUDIOSETTINGS_BALANCE"></span>**Saldo de AudioSettings \_**</span><span class="sxs-lookup"><span data-stu-id="18d7e-115"><span id="AudioSettings_Balance"></span><span id="audiosettings_balance"></span><span id="AUDIOSETTINGS_BALANCE"></span>**AudioSettings\_Balance**</span></span>
</dt> <dd>

<span data-ttu-id="18d7e-116">Propriedade Balance.</span><span class="sxs-lookup"><span data-stu-id="18d7e-116">Balance property.</span></span>

</dd> <dt>

<span data-ttu-id="18d7e-117"><span id="AudioSettings_Loudness"></span><span id="audiosettings_loudness"></span><span id="AUDIOSETTINGS_LOUDNESS"></span>**Intensidade de AudioSettings \_**</span><span class="sxs-lookup"><span data-stu-id="18d7e-117"><span id="AudioSettings_Loudness"></span><span id="audiosettings_loudness"></span><span id="AUDIOSETTINGS_LOUDNESS"></span>**AudioSettings\_Loudness**</span></span>
</dt> <dd>

<span data-ttu-id="18d7e-118">Propriedade de intensidade.</span><span class="sxs-lookup"><span data-stu-id="18d7e-118">Loudness property.</span></span>

</dd> <dt>

<span data-ttu-id="18d7e-119"><span id="AudioSettings_Treble"></span><span id="audiosettings_treble"></span><span id="AUDIOSETTINGS_TREBLE"></span>**AudioSettings \_ agudos**</span><span class="sxs-lookup"><span data-stu-id="18d7e-119"><span id="AudioSettings_Treble"></span><span id="audiosettings_treble"></span><span id="AUDIOSETTINGS_TREBLE"></span>**AudioSettings\_Treble**</span></span>
</dt> <dd>

<span data-ttu-id="18d7e-120">Propriedade agudos.</span><span class="sxs-lookup"><span data-stu-id="18d7e-120">Treble property.</span></span>

</dd> <dt>

<span data-ttu-id="18d7e-121"><span id="AudioSettings_Bass"></span><span id="audiosettings_bass"></span><span id="AUDIOSETTINGS_BASS"></span>**AudioSettings \_ Bass**</span><span class="sxs-lookup"><span data-stu-id="18d7e-121"><span id="AudioSettings_Bass"></span><span id="audiosettings_bass"></span><span id="AUDIOSETTINGS_BASS"></span>**AudioSettings\_Bass**</span></span>
</dt> <dd>

<span data-ttu-id="18d7e-122">Propriedade Bass.</span><span class="sxs-lookup"><span data-stu-id="18d7e-122">Bass property.</span></span>

</dd> <dt>

<span data-ttu-id="18d7e-123"><span id="AudioSettings_Mono"></span><span id="audiosettings_mono"></span><span id="AUDIOSETTINGS_MONO"></span>**AudioSettings \_ mono**</span><span class="sxs-lookup"><span data-stu-id="18d7e-123"><span id="AudioSettings_Mono"></span><span id="audiosettings_mono"></span><span id="AUDIOSETTINGS_MONO"></span>**AudioSettings\_Mono**</span></span>
</dt> <dd>

<span data-ttu-id="18d7e-124">Propriedade monaural.</span><span class="sxs-lookup"><span data-stu-id="18d7e-124">Monaural property.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18d7e-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="18d7e-125">Requirements</span></span>



| <span data-ttu-id="18d7e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="18d7e-126">Requirement</span></span> | <span data-ttu-id="18d7e-127">Valor</span><span class="sxs-lookup"><span data-stu-id="18d7e-127">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="18d7e-128">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="18d7e-128">TAPI version</span></span><br/> | <span data-ttu-id="18d7e-129">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="18d7e-129">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="18d7e-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="18d7e-130">Header</span></span><br/>       | <dl> <span data-ttu-id="18d7e-131"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="18d7e-131"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18d7e-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="18d7e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18d7e-133">**ITAudioSettings:: GetRange**</span><span class="sxs-lookup"><span data-stu-id="18d7e-133">**ITAudioSettings::GetRange**</span></span>](itaudiosettings-getrange.md)
</dt> <dt>

[<span data-ttu-id="18d7e-134">**ITAudioSettings:: Get**</span><span class="sxs-lookup"><span data-stu-id="18d7e-134">**ITAudioSettings::Get**</span></span>](itaudiosettings-get.md)
</dt> <dt>

[<span data-ttu-id="18d7e-135">**ITAudioSettings:: Set**</span><span class="sxs-lookup"><span data-stu-id="18d7e-135">**ITAudioSettings::Set**</span></span>](itaudiosettings-set.md)
</dt> </dl>

 

 




