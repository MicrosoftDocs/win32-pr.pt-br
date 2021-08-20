---
description: A enum AudioSettingsProperty é usada pelos métodos ITAudioSettings::GetRange, ITAudioSettings::Get e ITAudioSettings::Set para indicar a propriedade de configuração de áudio que está sendo resolvida.
ms.assetid: b91c8213-f102-4ebb-ad8a-e43709b3daad
title: Enumeração AudioSettingsProperty (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b15cfb5a0211f02ac333ba75e47b5e4cbd5c44865b4a18c2f19ea3a8769dde3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118871526"
---
# <a name="audiosettingsproperty-enumeration"></a>Enumeração AudioSettingsProperty

\[Essa enumeração não está disponível para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

A enum **AudioSettingsProperty** é usada pelos métodos [**ITAudioSettings::GetRange**](itaudiosettings-getrange.md), [**ITAudioSettings::Get**](itaudiosettings-get.md)e [**ITAudioSettings::Set**](itaudiosettings-set.md) para indicar a propriedade de configuração de áudio que está sendo resolvida.

## <a name="syntax"></a>Syntax


```C++
} AudioSettingsProperty;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="AudioSettings_SignalLevel"></span><span id="audiosettings_signallevel"></span><span id="AUDIOSETTINGS_SIGNALLEVEL"></span>**AudioSettings \_ SignalLevel**
</dt> <dd>

Propriedade configurações de sinal.

</dd> <dt>

<span id="AudioSettings_SilenceThreshold"></span><span id="audiosettings_silencethreshold"></span><span id="AUDIOSETTINGS_SILENCETHRESHOLD"></span>**AudioSettings \_ SilenceThreshold**
</dt> <dd>

Propriedade de limite de silêncio.

</dd> <dt>

<span id="AudioSettings_Volume"></span><span id="audiosettings_volume"></span><span id="AUDIOSETTINGS_VOLUME"></span>**Volume de AudioSettings \_**
</dt> <dd>

Propriedade volume.

</dd> <dt>

<span id="AudioSettings_Balance"></span><span id="audiosettings_balance"></span><span id="AUDIOSETTINGS_BALANCE"></span>**Saldo de \_ AudioSettings**
</dt> <dd>

Propriedade balancear.

</dd> <dt>

<span id="AudioSettings_Loudness"></span><span id="audiosettings_loudness"></span><span id="AUDIOSETTINGS_LOUDNESS"></span>**Intensidade de \_ AudioSettings**
</dt> <dd>

Propriedade de intensidade.

</dd> <dt>

<span id="AudioSettings_Treble"></span><span id="audiosettings_treble"></span><span id="AUDIOSETTINGS_TREBLE"></span>**AudioSettings \_ Treble**
</dt> <dd>

Propriedade treble.

</dd> <dt>

<span id="AudioSettings_Bass"></span><span id="audiosettings_bass"></span><span id="AUDIOSETTINGS_BASS"></span>**AudioSettings \_ Christopher**
</dt> <dd>

Propriedade Deão.

</dd> <dt>

<span id="AudioSettings_Mono"></span><span id="audiosettings_mono"></span><span id="AUDIOSETTINGS_MONO"></span>**AudioSettings \_ Mono**
</dt> <dd>

Propriedadeural.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.1<br/>                                                       |
| Cabeçalho<br/>       | <dl> <dt>Ipmsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITAudioSettings::GetRange**](itaudiosettings-getrange.md)
</dt> <dt>

[**ITAudioSettings::Get**](itaudiosettings-get.md)
</dt> <dt>

[**ITAudioSettings::Set**](itaudiosettings-set.md)
</dt> </dl>

 

 




