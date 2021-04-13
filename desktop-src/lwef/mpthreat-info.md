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
# <a name="mpthreat_info-structure"></a><span data-ttu-id="cd11d-105">Estrutura de informações do MPTHREAT \_</span><span class="sxs-lookup"><span data-stu-id="cd11d-105">MPTHREAT\_INFO structure</span></span>

<span data-ttu-id="cd11d-106">Contém informações sobre uma ameaça.</span><span class="sxs-lookup"><span data-stu-id="cd11d-106">Contains information about a threat.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd11d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd11d-107">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="cd11d-108">Membros</span><span class="sxs-lookup"><span data-stu-id="cd11d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="cd11d-109">**Threatid**</span><span class="sxs-lookup"><span data-stu-id="cd11d-109">**ThreatID**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-110">Tipo: **\_ ID de MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="cd11d-110">Type: **MPTHREAT\_ID**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-111">Identificador de ameaça.</span><span class="sxs-lookup"><span data-stu-id="cd11d-111">Threat identifier.</span></span> <span data-ttu-id="cd11d-112">O bit superior é definido para identificar ameaças relacionadas ao antivírus.</span><span class="sxs-lookup"><span data-stu-id="cd11d-112">Upper bit is set to identify antivirus-related threats.</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-113">**Detectid**</span><span class="sxs-lookup"><span data-stu-id="cd11d-113">**DetectionID**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-114">Tipo: **GUID**</span><span class="sxs-lookup"><span data-stu-id="cd11d-114">Type: **GUID**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-115">ID de detecção.</span><span class="sxs-lookup"><span data-stu-id="cd11d-115">Detection ID.</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-116">**Nome**</span><span class="sxs-lookup"><span data-stu-id="cd11d-116">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-117">Tipo: **PG \_ MIDL \_ String LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="cd11d-117">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-118">Nome da ameaça.</span><span class="sxs-lookup"><span data-stu-id="cd11d-118">Threat name.</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-119">**Threattype**</span><span class="sxs-lookup"><span data-stu-id="cd11d-119">**ThreatType**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-120">Tipo: **[ **\_ tipo de MPTHREAT**](mpthreat-type.md)**</span><span class="sxs-lookup"><span data-stu-id="cd11d-120">Type: **[**MPTHREAT\_TYPE**](mpthreat-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-121">Tipo de ameaça.</span><span class="sxs-lookup"><span data-stu-id="cd11d-121">Threat type.</span></span> <span data-ttu-id="cd11d-122">Usado para diferenciar entre diferentes tipos de ameaças, como conhecido, desconhecido ou conhecido como válido.</span><span class="sxs-lookup"><span data-stu-id="cd11d-122">Used to differentiate among different threat types such as known bad, unknown, or known good.</span></span> <span data-ttu-id="cd11d-123">Consulte [**\_ tipo de MPTHREAT**](mpthreat-type.md).</span><span class="sxs-lookup"><span data-stu-id="cd11d-123">See [**MPTHREAT\_TYPE**](mpthreat-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-124">**ThreatCriticality**</span><span class="sxs-lookup"><span data-stu-id="cd11d-124">**ThreatCriticality**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-125">Tipo: **[ **\_ severidade MPTHREAT**](mpthreat-severity.md)**</span><span class="sxs-lookup"><span data-stu-id="cd11d-125">Type: **[**MPTHREAT\_SEVERITY**](mpthreat-severity.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-126">Criticalidade da ameaça.</span><span class="sxs-lookup"><span data-stu-id="cd11d-126">Threat criticality.</span></span> <span data-ttu-id="cd11d-127">Consulte [**\_ severidade do MPTHREAT**](mpthreat-severity.md).</span><span class="sxs-lookup"><span data-stu-id="cd11d-127">See [**MPTHREAT\_SEVERITY**](mpthreat-severity.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-128">**ThreatCategory**</span><span class="sxs-lookup"><span data-stu-id="cd11d-128">**ThreatCategory**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-129">Tipo: **[ **\_ categoria MPTHREAT**](mpthreat-category.md)**</span><span class="sxs-lookup"><span data-stu-id="cd11d-129">Type: **[**MPTHREAT\_CATEGORY**](mpthreat-category.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-130">Categoria de ameaça, como um cavalo de Troia ou um keylogger.</span><span class="sxs-lookup"><span data-stu-id="cd11d-130">Threat category, such as a trojan or a keylogger.</span></span> <span data-ttu-id="cd11d-131">Consulte [**a \_ categoria MPTHREAT**](mpthreat-category.md).</span><span class="sxs-lookup"><span data-stu-id="cd11d-131">See [**MPTHREAT\_CATEGORY**](mpthreat-category.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-132">**ThreatShortDescriptionID**</span><span class="sxs-lookup"><span data-stu-id="cd11d-132">**ThreatShortDescriptionID**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-133">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="cd11d-133">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-134">ID da descrição curta da ameaça.</span><span class="sxs-lookup"><span data-stu-id="cd11d-134">Threat short description ID.</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-135">**ThreatAdviseDescriptionID**</span><span class="sxs-lookup"><span data-stu-id="cd11d-135">**ThreatAdviseDescriptionID**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-136">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="cd11d-136">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-137">ID da descrição do aviso de ameaça.</span><span class="sxs-lookup"><span data-stu-id="cd11d-137">Threat advise description ID.</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-138">**ThreatStatus**</span><span class="sxs-lookup"><span data-stu-id="cd11d-138">**ThreatStatus**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-139">Tipo: **[ **MPTHREAT \_ status**](mpthreat-status.md)**</span><span class="sxs-lookup"><span data-stu-id="cd11d-139">Type: **[**MPTHREAT\_STATUS**](mpthreat-status.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-140">Status de ameaça, como detectado, limpo ou em quarentena.</span><span class="sxs-lookup"><span data-stu-id="cd11d-140">Threat status such as detected, cleaned, or quarantined.</span></span> <span data-ttu-id="cd11d-141">Consulte [**\_ status do MPTHREAT**](mpthreat-status.md).</span><span class="sxs-lookup"><span data-stu-id="cd11d-141">See [**MPTHREAT\_STATUS**](mpthreat-status.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-142">**SuggestedActionCount**</span><span class="sxs-lookup"><span data-stu-id="cd11d-142">**SuggestedActionCount**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-143">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="cd11d-143">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-144">Contagem de ações sugeridas em **SuggestedActionArray**.</span><span class="sxs-lookup"><span data-stu-id="cd11d-144">Count of suggested actions in **SuggestedActionArray**.</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-145">**SuggestedActionArray**</span><span class="sxs-lookup"><span data-stu-id="cd11d-145">**SuggestedActionArray**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-146">Tipo: **[**MPTHREAT \_ Action**](mpthreat-action.md) \[ MP \_ Max \_ sugestões\]**</span><span class="sxs-lookup"><span data-stu-id="cd11d-146">Type: **[**MPTHREAT\_ACTION**](mpthreat-action.md)\[MP\_MAX\_SUGGESTIONS\]**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-147">Matriz de ações sugeridas.</span><span class="sxs-lookup"><span data-stu-id="cd11d-147">Array of suggested actions.</span></span> <span data-ttu-id="cd11d-148">Consulte [**a \_ ação MPTHREAT**](mpthreat-action.md).</span><span class="sxs-lookup"><span data-stu-id="cd11d-148">See [**MPTHREAT\_ACTION**](mpthreat-action.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-149">**ResourceCount**</span><span class="sxs-lookup"><span data-stu-id="cd11d-149">**ResourceCount**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-150">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="cd11d-150">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-151">Contagem de recursos na **resourceList**.</span><span class="sxs-lookup"><span data-stu-id="cd11d-151">Count of resources in **ResourceList**.</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-152">**ResourceList**</span><span class="sxs-lookup"><span data-stu-id="cd11d-152">**ResourceList**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-153">Tipo: \**PMPRESOURCE \_ info \** _</span><span class="sxs-lookup"><span data-stu-id="cd11d-153">Type: \**PMPRESOURCE\_INFO\** _</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-154">Lista de recursos identificados com a ameaça.</span><span class="sxs-lookup"><span data-stu-id="cd11d-154">List of resources identified with the threat.</span></span> <span data-ttu-id="cd11d-155">Consulte [_ *MPRESOURCE \_ info* \*](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="cd11d-155">See [_ *MPRESOURCE\_INFO*\*](mpresource-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-156">**ThreatStatusTime**</span><span class="sxs-lookup"><span data-stu-id="cd11d-156">**ThreatStatusTime**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-157">Tipo: **ULARGE \_ inteiro**</span><span class="sxs-lookup"><span data-stu-id="cd11d-157">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-158">Hora em que o status da ameaça foi alterado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="cd11d-158">Time when threat status last changed.</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-159">**ThreatStatusCode**</span><span class="sxs-lookup"><span data-stu-id="cd11d-159">**ThreatStatusCode**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-160">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="cd11d-160">Type: **HRESULT**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-161">Código de status associado ao status da ameaça.</span><span class="sxs-lookup"><span data-stu-id="cd11d-161">Status code associated with the threat status.</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-162">**ThreatDetection**</span><span class="sxs-lookup"><span data-stu-id="cd11d-162">**ThreatDetection**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-163">Tipo: **[ **\_ detecção de MPTHREAT**](mpthreat-detection.md)**</span><span class="sxs-lookup"><span data-stu-id="cd11d-163">Type: **[**MPTHREAT\_DETECTION**](mpthreat-detection.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-164">Tipo de detecção de ameaças, como concreto, suspeita ou genérico.</span><span class="sxs-lookup"><span data-stu-id="cd11d-164">Threat detection type, such as concrete, suspicious, or generic.</span></span> <span data-ttu-id="cd11d-165">Consulte [**\_ detecção de MPTHREAT**](mpthreat-detection.md).</span><span class="sxs-lookup"><span data-stu-id="cd11d-165">See [**MPTHREAT\_DETECTION**](mpthreat-detection.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-166">**QuarantineGuid**</span><span class="sxs-lookup"><span data-stu-id="cd11d-166">**QuarantineGuid**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-167">Tipo: **GUID**</span><span class="sxs-lookup"><span data-stu-id="cd11d-167">Type: **GUID**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-168">GUID de quarentena.</span><span class="sxs-lookup"><span data-stu-id="cd11d-168">Quarantine guid.</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-169">**ExecutionStatus**</span><span class="sxs-lookup"><span data-stu-id="cd11d-169">**ExecutionStatus**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-170">Tipo: **[ **MPEXECUTION \_ status**](mpexecution-status.md)**</span><span class="sxs-lookup"><span data-stu-id="cd11d-170">Type: **[**MPEXECUTION\_STATUS**](mpexecution-status.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-171">Status de execução da ameaça, como não conhecido, bloqueado ou ativo.</span><span class="sxs-lookup"><span data-stu-id="cd11d-171">Execution status of the threat, such as not known, blocked, or active.</span></span> <span data-ttu-id="cd11d-172">Consulte [**\_ status do MPEXECUTION**](mpexecution-status.md).</span><span class="sxs-lookup"><span data-stu-id="cd11d-172">See [**MPEXECUTION\_STATUS**](mpexecution-status.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-173">**Dados**</span><span class="sxs-lookup"><span data-stu-id="cd11d-173">**Data**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-174">Informações adicionais.</span><span class="sxs-lookup"><span data-stu-id="cd11d-174">Extra information.</span></span> <span data-ttu-id="cd11d-175">O ponteiro para a estrutura apropriada depende do valor de **threattype**.</span><span class="sxs-lookup"><span data-stu-id="cd11d-175">The pointer to the appropriate structure depends on the value of **ThreatType**.</span></span>

<dl> <dt>

<span data-ttu-id="cd11d-176">**pKnownBad**</span><span class="sxs-lookup"><span data-stu-id="cd11d-176">**pKnownBad**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-177">Tipo: **PMPTHREAT \_ INFOEX \_ não utilizado**</span><span class="sxs-lookup"><span data-stu-id="cd11d-177">Type: **PMPTHREAT\_INFOEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-178">Quando **threattype**  ==  **MPTHREAT, \_ digite \_ KNOWNBAD**.</span><span class="sxs-lookup"><span data-stu-id="cd11d-178">When **ThreatType** == **MPTHREAT\_TYPE\_KNOWNBAD**.</span></span> <span data-ttu-id="cd11d-179">Consulte [**MPTHREAT \_ INFOEX \_ não used**](mpthreat-infoex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="cd11d-179">See [**MPTHREAT\_INFOEX\_UNUSED**](mpthreat-infoex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-180">**pBehavior**</span><span class="sxs-lookup"><span data-stu-id="cd11d-180">**pBehavior**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-181">Tipo: **PMPTHREAT \_ INFOEX \_ Behavior**</span><span class="sxs-lookup"><span data-stu-id="cd11d-181">Type: **PMPTHREAT\_INFOEX\_BEHAVIOR**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-182">Quando **threattype**  ==  **MPTHREAT \_ tipo \_ Behavior**.</span><span class="sxs-lookup"><span data-stu-id="cd11d-182">When **ThreatType** == **MPTHREAT\_TYPE\_BEHAVIOR**.</span></span> <span data-ttu-id="cd11d-183">Consulte [**\_ \_ comportamento do MPTHREAT INFOEX**](mpthreat-infoex-behavior.md).</span><span class="sxs-lookup"><span data-stu-id="cd11d-183">See [**MPTHREAT\_INFOEX\_BEHAVIOR**](mpthreat-infoex-behavior.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-184">**pUnknown**</span><span class="sxs-lookup"><span data-stu-id="cd11d-184">**pUnknown**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-185">Tipo: **PMPTHREAT \_ INFOEX \_ não utilizado**</span><span class="sxs-lookup"><span data-stu-id="cd11d-185">Type: **PMPTHREAT\_INFOEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-186">Quando **threattype**  ==  **MPTHREAT \_ tipo \_ desconhecido**.</span><span class="sxs-lookup"><span data-stu-id="cd11d-186">When **ThreatType** == **MPTHREAT\_TYPE\_UNKNOWN**.</span></span> <span data-ttu-id="cd11d-187">Consulte [**MPTHREAT \_ INFOEX \_ não used**](mpthreat-infoex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="cd11d-187">See [**MPTHREAT\_INFOEX\_UNUSED**](mpthreat-infoex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-188">**pKnownGood**</span><span class="sxs-lookup"><span data-stu-id="cd11d-188">**pKnownGood**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-189">Tipo: **PMPTHREAT \_ INFOEX \_ não utilizado**</span><span class="sxs-lookup"><span data-stu-id="cd11d-189">Type: **PMPTHREAT\_INFOEX\_UNUSED**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-190">Quando **threattype** = = MPTHREAT, \_ digite \_ KNOWNGOOD.</span><span class="sxs-lookup"><span data-stu-id="cd11d-190">When **ThreatType** == MPTHREAT\_TYPE\_KNOWNGOOD.</span></span> <span data-ttu-id="cd11d-191">Consulte [**MPTHREAT \_ INFOEX \_ não used**](mpthreat-infoex-unused.md).</span><span class="sxs-lookup"><span data-stu-id="cd11d-191">See [**MPTHREAT\_INFOEX\_UNUSED**](mpthreat-infoex-unused.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-192">**pNis**</span><span class="sxs-lookup"><span data-stu-id="cd11d-192">**pNis**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-193">Tipo: **PMPTHREAT \_ INFOEX \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="cd11d-193">Type: **PMPTHREAT\_INFOEX\_NIS**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-194">Quando **threattype**  ==  **MPTHREAT \_ tipo \_ NIS**.</span><span class="sxs-lookup"><span data-stu-id="cd11d-194">When **ThreatType** == **MPTHREAT\_TYPE\_NIS**.</span></span> <span data-ttu-id="cd11d-195">Consulte [**MPTHREAT \_ INFOEX \_ NIS**](mpthreat-infoex-nis.md).</span><span class="sxs-lookup"><span data-stu-id="cd11d-195">See [**MPTHREAT\_INFOEX\_NIS**](mpthreat-infoex-nis.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="cd11d-196">**State**</span><span class="sxs-lookup"><span data-stu-id="cd11d-196">**State**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-197">Tipo: **[ **\_ estado MPDETECTION**](mpdetection-state.md)**</span><span class="sxs-lookup"><span data-stu-id="cd11d-197">Type: **[**MPDETECTION\_STATE**](mpdetection-state.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-198">O estado atual da detecção.</span><span class="sxs-lookup"><span data-stu-id="cd11d-198">The current state of the detection.</span></span> <span data-ttu-id="cd11d-199">Consulte [**\_ estado MPDETECTION**](mpdetection-state.md).</span><span class="sxs-lookup"><span data-stu-id="cd11d-199">See [**MPDETECTION\_STATE**](mpdetection-state.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-200">**DetectionUser**</span><span class="sxs-lookup"><span data-stu-id="cd11d-200">**DetectionUser**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-201">Tipo: **PG \_ MIDL \_ String LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="cd11d-201">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-202">O usuário associado à detecção, no formato "domínio/usuário".</span><span class="sxs-lookup"><span data-stu-id="cd11d-202">The user associated with the detection, in the format "domain/user".</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-203">**Detecção de**</span><span class="sxs-lookup"><span data-stu-id="cd11d-203">**DetectionSource**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-204">Tipo: **[ **MPSOURCE**](mpsource.md)**</span><span class="sxs-lookup"><span data-stu-id="cd11d-204">Type: **[**MPSOURCE**](mpsource.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-205">A origem da detecção.</span><span class="sxs-lookup"><span data-stu-id="cd11d-205">The source of the detection.</span></span> <span data-ttu-id="cd11d-206">Consulte [**MPSOURCE**](mpsource.md).</span><span class="sxs-lookup"><span data-stu-id="cd11d-206">See [**MPSOURCE**](mpsource.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-207">**ProcessName**</span><span class="sxs-lookup"><span data-stu-id="cd11d-207">**ProcessName**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-208">Tipo: **PG \_ MIDL \_ String LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="cd11d-208">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-209">Nome do processo associado à detecção.</span><span class="sxs-lookup"><span data-stu-id="cd11d-209">Process name associated with the detection.</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-210">**DetectionOrigin**</span><span class="sxs-lookup"><span data-stu-id="cd11d-210">**DetectionOrigin**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-211">Tipo: **[ **\_ origem do MPDETECTION**](mpdetection-origin.md)**</span><span class="sxs-lookup"><span data-stu-id="cd11d-211">Type: **[**MPDETECTION\_ORIGIN**](mpdetection-origin.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-212">A origem da detecção, como local ou rede.</span><span class="sxs-lookup"><span data-stu-id="cd11d-212">The origin of the detection, such as local or network.</span></span> <span data-ttu-id="cd11d-213">Consulte [**MPDETECTION \_ Origin**](mpdetection-origin.md).</span><span class="sxs-lookup"><span data-stu-id="cd11d-213">See [**MPDETECTION\_ORIGIN**](mpdetection-origin.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-214">**reserved1**</span><span class="sxs-lookup"><span data-stu-id="cd11d-214">**reserved1**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-215">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="cd11d-215">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-216">Metadados reservados sobre a detecção.</span><span class="sxs-lookup"><span data-stu-id="cd11d-216">Reserved metadata about the detection.</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-217">**Detecçãotime**</span><span class="sxs-lookup"><span data-stu-id="cd11d-217">**DetectionTime**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-218">Tipo: **ULARGE \_ inteiro**</span><span class="sxs-lookup"><span data-stu-id="cd11d-218">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-219">A hora da detecção inicial.</span><span class="sxs-lookup"><span data-stu-id="cd11d-219">The time of the initial detection.</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-220">**PreExecutionStatus**</span><span class="sxs-lookup"><span data-stu-id="cd11d-220">**PreExecutionStatus**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-221">Tipo: **[ **MPEXECUTION \_ status**](mpexecution-status.md)**</span><span class="sxs-lookup"><span data-stu-id="cd11d-221">Type: **[**MPEXECUTION\_STATUS**](mpexecution-status.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-222">Status de execução logo antes da correção.</span><span class="sxs-lookup"><span data-stu-id="cd11d-222">Execution status right before remediation.</span></span> <span data-ttu-id="cd11d-223">Consulte [**\_ status do MPEXECUTION**](mpexecution-status.md).</span><span class="sxs-lookup"><span data-stu-id="cd11d-223">See [**MPEXECUTION\_STATUS**](mpexecution-status.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-224">**Remediatime**</span><span class="sxs-lookup"><span data-stu-id="cd11d-224">**RemediationTime**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-225">Tipo: **ULARGE \_ inteiro**</span><span class="sxs-lookup"><span data-stu-id="cd11d-225">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-226">A correção de tempo ocorreu.</span><span class="sxs-lookup"><span data-stu-id="cd11d-226">The time remediation occured.</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-227">**PostExecutionStatus**</span><span class="sxs-lookup"><span data-stu-id="cd11d-227">**PostExecutionStatus**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-228">Tipo: **[ **MPEXECUTION \_ status**](mpexecution-status.md)**</span><span class="sxs-lookup"><span data-stu-id="cd11d-228">Type: **[**MPEXECUTION\_STATUS**](mpexecution-status.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-229">Status da execução após a correção.</span><span class="sxs-lookup"><span data-stu-id="cd11d-229">Execution status after remediation.</span></span> <span data-ttu-id="cd11d-230">Consulte [**\_ status do MPEXECUTION**](mpexecution-status.md).</span><span class="sxs-lookup"><span data-stu-id="cd11d-230">See [**MPEXECUTION\_STATUS**](mpexecution-status.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-231">**CriticalFailure**</span><span class="sxs-lookup"><span data-stu-id="cd11d-231">**CriticalFailure**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-232">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="cd11d-232">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-233">True se a falha de correção for crítica.</span><span class="sxs-lookup"><span data-stu-id="cd11d-233">True if the remediation failure was critical.</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-234">**NonCriticalReason**</span><span class="sxs-lookup"><span data-stu-id="cd11d-234">**NonCriticalReason**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-235">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="cd11d-235">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-236">O motivo pelo qual a falha de correção não é crítica.</span><span class="sxs-lookup"><span data-stu-id="cd11d-236">The reason the remediation failure is not critical.</span></span> <span data-ttu-id="cd11d-237">Não há garantia de que haja suporte para isso no futuro.</span><span class="sxs-lookup"><span data-stu-id="cd11d-237">This is not guaranteed to be supported in the future.</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-238">**RemediationUser**</span><span class="sxs-lookup"><span data-stu-id="cd11d-238">**RemediationUser**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-239">Tipo: **PG \_ MIDL \_ String LPWSTR**</span><span class="sxs-lookup"><span data-stu-id="cd11d-239">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-240">Usuário que solicitou a correção, no formato "domínio/usuário".</span><span class="sxs-lookup"><span data-stu-id="cd11d-240">User that requested the remediation, in the format "domain/user".</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-241">**RemediationResourceCount**</span><span class="sxs-lookup"><span data-stu-id="cd11d-241">**RemediationResourceCount**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-242">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="cd11d-242">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-243">Contagem de recursos no **RemediationResourceList**.</span><span class="sxs-lookup"><span data-stu-id="cd11d-243">Count of resources in **RemediationResourceList**.</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-244">**RemediationResourceList**</span><span class="sxs-lookup"><span data-stu-id="cd11d-244">**RemediationResourceList**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-245">Tipo: **PMPRESOURCE \_ info \[ RemediationResourceCount \]**</span><span class="sxs-lookup"><span data-stu-id="cd11d-245">Type: **PMPRESOURCE\_INFO\[RemediationResourceCount\]**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-246">Lista de recursos que falharam durante a correção.</span><span class="sxs-lookup"><span data-stu-id="cd11d-246">List of resources that failed during remediation.</span></span> <span data-ttu-id="cd11d-247">Consulte [**MPRESOURCE \_ info**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="cd11d-247">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-248">**FailureResolved**</span><span class="sxs-lookup"><span data-stu-id="cd11d-248">**FailureResolved**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-249">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="cd11d-249">Type: **BOOL**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-250">True se a falha de correção tiver sido resolvida.</span><span class="sxs-lookup"><span data-stu-id="cd11d-250">True if remediation failure been resolved.</span></span> <span data-ttu-id="cd11d-251">Isso moverá o Bucket para uma ação completa ou adicional.</span><span class="sxs-lookup"><span data-stu-id="cd11d-251">This will move the bucket to either complete or an additional action.</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-252">**ResolvedReason**</span><span class="sxs-lookup"><span data-stu-id="cd11d-252">**ResolvedReason**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-253">Tipo: **[ **MPRESOLVED \_ motivo**](mpresolved-reason.md)**</span><span class="sxs-lookup"><span data-stu-id="cd11d-253">Type: **[**MPRESOLVED\_REASON**](mpresolved-reason.md)**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-254">Motivo para a falha de correção ser resolvida.</span><span class="sxs-lookup"><span data-stu-id="cd11d-254">Reason for remediation failure being resolved.</span></span> <span data-ttu-id="cd11d-255">Esse é o motivo pelo qual a detecção foi movida de falha para uma ação adicional ou foi concluída.</span><span class="sxs-lookup"><span data-stu-id="cd11d-255">This is the reason the detection moved from failed to additional action or finished.</span></span> <span data-ttu-id="cd11d-256">Consulte [**o \_ motivo do MPRESOLVED**](mpresolved-reason.md).</span><span class="sxs-lookup"><span data-stu-id="cd11d-256">See [**MPRESOLVED\_REASON**](mpresolved-reason.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-257">**AdditionalActions**</span><span class="sxs-lookup"><span data-stu-id="cd11d-257">**AdditionalActions**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-258">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="cd11d-258">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-259">São necessárias ações adicionais.</span><span class="sxs-lookup"><span data-stu-id="cd11d-259">Are additional actions required.</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-260">**ResolvedActions**</span><span class="sxs-lookup"><span data-stu-id="cd11d-260">**ResolvedActions**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-261">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="cd11d-261">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-262">Qualquer ação adicional que tenha sido executada.</span><span class="sxs-lookup"><span data-stu-id="cd11d-262">Any additional actions that have been performed.</span></span>

</dd> <dt>

<span data-ttu-id="cd11d-263">**dwThreatStatusFlag**</span><span class="sxs-lookup"><span data-stu-id="cd11d-263">**dwThreatStatusFlag**</span></span>
</dt> <dd>

<span data-ttu-id="cd11d-264">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="cd11d-264">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="cd11d-265">Informações adicionais sobre a detecção de ameaças.</span><span class="sxs-lookup"><span data-stu-id="cd11d-265">Additonal information about the threat detection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cd11d-266">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd11d-266">Requirements</span></span>



| <span data-ttu-id="cd11d-267">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd11d-267">Requirement</span></span> | <span data-ttu-id="cd11d-268">Valor</span><span class="sxs-lookup"><span data-stu-id="cd11d-268">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cd11d-269">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd11d-269">Minimum supported client</span></span><br/> | <span data-ttu-id="cd11d-270">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="cd11d-270">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="cd11d-271">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cd11d-271">Minimum supported server</span></span><br/> | <span data-ttu-id="cd11d-272">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="cd11d-272">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cd11d-273">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cd11d-273">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd11d-274"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd11d-274"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd11d-275">Confira também</span><span class="sxs-lookup"><span data-stu-id="cd11d-275">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd11d-276">**MpFreeMemory**</span><span class="sxs-lookup"><span data-stu-id="cd11d-276">**MpFreeMemory**</span></span>](mpfreememory.md)
</dt> <dt>

[<span data-ttu-id="cd11d-277">**MpThreatEnumerate**</span><span class="sxs-lookup"><span data-stu-id="cd11d-277">**MpThreatEnumerate**</span></span>](mpthreatenumerate.md)
</dt> <dt>

[<span data-ttu-id="cd11d-278">**MpThreatQuery**</span><span class="sxs-lookup"><span data-stu-id="cd11d-278">**MpThreatQuery**</span></span>](mpthreatquery.md)
</dt> <dt>

[<span data-ttu-id="cd11d-279">**origem do MPDETECTION \_**</span><span class="sxs-lookup"><span data-stu-id="cd11d-279">**MPDETECTION\_ORIGIN**</span></span>](mpdetection-origin.md)
</dt> <dt>

[<span data-ttu-id="cd11d-280">**\_estado MPDETECTION**</span><span class="sxs-lookup"><span data-stu-id="cd11d-280">**MPDETECTION\_STATE**</span></span>](mpdetection-state.md)
</dt> <dt>

[<span data-ttu-id="cd11d-281">**STATUS do MPEXECUTION \_**</span><span class="sxs-lookup"><span data-stu-id="cd11d-281">**MPEXECUTION\_STATUS**</span></span>](mpexecution-status.md)
</dt> <dt>

[<span data-ttu-id="cd11d-282">**motivo do MPRESOLVED \_**</span><span class="sxs-lookup"><span data-stu-id="cd11d-282">**MPRESOLVED\_REASON**</span></span>](mpresolved-reason.md)
</dt> <dt>

[<span data-ttu-id="cd11d-283">**informações de MPRESOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="cd11d-283">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> <dt>

[<span data-ttu-id="cd11d-284">**MPSOURCE**</span><span class="sxs-lookup"><span data-stu-id="cd11d-284">**MPSOURCE**</span></span>](mpsource.md)
</dt> <dt>

[<span data-ttu-id="cd11d-285">**\_ação MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="cd11d-285">**MPTHREAT\_ACTION**</span></span>](mpthreat-action.md)
</dt> <dt>

[<span data-ttu-id="cd11d-286">**\_categoria MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="cd11d-286">**MPTHREAT\_CATEGORY**</span></span>](mpthreat-category.md)
</dt> <dt>

[<span data-ttu-id="cd11d-287">**detecção de MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="cd11d-287">**MPTHREAT\_DETECTION**</span></span>](mpthreat-detection.md)
</dt> <dt>

[<span data-ttu-id="cd11d-288">**\_comportamento MPTHREAT INFOEX \_**</span><span class="sxs-lookup"><span data-stu-id="cd11d-288">**MPTHREAT\_INFOEX\_BEHAVIOR**</span></span>](mpthreat-infoex-behavior.md)
</dt> <dt>

[<span data-ttu-id="cd11d-289">**MPTHREAT \_ INFOEX \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="cd11d-289">**MPTHREAT\_INFOEX\_NIS**</span></span>](mpthreat-infoex-nis.md)
</dt> <dt>

[<span data-ttu-id="cd11d-290">**MPTHREAT \_ INFOEX \_ não usado**</span><span class="sxs-lookup"><span data-stu-id="cd11d-290">**MPTHREAT\_INFOEX\_UNUSED**</span></span>](mpthreat-infoex-unused.md)
</dt> <dt>

[<span data-ttu-id="cd11d-291">**severidade de MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="cd11d-291">**MPTHREAT\_SEVERITY**</span></span>](mpthreat-severity.md)
</dt> <dt>

[<span data-ttu-id="cd11d-292">**STATUS do MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="cd11d-292">**MPTHREAT\_STATUS**</span></span>](mpthreat-status.md)
</dt> <dt>

[<span data-ttu-id="cd11d-293">**tipo de MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="cd11d-293">**MPTHREAT\_TYPE**</span></span>](mpthreat-type.md)
</dt> </dl>

 

 





