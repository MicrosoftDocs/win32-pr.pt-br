---
title: MPDETECTION_STATE enumeração (MpClient.h)
description: O estado da ameaça detectada no momento.
ms.assetid: 293771FF-A210-41D0-88A5-3B52ACAA9295
keywords:
- MPDETECTION_STATE enumeração herdada Windows recursos de ambiente
- PMPDETECTION_STATE de enumeração herdado Windows recursos de ambiente
topic_type:
- apiref
api_name:
- MPDETECTION_STATE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0443e0c47eef4d4943d39bd671c28c19db0ff5e1fbe79e5af8d034603b1ab78d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883513"
---
# <a name="mpdetection_state-enumeration"></a>Enumeração MPDETECTION \_ STATE

O estado da ameaça detectada no momento.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPDETECTION_STATE { 
  MPDETECTION_STATE_UNKNOWN             = 0,
  MPDETECTION_STATE_ACTIVE              = 1,
  MPDETECTION_STATE_FINISHED            = 2,
  MPDETECTION_STATE_ADDITIONAL_ACTIONS  = 3,
  MPDETECTION_STATE_FAILED              = 4,
  MPDETECTION_STATE_CRITICALLY_FAILED   = 5,
  MPDETECTION_STATE_CLEARED             = 6
} MPDETECTION_STATE, *PMPDETECTION_STATE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MPDETECTION_STATE_UNKNOWN"></span><span id="mpdetection_state_unknown"></span>**ESTADO DE MPDETECTION \_ \_ DESCONHECIDO**
</dt> <dd>

Em um estado de erro.

</dd> <dt>

<span id="MPDETECTION_STATE_ACTIVE"></span><span id="mpdetection_state_active"></span>**ESTADO DE MPDETECTION \_ \_ ATIVO**
</dt> <dd>

Ameaça ativa.

</dd> <dt>

<span id="MPDETECTION_STATE_FINISHED"></span><span id="mpdetection_state_finished"></span>**ESTADO DE MPDETECTION \_ \_ CONCLUÍDO**
</dt> <dd>

24 horas pendentes para uma movimentação para desempurada.

</dd> <dt>

<span id="MPDETECTION_STATE_ADDITIONAL_ACTIONS"></span><span id="mpdetection_state_additional_actions"></span>**AÇÕES ADICIONAIS DE ESTADO \_ MPDETECTION \_ \_**
</dt> <dd>

Ações adicionais necessárias.

</dd> <dt>

<span id="MPDETECTION_STATE_FAILED"></span><span id="mpdetection_state_failed"></span>**FALHA NO ESTADO DE MPDETECTION \_ \_**
</dt> <dd>

Falha de correção não crítica.

</dd> <dt>

<span id="MPDETECTION_STATE_CRITICALLY_FAILED"></span><span id="mpdetection_state_critically_failed"></span>**ESTADO DE MPDETECTION \_ \_ COM FALHA \_ CRÍTICA**
</dt> <dd>

Falha de correção crítica.

</dd> <dt>

<span id="MPDETECTION_STATE_CLEARED"></span><span id="mpdetection_state_cleared"></span>**ESTADO DE MPDETECTION \_ \_ LIMPO**
</dt> <dd>

A ameaça não aparece na consulta de estado, somente no histórico.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





