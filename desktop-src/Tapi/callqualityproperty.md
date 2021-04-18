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
# <a name="callqualityproperty-enumeration"></a>Enumeração CallQualityProperty

\[ Essa enumeração não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A enumeração **CallQualityProperty** é usada pelos métodos [**ITCallQualityControl:: GetRange**](itcallqualitycontrol-getrange.md), [**ITCallQualityControl:: Get**](itcallqualitycontrol-get.md)e [**ITCallQualityControl:: Set**](itcallqualitycontrol-set.md) para indicar a propriedade de qualidade da chamada que está sendo endereçada.

## <a name="syntax"></a>Syntax


```C++
} CallQualityProperty;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="CallQuality_ControlInterval"></span><span id="callquality_controlinterval"></span><span id="CALLQUALITY_CONTROLINTERVAL"></span>**CallQuality \_ ControlInterval**
</dt> <dd>

Intervalo de controle.

</dd> <dt>

<span id="CallQuality_ConfBitrate"></span><span id="callquality_confbitrate"></span><span id="CALLQUALITY_CONFBITRATE"></span>**CallQuality \_ ConfBitrate**
</dt> <dd>

Taxa de bits para a conferência.

</dd> <dt>

<span id="CallQuality_MaxInputBitrate"></span><span id="callquality_maxinputbitrate"></span><span id="CALLQUALITY_MAXINPUTBITRATE"></span>**CallQuality \_ MaxInputBitrate**
</dt> <dd>

Taxa máxima de bits de entrada.

</dd> <dt>

<span id="CallQuality_CurrInputBitrate"></span><span id="callquality_currinputbitrate"></span><span id="CALLQUALITY_CURRINPUTBITRATE"></span>**CallQuality \_ CurrInputBitrate**
</dt> <dd>

Taxa de bits de entrada atual.

</dd> <dt>

<span id="CallQuality_MaxOutputBitrate"></span><span id="callquality_maxoutputbitrate"></span><span id="CALLQUALITY_MAXOUTPUTBITRATE"></span>**CallQuality \_ MaxOutputBitrate**
</dt> <dd>

Taxa máxima de bits de saída.

</dd> <dt>

<span id="CallQuality_CurrOutputBitrate"></span><span id="callquality_curroutputbitrate"></span><span id="CALLQUALITY_CURROUTPUTBITRATE"></span>**CallQuality \_ CurrOutputBitrate**
</dt> <dd>

Taxa de bits de saída atual.

</dd> <dt>

<span id="CallQuality_MaxCPULoad"></span><span id="callquality_maxcpuload"></span><span id="CALLQUALITY_MAXCPULOAD"></span>**CallQuality \_ MaxCPULoad**
</dt> <dd>

Carga máxima de CPU.

</dd> <dt>

<span id="CallQuality_CurrCPULoad"></span><span id="callquality_currcpuload"></span><span id="CALLQUALITY_CURRCPULOAD"></span>**CallQuality \_ CurrCPULoad**
</dt> <dd>

Carga de CPU atual.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,1<br/>                                                       |
| parâmetro<br/>       | <dl> <dt>Ipmsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITCallQualityControl:: GetRange**](itcallqualitycontrol-getrange.md)
</dt> <dt>

[**ITCallQualityControl:: Get**](itcallqualitycontrol-get.md)
</dt> <dt>

[**ITCallQualityControl:: Set**](itcallqualitycontrol-set.md)
</dt> </dl>

 

 




