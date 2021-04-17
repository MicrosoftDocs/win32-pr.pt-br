---
title: Enumeração MPNOTIFY (MpClient. h)
description: Possíveis notificações de retorno de chamada.
ms.assetid: CCD0CD89-2C6E-453F-9437-E6ED87AD9F29
keywords:
- Recursos do ambiente Windows herdado de enumeração MPNOTIFY
- Ponteiro de enumeração PMPNOTIFY recursos de ambiente do Windows herdados
topic_type:
- apiref
api_name:
- MPNOTIFY
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afa0eeb6cb1d610f28cc82f578617f7bd71cf886
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105763295"
---
# <a name="mpnotify-enumeration"></a><span data-ttu-id="79b06-105">Enumeração MPNOTIFY</span><span class="sxs-lookup"><span data-stu-id="79b06-105">MPNOTIFY enumeration</span></span>

<span data-ttu-id="79b06-106">Possíveis notificações de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="79b06-106">Possible callback notifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="79b06-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="79b06-107">Syntax</span></span>


```C++
typedef enum tagMPNOTIFY { 
  MPNOTIFY_NONE,
  MPNOTIFY_CALL_START,
  MPNOTIFY_CALL_COMPLETE,
  MPNOTIFY_INTERNAL_FAILURE,
  MPNOTIFY_STATUS_SERVICE_START,
  MPNOTIFY_STATUS_SERVICE_RUNNING,
  MPNOTIFY_STATUS_SERVICE_STOP,
  MPNOTIFY_STATUS_COMPONENT,
  MPNOTIFY_STATUS_CHANGE,
  MPNOTIFY_STATUS_COMPONENT_CONFIGURATION,
  MPNOTIFY_STATUS_EXPIRATION_CHANGE,
  MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE,
  MPNOTIFY_SCAN_START,
  MPNOTIFY_SCAN_PAUSED,
  MPNOTIFY_SCAN_RESUMED,
  MPNOTIFY_SCAN_CANCEL,
  MPNOTIFY_SCAN_COMPLETE,
  MPNOTIFY_SCAN_PROGRESS,
  MPNOTIFY_SCAN_ERROR,
  MPNOTIFY_SCAN_INFECTED,
  MPNOTIFY_SCAN_MEMORYSTART,
  MPNOTIFY_SCAN_MEMORYCOMPLETE,
  MPNOTIFY_SCAN_SFC_BUILD_START,
  MPNOTIFY_SCAN_SFC_BUILD_COMPLETE,
  MPNOTIFY_SCAN_FASTPATH_START,
  MPNOTIFY_SCAN_FASTPATH_COMPLETE,
  MPNOTIFY_SCAN_FASTPATH_PROGRESS,
  MPNOTIFY_CLEAN_START,
  MPNOTIFY_CLEAN_COMPLETE,
  MPNOTIFY_CLEAN_RESTOREPOINT_START,
  MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED,
  MPNOTIFY_CLEAN_RESTOREPOINT_FAILED,
  MPNOTIFY_CLEAN_THREAT_START,
  MPNOTIFY_CLEAN_THREAT_SUCCEEDED,
  MPNOTIFY_CLEAN_THREAT_FAILED,
  MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED,
  MPNOTIFY_CLEAN_RESOURCE_FAILED,
  MPNOTIFY_CLEAN_THREAT_COMPLETE,
  MPNOTIFY_PRECHECK_START,
  MPNOTIFY_PRECHECK_COMPLETE,
  MPNOTIFY_PRECHECK_RESOURCE_BLOCKED,
  MPNOTIFY_THREAT_DETECTED,
  MPNOTIFY_THREAT_MODIFIED,
  MPNOTIFY_THREAT_CLEAN_SUCCEEDED,
  MPNOTIFY_THREAT_CLEAN_FAILED,
  MPNOTIFY_THREAT_ABANDONED,
  MPNOTIFY_THREAT_CLEAN_EVENT_START,
  MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE,
  MPNOTIFY_SIGUPDATE_START,
  MPNOTIFY_SIGUPDATE_SEARCH_START,
  MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE,
  MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_START,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE,
  MPNOTIFY_SIGUPDATE_INSTALL_START,
  MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS,
  MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE,
  MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED,
  MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED,
  MPNOTIFY_SIGUPDATE_COMPLETE,
  MPNOTIFY_SAMPLE_START,
  MPNOTIFY_SAMPLE_COMPLETE,
  MPNOTIFY_SAMPLE_ITEM_START,
  MPNOTIFY_SAMPLE_ITEM_SUCCEEDED,
  MPNOTIFY_SAMPLE_ITEM_FAILED,
  MPNOTIFY_RESERVED_DATA,
  MPNOTIFY_FASTPATH_SIG_ADDED,
  MPNOTIFY_FASTPATH_SIG_REMOVED,
  MPNOTIFY_NIS_PRIVATE,
  MPNOTIFY_HEALTH_CHANGE,
  MPNOTIFY_HEALTH_RECOVERY,
  MPNOTIFY_HEALTH_START,
  MPNOTIFY_ENDOFLIFE_CHANGE,
  MPNOTIFY_MALWARETOAST_DATA
} MPNOTIFY, *PMPNOTIFY;
```



## <a name="constants"></a><span data-ttu-id="79b06-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="79b06-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="79b06-109"><span id="MPNOTIFY_NONE"></span><span id="mpnotify_none"></span>**MPNOTIFY \_ nenhum**</span><span class="sxs-lookup"><span data-stu-id="79b06-109"><span id="MPNOTIFY_NONE"></span><span id="mpnotify_none"></span>**MPNOTIFY\_NONE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="79b06-110"><span id="MPNOTIFY_CALL_START"></span><span id="mpnotify_call_start"></span>**\_início da chamada do mpnotify \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-110"><span id="MPNOTIFY_CALL_START"></span><span id="mpnotify_call_start"></span>**MPNOTIFY\_CALL\_START**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-111">Início da chamada de notificação.</span><span class="sxs-lookup"><span data-stu-id="79b06-111">Notification call start.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-112"><span id="MPNOTIFY_CALL_COMPLETE"></span><span id="mpnotify_call_complete"></span>**\_chamada mpnotify \_ concluída**</span><span class="sxs-lookup"><span data-stu-id="79b06-112"><span id="MPNOTIFY_CALL_COMPLETE"></span><span id="mpnotify_call_complete"></span>**MPNOTIFY\_CALL\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-113">Chamada de notificação concluída.</span><span class="sxs-lookup"><span data-stu-id="79b06-113">Notification call completed.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-114"><span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span>**\_falha interna do mpnotify \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-114"><span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span>**MPNOTIFY\_INTERNAL\_FAILURE**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-115">Falha interna genérica.</span><span class="sxs-lookup"><span data-stu-id="79b06-115">Generic internal failure.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-116"><span id="MPNOTIFY_STATUS_SERVICE_START"></span><span id="mpnotify_status_service_start"></span>**\_início do \_ serviço de status mpnotify \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-116"><span id="MPNOTIFY_STATUS_SERVICE_START"></span><span id="mpnotify_status_service_start"></span>**MPNOTIFY\_STATUS\_SERVICE\_START**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-117">O serviço de proteção contra malware foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="79b06-117">Malware protection service has started.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-118"><span id="MPNOTIFY_STATUS_SERVICE_RUNNING"></span><span id="mpnotify_status_service_running"></span>**\_serviço de status mpnotify \_ \_ em execução**</span><span class="sxs-lookup"><span data-stu-id="79b06-118"><span id="MPNOTIFY_STATUS_SERVICE_RUNNING"></span><span id="mpnotify_status_service_running"></span>**MPNOTIFY\_STATUS\_SERVICE\_RUNNING**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-119">O serviço de proteção contra malware está em execução.</span><span class="sxs-lookup"><span data-stu-id="79b06-119">Malware protection service is running.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-120"><span id="MPNOTIFY_STATUS_SERVICE_STOP"></span><span id="mpnotify_status_service_stop"></span>**\_interrupção do \_ serviço de status mpnotify \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-120"><span id="MPNOTIFY_STATUS_SERVICE_STOP"></span><span id="mpnotify_status_service_stop"></span>**MPNOTIFY\_STATUS\_SERVICE\_STOP**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-121">O serviço de proteção contra malware foi interrompido.</span><span class="sxs-lookup"><span data-stu-id="79b06-121">Malware protection service has stopped.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-122"><span id="MPNOTIFY_STATUS_COMPONENT"></span><span id="mpnotify_status_component"></span>**\_componente de status do mpnotify \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-122"><span id="MPNOTIFY_STATUS_COMPONENT"></span><span id="mpnotify_status_component"></span>**MPNOTIFY\_STATUS\_COMPONENT**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-123">Componente específico habilitar/desabilitar status.</span><span class="sxs-lookup"><span data-stu-id="79b06-123">Particular component enable/disable status.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-124"><span id="MPNOTIFY_STATUS_CHANGE"></span><span id="mpnotify_status_change"></span>**\_alteração de status de mpnotify \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-124"><span id="MPNOTIFY_STATUS_CHANGE"></span><span id="mpnotify_status_change"></span>**MPNOTIFY\_STATUS\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-125">O status geral do produto foi alterado.</span><span class="sxs-lookup"><span data-stu-id="79b06-125">Overall product status has changed.</span></span> <span data-ttu-id="79b06-126">Chame [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md) para obter o status atual.</span><span class="sxs-lookup"><span data-stu-id="79b06-126">Call [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md) to obtain the current status.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-127"><span id="MPNOTIFY_STATUS_COMPONENT_CONFIGURATION"></span><span id="mpnotify_status_component_configuration"></span>**\_configuração do \_ componente de status do mpnotify \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-127"><span id="MPNOTIFY_STATUS_COMPONENT_CONFIGURATION"></span><span id="mpnotify_status_component_configuration"></span>**MPNOTIFY\_STATUS\_COMPONENT\_CONFIGURATION**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-128">Um componente específico alterou A configuração.</span><span class="sxs-lookup"><span data-stu-id="79b06-128">A particular component has changed configuration.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-129"><span id="MPNOTIFY_STATUS_EXPIRATION_CHANGE"></span><span id="mpnotify_status_expiration_change"></span>**\_alteração de \_ expiração de status do mpnotify \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-129"><span id="MPNOTIFY_STATUS_EXPIRATION_CHANGE"></span><span id="mpnotify_status_expiration_change"></span>**MPNOTIFY\_STATUS\_EXPIRATION\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-130">O status de expiração do produto foi alterado.</span><span class="sxs-lookup"><span data-stu-id="79b06-130">Product expiration status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-131"><span id="MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE"></span><span id="mpnotify_status_offline_scan_change"></span>**\_alteração da \_ \_ verificação offline de status \_ do mpnotify**</span><span class="sxs-lookup"><span data-stu-id="79b06-131"><span id="MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE"></span><span id="mpnotify_status_offline_scan_change"></span>**MPNOTIFY\_STATUS\_OFFLINE\_SCAN\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-132">Estado de verificação offline necessário alterado.</span><span class="sxs-lookup"><span data-stu-id="79b06-132">Offline scan required state changed.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-133"><span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span>**\_início da verificação de mpnotify \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-133"><span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span>**MPNOTIFY\_SCAN\_START**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-134">Verificação iniciada.</span><span class="sxs-lookup"><span data-stu-id="79b06-134">Scan started.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-135"><span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span>**verificação de MPNOTIFY \_ \_ pausada**</span><span class="sxs-lookup"><span data-stu-id="79b06-135"><span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span>**MPNOTIFY\_SCAN\_PAUSED**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-136">Verificação pausada.</span><span class="sxs-lookup"><span data-stu-id="79b06-136">Scan paused.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-137"><span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span>**verificação do MPNOTIFY \_ \_ retomada**</span><span class="sxs-lookup"><span data-stu-id="79b06-137"><span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span>**MPNOTIFY\_SCAN\_RESUMED**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-138">verificação retomada.</span><span class="sxs-lookup"><span data-stu-id="79b06-138">scan resumed.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-139"><span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span>**MPNOTIFY de \_ verificação \_ cancelada**</span><span class="sxs-lookup"><span data-stu-id="79b06-139"><span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span>**MPNOTIFY\_SCAN\_CANCEL**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-140">Verificação cancelada.</span><span class="sxs-lookup"><span data-stu-id="79b06-140">Scan cancelled.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-141"><span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span>**verificação de MPNOTIFY \_ \_ concluída**</span><span class="sxs-lookup"><span data-stu-id="79b06-141"><span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span>**MPNOTIFY\_SCAN\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-142">Verificação concluída.</span><span class="sxs-lookup"><span data-stu-id="79b06-142">Scan completed.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-143"><span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span>**\_progresso da verificação de mpnotify \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-143"><span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span>**MPNOTIFY\_SCAN\_PROGRESS**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-144">Notificação de progresso para o recurso específico que está sendo examinado.</span><span class="sxs-lookup"><span data-stu-id="79b06-144">Progress notification for the specific resource being scanned.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-145"><span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span>**\_erro de verificação de mpnotify \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-145"><span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span>**MPNOTIFY\_SCAN\_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-146">Falha ao verificar um recurso específico.</span><span class="sxs-lookup"><span data-stu-id="79b06-146">Failure to scan a particular resource.</span></span> <span data-ttu-id="79b06-147">A verificação ainda continuará.</span><span class="sxs-lookup"><span data-stu-id="79b06-147">Scan will still continue.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-148"><span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span>**verificação de MPNOTIFY \_ \_ infectada**</span><span class="sxs-lookup"><span data-stu-id="79b06-148"><span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span>**MPNOTIFY\_SCAN\_INFECTED**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-149">A verificação encontrou um recurso infectado.</span><span class="sxs-lookup"><span data-stu-id="79b06-149">Scan found an infected resource.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-150"><span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span>**MPNOTIFY \_ Scan \_ MEMORYSTART**</span><span class="sxs-lookup"><span data-stu-id="79b06-150"><span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span>**MPNOTIFY\_SCAN\_MEMORYSTART**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-151">O progresso da verificação para notificar a parte da verificação de memória do sistema foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="79b06-151">Scan progress to notify memory scan portion of the system scan has started.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-152"><span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span>**MPNOTIFY \_ Scan \_ MEMORYCOMPLETE**</span><span class="sxs-lookup"><span data-stu-id="79b06-152"><span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span>**MPNOTIFY\_SCAN\_MEMORYCOMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-153">O progresso da verificação para notificar a parte da verificação de memória do sistema foi concluído.</span><span class="sxs-lookup"><span data-stu-id="79b06-153">Scan progress to notify memory scan portion of the system scan has completed.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-154"><span id="MPNOTIFY_SCAN_SFC_BUILD_START"></span><span id="mpnotify_scan_sfc_build_start"></span>**\_início da \_ \_ compilação Sfc \_ do mpnotify Scan**</span><span class="sxs-lookup"><span data-stu-id="79b06-154"><span id="MPNOTIFY_SCAN_SFC_BUILD_START"></span><span id="mpnotify_scan_sfc_build_start"></span>**MPNOTIFY\_SCAN\_SFC\_BUILD\_START**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-155">O andamento da verificação para notificar a parte da compilação do Sfc foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="79b06-155">Scan progress to notify sfc build portion has started.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-156"><span id="MPNOTIFY_SCAN_SFC_BUILD_COMPLETE"></span><span id="mpnotify_scan_sfc_build_complete"></span>**compilação do Sfc de verificação do MPNOTIFY \_ \_ \_ \_ concluída**</span><span class="sxs-lookup"><span data-stu-id="79b06-156"><span id="MPNOTIFY_SCAN_SFC_BUILD_COMPLETE"></span><span id="mpnotify_scan_sfc_build_complete"></span>**MPNOTIFY\_SCAN\_SFC\_BUILD\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-157">O andamento da verificação para notificar a parte da compilação do Sfc foi concluído.</span><span class="sxs-lookup"><span data-stu-id="79b06-157">Scan progress to notify sfc build portion has completed.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-158"><span id="MPNOTIFY_SCAN_FASTPATH_START"></span><span id="mpnotify_scan_fastpath_start"></span>**MPNOTIFY \_ verificação \_ FASTPATH \_ Iniciar**</span><span class="sxs-lookup"><span data-stu-id="79b06-158"><span id="MPNOTIFY_SCAN_FASTPATH_START"></span><span id="mpnotify_scan_fastpath_start"></span>**MPNOTIFY\_SCAN\_FASTPATH\_START**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-159">A verificação do FastPath SpyNet foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="79b06-159">Scan fastpath spynet has begun.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-160"><span id="MPNOTIFY_SCAN_FASTPATH_COMPLETE"></span><span id="mpnotify_scan_fastpath_complete"></span>**MPNOTIFY \_ verificação \_ FASTPATH \_ concluída**</span><span class="sxs-lookup"><span data-stu-id="79b06-160"><span id="MPNOTIFY_SCAN_FASTPATH_COMPLETE"></span><span id="mpnotify_scan_fastpath_complete"></span>**MPNOTIFY\_SCAN\_FASTPATH\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-161">Exame FastPath SpyNet terminou.</span><span class="sxs-lookup"><span data-stu-id="79b06-161">Scan fastpath spynet has ended.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-162"><span id="MPNOTIFY_SCAN_FASTPATH_PROGRESS"></span><span id="mpnotify_scan_fastpath_progress"></span>**andamento da verificação do MPNOTIFY \_ \_ FASTPATH \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-162"><span id="MPNOTIFY_SCAN_FASTPATH_PROGRESS"></span><span id="mpnotify_scan_fastpath_progress"></span>**MPNOTIFY\_SCAN\_FASTPATH\_PROGRESS**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-163">Notificação de progresso para verificações de FastPath, usadas internamente e convertidas em **\_ \_ andamento da verificação do mpnotify** para o externo.</span><span class="sxs-lookup"><span data-stu-id="79b06-163">Progress notification for fastpath rescans, used internally and converted to **MPNOTIFY\_SCAN\_PROGRESS** for external.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-164"><span id="MPNOTIFY_CLEAN_START"></span><span id="mpnotify_clean_start"></span>**\_início da limpeza do mpnotify \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-164"><span id="MPNOTIFY_CLEAN_START"></span><span id="mpnotify_clean_start"></span>**MPNOTIFY\_CLEAN\_START**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-165">Limpeza iniciada.</span><span class="sxs-lookup"><span data-stu-id="79b06-165">Cleaning started.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-166"><span id="MPNOTIFY_CLEAN_COMPLETE"></span><span id="mpnotify_clean_complete"></span>**limpeza de MPNOTIFY \_ \_ concluída**</span><span class="sxs-lookup"><span data-stu-id="79b06-166"><span id="MPNOTIFY_CLEAN_COMPLETE"></span><span id="mpnotify_clean_complete"></span>**MPNOTIFY\_CLEAN\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-167">Limpeza concluída.</span><span class="sxs-lookup"><span data-stu-id="79b06-167">Cleaning completed.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-168"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_START"></span><span id="mpnotify_clean_restorepoint_start"></span>**MPNOTIFY \_ limpar \_ RESTOREPOINT \_ Iniciar**</span><span class="sxs-lookup"><span data-stu-id="79b06-168"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_START"></span><span id="mpnotify_clean_restorepoint_start"></span>**MPNOTIFY\_CLEAN\_RESTOREPOINT\_START**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-169">Iniciada a criação de um ponto de restauração do sistema.</span><span class="sxs-lookup"><span data-stu-id="79b06-169">Started to create a system restore point.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-170"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED"></span><span id="mpnotify_clean_restorepoint_succeeded"></span>**MPNOTIFY \_ limpar \_ RESTOREPOINT com \_ êxito**</span><span class="sxs-lookup"><span data-stu-id="79b06-170"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED"></span><span id="mpnotify_clean_restorepoint_succeeded"></span>**MPNOTIFY\_CLEAN\_RESTOREPOINT\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-171">Ponto de restauração do sistema criado com êxito.</span><span class="sxs-lookup"><span data-stu-id="79b06-171">System restore point successfully created.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-172"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_FAILED"></span><span id="mpnotify_clean_restorepoint_failed"></span>**MPNOTIFY \_ limpar \_ RESTOREPOINT \_ falhou**</span><span class="sxs-lookup"><span data-stu-id="79b06-172"><span id="MPNOTIFY_CLEAN_RESTOREPOINT_FAILED"></span><span id="mpnotify_clean_restorepoint_failed"></span>**MPNOTIFY\_CLEAN\_RESTOREPOINT\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-173">Falha na criação do ponto de restauração do sistema.</span><span class="sxs-lookup"><span data-stu-id="79b06-173">System restore point creation failed.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-174"><span id="MPNOTIFY_CLEAN_THREAT_START"></span><span id="mpnotify_clean_threat_start"></span>**\_início da \_ ameaça de limpeza do mpnotify \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-174"><span id="MPNOTIFY_CLEAN_THREAT_START"></span><span id="mpnotify_clean_threat_start"></span>**MPNOTIFY\_CLEAN\_THREAT\_START**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-175">A limpeza é iniciada para uma determinada ameaça.</span><span class="sxs-lookup"><span data-stu-id="79b06-175">Cleaning is started for a particular threat.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-176"><span id="MPNOTIFY_CLEAN_THREAT_SUCCEEDED"></span><span id="mpnotify_clean_threat_succeeded"></span>**ameaça de limpeza de MPNOTIFY \_ \_ \_ bem-sucedida**</span><span class="sxs-lookup"><span data-stu-id="79b06-176"><span id="MPNOTIFY_CLEAN_THREAT_SUCCEEDED"></span><span id="mpnotify_clean_threat_succeeded"></span>**MPNOTIFY\_CLEAN\_THREAT\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-177">A limpeza foi bem-sucedida para uma determinada ameaça.</span><span class="sxs-lookup"><span data-stu-id="79b06-177">Cleaning is succeeded for a particular threat.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-178"><span id="MPNOTIFY_CLEAN_THREAT_FAILED"></span><span id="mpnotify_clean_threat_failed"></span>**\_ \_ falha ao limpar ameaça mpnotify \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-178"><span id="MPNOTIFY_CLEAN_THREAT_FAILED"></span><span id="mpnotify_clean_threat_failed"></span>**MPNOTIFY\_CLEAN\_THREAT\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-179">A limpeza falhou para uma determinada ameaça.</span><span class="sxs-lookup"><span data-stu-id="79b06-179">Cleaning has failed for a particular threat.</span></span> <span data-ttu-id="79b06-180">**Erro \_ do O código de erro de ameaça de MP \_ \_ não \_ encontrado** indica que a ameaça não foi encontrada (e não foi uma falha de limpeza).</span><span class="sxs-lookup"><span data-stu-id="79b06-180">**ERROR\_MP\_THREAT\_NOT\_FOUND** error code indicates that the threat was not found (and was not a failure to clean).</span></span>

</dd> <dt>

<span data-ttu-id="79b06-181"><span id="MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED"></span><span id="mpnotify_clean_resource_succeeded"></span>**\_êxito ao limpar \_ recurso \_ mpnotify**</span><span class="sxs-lookup"><span data-stu-id="79b06-181"><span id="MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED"></span><span id="mpnotify_clean_resource_succeeded"></span>**MPNOTIFY\_CLEAN\_RESOURCE\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-182">A limpeza foi bem-sucedida para um recurso específico.</span><span class="sxs-lookup"><span data-stu-id="79b06-182">Cleaning is succeeded for a particular resource.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-183"><span id="MPNOTIFY_CLEAN_RESOURCE_FAILED"></span><span id="mpnotify_clean_resource_failed"></span>**\_ \_ falha ao limpar recurso mpnotify \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-183"><span id="MPNOTIFY_CLEAN_RESOURCE_FAILED"></span><span id="mpnotify_clean_resource_failed"></span>**MPNOTIFY\_CLEAN\_RESOURCE\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-184">A limpeza falhou para um recurso específico.</span><span class="sxs-lookup"><span data-stu-id="79b06-184">Cleaning has failed for a particular resource.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-185"><span id="MPNOTIFY_CLEAN_THREAT_COMPLETE"></span><span id="mpnotify_clean_threat_complete"></span>**MPNOTIFY \_ limpeza de \_ ameaças \_ concluída**</span><span class="sxs-lookup"><span data-stu-id="79b06-185"><span id="MPNOTIFY_CLEAN_THREAT_COMPLETE"></span><span id="mpnotify_clean_threat_complete"></span>**MPNOTIFY\_CLEAN\_THREAT\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-186">A limpeza foi concluída para uma determinada ameaça.</span><span class="sxs-lookup"><span data-stu-id="79b06-186">Cleaning has completed for a particular threat.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-187"><span id="MPNOTIFY_PRECHECK_START"></span><span id="mpnotify_precheck_start"></span>**\_início da PREverificação de mpnotify \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-187"><span id="MPNOTIFY_PRECHECK_START"></span><span id="mpnotify_precheck_start"></span>**MPNOTIFY\_PRECHECK\_START**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-188">Limpar preverificação iniciada.</span><span class="sxs-lookup"><span data-stu-id="79b06-188">Clean precheck started.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-189"><span id="MPNOTIFY_PRECHECK_COMPLETE"></span><span id="mpnotify_precheck_complete"></span>**preverificação de MPNOTIFY \_ \_ concluída**</span><span class="sxs-lookup"><span data-stu-id="79b06-189"><span id="MPNOTIFY_PRECHECK_COMPLETE"></span><span id="mpnotify_precheck_complete"></span>**MPNOTIFY\_PRECHECK\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-190">Limpeza de marca de seleção concluída.</span><span class="sxs-lookup"><span data-stu-id="79b06-190">Clean precheck completed.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-191"><span id="MPNOTIFY_PRECHECK_RESOURCE_BLOCKED"></span><span id="mpnotify_precheck_resource_blocked"></span>**recurso de MPNOTIFY de \_ verificação \_ \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="79b06-191"><span id="MPNOTIFY_PRECHECK_RESOURCE_BLOCKED"></span><span id="mpnotify_precheck_resource_blocked"></span>**MPNOTIFY\_PRECHECK\_RESOURCE\_BLOCKED**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-192">Limpar preverificação detectou recurso bloqueado.</span><span class="sxs-lookup"><span data-stu-id="79b06-192">Clean precheck detected blocked resource.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-193"><span id="MPNOTIFY_THREAT_DETECTED"></span><span id="mpnotify_threat_detected"></span>**\_ameaça mpnotify \_ detectada**</span><span class="sxs-lookup"><span data-stu-id="79b06-193"><span id="MPNOTIFY_THREAT_DETECTED"></span><span id="mpnotify_threat_detected"></span>**MPNOTIFY\_THREAT\_DETECTED**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-194">Nova ameaça detectada no sistema.</span><span class="sxs-lookup"><span data-stu-id="79b06-194">New threat detected in system.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-195"><span id="MPNOTIFY_THREAT_MODIFIED"></span><span id="mpnotify_threat_modified"></span>**\_ameaça mpnotify \_ modificada**</span><span class="sxs-lookup"><span data-stu-id="79b06-195"><span id="MPNOTIFY_THREAT_MODIFIED"></span><span id="mpnotify_threat_modified"></span>**MPNOTIFY\_THREAT\_MODIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-196">Informações de ameaças modificadas.</span><span class="sxs-lookup"><span data-stu-id="79b06-196">Threat information modified.</span></span> <span data-ttu-id="79b06-197">Por exemplo, um novo recurso foi adicionado.</span><span class="sxs-lookup"><span data-stu-id="79b06-197">For example, a new resource was added.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-198"><span id="MPNOTIFY_THREAT_CLEAN_SUCCEEDED"></span><span id="mpnotify_threat_clean_succeeded"></span>**limpeza de ameaça de MPNOTIFY \_ \_ \_ bem-sucedida**</span><span class="sxs-lookup"><span data-stu-id="79b06-198"><span id="MPNOTIFY_THREAT_CLEAN_SUCCEEDED"></span><span id="mpnotify_threat_clean_succeeded"></span>**MPNOTIFY\_THREAT\_CLEAN\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-199">Ação de limpeza bem-sucedida para uma ameaça.</span><span class="sxs-lookup"><span data-stu-id="79b06-199">Cleaning action succeeded for a threat.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-200"><span id="MPNOTIFY_THREAT_CLEAN_FAILED"></span><span id="mpnotify_threat_clean_failed"></span>**\_ \_ falha ao limpar ameaça mpnotify \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-200"><span id="MPNOTIFY_THREAT_CLEAN_FAILED"></span><span id="mpnotify_threat_clean_failed"></span>**MPNOTIFY\_THREAT\_CLEAN\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-201">Falha na ação de limpeza para uma ameaça.</span><span class="sxs-lookup"><span data-stu-id="79b06-201">Cleaning action failed for a threat.</span></span> <span data-ttu-id="79b06-202">**Erro \_ do O código de erro de ameaça de MP \_ \_ não \_ encontrado** indica que a ameaça não foi encontrada (e não foi uma falha de limpeza).</span><span class="sxs-lookup"><span data-stu-id="79b06-202">**ERROR\_MP\_THREAT\_NOT\_FOUND** error code indicates that the threat was not found (and was not a failure to clean).</span></span>

</dd> <dt>

<span data-ttu-id="79b06-203"><span id="MPNOTIFY_THREAT_ABANDONED"></span><span id="mpnotify_threat_abandoned"></span>**\_ameaça mpnotify \_ abandonada**</span><span class="sxs-lookup"><span data-stu-id="79b06-203"><span id="MPNOTIFY_THREAT_ABANDONED"></span><span id="mpnotify_threat_abandoned"></span>**MPNOTIFY\_THREAT\_ABANDONED**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-204">Nenhuma correção ocorreu antes da interrupção do serviço.</span><span class="sxs-lookup"><span data-stu-id="79b06-204">No remediation occurred before the service was stopped.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-205"><span id="MPNOTIFY_THREAT_CLEAN_EVENT_START"></span><span id="mpnotify_threat_clean_event_start"></span>**\_início do \_ evento de limpeza de ameaça mpnotify \_ \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-205"><span id="MPNOTIFY_THREAT_CLEAN_EVENT_START"></span><span id="mpnotify_threat_clean_event_start"></span>**MPNOTIFY\_THREAT\_CLEAN\_EVENT\_START**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-206">Uma ação de limpeza foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="79b06-206">A cleaning action has been started.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-207"><span id="MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE"></span><span id="mpnotify_threat_clean_event_complete"></span>**\_evento de limpeza de ameaça mpnotify \_ \_ \_ concluído**</span><span class="sxs-lookup"><span data-stu-id="79b06-207"><span id="MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE"></span><span id="mpnotify_threat_clean_event_complete"></span>**MPNOTIFY\_THREAT\_CLEAN\_EVENT\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-208">Uma ação de limpeza foi encerrada.</span><span class="sxs-lookup"><span data-stu-id="79b06-208">A cleaning action has ended.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-209"><span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span>**MPNOTIFY \_ SIGUPDATE \_ Start**</span><span class="sxs-lookup"><span data-stu-id="79b06-209"><span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span>**MPNOTIFY\_SIGUPDATE\_START**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-210">Atualização de assinatura iniciada.</span><span class="sxs-lookup"><span data-stu-id="79b06-210">Signature update started.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-211"><span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span>**início da pesquisa do MPNOTIFY \_ SIGUPDATE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-211"><span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span>**MPNOTIFY\_SIGUPDATE\_SEARCH\_START**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-212">Pesquisa de atualizações iniciada.</span><span class="sxs-lookup"><span data-stu-id="79b06-212">Search for updates started.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-213"><span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span>**pesquisa do MPNOTIFY \_ SIGUPDATE \_ \_ concluída**</span><span class="sxs-lookup"><span data-stu-id="79b06-213"><span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span>**MPNOTIFY\_SIGUPDATE\_SEARCH\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-214">Pesquisa de atualizações concluída.</span><span class="sxs-lookup"><span data-stu-id="79b06-214">Search for updates completed.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-215"><span id="MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE"></span><span id="mpnotify_sigupdate_software_update_available"></span>**\_atualização de \_ software mpnotify SIGUPDATE \_ \_ disponível**</span><span class="sxs-lookup"><span data-stu-id="79b06-215"><span id="MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE"></span><span id="mpnotify_sigupdate_software_update_available"></span>**MPNOTIFY\_SIGUPDATE\_SOFTWARE\_UPDATE\_AVAILABLE**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-216">Atualização de software disponível.</span><span class="sxs-lookup"><span data-stu-id="79b06-216">Software update available.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-217"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span>**início do download do MPNOTIFY \_ SIGUPDATE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-217"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_START**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-218">Download iniciado.</span><span class="sxs-lookup"><span data-stu-id="79b06-218">Download started.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-219"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span>**progresso do download do MPNOTIFY \_ SIGUPDATE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-219"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_PROGRESS**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-220">Download em andamento.</span><span class="sxs-lookup"><span data-stu-id="79b06-220">Download in progress.</span></span> <span data-ttu-id="79b06-221">Os dados de retorno de chamada contêm o progresso.</span><span class="sxs-lookup"><span data-stu-id="79b06-221">Callback data contains progress.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-222"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span>**Download do MPNOTIFY \_ SIGUPDATE \_ \_ concluído**</span><span class="sxs-lookup"><span data-stu-id="79b06-222"><span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span>**MPNOTIFY\_SIGUPDATE\_DOWNLOAD\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-223">Download concluído.</span><span class="sxs-lookup"><span data-stu-id="79b06-223">Download completed.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-224"><span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span>**início da instalação do MPNOTIFY \_ SIGUPDATE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-224"><span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span>**MPNOTIFY\_SIGUPDATE\_INSTALL\_START**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-225">Instalação iniciada.</span><span class="sxs-lookup"><span data-stu-id="79b06-225">Installation started.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-226"><span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span>**progresso da instalação do MPNOTIFY \_ SIGUPDATE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-226"><span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span>**MPNOTIFY\_SIGUPDATE\_INSTALL\_PROGRESS**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-227">Instalação em andamento.</span><span class="sxs-lookup"><span data-stu-id="79b06-227">Installation in progress.</span></span> <span data-ttu-id="79b06-228">Os dados de retorno de chamada contêm o progresso.</span><span class="sxs-lookup"><span data-stu-id="79b06-228">Callback data contains progress.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-229"><span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span>**instalação do MPNOTIFY \_ SIGUPDATE \_ \_ concluída**</span><span class="sxs-lookup"><span data-stu-id="79b06-229"><span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span>**MPNOTIFY\_SIGUPDATE\_INSTALL\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-230">Instalação concluída.</span><span class="sxs-lookup"><span data-stu-id="79b06-230">Installation complete.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-231"><span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span>**\_reinicialização mpnotify SIGUPDATE \_ \_ necessária**</span><span class="sxs-lookup"><span data-stu-id="79b06-231"><span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span>**MPNOTIFY\_SIGUPDATE\_REBOOT\_REQUIRED**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-232">A atualização requer reinicialização.</span><span class="sxs-lookup"><span data-stu-id="79b06-232">Update requires reboot.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-233"><span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span>**\_solicitação mpnotify \_ SIGUPDATE \_ processada**</span><span class="sxs-lookup"><span data-stu-id="79b06-233"><span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span>**MPNOTIFY\_SIGUPDATE\_REQUEST\_PROCESSED**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-234">O serviço processou uma solicitação de atualização de assinatura.</span><span class="sxs-lookup"><span data-stu-id="79b06-234">Service processed a signature update request.</span></span> <span data-ttu-id="79b06-235">A falha ou o êxito é indicado por **HRESULT** nos dados de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="79b06-235">Failure or success is indicated by **hResult** in the callback data.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-236"><span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span>**MPNOTIFY \_ SIGUPDATE \_ concluída**</span><span class="sxs-lookup"><span data-stu-id="79b06-236"><span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span>**MPNOTIFY\_SIGUPDATE\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-237">Atualização concluída.</span><span class="sxs-lookup"><span data-stu-id="79b06-237">Update complete.</span></span> <span data-ttu-id="79b06-238">**S \_** O status falso indica que nenhuma atualização foi necessária.</span><span class="sxs-lookup"><span data-stu-id="79b06-238">**S\_FALSE** status indicates that no updates were needed.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-239"><span id="MPNOTIFY_SAMPLE_START"></span><span id="mpnotify_sample_start"></span>**\_início de exemplo do mpnotify \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-239"><span id="MPNOTIFY_SAMPLE_START"></span><span id="mpnotify_sample_start"></span>**MPNOTIFY\_SAMPLE\_START**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-240">Envio de amostra iniciado.</span><span class="sxs-lookup"><span data-stu-id="79b06-240">Sample submission started.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-241"><span id="MPNOTIFY_SAMPLE_COMPLETE"></span><span id="mpnotify_sample_complete"></span>**exemplo de MPNOTIFY \_ \_ concluído**</span><span class="sxs-lookup"><span data-stu-id="79b06-241"><span id="MPNOTIFY_SAMPLE_COMPLETE"></span><span id="mpnotify_sample_complete"></span>**MPNOTIFY\_SAMPLE\_COMPLETE**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-242">Envio de amostra concluído.</span><span class="sxs-lookup"><span data-stu-id="79b06-242">Sample submission completed.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-243"><span id="MPNOTIFY_SAMPLE_ITEM_START"></span><span id="mpnotify_sample_item_start"></span>**\_início do \_ item de exemplo mpnotify \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-243"><span id="MPNOTIFY_SAMPLE_ITEM_START"></span><span id="mpnotify_sample_item_start"></span>**MPNOTIFY\_SAMPLE\_ITEM\_START**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-244">Envio de item de exemplo específico iniciado.</span><span class="sxs-lookup"><span data-stu-id="79b06-244">Specific sample item submission started.</span></span> <span data-ttu-id="79b06-245">O índice do item de exemplo está disponível nos [**\_ dados do MPSAMPLE**](mpsample-data.md).</span><span class="sxs-lookup"><span data-stu-id="79b06-245">Sample item index is available in [**MPSAMPLE\_DATA**](mpsample-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="79b06-246"><span id="MPNOTIFY_SAMPLE_ITEM_SUCCEEDED"></span><span id="mpnotify_sample_item_succeeded"></span>**ITEM de exemplo de MPNOTIFY \_ \_ \_ bem-sucedido**</span><span class="sxs-lookup"><span data-stu-id="79b06-246"><span id="MPNOTIFY_SAMPLE_ITEM_SUCCEEDED"></span><span id="mpnotify_sample_item_succeeded"></span>**MPNOTIFY\_SAMPLE\_ITEM\_SUCCEEDED**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-247">Envio de item de exemplo específico bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="79b06-247">Specific sample item submission succeeded.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-248"><span id="MPNOTIFY_SAMPLE_ITEM_FAILED"></span><span id="mpnotify_sample_item_failed"></span>**\_ \_ falha no item de exemplo mpnotify \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-248"><span id="MPNOTIFY_SAMPLE_ITEM_FAILED"></span><span id="mpnotify_sample_item_failed"></span>**MPNOTIFY\_SAMPLE\_ITEM\_FAILED**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-249">Falha ao enviar o item de exemplo específico.</span><span class="sxs-lookup"><span data-stu-id="79b06-249">Specific sample item submission failed.</span></span> <span data-ttu-id="79b06-250">O código de erro está disponível nos [**\_ dados do MPCALLBACK**](mpcallback-data.md).</span><span class="sxs-lookup"><span data-stu-id="79b06-250">Error code is available in [**MPCALLBACK\_DATA**](mpcallback-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="79b06-251"><span id="MPNOTIFY_RESERVED_DATA"></span><span id="mpnotify_reserved_data"></span>**MPNOTIFY \_ \_ dados reservados**</span><span class="sxs-lookup"><span data-stu-id="79b06-251"><span id="MPNOTIFY_RESERVED_DATA"></span><span id="mpnotify_reserved_data"></span>**MPNOTIFY\_RESERVED\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-252">Dados reservados internos.</span><span class="sxs-lookup"><span data-stu-id="79b06-252">Internal reserved data.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-253"><span id="MPNOTIFY_FASTPATH_SIG_ADDED"></span><span id="mpnotify_fastpath_sig_added"></span>**MPNOTIFY \_ FASTPATH \_ SIG \_ adicionado**</span><span class="sxs-lookup"><span data-stu-id="79b06-253"><span id="MPNOTIFY_FASTPATH_SIG_ADDED"></span><span id="mpnotify_fastpath_sig_added"></span>**MPNOTIFY\_FASTPATH\_SIG\_ADDED**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-254">Uma assinatura FastPath adicionou ou desabilitou uma assinatura.</span><span class="sxs-lookup"><span data-stu-id="79b06-254">A Fastpath signature has either added or disabled a signature.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-255"><span id="MPNOTIFY_FASTPATH_SIG_REMOVED"></span><span id="mpnotify_fastpath_sig_removed"></span>**\_SIG mpnotify \_ FASTPATH \_ removido**</span><span class="sxs-lookup"><span data-stu-id="79b06-255"><span id="MPNOTIFY_FASTPATH_SIG_REMOVED"></span><span id="mpnotify_fastpath_sig_removed"></span>**MPNOTIFY\_FASTPATH\_SIG\_REMOVED**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-256">Uma assinatura do FastPath foi removida.</span><span class="sxs-lookup"><span data-stu-id="79b06-256">A FastPath signature has been removed.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-257"><span id="MPNOTIFY_NIS_PRIVATE"></span><span id="mpnotify_nis_private"></span>**MPNOTIFY \_ NIS \_ particular**</span><span class="sxs-lookup"><span data-stu-id="79b06-257"><span id="MPNOTIFY_NIS_PRIVATE"></span><span id="mpnotify_nis_private"></span>**MPNOTIFY\_NIS\_PRIVATE**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-258">Notificações privada NIS.</span><span class="sxs-lookup"><span data-stu-id="79b06-258">NIS private notifcations.</span></span> <span data-ttu-id="79b06-259">Nenhum parceiro deve se registrar para isso.</span><span class="sxs-lookup"><span data-stu-id="79b06-259">No partners should register for this.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-260"><span id="MPNOTIFY_HEALTH_CHANGE"></span><span id="mpnotify_health_change"></span>**\_alteração de integridade do mpnotify \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-260"><span id="MPNOTIFY_HEALTH_CHANGE"></span><span id="mpnotify_health_change"></span>**MPNOTIFY\_HEALTH\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-261">O serviço AM entrou em um novo estado.</span><span class="sxs-lookup"><span data-stu-id="79b06-261">The AM service has entered a new state.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-262"><span id="MPNOTIFY_HEALTH_RECOVERY"></span><span id="mpnotify_health_recovery"></span>**\_recuperação de integridade do mpnotify \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-262"><span id="MPNOTIFY_HEALTH_RECOVERY"></span><span id="mpnotify_health_recovery"></span>**MPNOTIFY\_HEALTH\_RECOVERY**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-263">O serviço AM foi recuperado de um estado.</span><span class="sxs-lookup"><span data-stu-id="79b06-263">The AM service has recovered from a state.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-264"><span id="MPNOTIFY_HEALTH_START"></span><span id="mpnotify_health_start"></span>**\_início da integridade do mpnotify \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-264"><span id="MPNOTIFY_HEALTH_START"></span><span id="mpnotify_health_start"></span>**MPNOTIFY\_HEALTH\_START**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-265">O serviço AM inicializou a integridade do sistema.</span><span class="sxs-lookup"><span data-stu-id="79b06-265">The AM service has initialized the health of the system.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-266"><span id="MPNOTIFY_ENDOFLIFE_CHANGE"></span><span id="mpnotify_endoflife_change"></span>**MPNOTIFY \_ ENDOFLIFE \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-266"><span id="MPNOTIFY_ENDOFLIFE_CHANGE"></span><span id="mpnotify_endoflife_change"></span>**MPNOTIFY\_ENDOFLIFE\_CHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-267">As datas de expiração do "fim da vida útil" do serviço AM foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="79b06-267">The "End Of Life" expiry dates for the AM service have changed.</span></span>

</dd> <dt>

<span data-ttu-id="79b06-268"><span id="MPNOTIFY_MALWARETOAST_DATA"></span><span id="mpnotify_malwaretoast_data"></span>**MPNOTIFY \_ MALWARETOAST \_ Data**</span><span class="sxs-lookup"><span data-stu-id="79b06-268"><span id="MPNOTIFY_MALWARETOAST_DATA"></span><span id="mpnotify_malwaretoast_data"></span>**MPNOTIFY\_MALWARETOAST\_DATA**</span></span>
</dt> <dd>

<span data-ttu-id="79b06-269">O serviço AM encontrou malware que pode ter causado alteração de configurações críticas no computador.</span><span class="sxs-lookup"><span data-stu-id="79b06-269">The AM service has encountered malware that might have caused critical settings change in the machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="79b06-270">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79b06-270">Requirements</span></span>



| <span data-ttu-id="79b06-271">Requisito</span><span class="sxs-lookup"><span data-stu-id="79b06-271">Requirement</span></span> | <span data-ttu-id="79b06-272">Valor</span><span class="sxs-lookup"><span data-stu-id="79b06-272">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79b06-273">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79b06-273">Minimum supported client</span></span><br/> | <span data-ttu-id="79b06-274">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="79b06-274">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="79b06-275">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79b06-275">Minimum supported server</span></span><br/> | <span data-ttu-id="79b06-276">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="79b06-276">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="79b06-277">parâmetro</span><span class="sxs-lookup"><span data-stu-id="79b06-277">Header</span></span><br/>                   | <dl> <span data-ttu-id="79b06-278"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="79b06-278"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79b06-279">Confira também</span><span class="sxs-lookup"><span data-stu-id="79b06-279">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79b06-280">**MpManagerStatusQueryEx**</span><span class="sxs-lookup"><span data-stu-id="79b06-280">**MpManagerStatusQueryEx**</span></span>](mpmanagerstatusqueryex.md)
</dt> <dt>

[<span data-ttu-id="79b06-281">**dados do MPCALLBACK \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-281">**MPCALLBACK\_DATA**</span></span>](mpcallback-data.md)
</dt> <dt>

[<span data-ttu-id="79b06-282">**dados do MPSAMPLE \_**</span><span class="sxs-lookup"><span data-stu-id="79b06-282">**MPSAMPLE\_DATA**</span></span>](mpsample-data.md)
</dt> </dl>

 

 





