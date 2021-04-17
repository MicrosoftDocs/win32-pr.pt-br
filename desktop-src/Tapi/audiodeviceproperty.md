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
# <a name="audiodeviceproperty-enumeration"></a>Enumeração AudioDeviceProperty

\[ Essa enumeração não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A enumeração **AudioDeviceProperty** é usada pelos métodos [**ITAudioDeviceControl:: GetRange**](itaudiodevicecontrol-getrange.md), [**ITAudioDeviceControl:: Get**](itaudiodevicecontrol-get.md)e [**ITAudioDeviceControl:: Set**](itaudiodevicecontrol-set.md) para indicar a propriedade que está sendo endereçada.

## <a name="syntax"></a>Syntax


```C++
} AudioDeviceProperty;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="AudioDevice_DuplexMode"></span><span id="audiodevice_duplexmode"></span><span id="AUDIODEVICE_DUPLEXMODE"></span>**AudioDevice \_ duplexmode**
</dt> <dd>

Indica que o modo duplex do dispositivo está sendo definido ou recuperado.

</dd> <dt>

<span id="AudioDevice_AutomaticGainControl"></span><span id="audiodevice_automaticgaincontrol"></span><span id="AUDIODEVICE_AUTOMATICGAINCONTROL"></span>**AudioDevice \_ AutomaticGainControl**
</dt> <dd>

Indica que o controle de lucro automático do dispositivo está sendo definido ou recuperado.

</dd> <dt>

<span id="AudioDevice_AcousticEchoCancellation"></span><span id="audiodevice_acousticechocancellation"></span><span id="AUDIODEVICE_ACOUSTICECHOCANCELLATION"></span>**AudioDevice \_ AcousticEchoCancellation**
</dt> <dd>

Indica que as propriedades de cancelamento de eco acústico do dispositivo estão sendo definidas ou recuperadas.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,1<br/>                                                       |
| parâmetro<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITAudioDeviceControl:: GetRange**](itaudiodevicecontrol-getrange.md)
</dt> <dt>

[**ITAudioDeviceControl:: Get**](itaudiodevicecontrol-get.md)
</dt> <dt>

[**ITAudioDeviceControl:: Set**](itaudiodevicecontrol-set.md)
</dt> </dl>

 

 




