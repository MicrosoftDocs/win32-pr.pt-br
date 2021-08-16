---
title: Enumeração de MPRESOLVED_REASON (MpClient. h)
description: Possíveis motivos para uma falha de correção ser resolvida.
ms.assetid: 29E875D7-97DA-4129-AB71-B261CD0E682A
keywords:
- recursos do ambiente de Windows herdado de enumeração de MPRESOLVED_REASON
- Windows recursos de ambiente herdados do ponteiro de enumeração PMPRESOLVED_REASON
topic_type:
- apiref
api_name:
- MPRESOLVED_REASON
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a365ef55d9fe2d76e619f3c772cc1df2e6c5e1c8c33721f24dc844d064b33398
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975976"
---
# <a name="mpresolved_reason-enumeration"></a>\_Enumeração de motivo MPRESOLVED

Possíveis motivos para uma falha de correção ser resolvida.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPRESOLVED_REASON { 
  MPRESOLVED_REASON_UNKNOWN    = 0,
  MPRESOLVED_REASON_FULL_SCAN  = 1,
  MPRESOLVED_REASON_TIMED_OUT  = 2
} MPRESOLVED_REASON, *PMPRESOLVED_REASON;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MPRESOLVED_REASON_UNKNOWN"></span><span id="mpresolved_reason_unknown"></span>**\_motivo MPRESOLVED \_ desconhecido**
</dt> <dd>

Em um estado de erro.

</dd> <dt>

<span id="MPRESOLVED_REASON_FULL_SCAN"></span><span id="mpresolved_reason_full_scan"></span>**\_ \_ verificação completa do motivo do MPRESOLVED \_**
</dt> <dd>

Uma verificação completa foi executada.

</dd> <dt>

<span id="MPRESOLVED_REASON_TIMED_OUT"></span><span id="mpresolved_reason_timed_out"></span>**o \_ motivo do MPRESOLVED \_ atingiu o tempo \_ limite**
</dt> <dd>

Tempo suficiente aprovado. O padrão é uma semana.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





