---
title: Estrutura de MPTHREAT_INFO (MpClient. h)
description: Contém informações sobre uma ameaça.
ms.assetid: ED2A0BDB-0E7C-479D-ADA1-95B9A259F57E
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPTHREAT_INFO
- Ponteiro de estrutura de PMPTHREAT_INFO recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPTHREAT_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfa850a4293006a2f4b107a3f2579fdc14c1ea6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455820"
---
# <a name="mpthreat_info-structure"></a>Estrutura de informações do MPTHREAT \_

Contém informações sobre uma ameaça.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPTHREAT_INFO {
  MPTHREAT_ID           ThreatID;
  GUID                  DetectionID;
  MP_MIDL_STRING LPWSTR Name;
  MPTHREAT_TYPE         ThreatType;
  MPTHREAT_SEVERITY     ThreatCriticality;
  MPTHREAT_CATEGORY     ThreatCategory;
  DWORD                 ThreatShortDescriptionID;
  DWORD                 ThreatAdviseDescriptionID;
  MPTHREAT_STATUS       ThreatStatus;
  DWORD                 SuggestedActionCount;
  MPTHREAT_ACTION       SuggestedActionArray[MP_MAX_SUGGESTIONS];
  DWORD                 ResourceCount;
  PMPRESOURCE_INFO      *ResourceList[ResourceCount];
  ULARGE_INTEGER        ThreatStatusTime;
  HRESULT               ThreatStatusCode;
  MPTHREAT_DETECTION    ThreatDetection;
  GUID                  QuarantineGuid;
  MPEXECUTION_STATUS    ExecutionStatus;
  union {
    PMPTHREAT_INFOEX_UNUSED   pKnownBad;
    PMPTHREAT_INFOEX_BEHAVIOR pBehavior;
    PMPTHREAT_INFOEX_UNUSED   pUnknown;
    PMPTHREAT_INFOEX_UNUSED   pKnownGood;
    PMPTHREAT_INFOEX_NIS      pNis;
  } Data;
  MPDETECTION_STATE     State;
  MP_MIDL_STRING LPWSTR DetectionUser;
  MPSOURCE              DetectionSource;
  MP_MIDL_STRING LPWSTR ProcessName;
  MPDETECTION_ORIGIN    DetectionOrigin;
  DWORD                 reserved1;
  ULARGE_INTEGER        DetectionTime;
  MPEXECUTION_STATUS    PreExecutionStatus;
  ULARGE_INTEGER        RemediationTime;
  MPEXECUTION_STATUS    PostExecutionStatus;
  BOOL                  CriticalFailure;
  DWORD                 NonCriticalReason;
  MP_MIDL_STRING LPWSTR RemediationUser;
  DWORD                 RemediationResourceCount;
  PMPRESOURCE_INFO      RemediationResourceList[RemediationResourceCount];
  BOOL                  FailureResolved;
  MPRESOLVED_REASON     ResolvedReason;
  DWORD                 AdditionalActions;
  DWORD                 ResolvedActions;
  DWORD                 dwThreatStatusFlag;
} MPTHREAT_INFO, *PMPTHREAT_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**Threatid**
</dt> <dd>

Tipo: **\_ ID de MPTHREAT**

</dd> <dd>

Identificador de ameaça. O bit superior é definido para identificar ameaças relacionadas ao antivírus.

</dd> <dt>

**Detectid**
</dt> <dd>

Tipo: **GUID**

</dd> <dd>

ID de detecção.

</dd> <dt>

**Nome**
</dt> <dd>

Tipo: **PG \_ MIDL \_ String LPWSTR**

</dd> <dd>

Nome da ameaça.

</dd> <dt>

**Threattype**
</dt> <dd>

Tipo: **[ **\_ tipo de MPTHREAT**](mpthreat-type.md)**

</dd> <dd>

Tipo de ameaça. Usado para diferenciar entre diferentes tipos de ameaças, como conhecido, desconhecido ou conhecido como válido. Consulte [**\_ tipo de MPTHREAT**](mpthreat-type.md).

</dd> <dt>

**ThreatCriticality**
</dt> <dd>

Tipo: **[ **\_ severidade MPTHREAT**](mpthreat-severity.md)**

</dd> <dd>

Criticalidade da ameaça. Consulte [**\_ severidade do MPTHREAT**](mpthreat-severity.md).

</dd> <dt>

**ThreatCategory**
</dt> <dd>

Tipo: **[ **\_ categoria MPTHREAT**](mpthreat-category.md)**

</dd> <dd>

Categoria de ameaça, como um cavalo de Troia ou um keylogger. Consulte [**a \_ categoria MPTHREAT**](mpthreat-category.md).

</dd> <dt>

**ThreatShortDescriptionID**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

ID da descrição curta da ameaça.

</dd> <dt>

**ThreatAdviseDescriptionID**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

ID da descrição do aviso de ameaça.

</dd> <dt>

**ThreatStatus**
</dt> <dd>

Tipo: **[ **MPTHREAT \_ status**](mpthreat-status.md)**

</dd> <dd>

Status de ameaça, como detectado, limpo ou em quarentena. Consulte [**\_ status do MPTHREAT**](mpthreat-status.md).

</dd> <dt>

**SuggestedActionCount**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Contagem de ações sugeridas em **SuggestedActionArray**.

</dd> <dt>

**SuggestedActionArray**
</dt> <dd>

Tipo: **[**MPTHREAT \_ Action**](mpthreat-action.md) \[ MP \_ Max \_ sugestões\]**

</dd> <dd>

Matriz de ações sugeridas. Consulte [**a \_ ação MPTHREAT**](mpthreat-action.md).

</dd> <dt>

**ResourceCount**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Contagem de recursos na **resourceList**.

</dd> <dt>

**ResourceList**
</dt> <dd>

Tipo: **PMPRESOURCE \_ info \** _

</dd> <dd>

Lista de recursos identificados com a ameaça. Consulte [_ *MPRESOURCE \_ info* *](mpresource-info.md).

</dd> <dt>

**ThreatStatusTime**
</dt> <dd>

Tipo: **ULARGE \_ inteiro**

</dd> <dd>

Hora em que o status da ameaça foi alterado pela última vez.

</dd> <dt>

**ThreatStatusCode**
</dt> <dd>

Tipo: **HRESULT**

</dd> <dd>

Código de status associado ao status da ameaça.

</dd> <dt>

**ThreatDetection**
</dt> <dd>

Tipo: **[ **\_ detecção de MPTHREAT**](mpthreat-detection.md)**

</dd> <dd>

Tipo de detecção de ameaças, como concreto, suspeita ou genérico. Consulte [**\_ detecção de MPTHREAT**](mpthreat-detection.md).

</dd> <dt>

**QuarantineGuid**
</dt> <dd>

Tipo: **GUID**

</dd> <dd>

GUID de quarentena.

</dd> <dt>

**ExecutionStatus**
</dt> <dd>

Tipo: **[ **MPEXECUTION \_ status**](mpexecution-status.md)**

</dd> <dd>

Status de execução da ameaça, como não conhecido, bloqueado ou ativo. Consulte [**\_ status do MPEXECUTION**](mpexecution-status.md).

</dd> <dt>

**Dados**
</dt> <dd>

Informações adicionais. O ponteiro para a estrutura apropriada depende do valor de **threattype**.

<dl> <dt>

**pKnownBad**
</dt> <dd>

Tipo: **PMPTHREAT \_ INFOEX \_ não utilizado**

</dd> <dd>

Quando **threattype**  ==  **MPTHREAT, \_ digite \_ KNOWNBAD**. Consulte [**MPTHREAT \_ INFOEX \_ não used**](mpthreat-infoex-unused.md).

</dd> <dt>

**pBehavior**
</dt> <dd>

Tipo: **PMPTHREAT \_ INFOEX \_ Behavior**

</dd> <dd>

Quando **threattype**  ==  **MPTHREAT \_ tipo \_ Behavior**. Consulte [**\_ \_ comportamento do MPTHREAT INFOEX**](mpthreat-infoex-behavior.md).

</dd> <dt>

**pUnknown**
</dt> <dd>

Tipo: **PMPTHREAT \_ INFOEX \_ não utilizado**

</dd> <dd>

Quando **threattype**  ==  **MPTHREAT \_ tipo \_ desconhecido**. Consulte [**MPTHREAT \_ INFOEX \_ não used**](mpthreat-infoex-unused.md).

</dd> <dt>

**pKnownGood**
</dt> <dd>

Tipo: **PMPTHREAT \_ INFOEX \_ não utilizado**

</dd> <dd>

Quando **threattype** = = MPTHREAT, \_ digite \_ KNOWNGOOD. Consulte [**MPTHREAT \_ INFOEX \_ não used**](mpthreat-infoex-unused.md).

</dd> <dt>

**pNis**
</dt> <dd>

Tipo: **PMPTHREAT \_ INFOEX \_ NIS**

</dd> <dd>

Quando **threattype**  ==  **MPTHREAT \_ tipo \_ NIS**. Consulte [**MPTHREAT \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md).

</dd> </dl> </dd> <dt>

**State**
</dt> <dd>

Tipo: **[ **\_ estado MPDETECTION**](mpdetection-state.md)**

</dd> <dd>

O estado atual da detecção. Consulte [**\_ estado MPDETECTION**](mpdetection-state.md).

</dd> <dt>

**DetectionUser**
</dt> <dd>

Tipo: **PG \_ MIDL \_ String LPWSTR**

</dd> <dd>

O usuário associado à detecção, no formato "domínio/usuário".

</dd> <dt>

**Detecção de**
</dt> <dd>

Tipo: **[ **MPSOURCE**](mpsource.md)**

</dd> <dd>

A origem da detecção. Consulte [**MPSOURCE**](mpsource.md).

</dd> <dt>

**ProcessName**
</dt> <dd>

Tipo: **PG \_ MIDL \_ String LPWSTR**

</dd> <dd>

Nome do processo associado à detecção.

</dd> <dt>

**DetectionOrigin**
</dt> <dd>

Tipo: **[ **\_ origem do MPDETECTION**](mpdetection-origin.md)**

</dd> <dd>

A origem da detecção, como local ou rede. Consulte [**MPDETECTION \_ Origin**](mpdetection-origin.md).

</dd> <dt>

**reserved1**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Metadados reservados sobre a detecção.

</dd> <dt>

**Detecçãotime**
</dt> <dd>

Tipo: **ULARGE \_ inteiro**

</dd> <dd>

A hora da detecção inicial.

</dd> <dt>

**PreExecutionStatus**
</dt> <dd>

Tipo: **[ **MPEXECUTION \_ status**](mpexecution-status.md)**

</dd> <dd>

Status de execução logo antes da correção. Consulte [**\_ status do MPEXECUTION**](mpexecution-status.md).

</dd> <dt>

**Remediatime**
</dt> <dd>

Tipo: **ULARGE \_ inteiro**

</dd> <dd>

A correção de tempo ocorreu.

</dd> <dt>

**PostExecutionStatus**
</dt> <dd>

Tipo: **[ **MPEXECUTION \_ status**](mpexecution-status.md)**

</dd> <dd>

Status da execução após a correção. Consulte [**\_ status do MPEXECUTION**](mpexecution-status.md).

</dd> <dt>

**CriticalFailure**
</dt> <dd>

Tipo: **bool**

</dd> <dd>

True se a falha de correção for crítica.

</dd> <dt>

**NonCriticalReason**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

O motivo pelo qual a falha de correção não é crítica. Não há garantia de que haja suporte para isso no futuro.

</dd> <dt>

**RemediationUser**
</dt> <dd>

Tipo: **PG \_ MIDL \_ String LPWSTR**

</dd> <dd>

Usuário que solicitou a correção, no formato "domínio/usuário".

</dd> <dt>

**RemediationResourceCount**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Contagem de recursos no **RemediationResourceList**.

</dd> <dt>

**RemediationResourceList**
</dt> <dd>

Tipo: **PMPRESOURCE \_ info \[ RemediationResourceCount \]**

</dd> <dd>

Lista de recursos que falharam durante a correção. Consulte [**MPRESOURCE \_ info**](mpresource-info.md).

</dd> <dt>

**FailureResolved**
</dt> <dd>

Tipo: **bool**

</dd> <dd>

True se a falha de correção tiver sido resolvida. Isso moverá o Bucket para uma ação completa ou adicional.

</dd> <dt>

**ResolvedReason**
</dt> <dd>

Tipo: **[ **MPRESOLVED \_ motivo**](mpresolved-reason.md)**

</dd> <dd>

Motivo para a falha de correção ser resolvida. Esse é o motivo pelo qual a detecção foi movida de falha para uma ação adicional ou foi concluída. Consulte [**o \_ motivo do MPRESOLVED**](mpresolved-reason.md).

</dd> <dt>

**AdditionalActions**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

São necessárias ações adicionais.

</dd> <dt>

**ResolvedActions**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Qualquer ação adicional que tenha sido executada.

</dd> <dt>

**dwThreatStatusFlag**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Informações adicionais sobre a detecção de ameaças.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MpFreeMemory**](mpfreememory.md)
</dt> <dt>

[**MpThreatEnumerate**](mpthreatenumerate.md)
</dt> <dt>

[**MpThreatQuery**](mpthreatquery.md)
</dt> <dt>

[**origem do MPDETECTION \_**](mpdetection-origin.md)
</dt> <dt>

[**\_estado MPDETECTION**](mpdetection-state.md)
</dt> <dt>

[**STATUS do MPEXECUTION \_**](mpexecution-status.md)
</dt> <dt>

[**motivo do MPRESOLVED \_**](mpresolved-reason.md)
</dt> <dt>

[**informações de MPRESOURCE \_**](mpresource-info.md)
</dt> <dt>

[**MPSOURCE**](mpsource.md)
</dt> <dt>

[**\_ação MPTHREAT**](mpthreat-action.md)
</dt> <dt>

[**\_categoria MPTHREAT**](mpthreat-category.md)
</dt> <dt>

[**detecção de MPTHREAT \_**](mpthreat-detection.md)
</dt> <dt>

[**\_comportamento MPTHREAT INFOEX \_**](mpthreat-infoex-behavior.md)
</dt> <dt>

[**MPTHREAT \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md)
</dt> <dt>

[**MPTHREAT \_ INFOEX \_ não usado**](mpthreat-infoex-unused.md)
</dt> <dt>

[**severidade de MPTHREAT \_**](mpthreat-severity.md)
</dt> <dt>

[**STATUS do MPTHREAT \_**](mpthreat-status.md)
</dt> <dt>

[**tipo de MPTHREAT \_**](mpthreat-type.md)
</dt> </dl>

 

 





