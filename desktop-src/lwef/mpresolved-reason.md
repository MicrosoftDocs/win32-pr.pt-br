---
title: Enumeração de MPRESOLVED_REASON (MpClient. h)
description: Possíveis motivos para uma falha de correção ser resolvida.
ms.assetid: 29E875D7-97DA-4129-AB71-B261CD0E682A
keywords:
- Recursos do ambiente Windows herdado de enumeração de MPRESOLVED_REASON
- PMPRESOLVED_REASON recursos de ambiente herdados do ponteiro de enumeração do Windows
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
ms.openlocfilehash: ab31fc8b734852ccdf15278f535d916228b43976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009533"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





