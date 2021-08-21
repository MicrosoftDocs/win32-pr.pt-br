---
title: Enumeração de MPSTATUS_FLAG (MpClient. h)
description: Possíveis sinalizadores de bit de status de produto geral.
ms.assetid: BF2E6506-E76A-4785-8E91-99937B413548
keywords:
- recursos do ambiente de Windows herdado de enumeração de MPSTATUS_FLAG
- Windows recursos de ambiente herdados do ponteiro de enumeração PMPSTATUS_FLAG
topic_type:
- apiref
api_name:
- MPSTATUS_FLAG
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d850f0e8de9a3b0ed18a1a1353dfdef40d41bcb1ce4d17265ec245e82ba73f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747030"
---
# <a name="mpstatus_flag-enumeration"></a>\_Enumeração de sinalizador MPSTATUS

Possíveis sinalizadores de bit de status de produto geral.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagMPSTATUS_FLAG { 
  MP_STATUS_FLAG_NONE                           = 0,
  MP_STATUS_FLAG_SERVICE_UNAVAILABLE            = 1 << 0,
  MP_STATUS_FLAG_MPENGINE_UNAVAILABLE           = 1 << 1,
  MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED       = 1 << 2,
  MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED         = 1 << 3,
  MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED   = 1 << 4,
  MP_STATUS_FLAG_DUE_AV_SIGNATURE               = 1 << 5,
  MP_STATUS_FLAG_DUE_AS_SIGNATURE               = 1 << 6,
  MP_STATUS_FLAG_DUE_QUICK_SCAN                 = 1 << 7,
  MP_STATUS_FLAG_DUE_FULL_SCAN                  = 1 << 8,
  MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN         = 1 << 9,
  MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING    = 1 << 10,
  MP_STATUS_FLAG_DUE_SAMPLES                    = 1 << 11,
  MP_STATUS_FLAG_EVALUATION_MODE                = 1 << 12,
  MP_STATUS_FLAG_NONGENUINE                     = 1 << 13,
  MP_STATUS_FLAG_PRODUCT_EXPIRED                = 1 << 14,
  MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED       = 1 << 15,
  MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN     = 1 << 16,
  MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE       = 1 << 17,
  MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE   = 1 << 18,
  MP_STATUS_FLAG_HEALTH_INITIALIZED             = 1 << 19,
  MP_STATUS_FLAG_DUE_PLATFORM_UPDATE            = 1 << 20,
  MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE     = 1 << 21,
  MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED  = 1 << 22,
  MP_STATUS_FLAG_END_OF_LIFE                    = 1 << 23,
  MP_STATUS_FLAG_MAX                            = 1 << 23,
  MP_STATUS_FLAG_ALL                            = (1 << 24)-1
} MPSTATUS_FLAG, *PMPSTATUS_FLAG;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MP_STATUS_FLAG_NONE"></span><span id="mp_status_flag_none"></span>**sinalizador de status do MP \_ \_ \_ None**
</dt> <dd>

Nenhum sinalizador de status definido (estado não inicializado).

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_UNAVAILABLE"></span><span id="mp_status_flag_service_unavailable"></span>**serviço de sinalizador de status do MP \_ \_ \_ \_ indisponível**
</dt> <dd>

O serviço não está em execução.

</dd> <dt>

<span id="MP_STATUS_FLAG_MPENGINE_UNAVAILABLE"></span><span id="mp_status_flag_mpengine_unavailable"></span>**sinalizador de status do MP \_ \_ \_ MPENGINE \_ indisponível**
</dt> <dd>

O serviço foi iniciado sem nenhum mecanismo de proteção contra malware.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED"></span><span id="mp_status_flag_threat_fullscan_required"></span>**sinalizador de status do MP \_ \_ \_ ameaça \_ FULLSCAN \_ necessário**
</dt> <dd>

Verificação completa pendente devido à ação de ameaça.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED"></span><span id="mp_status_flag_threat_reboot_required"></span>**sinalizador de status do MP \_ \_ \_ \_ reinicialização de ameaças \_ necessária**
</dt> <dd>

Reinicialização pendente devido à ação de ameaça.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED"></span><span id="mp_status_flag_threat_manual_steps_required"></span>**sinalizador de status do MP \_ \_ \_ \_ etapas manuais de ameaça \_ \_ necessárias**
</dt> <dd>

Etapas manuais pendentes devido à ação de ameaça.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_AV_SIGNATURE"></span><span id="mp_status_flag_due_av_signature"></span>**sinalizador de status do MP \_ \_ \_ devido à \_ assinatura do AV \_**
</dt> <dd>

Assinaturas de antivírus desatualizadas.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_AS_SIGNATURE"></span><span id="mp_status_flag_due_as_signature"></span>**\_sinalizador de status do MP \_ devido à \_ \_ \_ assinatura**
</dt> <dd>

Assinaturas AntiSpyware desatualizadas.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_QUICK_SCAN"></span><span id="mp_status_flag_due_quick_scan"></span>**sinalizador de status do MP \_ \_ \_ devido à \_ \_ verificação rápida**
</dt> <dd>

Nenhuma verificação rápida ocorreu por um período especificado.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_FULL_SCAN"></span><span id="mp_status_flag_due_full_scan"></span>**sinalizador de status do MP \_ \_ \_ devido à \_ \_ verificação completa**
</dt> <dd>

nenhuma verificação completa aconteceu por um período especificado

</dd> <dt>

<span id="MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN"></span><span id="mp_status_flag_inprogress_system_scan"></span>**sinalizador de status do MP \_ \_ \_ verificação do sistema InProgress \_ \_**
</dt> <dd>

Verificação iniciada pelo sistema em andamento.

</dd> <dt>

<span id="MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING"></span><span id="mp_status_flag_inprogress_routine_cleaning"></span>**\_limpeza de \_ rotina do sinalizador de status do \_ \_ MP \_**
</dt> <dd>

Limpeza iniciada pelo sistema em andamento.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_SAMPLES"></span><span id="mp_status_flag_due_samples"></span>**amostras de sinalizador de status do MP \_ \_ \_ devido \_**
</dt> <dd>

Há amostras com envio pendente.

</dd> <dt>

<span id="MP_STATUS_FLAG_EVALUATION_MODE"></span><span id="mp_status_flag_evaluation_mode"></span>**\_modo de \_ avaliação do sinalizador de status do MP \_ \_**
</dt> <dd>

O produto está sendo executado no modo de avaliação.

</dd> <dt>

<span id="MP_STATUS_FLAG_NONGENUINE"></span><span id="mp_status_flag_nongenuine"></span>**sinalizador de status do MP não \_ \_ \_ original**
</dt> <dd>

o produto está sendo executado no modo de Windows não original.

</dd> <dt>

<span id="MP_STATUS_FLAG_PRODUCT_EXPIRED"></span><span id="mp_status_flag_product_expired"></span>**sinalizador de status do MP \_ \_ \_ produto \_ expirado**
</dt> <dd>

Produto expirado.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED"></span><span id="mp_status_flag_threat_callisto_required"></span>**sinalizador de status do MP \_ \_ \_ ameaça \_ Callisto \_ necessário**
</dt> <dd>

Verificação offline Callisto necessária.

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN"></span><span id="mp_status_flag_service_on_system_shutdown"></span>**\_ \_ \_ serviço \_ de sinalizador de status do MP no \_ \_ desligamento do sistema**
</dt> <dd>

O serviço está sendo desligado como parte do desligamento do sistema.

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_critical_failure"></span>**\_ \_ \_ falha crítica do serviço \_ sinalizador \_ de estado do MP**
</dt> <dd>

A correção de ameaças falhou criticamente.

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_non_critical_failure"></span>**\_ \_ \_ \_ \_ falha não crítica do serviço sinalizador de estado \_ do MP**
</dt> <dd>

Falha de correção de ameaça não crítica.

</dd> <dt>

<span id="MP_STATUS_FLAG_HEALTH_INITIALIZED"></span><span id="mp_status_flag_health_initialized"></span>**integridade do sinalizador de status do MP \_ \_ \_ \_ inicializada**
</dt> <dd>

Nenhum sinalizador de status definido (estado bem inicializado).

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_PLATFORM_UPDATE"></span><span id="mp_status_flag_due_platform_update"></span>**sinalizador de status do MP \_ \_ \_ devido à \_ atualização da plataforma \_**
</dt> <dd>

A plataforma está desatualizada.

</dd> <dt>

<span id="MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE"></span><span id="mp_status_flag_inprogress_platform_update"></span>**sinalizador de status do MP \_ \_ atualização da \_ plataforma de InProgress \_ \_**
</dt> <dd>

A atualização da plataforma está em andamento.

</dd> <dt>

<span id="MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED"></span><span id="mp_status_flag_platform_about_to_be_outdated"></span>**\_ \_ plataforma de sinalizador de status do MP \_ \_ prestes \_ a \_ ser \_ desatualizada**
</dt> <dd>

A plataforma está prestes a ser desatualizada

</dd> <dt>

<span id="MP_STATUS_FLAG_END_OF_LIFE"></span><span id="mp_status_flag_end_of_life"></span>**\_ \_ \_ fim \_ da vida útil do sinalizador de status do MP \_**
</dt> <dd>

A assinatura ou o fim da vida da plataforma é anterior ou está pendente.

</dd> <dt>

<span id="MP_STATUS_FLAG_MAX"></span><span id="mp_status_flag_max"></span>**sinalizador de status do MP \_ \_ \_ máx.**
</dt> <dd>

Sinalizador máximo válido.

</dd> <dt>

<span id="MP_STATUS_FLAG_ALL"></span><span id="mp_status_flag_all"></span>**sinalizador de status do MP \_ \_ \_ tudo**
</dt> <dd>

Valor máximo possível.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





