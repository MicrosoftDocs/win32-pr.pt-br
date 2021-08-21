---
description: A enum CallQualityProperty é usada pelos métodos ITCallQualityControl::GetRange, ITCallQualityControl::Get e ITCallQualityControl::Set para indicar a propriedade de qualidade de chamada que está sendo resolvida.
ms.assetid: d9a04cc4-9b7d-4b01-918f-e4938c172b8e
title: Enumeração CallQualityProperty (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 767a322d4a65b09acbcf1ff6e0ad4bad84c4a653f2d0f5fd1b207e99592315aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118869831"
---
# <a name="callqualityproperty-enumeration"></a>Enumeração CallQualityProperty

\[Essa enumeração não está disponível para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

A **enum CallQualityProperty** é usada pelos métodos [**ITCallQualityControl::GetRange**](itcallqualitycontrol-getrange.md), [**ITCallQualityControl::Get**](itcallqualitycontrol-get.md)e [**ITCallQualityControl::Set**](itcallqualitycontrol-set.md) para indicar a propriedade de qualidade de chamada que está sendo resolvida.

## <a name="syntax"></a>Syntax


```C++
} CallQualityProperty;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="CallQuality_ControlInterval"></span><span id="callquality_controlinterval"></span><span id="CALLQUALITY_CONTROLINTERVAL"></span>**Controle de \_ Igualdade de ChamadaInterval**
</dt> <dd>

Intervalo de controle.

</dd> <dt>

<span id="CallQuality_ConfBitrate"></span><span id="callquality_confbitrate"></span><span id="CALLQUALITY_CONFBITRATE"></span>**CallQuality \_ ConfBitrate**
</dt> <dd>

Taxa de bits para conferência.

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

Carga máxima da CPU.

</dd> <dt>

<span id="CallQuality_CurrCPULoad"></span><span id="callquality_currcpuload"></span><span id="CALLQUALITY_CURRCPULOAD"></span>**\_CurrCPULoad de Igualdade de Chamada**
</dt> <dd>

Carga atual da CPU.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.1<br/>                                                       |
| Cabeçalho<br/>       | <dl> <dt>Ipmsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITCallQualityControl::GetRange**](itcallqualitycontrol-getrange.md)
</dt> <dt>

[**ITCallQualityControl::Get**](itcallqualitycontrol-get.md)
</dt> <dt>

[**ITCallQualityControl::Set**](itcallqualitycontrol-set.md)
</dt> </dl>

 

 




