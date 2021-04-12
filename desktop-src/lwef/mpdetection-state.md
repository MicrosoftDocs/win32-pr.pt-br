---
title: Enumeração de MPDETECTION_STATE (MpClient. h)
description: O estado da ameaça detectada no momento.
ms.assetid: 293771FF-A210-41D0-88A5-3B52ACAA9295
keywords:
- Recursos do ambiente Windows herdado de enumeração de MPDETECTION_STATE
- PMPDETECTION_STATE recursos de ambiente herdados do ponteiro de enumeração do Windows
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
ms.openlocfilehash: f9265a15641d2072d87b33af2782f17974bf07be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454945"
---
# <a name="mpdetection_state-enumeration"></a>\_Enumeração de estado MPDETECTION

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

<span id="MPDETECTION_STATE_UNKNOWN"></span><span id="mpdetection_state_unknown"></span>**Estado de MPDETECTION \_ \_ desconhecido**
</dt> <dd>

Em um estado de erro.

</dd> <dt>

<span id="MPDETECTION_STATE_ACTIVE"></span><span id="mpdetection_state_active"></span>**\_estado \_ ativo do MPDETECTION**
</dt> <dd>

Ameaça ativa.

</dd> <dt>

<span id="MPDETECTION_STATE_FINISHED"></span><span id="mpdetection_state_finished"></span>**\_estado MPDETECTION \_ concluído**
</dt> <dd>

24 horas pendentes para mover para limpo.

</dd> <dt>

<span id="MPDETECTION_STATE_ADDITIONAL_ACTIONS"></span><span id="mpdetection_state_additional_actions"></span>**\_ \_ ações adicionais de estado MPDETECTION \_**
</dt> <dd>

Ações adicionais necessárias.

</dd> <dt>

<span id="MPDETECTION_STATE_FAILED"></span><span id="mpdetection_state_failed"></span>**\_ \_ falha no estado MPDETECTION**
</dt> <dd>

Falha de correção não crítica.

</dd> <dt>

<span id="MPDETECTION_STATE_CRITICALLY_FAILED"></span><span id="mpdetection_state_critically_failed"></span>**o \_ estado MPDETECTION \_ falhou criticamente \_**
</dt> <dd>

Falha de correção crítica.

</dd> <dt>

<span id="MPDETECTION_STATE_CLEARED"></span><span id="mpdetection_state_cleared"></span>**\_estado MPDETECTION \_ limpo**
</dt> <dd>

A ameaça não aparece na consulta de estado, somente no histórico.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





