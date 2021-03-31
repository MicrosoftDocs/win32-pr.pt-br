---
title: Estrutura de MPSTATUS_INFO (MpClient. h)
description: Informações de status do Malware Protection Manager.
ms.assetid: 614F14EC-64CC-4E3F-8A89-42AA1E0DC95D
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPSTATUS_INFO
- Ponteiro de estrutura de PMPSTATUS_INFO recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPSTATUS_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efe31981f819d85d13457553beb1ce3c869b98bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644307"
---
# <a name="mpstatus_info-structure"></a><span data-ttu-id="8ef5e-105">Estrutura de informações do MPSTATUS \_</span><span class="sxs-lookup"><span data-stu-id="8ef5e-105">MPSTATUS\_INFO structure</span></span>

<span data-ttu-id="8ef5e-106">Informações de status do Malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="8ef5e-106">Status information for the malware protection manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ef5e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8ef5e-107">Syntax</span></span>


```C++
typedef struct tagMPSTATUS_INFO {
  DWORD               ProductStatus;
  MPSCAN_RESULT       LastQuickScan;
  MPSCAN_RESULT       LastFullScan;
  MPTHREAT_STATS      ThreatStats;
  MPTHREAT_STATS_DATA ThreatState[MP_THREAT_STAT_MAX_VALUE+1];
  MPCOMPONENT_STATUS  Component[MPCOMPONENT_MAXVALUE+1];
  ULARGE_INTEGER      ProductExpirationTime;
} MPSTATUS_INFO, *PMPSTATUS_INFO;
```



## <a name="members"></a><span data-ttu-id="8ef5e-108">Membros</span><span class="sxs-lookup"><span data-stu-id="8ef5e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="8ef5e-109">**ProductStatus**</span><span class="sxs-lookup"><span data-stu-id="8ef5e-109">**ProductStatus**</span></span>
</dt> <dd>

<span data-ttu-id="8ef5e-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="8ef5e-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="8ef5e-111">Status geral do produto.</span><span class="sxs-lookup"><span data-stu-id="8ef5e-111">Overall product status.</span></span> <span data-ttu-id="8ef5e-112">Essa é uma combinação de sinalizadores de bit [**do \_ sinalizador MPSTATUS**](mpstatus-flag.md).</span><span class="sxs-lookup"><span data-stu-id="8ef5e-112">This is a combination of bit flags from [**MPSTATUS\_FLAG**](mpstatus-flag.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ef5e-113">**LastQuickScan**</span><span class="sxs-lookup"><span data-stu-id="8ef5e-113">**LastQuickScan**</span></span>
</dt> <dd>

<span data-ttu-id="8ef5e-114">Tipo: **[ **\_ resultado de MPSCAN**](mpscan-result.md)**</span><span class="sxs-lookup"><span data-stu-id="8ef5e-114">Type: **[**MPSCAN\_RESULT**](mpscan-result.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8ef5e-115">Resultados da última verificação pelo Gerenciador de proteção contra malware.</span><span class="sxs-lookup"><span data-stu-id="8ef5e-115">Results of the last scan by the malware protection manager.</span></span> <span data-ttu-id="8ef5e-116">Consulte [**\_ resultado do MPSCAN**](mpscan-result.md).</span><span class="sxs-lookup"><span data-stu-id="8ef5e-116">See [**MPSCAN\_RESULT**](mpscan-result.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ef5e-117">**LastFullScan**</span><span class="sxs-lookup"><span data-stu-id="8ef5e-117">**LastFullScan**</span></span>
</dt> <dd>

<span data-ttu-id="8ef5e-118">Tipo: **[ **\_ resultado de MPSCAN**](mpscan-result.md)**</span><span class="sxs-lookup"><span data-stu-id="8ef5e-118">Type: **[**MPSCAN\_RESULT**](mpscan-result.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8ef5e-119">Resultados da última verificação completa pelo Malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="8ef5e-119">Results of the last full scan by the malware protection manager.</span></span> <span data-ttu-id="8ef5e-120">Consulte [**\_ resultado do MPSCAN**](mpscan-result.md).</span><span class="sxs-lookup"><span data-stu-id="8ef5e-120">See [**MPSCAN\_RESULT**](mpscan-result.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ef5e-121">**ThreatStats**</span><span class="sxs-lookup"><span data-stu-id="8ef5e-121">**ThreatStats**</span></span>
</dt> <dd>

<span data-ttu-id="8ef5e-122">Tipo: **[ **\_ Estatísticas de MPTHREAT**](mpthreat-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="8ef5e-122">Type: **[**MPTHREAT\_STATS**](mpthreat-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="8ef5e-123">Estatísticas de ameaça ativas.</span><span class="sxs-lookup"><span data-stu-id="8ef5e-123">Active threat statistics.</span></span> <span data-ttu-id="8ef5e-124">Consulte [**\_ Estatísticas de MPTHREAT**](mpthreat-stats.md).</span><span class="sxs-lookup"><span data-stu-id="8ef5e-124">See [**MPTHREAT\_STATS**](mpthreat-stats.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ef5e-125">**Threatstate**</span><span class="sxs-lookup"><span data-stu-id="8ef5e-125">**ThreatState**</span></span>
</dt> <dd>

<span data-ttu-id="8ef5e-126">Tipo: **[**MPTHREAT \_ estatísticas \_ dados**](mpthreat-stats-data.md) \[ MP \_ ameaça \_ \_ máximo \_ valor + 1\]**</span><span class="sxs-lookup"><span data-stu-id="8ef5e-126">Type: **[**MPTHREAT\_STATS\_DATA**](mpthreat-stats-data.md)\[MP\_THREAT\_STAT\_MAX\_VALUE+1\]**</span></span>

</dd> <dd>

<span data-ttu-id="8ef5e-127">Dados de estatísticas de ameaças adicionais, como o número de ameaças.</span><span class="sxs-lookup"><span data-stu-id="8ef5e-127">Additional threat statistics data, such as the number of threats.</span></span> <span data-ttu-id="8ef5e-128">Consulte [**\_ \_ dados de estatísticas do MPTHREAT**](mpthreat-stats-data.md).</span><span class="sxs-lookup"><span data-stu-id="8ef5e-128">See [**MPTHREAT\_STATS\_DATA**](mpthreat-stats-data.md).</span></span>

</dd> <dt>

<span data-ttu-id="8ef5e-129">**Componente**</span><span class="sxs-lookup"><span data-stu-id="8ef5e-129">**Component**</span></span>
</dt> <dd>

<span data-ttu-id="8ef5e-130">Tipo: **[**MPCOMPONENT \_ status**](mpcomponent-status.md) \[ MPCOMPONENT \_ MaxValue + 1\]**</span><span class="sxs-lookup"><span data-stu-id="8ef5e-130">Type: **[**MPCOMPONENT\_STATUS**](mpcomponent-status.md)\[MPCOMPONENT\_MAXVALUE+1\]**</span></span>

</dd> <dd>

<span data-ttu-id="8ef5e-131">Uma matriz de status para vários componentes.</span><span class="sxs-lookup"><span data-stu-id="8ef5e-131">An array of statuses for multiple components.</span></span> <span data-ttu-id="8ef5e-132">Use um valor da enumeração [**de \_ ID MPCOMPONENT**](mpcomponent-id.md) como um índice na matriz.</span><span class="sxs-lookup"><span data-stu-id="8ef5e-132">Use a value from the [**MPCOMPONENT\_ID**](mpcomponent-id.md) enumeration as an index into the array.</span></span>

</dd> <dt>

<span data-ttu-id="8ef5e-133">**ProductExpirationTime**</span><span class="sxs-lookup"><span data-stu-id="8ef5e-133">**ProductExpirationTime**</span></span>
</dt> <dd>

<span data-ttu-id="8ef5e-134">Tipo: **ULARGE \_ inteiro**</span><span class="sxs-lookup"><span data-stu-id="8ef5e-134">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="8ef5e-135">Carimbo de data/hora de validade do produto em UNC.</span><span class="sxs-lookup"><span data-stu-id="8ef5e-135">Product expiration timestamp in UNC.</span></span> <span data-ttu-id="8ef5e-136">Isso será válido somente se o status de expiração for definido.</span><span class="sxs-lookup"><span data-stu-id="8ef5e-136">This is valid only if the expiration status is set.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8ef5e-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ef5e-137">Requirements</span></span>



| <span data-ttu-id="8ef5e-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ef5e-138">Requirement</span></span> | <span data-ttu-id="8ef5e-139">Valor</span><span class="sxs-lookup"><span data-stu-id="8ef5e-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8ef5e-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ef5e-140">Minimum supported client</span></span><br/> | <span data-ttu-id="8ef5e-141">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="8ef5e-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="8ef5e-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8ef5e-142">Minimum supported server</span></span><br/> | <span data-ttu-id="8ef5e-143">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="8ef5e-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8ef5e-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8ef5e-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ef5e-145"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="8ef5e-145"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ef5e-146">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8ef5e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ef5e-147">**ID do MPCOMPONENT \_**</span><span class="sxs-lookup"><span data-stu-id="8ef5e-147">**MPCOMPONENT\_ID**</span></span>](mpcomponent-id.md)
</dt> <dt>

[<span data-ttu-id="8ef5e-148">**STATUS do MPCOMPONENT \_**</span><span class="sxs-lookup"><span data-stu-id="8ef5e-148">**MPCOMPONENT\_STATUS**</span></span>](mpcomponent-status.md)
</dt> <dt>

[<span data-ttu-id="8ef5e-149">**resultado do MPSCAN \_**</span><span class="sxs-lookup"><span data-stu-id="8ef5e-149">**MPSCAN\_RESULT**</span></span>](mpscan-result.md)
</dt> <dt>

[<span data-ttu-id="8ef5e-150">**\_sinalizador MPSTATUS**</span><span class="sxs-lookup"><span data-stu-id="8ef5e-150">**MPSTATUS\_FLAG**</span></span>](mpstatus-flag.md)
</dt> <dt>

[<span data-ttu-id="8ef5e-151">**Estatísticas de MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="8ef5e-151">**MPTHREAT\_STATS**</span></span>](mpthreat-stats.md)
</dt> <dt>

[<span data-ttu-id="8ef5e-152">**\_dados de estatísticas do MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="8ef5e-152">**MPTHREAT\_STATS\_DATA**</span></span>](mpthreat-stats-data.md)
</dt> </dl>

 

 





