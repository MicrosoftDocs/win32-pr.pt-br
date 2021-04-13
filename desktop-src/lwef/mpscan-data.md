---
title: Estrutura de MPSCAN_DATA (MpClient. h)
description: Verifique os dados passados para o retorno de chamada.
ms.assetid: 6C9AAF1E-7566-43EE-A100-5112E9B8878C
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPSCAN_DATA
- Ponteiro de estrutura de PMPSCAN_DATA recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPSCAN_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e78508313f102e2baad19cf359a5c3a7c172db0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455963"
---
# <a name="mpscan_data-structure"></a><span data-ttu-id="12fd2-105">\_Estrutura de dados MPSCAN</span><span class="sxs-lookup"><span data-stu-id="12fd2-105">MPSCAN\_DATA structure</span></span>

<span data-ttu-id="12fd2-106">Verifique os dados passados para o retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="12fd2-106">Scan data passed to the callback.</span></span>

<span data-ttu-id="12fd2-107">Essa estrutura contém as estatísticas de recursos e ameaças cumulativas.</span><span class="sxs-lookup"><span data-stu-id="12fd2-107">This structure contains cumulative threat and resource statistics.</span></span> <span data-ttu-id="12fd2-108">Esses campos de estatística são sempre válidos.</span><span class="sxs-lookup"><span data-stu-id="12fd2-108">These stat fields are always valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="12fd2-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12fd2-109">Syntax</span></span>


```C++
typedef struct tagMPSCAN_DATA {
  MPSCAN_TYPE      ScanType;
  PMPRESOURCE_INFO ResourceInfo;
  MPRESOURCE_STATS ResourceStats;
  MPTHREAT_STATS   ThreatStats;
} MPSCAN_DATA, *PMPSCAN_DATA;
```



## <a name="members"></a><span data-ttu-id="12fd2-110">Membros</span><span class="sxs-lookup"><span data-stu-id="12fd2-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="12fd2-111">**ScanType**</span><span class="sxs-lookup"><span data-stu-id="12fd2-111">**ScanType**</span></span>
</dt> <dd>

<span data-ttu-id="12fd2-112">Tipo: **[ **\_ tipo de MPSCAN**](mpscan-type.md)**</span><span class="sxs-lookup"><span data-stu-id="12fd2-112">Type: **[**MPSCAN\_TYPE**](mpscan-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="12fd2-113">Tipo de verificação.</span><span class="sxs-lookup"><span data-stu-id="12fd2-113">Scan type.</span></span>

</dd> <dt>

<span data-ttu-id="12fd2-114">**ResourceInfo**</span><span class="sxs-lookup"><span data-stu-id="12fd2-114">**ResourceInfo**</span></span>
</dt> <dd>

<span data-ttu-id="12fd2-115">Tipo: **\_ informações de PMPRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="12fd2-115">Type: **PMPRESOURCE\_INFO**</span></span>

</dd> <dd>

<span data-ttu-id="12fd2-116">Informações sobre o recurso.</span><span class="sxs-lookup"><span data-stu-id="12fd2-116">Resource information.</span></span> <span data-ttu-id="12fd2-117">Consulte [**MPRESOURCE \_ info**](mpresource-info.md).</span><span class="sxs-lookup"><span data-stu-id="12fd2-117">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="12fd2-118">**ResourceStats**</span><span class="sxs-lookup"><span data-stu-id="12fd2-118">**ResourceStats**</span></span>
</dt> <dd>

<span data-ttu-id="12fd2-119">Tipo: **[ **\_ Estatísticas de MPRESOURCE**](mpresource-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="12fd2-119">Type: **[**MPRESOURCE\_STATS**](mpresource-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="12fd2-120">Estatísticas cumulativas relacionadas a recursos.</span><span class="sxs-lookup"><span data-stu-id="12fd2-120">Resource-related cumulative statistics.</span></span>

</dd> <dt>

<span data-ttu-id="12fd2-121">**ThreatStats**</span><span class="sxs-lookup"><span data-stu-id="12fd2-121">**ThreatStats**</span></span>
</dt> <dd>

<span data-ttu-id="12fd2-122">Tipo: **[ **\_ Estatísticas de MPTHREAT**](mpthreat-stats.md)**</span><span class="sxs-lookup"><span data-stu-id="12fd2-122">Type: **[**MPTHREAT\_STATS**](mpthreat-stats.md)**</span></span>

</dd> <dd>

<span data-ttu-id="12fd2-123">Estatísticas de ameaças com conclusões de verificação bem-sucedidas.</span><span class="sxs-lookup"><span data-stu-id="12fd2-123">Threat statistics with successful scan completions.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="12fd2-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12fd2-124">Requirements</span></span>



| <span data-ttu-id="12fd2-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="12fd2-125">Requirement</span></span> | <span data-ttu-id="12fd2-126">Valor</span><span class="sxs-lookup"><span data-stu-id="12fd2-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="12fd2-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12fd2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="12fd2-128">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="12fd2-128">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="12fd2-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12fd2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="12fd2-130">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="12fd2-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="12fd2-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12fd2-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="12fd2-132"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="12fd2-132"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12fd2-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="12fd2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12fd2-134">**informações de MPRESOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="12fd2-134">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> <dt>

[<span data-ttu-id="12fd2-135">**Estatísticas de MPRESOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="12fd2-135">**MPRESOURCE\_STATS**</span></span>](mpresource-stats.md)
</dt> <dt>

[<span data-ttu-id="12fd2-136">**tipo de MPSCAN \_**</span><span class="sxs-lookup"><span data-stu-id="12fd2-136">**MPSCAN\_TYPE**</span></span>](mpscan-type.md)
</dt> <dt>

[<span data-ttu-id="12fd2-137">**Estatísticas de MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="12fd2-137">**MPTHREAT\_STATS**</span></span>](mpthreat-stats.md)
</dt> </dl>

 

 





