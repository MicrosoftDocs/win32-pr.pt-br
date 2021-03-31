---
title: Estrutura de MPCALLBACK_DATA (MpClient. h)
description: Dados passados para a função de retorno de chamada.
ms.assetid: EA8E6C1E-F80B-4247-B073-C78D49A354CF
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPCALLBACK_DATA
- Ponteiro de estrutura de PMPCALLBACK_DATA recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPCALLBACK_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9741ca479eeb9770a3ae8c2aedbc51a8a2643033
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085507"
---
# <a name="mpcallback_data-structure"></a><span data-ttu-id="95a01-105">\_Estrutura de dados MPCALLBACK</span><span class="sxs-lookup"><span data-stu-id="95a01-105">MPCALLBACK\_DATA structure</span></span>

<span data-ttu-id="95a01-106">Dados passados para a função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="95a01-106">Data passed to the callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="95a01-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="95a01-107">Syntax</span></span>


```C++
typedef struct tagMPCALLBACK_DATA {
  MPNOTIFY        Notify;
  HRESULT         hResult;
  ULARGE_INTEGER  TimeStamp;
  MPCALLBACK_TYPE Type;
  union {
    PMPSTATUS_DATA         pStatusData;
    PMPSCAN_DATA           pScanData;
    PMPCLEAN_DATA          pCleanData;
    PMPCLEAN_PRECHECK_DATA pPrecheckData;
    PMPTHREAT_DATA         pThreatData;
    PMPSIGUPDATE_DATA      pSigUpdateData;
    PMPSAMPLE_DATA         pSampleData;
    PMPRESERVED_DATA       pReservedData;
    PMPCONFIGURATION_DATA  pConfigurationData;
    PMPFASTPATH_DATA       pFastPathData;
    PMPEXPIRATION_DATA     pExpirationData;
    PMPNIS_PRIVATE_DATA    pNISPrivateData;
    PMPHEALTH_DATA         pHealthData;
    PMPENDOFLIFE_DATA      pEndOfLifeData;
    PMPMALWARETOAST_DATA   pMalwareToastData;
  } Data;
} MPCALLBACK_DATA, *PMPCALLBACK_DATA;
```



## <a name="members"></a><span data-ttu-id="95a01-108">Membros</span><span class="sxs-lookup"><span data-stu-id="95a01-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="95a01-109">**Notificar**</span><span class="sxs-lookup"><span data-stu-id="95a01-109">**Notify**</span></span>
</dt> <dd>

<span data-ttu-id="95a01-110">Tipo: **[ **mpnotify**](mpnotify.md)**</span><span class="sxs-lookup"><span data-stu-id="95a01-110">Type: **[**MPNOTIFY**](mpnotify.md)**</span></span>

</dd> <dd>

<span data-ttu-id="95a01-111">Notificação de alteração para o relatório.</span><span class="sxs-lookup"><span data-stu-id="95a01-111">Change notification to report.</span></span>

</dd> <dt>

<span data-ttu-id="95a01-112">**Resultado**</span><span class="sxs-lookup"><span data-stu-id="95a01-112">**hResult**</span></span>
</dt> <dd>

<span data-ttu-id="95a01-113">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="95a01-113">Type: **HRESULT**</span></span>

</dd> <dd>

<span data-ttu-id="95a01-114">Código de erro, no caso de uma falha interna.</span><span class="sxs-lookup"><span data-stu-id="95a01-114">Error code, in case of an internal failure.</span></span>

</dd> <dt>

<span data-ttu-id="95a01-115">**Estampa**</span><span class="sxs-lookup"><span data-stu-id="95a01-115">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="95a01-116">Tipo: **ULARGE \_ inteiro**</span><span class="sxs-lookup"><span data-stu-id="95a01-116">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="95a01-117">Carimbo de data/hora atual.</span><span class="sxs-lookup"><span data-stu-id="95a01-117">Current timestamp.</span></span>

</dd> <dt>

<span data-ttu-id="95a01-118">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="95a01-118">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="95a01-119">Tipo: **[ **\_ tipo de MPCALLBACK**](mpcallback-type.md)**</span><span class="sxs-lookup"><span data-stu-id="95a01-119">Type: **[**MPCALLBACK\_TYPE**](mpcallback-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="95a01-120">Tipo de dados especial de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="95a01-120">Callback special data type.</span></span>

</dd> <dt>

<span data-ttu-id="95a01-121">**Dados**</span><span class="sxs-lookup"><span data-stu-id="95a01-121">**Data**</span></span>
</dt> <dd>

<span data-ttu-id="95a01-122">Dados especiais de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="95a01-122">Callback special data.</span></span> <span data-ttu-id="95a01-123">O ponteiro para a estrutura apropriada depende do valor do **tipo**.</span><span class="sxs-lookup"><span data-stu-id="95a01-123">The pointer to the appropriate structure depends on the value of **Type**.</span></span>

<dl> <dt>

<span data-ttu-id="95a01-124">**pStatusData**</span><span class="sxs-lookup"><span data-stu-id="95a01-124">**pStatusData**</span></span>
</dt> <dd>

<span data-ttu-id="95a01-125">Tipo: **\_ dados de PMPSTATUS**</span><span class="sxs-lookup"><span data-stu-id="95a01-125">Type: **PMPSTATUS\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="95a01-126">Ao **digitar** o  ==  **\_ status de MPCALLBACK**.</span><span class="sxs-lookup"><span data-stu-id="95a01-126">When **Type** == **MPCALLBACK\_STATUS**.</span></span> <span data-ttu-id="95a01-127">Consulte [**\_ dados do MPSTATUS**](mpstatus-data.md).</span><span class="sxs-lookup"><span data-stu-id="95a01-127">See [**MPSTATUS\_DATA**](mpstatus-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="95a01-128">**pScanData**</span><span class="sxs-lookup"><span data-stu-id="95a01-128">**pScanData**</span></span>
</dt> <dd>

<span data-ttu-id="95a01-129">Tipo: **\_ dados de PMPSCAN**</span><span class="sxs-lookup"><span data-stu-id="95a01-129">Type: **PMPSCAN\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="95a01-130">Quando o **tipo**  ==  **MPCALLBACK \_ Scan**.</span><span class="sxs-lookup"><span data-stu-id="95a01-130">When **Type** == **MPCALLBACK\_SCAN**.</span></span> <span data-ttu-id="95a01-131">Consulte [**\_ dados do MPSCAN**](mpscan-data.md).</span><span class="sxs-lookup"><span data-stu-id="95a01-131">See [**MPSCAN\_DATA**](mpscan-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="95a01-132">**pCleanData**</span><span class="sxs-lookup"><span data-stu-id="95a01-132">**pCleanData**</span></span>
</dt> <dd>

<span data-ttu-id="95a01-133">Tipo: **\_ dados de PMPCLEAN**</span><span class="sxs-lookup"><span data-stu-id="95a01-133">Type: **PMPCLEAN\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="95a01-134">Quando **digite**  ==  **MPCALLBACK \_ Clean**.</span><span class="sxs-lookup"><span data-stu-id="95a01-134">When **Type** == **MPCALLBACK\_CLEAN**.</span></span> <span data-ttu-id="95a01-135">Consulte [**\_ dados do MPCLEAN**](mpclean-data.md).</span><span class="sxs-lookup"><span data-stu-id="95a01-135">See [**MPCLEAN\_DATA**](mpclean-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="95a01-136">**pPrecheckData**</span><span class="sxs-lookup"><span data-stu-id="95a01-136">**pPrecheckData**</span></span>
</dt> <dd>

<span data-ttu-id="95a01-137">Tipo: **PMPCLEAN \_ \_ dados de verificação**</span><span class="sxs-lookup"><span data-stu-id="95a01-137">Type: **PMPCLEAN\_PRECHECK\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="95a01-138">Quando MPCALLBACK, **digite**  ==  **\_ precheck**.</span><span class="sxs-lookup"><span data-stu-id="95a01-138">When **Type** == **MPCALLBACK\_PRECHECK**.</span></span> <span data-ttu-id="95a01-139">Consulte [**MPCLEAN \_ precheck \_ Data**](mpclean-precheck-data.md).</span><span class="sxs-lookup"><span data-stu-id="95a01-139">See [**MPCLEAN\_PRECHECK\_DATA**](mpclean-precheck-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="95a01-140">**pThreatData**</span><span class="sxs-lookup"><span data-stu-id="95a01-140">**pThreatData**</span></span>
</dt> <dd>

<span data-ttu-id="95a01-141">Tipo: **\_ dados de PMPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="95a01-141">Type: **PMPTHREAT\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="95a01-142">Quando **digitar**  ==  **\_ ameaça MPCALLBACK**.</span><span class="sxs-lookup"><span data-stu-id="95a01-142">When **Type** == **MPCALLBACK\_THREAT**.</span></span> <span data-ttu-id="95a01-143">Consulte [**\_ dados do MPTHREAT**](mpthreat-data.md).</span><span class="sxs-lookup"><span data-stu-id="95a01-143">See [**MPTHREAT\_DATA**](mpthreat-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="95a01-144">**pSigUpdateData**</span><span class="sxs-lookup"><span data-stu-id="95a01-144">**pSigUpdateData**</span></span>
</dt> <dd>

<span data-ttu-id="95a01-145">Tipo: **\_ dados de PMPSIGUPDATE**</span><span class="sxs-lookup"><span data-stu-id="95a01-145">Type: **PMPSIGUPDATE\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="95a01-146">Quando **digite**  ==  **MPCALLBACK \_ SIGUPDATE**.</span><span class="sxs-lookup"><span data-stu-id="95a01-146">When **Type** == **MPCALLBACK\_SIGUPDATE**.</span></span> <span data-ttu-id="95a01-147">Consulte [**\_ dados do MPSIGUPDATE**](mpsigupdate-data.md).</span><span class="sxs-lookup"><span data-stu-id="95a01-147">See [**MPSIGUPDATE\_DATA**](mpsigupdate-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="95a01-148">**pSampleData**</span><span class="sxs-lookup"><span data-stu-id="95a01-148">**pSampleData**</span></span>
</dt> <dd>

<span data-ttu-id="95a01-149">Tipo: **\_ dados de PMPSAMPLE**</span><span class="sxs-lookup"><span data-stu-id="95a01-149">Type: **PMPSAMPLE\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="95a01-150">Ao **digitar** o  ==  **\_ exemplo MPCALLBACK**.</span><span class="sxs-lookup"><span data-stu-id="95a01-150">When **Type** == **MPCALLBACK\_SAMPLE**.</span></span> <span data-ttu-id="95a01-151">Consulte [**\_ dados do MPSAMPLE**](mpsample-data.md).</span><span class="sxs-lookup"><span data-stu-id="95a01-151">See [**MPSAMPLE\_DATA**](mpsample-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="95a01-152">**pReservedData**</span><span class="sxs-lookup"><span data-stu-id="95a01-152">**pReservedData**</span></span>
</dt> <dd>

<span data-ttu-id="95a01-153">Tipo: **\_ dados de PMPRESERVED**</span><span class="sxs-lookup"><span data-stu-id="95a01-153">Type: **PMPRESERVED\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="95a01-154">Quando o **tipo**  ==  **MPCALLBACK \_ reservado**.</span><span class="sxs-lookup"><span data-stu-id="95a01-154">When **Type** == **MPCALLBACK\_RESERVED**.</span></span> <span data-ttu-id="95a01-155">Consulte [**\_ dados do MPRESERVED**](mpreserved-data.md).</span><span class="sxs-lookup"><span data-stu-id="95a01-155">See [**MPRESERVED\_DATA**](mpreserved-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="95a01-156">**pConfigurationData**</span><span class="sxs-lookup"><span data-stu-id="95a01-156">**pConfigurationData**</span></span>
</dt> <dd>

<span data-ttu-id="95a01-157">Tipo: **\_ dados de PMPCONFIGURATION**</span><span class="sxs-lookup"><span data-stu-id="95a01-157">Type: **PMPCONFIGURATION\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="95a01-158">Quando **tipo** de  ==  **\_ \_ notificação de configuração MPCALLBACK**.</span><span class="sxs-lookup"><span data-stu-id="95a01-158">When **Type** == **MPCALLBACK\_CONFIGURATION\_NOTIFICATION**.</span></span> <span data-ttu-id="95a01-159">Consulte [**\_ dados do MPCONFIGURATION**](mpconfiguration-data.md).</span><span class="sxs-lookup"><span data-stu-id="95a01-159">See [**MPCONFIGURATION\_DATA**](mpconfiguration-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="95a01-160">**pFastPathData**</span><span class="sxs-lookup"><span data-stu-id="95a01-160">**pFastPathData**</span></span>
</dt> <dd>

<span data-ttu-id="95a01-161">Tipo: **\_ dados de PMPFASTPATH**</span><span class="sxs-lookup"><span data-stu-id="95a01-161">Type: **PMPFASTPATH\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="95a01-162">Quando **digite**  ==  **MPCALLBACK \_ FASTPATH**.</span><span class="sxs-lookup"><span data-stu-id="95a01-162">When **Type** == **MPCALLBACK\_FASTPATH**.</span></span> <span data-ttu-id="95a01-163">Consulte [**\_ dados do MPFASTPATH**](mpfastpath-data.md).</span><span class="sxs-lookup"><span data-stu-id="95a01-163">See [**MPFASTPATH\_DATA**](mpfastpath-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="95a01-164">**pExpirationData**</span><span class="sxs-lookup"><span data-stu-id="95a01-164">**pExpirationData**</span></span>
</dt> <dd>

<span data-ttu-id="95a01-165">Tipo: **\_ dados de PMPEXPIRATION**</span><span class="sxs-lookup"><span data-stu-id="95a01-165">Type: **PMPEXPIRATION\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="95a01-166">Quando **tipo**  ==  **MPCALLBACK \_ \_ expiração do produto**.</span><span class="sxs-lookup"><span data-stu-id="95a01-166">When **Type** == **MPCALLBACK\_PRODUCT\_EXPIRATION**.</span></span> <span data-ttu-id="95a01-167">Consulte [**\_ dados do MPEXPIRATION**](mpexpiration-data.md).</span><span class="sxs-lookup"><span data-stu-id="95a01-167">See [**MPEXPIRATION\_DATA**](mpexpiration-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="95a01-168">**pNISPrivateData**</span><span class="sxs-lookup"><span data-stu-id="95a01-168">**pNISPrivateData**</span></span>
</dt> <dd>

<span data-ttu-id="95a01-169">Tipo: **PMPNIS \_ Private \_ Data**</span><span class="sxs-lookup"><span data-stu-id="95a01-169">Type: **PMPNIS\_PRIVATE\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="95a01-170">Quando o **tipo**  ==  **MPCALLBACK \_ NIS \_ privado**.</span><span class="sxs-lookup"><span data-stu-id="95a01-170">When **Type** == **MPCALLBACK\_NIS\_PRIVATE**.</span></span> <span data-ttu-id="95a01-171">Consulte [**MPNIS \_ Private \_ Data**](mpnis-private-data.md).</span><span class="sxs-lookup"><span data-stu-id="95a01-171">See [**MPNIS\_PRIVATE\_DATA**](mpnis-private-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="95a01-172">**pHealthData**</span><span class="sxs-lookup"><span data-stu-id="95a01-172">**pHealthData**</span></span>
</dt> <dd>

<span data-ttu-id="95a01-173">Tipo: **\_ dados de PMPHEALTH**</span><span class="sxs-lookup"><span data-stu-id="95a01-173">Type: **PMPHEALTH\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="95a01-174">Ao **digitar**  ==  **MPCALLBACK \_ Health**.</span><span class="sxs-lookup"><span data-stu-id="95a01-174">When **Type** == **MPCALLBACK\_HEALTH**.</span></span> <span data-ttu-id="95a01-175">Consulte [**\_ dados do MPHEALTH**](mphealth-data.md).</span><span class="sxs-lookup"><span data-stu-id="95a01-175">See [**MPHEALTH\_DATA**](mphealth-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="95a01-176">**pEndOfLifeData**</span><span class="sxs-lookup"><span data-stu-id="95a01-176">**pEndOfLifeData**</span></span>
</dt> <dd>

<span data-ttu-id="95a01-177">Tipo: **\_ dados de PMPENDOFLIFE**</span><span class="sxs-lookup"><span data-stu-id="95a01-177">Type: **PMPENDOFLIFE\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="95a01-178">Quando **digite**  ==  **MPCALLBACK \_ ENDOFLIFE**.</span><span class="sxs-lookup"><span data-stu-id="95a01-178">When **Type** == **MPCALLBACK\_ENDOFLIFE**.</span></span> <span data-ttu-id="95a01-179">Consulte [**\_ dados do MPENDOFLIFE**](mpendoflife-data.md).</span><span class="sxs-lookup"><span data-stu-id="95a01-179">See [**MPENDOFLIFE\_DATA**](mpendoflife-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="95a01-180">**pMalwareToastData**</span><span class="sxs-lookup"><span data-stu-id="95a01-180">**pMalwareToastData**</span></span>
</dt> <dd>

<span data-ttu-id="95a01-181">Tipo: **\_ dados de PMPMALWARETOAST**</span><span class="sxs-lookup"><span data-stu-id="95a01-181">Type: **PMPMALWARETOAST\_DATA**</span></span>

</dd> <dd>

<span data-ttu-id="95a01-182">Quando **digite**  ==  **MPCALLBACK \_ MALWARETOAST**.</span><span class="sxs-lookup"><span data-stu-id="95a01-182">When **Type** == **MPCALLBACK\_MALWARETOAST**.</span></span> <span data-ttu-id="95a01-183">Consulte [**\_ dados do MPMALWARETOAST**](mpmalwaretoast-data.md).</span><span class="sxs-lookup"><span data-stu-id="95a01-183">See [**MPMALWARETOAST\_DATA**](mpmalwaretoast-data.md).</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="95a01-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95a01-184">Requirements</span></span>



| <span data-ttu-id="95a01-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="95a01-185">Requirement</span></span> | <span data-ttu-id="95a01-186">Valor</span><span class="sxs-lookup"><span data-stu-id="95a01-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="95a01-187">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95a01-187">Minimum supported client</span></span><br/> | <span data-ttu-id="95a01-188">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="95a01-188">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="95a01-189">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="95a01-189">Minimum supported server</span></span><br/> | <span data-ttu-id="95a01-190">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="95a01-190">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="95a01-191">parâmetro</span><span class="sxs-lookup"><span data-stu-id="95a01-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="95a01-192"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="95a01-192"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95a01-193">Consulte também</span><span class="sxs-lookup"><span data-stu-id="95a01-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95a01-194">**tipo de MPCALLBACK \_**</span><span class="sxs-lookup"><span data-stu-id="95a01-194">**MPCALLBACK\_TYPE**</span></span>](mpcallback-type.md)
</dt> <dt>

[<span data-ttu-id="95a01-195">**dados do MPCLEAN \_**</span><span class="sxs-lookup"><span data-stu-id="95a01-195">**MPCLEAN\_DATA**</span></span>](mpclean-data.md)
</dt> <dt>

[<span data-ttu-id="95a01-196">**MPCLEAN \_ dados de verificação \_**</span><span class="sxs-lookup"><span data-stu-id="95a01-196">**MPCLEAN\_PRECHECK\_DATA**</span></span>](mpclean-precheck-data.md)
</dt> <dt>

[<span data-ttu-id="95a01-197">**dados do MPCONFIGURATION \_**</span><span class="sxs-lookup"><span data-stu-id="95a01-197">**MPCONFIGURATION\_DATA**</span></span>](mpconfiguration-data.md)
</dt> <dt>

[<span data-ttu-id="95a01-198">**dados do MPENDOFLIFE \_**</span><span class="sxs-lookup"><span data-stu-id="95a01-198">**MPENDOFLIFE\_DATA**</span></span>](mpendoflife-data.md)
</dt> <dt>

[<span data-ttu-id="95a01-199">**dados do MPEXPIRATION \_**</span><span class="sxs-lookup"><span data-stu-id="95a01-199">**MPEXPIRATION\_DATA**</span></span>](mpexpiration-data.md)
</dt> <dt>

[<span data-ttu-id="95a01-200">**dados do MPFASTPATH \_**</span><span class="sxs-lookup"><span data-stu-id="95a01-200">**MPFASTPATH\_DATA**</span></span>](mpfastpath-data.md)
</dt> <dt>

[<span data-ttu-id="95a01-201">**dados do MPHEALTH \_**</span><span class="sxs-lookup"><span data-stu-id="95a01-201">**MPHEALTH\_DATA**</span></span>](mphealth-data.md)
</dt> <dt>

[<span data-ttu-id="95a01-202">**dados do MPMALWARETOAST \_**</span><span class="sxs-lookup"><span data-stu-id="95a01-202">**MPMALWARETOAST\_DATA**</span></span>](mpmalwaretoast-data.md)
</dt> <dt>

[<span data-ttu-id="95a01-203">**MPNIS \_ \_ dados privados**</span><span class="sxs-lookup"><span data-stu-id="95a01-203">**MPNIS\_PRIVATE\_DATA**</span></span>](mpnis-private-data.md)
</dt> <dt>

[<span data-ttu-id="95a01-204">**MPNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="95a01-204">**MPNOTIFY**</span></span>](mpnotify.md)
</dt> <dt>

[<span data-ttu-id="95a01-205">**dados do MPRESERVED \_**</span><span class="sxs-lookup"><span data-stu-id="95a01-205">**MPRESERVED\_DATA**</span></span>](mpreserved-data.md)
</dt> <dt>

[<span data-ttu-id="95a01-206">**dados do MPSAMPLE \_**</span><span class="sxs-lookup"><span data-stu-id="95a01-206">**MPSAMPLE\_DATA**</span></span>](mpsample-data.md)
</dt> <dt>

[<span data-ttu-id="95a01-207">**dados do MPSCAN \_**</span><span class="sxs-lookup"><span data-stu-id="95a01-207">**MPSCAN\_DATA**</span></span>](mpscan-data.md)
</dt> <dt>

[<span data-ttu-id="95a01-208">**dados do MPSIGUPDATE \_**</span><span class="sxs-lookup"><span data-stu-id="95a01-208">**MPSIGUPDATE\_DATA**</span></span>](mpsigupdate-data.md)
</dt> <dt>

[<span data-ttu-id="95a01-209">**dados do MPSTATUS \_**</span><span class="sxs-lookup"><span data-stu-id="95a01-209">**MPSTATUS\_DATA**</span></span>](mpstatus-data.md)
</dt> <dt>

[<span data-ttu-id="95a01-210">**dados do MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="95a01-210">**MPTHREAT\_DATA**</span></span>](mpthreat-data.md)
</dt> </dl>

 

 





