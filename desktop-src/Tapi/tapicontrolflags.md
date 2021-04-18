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
# <a name="tapicontrolflags-enumeration"></a>Enumeração TAPIControlFlags

\[ Essa enumeração não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A enumeração **TAPIControlFlags** é usada por vários métodos para indicar se uma determinada propriedade é controlada automaticamente ou manualmente.

## <a name="syntax"></a>Syntax


```C++
} TAPIControlFlags;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="TAPIControl_Flags_None"></span><span id="tapicontrol_flags_none"></span><span id="TAPICONTROL_FLAGS_NONE"></span>**TAPIControl \_ flags \_ None**
</dt> <dd>

A TAPI não tem sinalizadores de controle para a propriedade.

</dd> <dt>

<span id="TAPIControl_Flags_Auto"></span><span id="tapicontrol_flags_auto"></span><span id="TAPICONTROL_FLAGS_AUTO"></span>**TAPIControl \_ sinalizadores \_ automáticos**
</dt> <dd>

A propriedade é controlada automaticamente.

</dd> <dt>

<span id="TAPIControl_Flags_Manual"></span><span id="tapicontrol_flags_manual"></span><span id="TAPICONTROL_FLAGS_MANUAL"></span>**\_Manual de sinalizadores TAPIControl \_**
</dt> <dd>

A propriedade é controlada manualmente.

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
</dt> <dt>

[**ITAudioSettings:: GetRange**](itaudiosettings-getrange.md)
</dt> <dt>

[**ITAudioSettings:: Get**](itaudiosettings-get.md)
</dt> <dt>

[**ITAudioSettings:: Set**](itaudiosettings-set.md)
</dt> <dt>

[**ITCallQualityControl:: GetRange**](itcallqualitycontrol-getrange.md)
</dt> <dt>

[**ITCallQualityControl:: Get**](itcallqualitycontrol-get.md)
</dt> <dt>

[**ITCallQualityControl:: Set**](itcallqualitycontrol-set.md)
</dt> <dt>

[**ITStreamQualityControl:: GetRange**](itstreamqualitycontrol-getrange.md)
</dt> <dt>

[**ITStreamQualityControl:: Get**](itstreamqualitycontrol-get.md)
</dt> <dt>

[**ITStreamQualityControl:: Set**](itstreamqualitycontrol-set.md)
</dt> </dl>

 

 




