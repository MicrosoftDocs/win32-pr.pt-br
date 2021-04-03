---
title: Enumeração de MPTHREAT_DETECTION (MpClient. h)
description: Possíveis tipos conhecidos de detecção de ameaças inválidas.
ms.assetid: 14FCA9BD-A9A1-488B-B8E8-88DE0DF18F27
keywords:
- Recursos do ambiente Windows herdado de enumeração de MPTHREAT_DETECTION
- PMPTHREAT_DETECTION recursos de ambiente herdados do ponteiro de enumeração do Windows
topic_type:
- apiref
api_name:
- MPTHREAT_DETECTION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86edc0e1ca4ee130f2a2a4a678447771f1ae40ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644526"
---
# <a name="mpthreat_detection-enumeration"></a>Enumeração de detecção de MPTHREAT \_

Possíveis tipos conhecidos de detecção de ameaças inválidas.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPTHREAT_DETECTION { 
  MP_THREAT_DETECTION_CONCRETE    = 0,
  MP_THREAT_DETECTION_HEURISTIC   = 1,
  MP_THREAT_DETECTION_GENERIC     = 2,
  MP_THREAT_DETECTION_SUSPICIOUS  = 4,
  MP_THREAT_DETECTION_FASTPATH    = 8
} MPTHREAT_DETECTION, *PMPTHREAT_DETECTION;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MP_THREAT_DETECTION_CONCRETE"></span><span id="mp_threat_detection_concrete"></span>**\_ \_ concreta detecção de ameaças do MP \_**
</dt> <dd>

A ameaça foi detectada por meio de assinaturas concretas.

</dd> <dt>

<span id="MP_THREAT_DETECTION_HEURISTIC"></span><span id="mp_threat_detection_heuristic"></span>**\_heurística de \_ detecção de ameaças MP \_**
</dt> <dd>

A ameaça foi detectada por meio de heurística.

</dd> <dt>

<span id="MP_THREAT_DETECTION_GENERIC"></span><span id="mp_threat_detection_generic"></span>**detecção de ameaças do MP \_ \_ \_ genérica**
</dt> <dd>

A ameaça foi detectada por meio de assinaturas genéricas.

</dd> <dt>

<span id="MP_THREAT_DETECTION_SUSPICIOUS"></span><span id="mp_threat_detection_suspicious"></span>**detecção de ameaças do MP \_ \_ \_ suspeita**
</dt> <dd>

A ameaça foi detectada por meio do monitoramento de comportamento.

</dd> <dt>

<span id="MP_THREAT_DETECTION_FASTPATH"></span><span id="mp_threat_detection_fastpath"></span>**\_FASTPATH de \_ detecção de ameaças MP \_**
</dt> <dd>

A ameaça foi detectada via FastPath.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





