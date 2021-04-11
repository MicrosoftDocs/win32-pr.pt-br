---
title: Estrutura de MPSCAN_RESULT (MpClient. h)
description: Os resultados de uma verificação.
ms.assetid: 9031A371-092A-4175-BE1D-90442A5BED2D
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPSCAN_RESULT
- Ponteiro de estrutura de PMPSCAN_RESULT recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPSCAN_RESULT
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7be60df7993732bafcd7c44ac2fb581c111aed6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104163623"
---
# <a name="mpscan_result-structure"></a><span data-ttu-id="04de0-105">\_Estrutura de resultados MPSCAN</span><span class="sxs-lookup"><span data-stu-id="04de0-105">MPSCAN\_RESULT structure</span></span>

<span data-ttu-id="04de0-106">Os resultados de uma verificação.</span><span class="sxs-lookup"><span data-stu-id="04de0-106">The results of a scan.</span></span>

## <a name="syntax"></a><span data-ttu-id="04de0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="04de0-107">Syntax</span></span>


```C++
typedef struct tagMPSCAN_RESULT {
  MPSCAN_TYPE      ScanType;
  MPSOURCE         Source;
  GUID             ScanGuid;
  ULARGE_INTEGER   StartTime;
  ULARGE_INTEGER   EndTime;
  MPTHREAT_STATS   ThreatStats;
  MPRESOURCE_STATS ResourceStats;
  ULONGLONG        SignatureVersion;
} MPSCAN_RESULT, *PMPSCAN_RESULT;
```



## <a name="members"></a><span data-ttu-id="04de0-108">Membros</span><span class="sxs-lookup"><span data-stu-id="04de0-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="04de0-109">**ScanType**</span><span class="sxs-lookup"><span data-stu-id="04de0-109">**ScanType**</span></span>
</dt> <dd>

<span data-ttu-id="04de0-110">Tipo: **[ **\_ tipo de MPSCAN**](mpscan-type.md)**</span><span class="sxs-lookup"><span data-stu-id="04de0-110">Type: **[**MPSCAN\_TYPE**](mpscan-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="04de0-111">Tipo de verificação.</span><span class="sxs-lookup"><span data-stu-id="04de0-111">Scan type.</span></span> <span data-ttu-id="04de0-112">Consulte [**\_ tipo de MPSCAN**](mpscan-type.md).</span><span class="sxs-lookup"><span data-stu-id="04de0-112">See [**MPSCAN\_TYPE**](mpscan-type.md).</span></span>

</dd> <dt>

<span data-ttu-id="04de0-113">**Origem**</span><span class="sxs-lookup"><span data-stu-id="04de0-113">**Source**</span></span>
</dt> <dd>

<span data-ttu-id="04de0-114">Tipo: **[ **MPSOURCE**](mpsource.md)**</span><span class="sxs-lookup"><span data-stu-id="04de0-114">Type: **[**MPSOURCE**](mpsource.md)**</span></span>

</dd> <dd>

<span data-ttu-id="04de0-115">Verifique a origem, como o usuário ou o sistema iniciado.</span><span class="sxs-lookup"><span data-stu-id="04de0-115">Scan source, such as user or system initiated.</span></span> <span data-ttu-id="04de0-116">Consulte [**MPSOURCE**](mpsource.md).</span><span class="sxs-lookup"><span data-stu-id="04de0-116">See [**MPSOURCE**](mpsource.md).</span></span>

</dd> <dt>

<span data-ttu-id="04de0-117">**ScanGuid**</span><span class="sxs-lookup"><span data-stu-id="04de0-117">**ScanGuid**</span></span>
</dt> <dd>

<span data-ttu-id="04de0-118">Tipo: **GUID**</span><span class="sxs-lookup"><span data-stu-id="04de0-118">Type: **GUID**</span></span>

</dd> <dd>

<span data-ttu-id="04de0-119">Identificador de verificação.</span><span class="sxs-lookup"><span data-stu-id="04de0-119">Scan identifier.</span></span>

</dd> <dt>

<span data-ttu-id="04de0-120">**StartTime**</span><span class="sxs-lookup"><span data-stu-id="04de0-120">**StartTime**</span></span>
</dt> <dd>

<span data-ttu-id="04de0-121">Tipo: **ULARGE \_ inteiro**</span><span class="sxs-lookup"><span data-stu-id="04de0-121">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="04de0-122">Hora de início da verificação.</span><span class="sxs-lookup"><span data-stu-id="04de0-122">Scan start time.</span></span>

</dd> <dt>

<span data-ttu-id="04de0-123">**EndTime**</span><span class="sxs-lookup"><span data-stu-id="04de0-123">**EndTime**</span></span>
</dt> <dd>

<span data-ttu-id="04de0-124">Tipo: **ULARGE \_ inteiro**</span><span class="sxs-lookup"><span data-stu-id="04de0-124">Type: **ULARGE\_INTEGER**</span></span>

</dd> <dd>

<span data-ttu-id="04de0-125">Hora de término da verificação.</span><span class="sxs-lookup"><span data-stu-id="04de0-125">Scan end time.</span></span>

</dd> <dt>

<span data-ttu-id="04de0-126">**ThreatStats**</span><span class="sxs-lookup"><span data-stu-id="04de0-126">**ThreatStats**</span></span>
</dt> <dd>

<span data-ttu-id="04de0-127">Tipo: **[ **\_ Estatísticas de MPTHREAT**](mpthreat-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="04de0-127">Type: **[**MPTHREAT\_STATS**](mpthreat-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="04de0-128">Estatísticas relacionadas a ameaças.</span><span class="sxs-lookup"><span data-stu-id="04de0-128">Threat-related statistics.</span></span> <span data-ttu-id="04de0-129">Consulte [**\_ Estatísticas de MPTHREAT**](mpthreat-stats.md).</span><span class="sxs-lookup"><span data-stu-id="04de0-129">See [**MPTHREAT\_STATS**](mpthreat-stats.md).</span></span>

</dd> <dt>

<span data-ttu-id="04de0-130">**ResourceStats**</span><span class="sxs-lookup"><span data-stu-id="04de0-130">**ResourceStats**</span></span>
</dt> <dd>

<span data-ttu-id="04de0-131">Tipo: **[ **\_ Estatísticas de MPRESOURCE**](mpresource-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="04de0-131">Type: **[**MPRESOURCE\_STATS**](mpresource-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="04de0-132">Estatísticas relacionadas a recursos.</span><span class="sxs-lookup"><span data-stu-id="04de0-132">Resource-related statistics.</span></span> <span data-ttu-id="04de0-133">Consulte [**\_ Estatísticas de MPRESOURCE**](mpresource-stats.md).</span><span class="sxs-lookup"><span data-stu-id="04de0-133">See [**MPRESOURCE\_STATS**](mpresource-stats.md).</span></span>

</dd> <dt>

<span data-ttu-id="04de0-134">**SignatureVersion**</span><span class="sxs-lookup"><span data-stu-id="04de0-134">**SignatureVersion**</span></span>
</dt> <dd>

<span data-ttu-id="04de0-135">Tipo: **ULONGLONG**</span><span class="sxs-lookup"><span data-stu-id="04de0-135">Type: **ULONGLONG**</span></span>

</dd> <dd>

<span data-ttu-id="04de0-136">Versão da assinatura usada para verificação.</span><span class="sxs-lookup"><span data-stu-id="04de0-136">Version of signature used for scan.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="04de0-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04de0-137">Requirements</span></span>



| <span data-ttu-id="04de0-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="04de0-138">Requirement</span></span> | <span data-ttu-id="04de0-139">Valor</span><span class="sxs-lookup"><span data-stu-id="04de0-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="04de0-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04de0-140">Minimum supported client</span></span><br/> | <span data-ttu-id="04de0-141">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="04de0-141">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="04de0-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04de0-142">Minimum supported server</span></span><br/> | <span data-ttu-id="04de0-143">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="04de0-143">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="04de0-144">parâmetro</span><span class="sxs-lookup"><span data-stu-id="04de0-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="04de0-145"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="04de0-145"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04de0-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="04de0-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04de0-147">**Estatísticas de MPRESOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="04de0-147">**MPRESOURCE\_STATS**</span></span>](mpresource-stats.md)
</dt> <dt>

[<span data-ttu-id="04de0-148">**tipo de MPSCAN \_**</span><span class="sxs-lookup"><span data-stu-id="04de0-148">**MPSCAN\_TYPE**</span></span>](mpscan-type.md)
</dt> <dt>

[<span data-ttu-id="04de0-149">**MPSOURCE**</span><span class="sxs-lookup"><span data-stu-id="04de0-149">**MPSOURCE**</span></span>](mpsource.md)
</dt> <dt>

[<span data-ttu-id="04de0-150">**Estatísticas de MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="04de0-150">**MPTHREAT\_STATS**</span></span>](mpthreat-stats.md)
</dt> </dl>

 

 





