---
description: A enum AudioDeviceProperty é usada pelos métodos ITAudioDeviceControl::GetRange, ITAudioDeviceControl::Get e ITAudioDeviceControl::Set para indicar a propriedade que está sendo endereçada.
ms.assetid: 0ed9b75e-3c79-4e41-9883-63b85ebfae06
title: Enumeração AudioDeviceProperty (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a634caa627f5d518e8783ce056e89a69931aa981466754a9d320f36787186f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117948788"
---
# <a name="audiodeviceproperty-enumeration"></a>Enumeração AudioDeviceProperty

\[Essa enumeração não está disponível para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

A enum **AudioDeviceProperty** é usada pelos métodos [**ITAudioDeviceControl::GetRange**](itaudiodevicecontrol-getrange.md), [**ITAudioDeviceControl::Get**](itaudiodevicecontrol-get.md)e [**ITAudioDeviceControl::Set**](itaudiodevicecontrol-set.md) para indicar a propriedade que está sendo resolvida.

## <a name="syntax"></a>Syntax


```C++
} AudioDeviceProperty;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="AudioDevice_DuplexMode"></span><span id="audiodevice_duplexmode"></span><span id="AUDIODEVICE_DUPLEXMODE"></span>**AudioDevice \_ DuplexMode**
</dt> <dd>

Indica que o modo duplex do dispositivo está sendo definido ou recuperado.

</dd> <dt>

<span id="AudioDevice_AutomaticGainControl"></span><span id="audiodevice_automaticgaincontrol"></span><span id="AUDIODEVICE_AUTOMATICGAINCONTROL"></span>**AudioDevice \_ AutomaticGainControl**
</dt> <dd>

Indica que o controle de ganho automático do dispositivo está sendo definido ou recuperado.

</dd> <dt>

<span id="AudioDevice_AcousticEchoCancellation"></span><span id="audiodevice_acousticechocancellation"></span><span id="AUDIODEVICE_ACOUSTICECHOCANCELLATION"></span>**AudioDevice \_ AcousticEchoCancellation**
</dt> <dd>

Indica que as propriedades de cancelamento de eco acústico do dispositivo estão sendo definidas ou recuperadas.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.1<br/>                                                       |
| Cabeçalho<br/>       | <dl> <dt>Ipmsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITAudioDeviceControl::GetRange**](itaudiodevicecontrol-getrange.md)
</dt> <dt>

[**ITAudioDeviceControl::Get**](itaudiodevicecontrol-get.md)
</dt> <dt>

[**ITAudioDeviceControl::Set**](itaudiodevicecontrol-set.md)
</dt> </dl>

 

 




