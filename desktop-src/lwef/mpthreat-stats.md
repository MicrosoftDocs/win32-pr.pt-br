---
title: Estrutura de MPTHREAT_STATS (MpClient. h)
description: Estatísticas relacionadas a ameaças.
ms.assetid: 78B7E2A8-1BB4-4610-8E90-1F8ECBE740A8
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPTHREAT_STATS
- Ponteiro de estrutura de PMPTHREAT_STATS recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPTHREAT_STATS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a2eef7acde5fbeac2cf9951dfad3e6923ccea2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824372"
---
# <a name="mpthreat_stats-structure"></a><span data-ttu-id="1588f-105">\_Estrutura de estatísticas MPTHREAT</span><span class="sxs-lookup"><span data-stu-id="1588f-105">MPTHREAT\_STATS structure</span></span>

<span data-ttu-id="1588f-106">Estatísticas relacionadas a ameaças.</span><span class="sxs-lookup"><span data-stu-id="1588f-106">Threat-related statistics.</span></span>

## <a name="syntax"></a><span data-ttu-id="1588f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1588f-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_STATS {
  UINT ThreatCount;
  UINT SuspiciousThreatCount;
  UINT Reserved[4];
} MPTHREAT_STATS, *PMPTHREAT_STATS;
```



## <a name="members"></a><span data-ttu-id="1588f-108">Membros</span><span class="sxs-lookup"><span data-stu-id="1588f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="1588f-109">**ThreatCount**</span><span class="sxs-lookup"><span data-stu-id="1588f-109">**ThreatCount**</span></span>
</dt> <dd>

<span data-ttu-id="1588f-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="1588f-110">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="1588f-111">Número de ameaças detectadas.</span><span class="sxs-lookup"><span data-stu-id="1588f-111">Number of threats detected.</span></span>

</dd> <dt>

<span data-ttu-id="1588f-112">**SuspiciousThreatCount**</span><span class="sxs-lookup"><span data-stu-id="1588f-112">**SuspiciousThreatCount**</span></span>
</dt> <dd>

<span data-ttu-id="1588f-113">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="1588f-113">Type: **UINT**</span></span>

</dd> <dd>

<span data-ttu-id="1588f-114">Número de ameaças detectadas com monitoramento de comportamento.</span><span class="sxs-lookup"><span data-stu-id="1588f-114">Number of threats detected with behavior monitoring.</span></span>

</dd> <dt>

<span data-ttu-id="1588f-115">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="1588f-115">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="1588f-116">Tipo: **uint \[ 4 \]**</span><span class="sxs-lookup"><span data-stu-id="1588f-116">Type: **UINT\[4\]**</span></span>

</dd> <dd>

<span data-ttu-id="1588f-117">Campos reservados para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="1588f-117">Fields reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1588f-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1588f-118">Requirements</span></span>



| <span data-ttu-id="1588f-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1588f-119">Requirement</span></span> | <span data-ttu-id="1588f-120">Valor</span><span class="sxs-lookup"><span data-stu-id="1588f-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1588f-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1588f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1588f-122">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="1588f-122">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1588f-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1588f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1588f-124">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="1588f-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1588f-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1588f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1588f-126"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="1588f-126"><dt>MpClient.h</dt></span></span> </dl> |



 

 





