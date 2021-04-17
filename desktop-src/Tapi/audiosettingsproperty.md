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
# <a name="audiosettingsproperty-enumeration"></a>Enumeração AudioSettingsProperty

\[ Essa enumeração não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A enumeração **AudioSettingsProperty** é usada pelos métodos [**ITAudioSettings:: GetRange**](itaudiosettings-getrange.md), [**ITAudioSettings:: Get**](itaudiosettings-get.md)e [**ITAudioSettings:: Set**](itaudiosettings-set.md) para indicar a propriedade de configuração de áudio que está sendo endereçada.

## <a name="syntax"></a>Syntax


```C++
} AudioSettingsProperty;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="AudioSettings_SignalLevel"></span><span id="audiosettings_signallevel"></span><span id="AUDIOSETTINGS_SIGNALLEVEL"></span>**AudioSettings \_ SignalLevel**
</dt> <dd>

Propriedade de configurações de sinal.

</dd> <dt>

<span id="AudioSettings_SilenceThreshold"></span><span id="audiosettings_silencethreshold"></span><span id="AUDIOSETTINGS_SILENCETHRESHOLD"></span>**AudioSettings \_ SilenceThreshold**
</dt> <dd>

Propriedade de limite de silêncio.

</dd> <dt>

<span id="AudioSettings_Volume"></span><span id="audiosettings_volume"></span><span id="AUDIOSETTINGS_VOLUME"></span>**\_Volume AudioSettings**
</dt> <dd>

Propriedade de volume.

</dd> <dt>

<span id="AudioSettings_Balance"></span><span id="audiosettings_balance"></span><span id="AUDIOSETTINGS_BALANCE"></span>**Saldo de AudioSettings \_**
</dt> <dd>

Propriedade Balance.

</dd> <dt>

<span id="AudioSettings_Loudness"></span><span id="audiosettings_loudness"></span><span id="AUDIOSETTINGS_LOUDNESS"></span>**Intensidade de AudioSettings \_**
</dt> <dd>

Propriedade de intensidade.

</dd> <dt>

<span id="AudioSettings_Treble"></span><span id="audiosettings_treble"></span><span id="AUDIOSETTINGS_TREBLE"></span>**AudioSettings \_ agudos**
</dt> <dd>

Propriedade agudos.

</dd> <dt>

<span id="AudioSettings_Bass"></span><span id="audiosettings_bass"></span><span id="AUDIOSETTINGS_BASS"></span>**AudioSettings \_ Bass**
</dt> <dd>

Propriedade Bass.

</dd> <dt>

<span id="AudioSettings_Mono"></span><span id="audiosettings_mono"></span><span id="AUDIOSETTINGS_MONO"></span>**AudioSettings \_ mono**
</dt> <dd>

Propriedade monaural.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,1<br/>                                                       |
| parâmetro<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITAudioSettings:: GetRange**](itaudiosettings-getrange.md)
</dt> <dt>

[**ITAudioSettings:: Get**](itaudiosettings-get.md)
</dt> <dt>

[**ITAudioSettings:: Set**](itaudiosettings-set.md)
</dt> </dl>

 

 




