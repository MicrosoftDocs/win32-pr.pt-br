---
description: 'A enumeração AudioDeviceProperty é usada pelos métodos ITAudioDeviceControl:: GetRange, ITAudioDeviceControl:: Get e ITAudioDeviceControl:: set para indicar a propriedade que está sendo endereçada.'
ms.assetid: 0ed9b75e-3c79-4e41-9883-63b85ebfae06
title: Enumeração AudioDeviceProperty (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab807759bfb316858be41ea9bb4b78d795ee1a1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811936"
---
# <a name="audiodeviceproperty-enumeration"></a><span data-ttu-id="abf0d-103">Enumeração AudioDeviceProperty</span><span class="sxs-lookup"><span data-stu-id="abf0d-103">AudioDeviceProperty enumeration</span></span>

<span data-ttu-id="abf0d-104">\[ Essa enumeração não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="abf0d-104">\[ This enumeration is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="abf0d-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="abf0d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="abf0d-106">A enumeração **AudioDeviceProperty** é usada pelos métodos [**ITAudioDeviceControl:: GetRange**](itaudiodevicecontrol-getrange.md), [**ITAudioDeviceControl:: Get**](itaudiodevicecontrol-get.md)e [**ITAudioDeviceControl:: Set**](itaudiodevicecontrol-set.md) para indicar a propriedade que está sendo endereçada.</span><span class="sxs-lookup"><span data-stu-id="abf0d-106">The **AudioDeviceProperty** enum is used by the [**ITAudioDeviceControl::GetRange**](itaudiodevicecontrol-getrange.md), [**ITAudioDeviceControl::Get**](itaudiodevicecontrol-get.md), and [**ITAudioDeviceControl::Set**](itaudiodevicecontrol-set.md) methods to indicate the property being addressed.</span></span>

## <a name="syntax"></a><span data-ttu-id="abf0d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="abf0d-107">Syntax</span></span>


```C++
} AudioDeviceProperty;
```



## <a name="constants"></a><span data-ttu-id="abf0d-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="abf0d-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="abf0d-109"><span id="AudioDevice_DuplexMode"></span><span id="audiodevice_duplexmode"></span><span id="AUDIODEVICE_DUPLEXMODE"></span>**AudioDevice \_ duplexmode**</span><span class="sxs-lookup"><span data-stu-id="abf0d-109"><span id="AudioDevice_DuplexMode"></span><span id="audiodevice_duplexmode"></span><span id="AUDIODEVICE_DUPLEXMODE"></span>**AudioDevice\_DuplexMode**</span></span>
</dt> <dd>

<span data-ttu-id="abf0d-110">Indica que o modo duplex do dispositivo está sendo definido ou recuperado.</span><span class="sxs-lookup"><span data-stu-id="abf0d-110">Indicates that the duplex mode of the device is being set or retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="abf0d-111"><span id="AudioDevice_AutomaticGainControl"></span><span id="audiodevice_automaticgaincontrol"></span><span id="AUDIODEVICE_AUTOMATICGAINCONTROL"></span>**AudioDevice \_ AutomaticGainControl**</span><span class="sxs-lookup"><span data-stu-id="abf0d-111"><span id="AudioDevice_AutomaticGainControl"></span><span id="audiodevice_automaticgaincontrol"></span><span id="AUDIODEVICE_AUTOMATICGAINCONTROL"></span>**AudioDevice\_AutomaticGainControl**</span></span>
</dt> <dd>

<span data-ttu-id="abf0d-112">Indica que o controle de lucro automático do dispositivo está sendo definido ou recuperado.</span><span class="sxs-lookup"><span data-stu-id="abf0d-112">Indicates that the automatic gain control of the device is being set or retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="abf0d-113"><span id="AudioDevice_AcousticEchoCancellation"></span><span id="audiodevice_acousticechocancellation"></span><span id="AUDIODEVICE_ACOUSTICECHOCANCELLATION"></span>**AudioDevice \_ AcousticEchoCancellation**</span><span class="sxs-lookup"><span data-stu-id="abf0d-113"><span id="AudioDevice_AcousticEchoCancellation"></span><span id="audiodevice_acousticechocancellation"></span><span id="AUDIODEVICE_ACOUSTICECHOCANCELLATION"></span>**AudioDevice\_AcousticEchoCancellation**</span></span>
</dt> <dd>

<span data-ttu-id="abf0d-114">Indica que as propriedades de cancelamento de eco acústico do dispositivo estão sendo definidas ou recuperadas.</span><span class="sxs-lookup"><span data-stu-id="abf0d-114">Indicates that the acoustic echo cancellation properties of the device are being set or retrieved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="abf0d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="abf0d-115">Requirements</span></span>



| <span data-ttu-id="abf0d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="abf0d-116">Requirement</span></span> | <span data-ttu-id="abf0d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="abf0d-117">Value</span></span> |
|-------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="abf0d-118">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="abf0d-118">TAPI version</span></span><br/> | <span data-ttu-id="abf0d-119">Requer TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="abf0d-119">Requires TAPI 3.1</span></span><br/>                                                       |
| <span data-ttu-id="abf0d-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="abf0d-120">Header</span></span><br/>       | <dl> <span data-ttu-id="abf0d-121"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="abf0d-121"><dt>Ipmsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abf0d-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="abf0d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abf0d-123">**ITAudioDeviceControl:: GetRange**</span><span class="sxs-lookup"><span data-stu-id="abf0d-123">**ITAudioDeviceControl::GetRange**</span></span>](itaudiodevicecontrol-getrange.md)
</dt> <dt>

[<span data-ttu-id="abf0d-124">**ITAudioDeviceControl:: Get**</span><span class="sxs-lookup"><span data-stu-id="abf0d-124">**ITAudioDeviceControl::Get**</span></span>](itaudiodevicecontrol-get.md)
</dt> <dt>

[<span data-ttu-id="abf0d-125">**ITAudioDeviceControl:: Set**</span><span class="sxs-lookup"><span data-stu-id="abf0d-125">**ITAudioDeviceControl::Set**</span></span>](itaudiodevicecontrol-set.md)
</dt> </dl>

 

 




