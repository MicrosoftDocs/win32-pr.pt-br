---
description: 'A enumeração StreamQualityProperty usada pelos métodos ITStreamQualityControl:: GetRange, ITStreamQualityControl:: Get e ITStreamQualityControl:: set para indicar a propriedade de qualidade de fluxo que está sendo endereçada.'
ms.assetid: 28c9257f-6fbb-440f-9b84-c15a74229b5b
title: Enumeração StreamQualityProperty (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea006b614522ffcab6f96e630df03087b78864ff7d7af6ddcd5c515bc090e821
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905746"
---
# <a name="streamqualityproperty-enumeration"></a>Enumeração StreamQualityProperty

\[essa enumeração não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A enumeração **StreamQualityProperty** usada pelos métodos [**ITStreamQualityControl:: GetRange**](itstreamqualitycontrol-getrange.md), [**ITStreamQualityControl:: Get**](itstreamqualitycontrol-get.md)e [**ITStreamQualityControl:: Set**](itstreamqualitycontrol-set.md) para indicar a propriedade de qualidade de fluxo que está sendo endereçada.

## <a name="syntax"></a>Syntax


```C++
} StreamQualityProperty;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="StreamQuality_MaxBitrate"></span><span id="streamquality_maxbitrate"></span><span id="STREAMQUALITY_MAXBITRATE"></span>**StreamQuality \_ MaxBitrate**
</dt> <dd>

Taxa máxima de bits.

</dd> <dt>

<span id="StreamQuality_CurrBitrate"></span><span id="streamquality_currbitrate"></span><span id="STREAMQUALITY_CURRBITRATE"></span>**StreamQuality \_ CurrBitrate**
</dt> <dd>

Taxa mínima de bits.

</dd> <dt>

<span id="StreamQuality_MinFrameInterval"></span><span id="streamquality_minframeinterval"></span><span id="STREAMQUALITY_MINFRAMEINTERVAL"></span>**StreamQuality \_ MinFrameInterval**
</dt> <dd>

Intervalo máximo de quadros.

</dd> <dt>

<span id="StreamQuality_AvgFrameInterval"></span><span id="streamquality_avgframeinterval"></span><span id="STREAMQUALITY_AVGFRAMEINTERVAL"></span>**StreamQuality \_ AvgFrameInterval**
</dt> <dd>

Intervalo mínimo de quadros.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,1<br/>                                                       |
| Cabeçalho<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITStreamQualityControl:: GetRange**](itstreamqualitycontrol-getrange.md)
</dt> <dt>

[**ITStreamQualityControl:: Get**](itstreamqualitycontrol-get.md)
</dt> <dt>

[**ITStreamQualityControl:: Set**](itstreamqualitycontrol-set.md)
</dt> </dl>

 

 




