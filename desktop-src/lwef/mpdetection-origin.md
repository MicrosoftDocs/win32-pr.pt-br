---
title: Enumeração de MPDETECTION_ORIGIN (MpClient. h)
description: Origem da detecção.
ms.assetid: 9FEE2FAD-3E44-4134-B968-53E971F6B092
keywords:
- Recursos do ambiente Windows herdado de enumeração de MPDETECTION_ORIGIN
- PMPDETECTION_ORIGIN recursos de ambiente herdados do ponteiro de enumeração do Windows
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
ms.openlocfilehash: ed4224aafef2c72db2a8d3b27f338ca83feaf64f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105771734"
---
# <a name="mpdetection_origin-enumeration"></a>\_Enumeração de origem MPDETECTION

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

<span id="MPDETECTION_ORIGIN_UNKNOWN"></span><span id="mpdetection_origin_unknown"></span>**\_origem MPDETECTION \_ desconhecida**
</dt> <dd>

A origem detectada era desconhecida.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_LOCAL_MACHINE"></span><span id="mpdetection_origin_local_machine"></span>**\_ \_ máquina local de origem do MPDETECTION \_**
</dt> <dd>

Ameaça detectada no computador local.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_NETWORKSHARE"></span><span id="mpdetection_origin_networkshare"></span>**MPDETECTION \_ Origin \_ NETWORKSHARE**
</dt> <dd>

Ameaça detectada no compartilhamento de rede.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_INTERNET"></span><span id="mpdetection_origin_internet"></span>**\_Internet de origem MPDETECTION \_**
</dt> <dd>

Ameaça detectada na Internet.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_OUTBOUND"></span><span id="mpdetection_origin_outbound"></span>**\_saída de origem MPDETECTION \_**
</dt> <dd>

Ameaça detectada em uma conexão de saída.

</dd> <dt>

<span id="MPDETECTION_ORIGIN_INBOUND"></span><span id="mpdetection_origin_inbound"></span>**\_entrada de origem MPDETECTION \_**
</dt> <dd>

Ameaça detectada em uma conexão de entrada.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





