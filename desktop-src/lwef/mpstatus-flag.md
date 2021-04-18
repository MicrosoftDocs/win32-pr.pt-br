---
title: Enumeração de MPSTATUS_FLAG (MpClient. h)
description: Possíveis sinalizadores de bit de status de produto geral.
ms.assetid: BF2E6506-E76A-4785-8E91-99937B413548
keywords:
- Recursos do ambiente Windows herdado de enumeração de MPSTATUS_FLAG
- PMPSTATUS_FLAG recursos de ambiente herdados do ponteiro de enumeração do Windows
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
ms.openlocfilehash: 9c7175980c09c63938be04626091c31b53335756
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756839"
---
# <a name="mpstatus_flag-enumeration"></a><span data-ttu-id="0be9d-105">\_Enumeração de sinalizador MPSTATUS</span><span class="sxs-lookup"><span data-stu-id="0be9d-105">MPSTATUS\_FLAG enumeration</span></span>

<span data-ttu-id="0be9d-106">Possíveis sinalizadores de bit de status de produto geral.</span><span class="sxs-lookup"><span data-stu-id="0be9d-106">Possible overall product status bit flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="0be9d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="0be9d-107">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="0be9d-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="0be9d-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0be9d-109"><span id="MP_STATUS_FLAG_NONE"></span><span id="mp_status_flag_none"></span>**sinalizador de status do MP \_ \_ \_ None**</span><span class="sxs-lookup"><span data-stu-id="0be9d-109"><span id="MP_STATUS_FLAG_NONE"></span><span id="mp_status_flag_none"></span>**MP\_STATUS\_FLAG\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="0be9d-110">Nenhum sinalizador de status definido (estado não inicializado).</span><span class="sxs-lookup"><span data-stu-id="0be9d-110">No status flags set (non-initialized state).</span></span>

</dd> <dt>

<span data-ttu-id="0be9d-111"><span id="MP_STATUS_FLAG_SERVICE_UNAVAILABLE"></span><span id="mp_status_flag_service_unavailable"></span>**serviço de sinalizador de status do MP \_ \_ \_ \_ indisponível**</span><span class="sxs-lookup"><span data-stu-id="0be9d-111"><span id="MP_STATUS_FLAG_SERVICE_UNAVAILABLE"></span><span id="mp_status_flag_service_unavailable"></span>**MP\_STATUS\_FLAG\_SERVICE\_UNAVAILABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0be9d-112">O serviço não está em execução.</span><span class="sxs-lookup"><span data-stu-id="0be9d-112">Service not running.</span></span>

</dd> <dt>

<span data-ttu-id="0be9d-113"><span id="MP_STATUS_FLAG_MPENGINE_UNAVAILABLE"></span><span id="mp_status_flag_mpengine_unavailable"></span>**sinalizador de status do MP \_ \_ \_ MPENGINE \_ indisponível**</span><span class="sxs-lookup"><span data-stu-id="0be9d-113"><span id="MP_STATUS_FLAG_MPENGINE_UNAVAILABLE"></span><span id="mp_status_flag_mpengine_unavailable"></span>**MP\_STATUS\_FLAG\_MPENGINE\_UNAVAILABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0be9d-114">O serviço foi iniciado sem nenhum mecanismo de proteção contra malware.</span><span class="sxs-lookup"><span data-stu-id="0be9d-114">Service started without any malware protection engine.</span></span>

</dd> <dt>

<span data-ttu-id="0be9d-115"><span id="MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED"></span><span id="mp_status_flag_threat_fullscan_required"></span>**sinalizador de status do MP \_ \_ \_ ameaça \_ FULLSCAN \_ necessário**</span><span class="sxs-lookup"><span data-stu-id="0be9d-115"><span id="MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED"></span><span id="mp_status_flag_threat_fullscan_required"></span>**MP\_STATUS\_FLAG\_THREAT\_FULLSCAN\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="0be9d-116">Verificação completa pendente devido à ação de ameaça.</span><span class="sxs-lookup"><span data-stu-id="0be9d-116">Pending full scan due to threat action.</span></span>

</dd> <dt>

<span data-ttu-id="0be9d-117"><span id="MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED"></span><span id="mp_status_flag_threat_reboot_required"></span>**sinalizador de status do MP \_ \_ \_ \_ reinicialização de ameaças \_ necessária**</span><span class="sxs-lookup"><span data-stu-id="0be9d-117"><span id="MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED"></span><span id="mp_status_flag_threat_reboot_required"></span>**MP\_STATUS\_FLAG\_THREAT\_REBOOT\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="0be9d-118">Reinicialização pendente devido à ação de ameaça.</span><span class="sxs-lookup"><span data-stu-id="0be9d-118">Pending reboot due to threat action.</span></span>

</dd> <dt>

<span data-ttu-id="0be9d-119"><span id="MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED"></span><span id="mp_status_flag_threat_manual_steps_required"></span>**sinalizador de status do MP \_ \_ \_ \_ etapas manuais de ameaça \_ \_ necessárias**</span><span class="sxs-lookup"><span data-stu-id="0be9d-119"><span id="MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED"></span><span id="mp_status_flag_threat_manual_steps_required"></span>**MP\_STATUS\_FLAG\_THREAT\_MANUAL\_STEPS\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="0be9d-120">Etapas manuais pendentes devido à ação de ameaça.</span><span class="sxs-lookup"><span data-stu-id="0be9d-120">Pending manual steps due to threat action.</span></span>

</dd> <dt>

<span data-ttu-id="0be9d-121"><span id="MP_STATUS_FLAG_DUE_AV_SIGNATURE"></span><span id="mp_status_flag_due_av_signature"></span>**sinalizador de status do MP \_ \_ \_ devido à \_ assinatura do AV \_**</span><span class="sxs-lookup"><span data-stu-id="0be9d-121"><span id="MP_STATUS_FLAG_DUE_AV_SIGNATURE"></span><span id="mp_status_flag_due_av_signature"></span>**MP\_STATUS\_FLAG\_DUE\_AV\_SIGNATURE**</span></span>
</dt> <dd>

<span data-ttu-id="0be9d-122">Assinaturas de antivírus desatualizadas.</span><span class="sxs-lookup"><span data-stu-id="0be9d-122">Antivirus signatures out of date.</span></span>

</dd> <dt>

<span data-ttu-id="0be9d-123"><span id="MP_STATUS_FLAG_DUE_AS_SIGNATURE"></span><span id="mp_status_flag_due_as_signature"></span>**\_sinalizador de status do MP \_ devido à \_ \_ \_ assinatura**</span><span class="sxs-lookup"><span data-stu-id="0be9d-123"><span id="MP_STATUS_FLAG_DUE_AS_SIGNATURE"></span><span id="mp_status_flag_due_as_signature"></span>**MP\_STATUS\_FLAG\_DUE\_AS\_SIGNATURE**</span></span>
</dt> <dd>

<span data-ttu-id="0be9d-124">Assinaturas AntiSpyware desatualizadas.</span><span class="sxs-lookup"><span data-stu-id="0be9d-124">Antispyware signatures out of date.</span></span>

</dd> <dt>

<span data-ttu-id="0be9d-125"><span id="MP_STATUS_FLAG_DUE_QUICK_SCAN"></span><span id="mp_status_flag_due_quick_scan"></span>**sinalizador de status do MP \_ \_ \_ devido à \_ \_ verificação rápida**</span><span class="sxs-lookup"><span data-stu-id="0be9d-125"><span id="MP_STATUS_FLAG_DUE_QUICK_SCAN"></span><span id="mp_status_flag_due_quick_scan"></span>**MP\_STATUS\_FLAG\_DUE\_QUICK\_SCAN**</span></span>
</dt> <dd>

<span data-ttu-id="0be9d-126">Nenhuma verificação rápida ocorreu por um período especificado.</span><span class="sxs-lookup"><span data-stu-id="0be9d-126">No quick scan has happened for a specified period.</span></span>

</dd> <dt>

<span data-ttu-id="0be9d-127"><span id="MP_STATUS_FLAG_DUE_FULL_SCAN"></span><span id="mp_status_flag_due_full_scan"></span>**sinalizador de status do MP \_ \_ \_ devido à \_ \_ verificação completa**</span><span class="sxs-lookup"><span data-stu-id="0be9d-127"><span id="MP_STATUS_FLAG_DUE_FULL_SCAN"></span><span id="mp_status_flag_due_full_scan"></span>**MP\_STATUS\_FLAG\_DUE\_FULL\_SCAN**</span></span>
</dt> <dd>

<span data-ttu-id="0be9d-128">nenhuma verificação completa aconteceu por um período especificado</span><span class="sxs-lookup"><span data-stu-id="0be9d-128">no full scan has happened for a specified period</span></span>

</dd> <dt>

<span data-ttu-id="0be9d-129"><span id="MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN"></span><span id="mp_status_flag_inprogress_system_scan"></span>**sinalizador de status do MP \_ \_ \_ verificação do sistema InProgress \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0be9d-129"><span id="MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN"></span><span id="mp_status_flag_inprogress_system_scan"></span>**MP\_STATUS\_FLAG\_INPROGRESS\_SYSTEM\_SCAN**</span></span>
</dt> <dd>

<span data-ttu-id="0be9d-130">Verificação iniciada pelo sistema em andamento.</span><span class="sxs-lookup"><span data-stu-id="0be9d-130">System-initiated scan in progress.</span></span>

</dd> <dt>

<span data-ttu-id="0be9d-131"><span id="MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING"></span><span id="mp_status_flag_inprogress_routine_cleaning"></span>**\_limpeza de \_ rotina do sinalizador de status do \_ \_ MP \_**</span><span class="sxs-lookup"><span data-stu-id="0be9d-131"><span id="MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING"></span><span id="mp_status_flag_inprogress_routine_cleaning"></span>**MP\_STATUS\_FLAG\_INPROGRESS\_ROUTINE\_CLEANING**</span></span>
</dt> <dd>

<span data-ttu-id="0be9d-132">Limpeza iniciada pelo sistema em andamento.</span><span class="sxs-lookup"><span data-stu-id="0be9d-132">System-initiated clean in progress.</span></span>

</dd> <dt>

<span data-ttu-id="0be9d-133"><span id="MP_STATUS_FLAG_DUE_SAMPLES"></span><span id="mp_status_flag_due_samples"></span>**amostras de sinalizador de status do MP \_ \_ \_ devido \_**</span><span class="sxs-lookup"><span data-stu-id="0be9d-133"><span id="MP_STATUS_FLAG_DUE_SAMPLES"></span><span id="mp_status_flag_due_samples"></span>**MP\_STATUS\_FLAG\_DUE\_SAMPLES**</span></span>
</dt> <dd>

<span data-ttu-id="0be9d-134">Há amostras com envio pendente.</span><span class="sxs-lookup"><span data-stu-id="0be9d-134">There are samples pending submission.</span></span>

</dd> <dt>

<span data-ttu-id="0be9d-135"><span id="MP_STATUS_FLAG_EVALUATION_MODE"></span><span id="mp_status_flag_evaluation_mode"></span>**\_modo de \_ avaliação do sinalizador de status do MP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0be9d-135"><span id="MP_STATUS_FLAG_EVALUATION_MODE"></span><span id="mp_status_flag_evaluation_mode"></span>**MP\_STATUS\_FLAG\_EVALUATION\_MODE**</span></span>
</dt> <dd>

<span data-ttu-id="0be9d-136">O produto está sendo executado no modo de avaliação.</span><span class="sxs-lookup"><span data-stu-id="0be9d-136">Product is running in evaluation mode.</span></span>

</dd> <dt>

<span data-ttu-id="0be9d-137"><span id="MP_STATUS_FLAG_NONGENUINE"></span><span id="mp_status_flag_nongenuine"></span>**sinalizador de status do MP não \_ \_ \_ original**</span><span class="sxs-lookup"><span data-stu-id="0be9d-137"><span id="MP_STATUS_FLAG_NONGENUINE"></span><span id="mp_status_flag_nongenuine"></span>**MP\_STATUS\_FLAG\_NONGENUINE**</span></span>
</dt> <dd>

<span data-ttu-id="0be9d-138">O produto está sendo executado no modo Windows não original.</span><span class="sxs-lookup"><span data-stu-id="0be9d-138">Product is running in non-genuine Windows mode.</span></span>

</dd> <dt>

<span data-ttu-id="0be9d-139"><span id="MP_STATUS_FLAG_PRODUCT_EXPIRED"></span><span id="mp_status_flag_product_expired"></span>**sinalizador de status do MP \_ \_ \_ produto \_ expirado**</span><span class="sxs-lookup"><span data-stu-id="0be9d-139"><span id="MP_STATUS_FLAG_PRODUCT_EXPIRED"></span><span id="mp_status_flag_product_expired"></span>**MP\_STATUS\_FLAG\_PRODUCT\_EXPIRED**</span></span>
</dt> <dd>

<span data-ttu-id="0be9d-140">Produto expirado.</span><span class="sxs-lookup"><span data-stu-id="0be9d-140">Product expired.</span></span>

</dd> <dt>

<span data-ttu-id="0be9d-141"><span id="MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED"></span><span id="mp_status_flag_threat_callisto_required"></span>**sinalizador de status do MP \_ \_ \_ ameaça \_ Callisto \_ necessário**</span><span class="sxs-lookup"><span data-stu-id="0be9d-141"><span id="MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED"></span><span id="mp_status_flag_threat_callisto_required"></span>**MP\_STATUS\_FLAG\_THREAT\_CALLISTO\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="0be9d-142">Verificação offline Callisto necessária.</span><span class="sxs-lookup"><span data-stu-id="0be9d-142">Callisto off-line scan required.</span></span>

</dd> <dt>

<span data-ttu-id="0be9d-143"><span id="MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN"></span><span id="mp_status_flag_service_on_system_shutdown"></span>**\_ \_ \_ serviço \_ de sinalizador de status do MP no \_ \_ desligamento do sistema**</span><span class="sxs-lookup"><span data-stu-id="0be9d-143"><span id="MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN"></span><span id="mp_status_flag_service_on_system_shutdown"></span>**MP\_STATUS\_FLAG\_SERVICE\_ON\_SYSTEM\_SHUTDOWN**</span></span>
</dt> <dd>

<span data-ttu-id="0be9d-144">O serviço está sendo desligado como parte do desligamento do sistema.</span><span class="sxs-lookup"><span data-stu-id="0be9d-144">Service is shutting down as part of system shutdown.</span></span>

</dd> <dt>

<span data-ttu-id="0be9d-145"><span id="MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_critical_failure"></span>**\_ \_ \_ falha crítica do serviço \_ sinalizador \_ de estado do MP**</span><span class="sxs-lookup"><span data-stu-id="0be9d-145"><span id="MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_critical_failure"></span>**MP\_STATUS\_FLAG\_SERVICE\_CRITICAL\_FAILURE**</span></span>
</dt> <dd>

<span data-ttu-id="0be9d-146">A correção de ameaças falhou criticamente.</span><span class="sxs-lookup"><span data-stu-id="0be9d-146">Threat remediation failed critically.</span></span>

</dd> <dt>

<span data-ttu-id="0be9d-147"><span id="MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_non_critical_failure"></span>**\_ \_ \_ \_ \_ falha não crítica do serviço sinalizador de estado \_ do MP**</span><span class="sxs-lookup"><span data-stu-id="0be9d-147"><span id="MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_non_critical_failure"></span>**MP\_STATUS\_FLAG\_SERVICE\_NON\_CRITICAL\_FAILURE**</span></span>
</dt> <dd>

<span data-ttu-id="0be9d-148">Falha de correção de ameaça não crítica.</span><span class="sxs-lookup"><span data-stu-id="0be9d-148">Threat remediation failed non-critically.</span></span>

</dd> <dt>

<span data-ttu-id="0be9d-149"><span id="MP_STATUS_FLAG_HEALTH_INITIALIZED"></span><span id="mp_status_flag_health_initialized"></span>**integridade do sinalizador de status do MP \_ \_ \_ \_ inicializada**</span><span class="sxs-lookup"><span data-stu-id="0be9d-149"><span id="MP_STATUS_FLAG_HEALTH_INITIALIZED"></span><span id="mp_status_flag_health_initialized"></span>**MP\_STATUS\_FLAG\_HEALTH\_INITIALIZED**</span></span>
</dt> <dd>

<span data-ttu-id="0be9d-150">Nenhum sinalizador de status definido (estado bem inicializado).</span><span class="sxs-lookup"><span data-stu-id="0be9d-150">No status flags set (well-initialized state).</span></span>

</dd> <dt>

<span data-ttu-id="0be9d-151"><span id="MP_STATUS_FLAG_DUE_PLATFORM_UPDATE"></span><span id="mp_status_flag_due_platform_update"></span>**sinalizador de status do MP \_ \_ \_ devido à \_ atualização da plataforma \_**</span><span class="sxs-lookup"><span data-stu-id="0be9d-151"><span id="MP_STATUS_FLAG_DUE_PLATFORM_UPDATE"></span><span id="mp_status_flag_due_platform_update"></span>**MP\_STATUS\_FLAG\_DUE\_PLATFORM\_UPDATE**</span></span>
</dt> <dd>

<span data-ttu-id="0be9d-152">A plataforma está desatualizada.</span><span class="sxs-lookup"><span data-stu-id="0be9d-152">The platform is out of date.</span></span>

</dd> <dt>

<span data-ttu-id="0be9d-153"><span id="MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE"></span><span id="mp_status_flag_inprogress_platform_update"></span>**sinalizador de status do MP \_ \_ atualização da \_ plataforma de InProgress \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0be9d-153"><span id="MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE"></span><span id="mp_status_flag_inprogress_platform_update"></span>**MP\_STATUS\_FLAG\_INPROGRESS\_PLATFORM\_UPDATE**</span></span>
</dt> <dd>

<span data-ttu-id="0be9d-154">A atualização da plataforma está em andamento.</span><span class="sxs-lookup"><span data-stu-id="0be9d-154">Platform update is in progress.</span></span>

</dd> <dt>

<span data-ttu-id="0be9d-155"><span id="MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED"></span><span id="mp_status_flag_platform_about_to_be_outdated"></span>**\_ \_ plataforma de sinalizador de status do MP \_ \_ prestes \_ a \_ ser \_ desatualizada**</span><span class="sxs-lookup"><span data-stu-id="0be9d-155"><span id="MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED"></span><span id="mp_status_flag_platform_about_to_be_outdated"></span>**MP\_STATUS\_FLAG\_PLATFORM\_ABOUT\_TO\_BE\_OUTDATED**</span></span>
</dt> <dd>

<span data-ttu-id="0be9d-156">A plataforma está prestes a ser desatualizada</span><span class="sxs-lookup"><span data-stu-id="0be9d-156">The platform is about to be outdated</span></span>

</dd> <dt>

<span data-ttu-id="0be9d-157"><span id="MP_STATUS_FLAG_END_OF_LIFE"></span><span id="mp_status_flag_end_of_life"></span>**\_ \_ \_ fim \_ da vida útil do sinalizador de status do MP \_**</span><span class="sxs-lookup"><span data-stu-id="0be9d-157"><span id="MP_STATUS_FLAG_END_OF_LIFE"></span><span id="mp_status_flag_end_of_life"></span>**MP\_STATUS\_FLAG\_END\_OF\_LIFE**</span></span>
</dt> <dd>

<span data-ttu-id="0be9d-158">A assinatura ou o fim da vida da plataforma é anterior ou está pendente.</span><span class="sxs-lookup"><span data-stu-id="0be9d-158">The signature or platform end of life is past or is pending.</span></span>

</dd> <dt>

<span data-ttu-id="0be9d-159"><span id="MP_STATUS_FLAG_MAX"></span><span id="mp_status_flag_max"></span>**sinalizador de status do MP \_ \_ \_ máx.**</span><span class="sxs-lookup"><span data-stu-id="0be9d-159"><span id="MP_STATUS_FLAG_MAX"></span><span id="mp_status_flag_max"></span>**MP\_STATUS\_FLAG\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="0be9d-160">Sinalizador máximo válido.</span><span class="sxs-lookup"><span data-stu-id="0be9d-160">Maximum valid flag.</span></span>

</dd> <dt>

<span data-ttu-id="0be9d-161"><span id="MP_STATUS_FLAG_ALL"></span><span id="mp_status_flag_all"></span>**sinalizador de status do MP \_ \_ \_ tudo**</span><span class="sxs-lookup"><span data-stu-id="0be9d-161"><span id="MP_STATUS_FLAG_ALL"></span><span id="mp_status_flag_all"></span>**MP\_STATUS\_FLAG\_ALL**</span></span>
</dt> <dd>

<span data-ttu-id="0be9d-162">Valor máximo possível.</span><span class="sxs-lookup"><span data-stu-id="0be9d-162">Maximum value possible.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0be9d-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0be9d-163">Requirements</span></span>



| <span data-ttu-id="0be9d-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="0be9d-164">Requirement</span></span> | <span data-ttu-id="0be9d-165">Valor</span><span class="sxs-lookup"><span data-stu-id="0be9d-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0be9d-166">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0be9d-166">Minimum supported client</span></span><br/> | <span data-ttu-id="0be9d-167">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0be9d-167">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0be9d-168">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0be9d-168">Minimum supported server</span></span><br/> | <span data-ttu-id="0be9d-169">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0be9d-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0be9d-170">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0be9d-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="0be9d-171"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="0be9d-171"><dt>MpClient.h</dt></span></span> </dl> |



 

 





