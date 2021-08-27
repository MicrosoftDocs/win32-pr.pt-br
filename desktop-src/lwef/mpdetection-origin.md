---
title: MPDETECTION_ORIGIN enumeração (MpClient.h)
description: Origem da detecção.
ms.assetid: 9FEE2FAD-3E44-4134-B968-53E971F6B092
keywords:
- MPDETECTION_ORIGIN de enumeração herdada Windows de ambiente
- PMPDETECTION_ORIGIN de enumeração herdado Windows recursos de ambiente
topic_type:
- apiref
api_name:
- MPDETECTION_ORIGIN
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70b46ed86276ccb3fc3bd4d2b26388d778c102c1c1fa3bb7ced8f1ad64cd0203
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092356"
---
# <a name="mpdetection_origin-enumeration"></a>Enumeração MPDETECTION \_ ORIGIN

Origem da detecção.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPDETECTION_ORIGIN { 
  MPDETECTION_ORIGIN_UNKNOWN        = 0,
  MPDETECTION_ORIGIN_LOCAL_MACHINE  = 1 << 0,
  MPDETECTION_ORIGIN_NETWORKSHARE   = 1 << 1,
  MPDETECTION_ORIGIN_INTERNET       = 1 << 2,
  MPDETECTION_ORIGIN_OUTBOUND       = 1 << 3,
  MPDETECTION_ORIGIN_INBOUND        = 1 << 4
} MPDETECTION_ORIGIN, *PMPDETECTION_ORIGIN;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MPDETECTION_ORIGIN_UNKNOWN"></span><span id="mpdetection_origin_unknown"></span>**MPDETECTION \_ ORIGIN \_ UNKNOWN**
</dt> <dd>

Ameaça detectada de origem desconhecida.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_LOCAL_MACHINE"></span><span id="mpdetection_origin_local_machine"></span>**COMPUTADOR LOCAL DE ORIGEM MPDETECTION \_ \_ \_**
</dt> <dd>

Ameaça detectada no computador local.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_NETWORKSHARE"></span><span id="mpdetection_origin_networkshare"></span>**MPDETECTION \_ ORIGIN \_ NETWORKSHARE**
</dt> <dd>

Ameaça detectada no compartilhamento de rede.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_INTERNET"></span><span id="mpdetection_origin_internet"></span>**INTERNET DE ORIGEM MPDETECTION \_ \_**
</dt> <dd>

Ameaça detectada na Internet.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_OUTBOUND"></span><span id="mpdetection_origin_outbound"></span>**SAÍDA DA ORIGEM DE MPDETECTION \_ \_**
</dt> <dd>

Ameaça detectada em uma conexão de saída.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_INBOUND"></span><span id="mpdetection_origin_inbound"></span>**ENTRADA DE ORIGEM \_ MPDETECTION \_**
</dt> <dd>

Ameaça detectada em uma conexão de entrada.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





