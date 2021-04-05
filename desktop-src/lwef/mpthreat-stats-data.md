---
title: Estrutura de MPTHREAT_STATS_DATA (MpClient. h)
description: Dados de estatísticas de ameaças adicionais.
ms.assetid: 8C01C746-8FD8-4311-908D-D1F4E3488480
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPTHREAT_STATS_DATA
- Ponteiro de estrutura de PMPTHREAT_STATS_DATA recursos de ambiente herdados do Windows
topic_type:
- apiref
api_name:
- MPTHREAT_STATS_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9525ddcfc580e9a82ffdb191d20e3748f7a1e16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085503"
---
# <a name="mpthreat_stats_data-structure"></a><span data-ttu-id="4ca3e-105">Estrutura de dados de \_ estatísticas MPTHREAT \_</span><span class="sxs-lookup"><span data-stu-id="4ca3e-105">MPTHREAT\_STATS\_DATA structure</span></span>

<span data-ttu-id="4ca3e-106">Dados de estatísticas de ameaças adicionais.</span><span class="sxs-lookup"><span data-stu-id="4ca3e-106">Additional threat statistics data.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ca3e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4ca3e-107">Syntax</span></span>


```C++
typedef struct tagMPTHREAT_STATS_DATA {
  DWORD dwThreatCount;
} MPTHREAT_STATS_DATA, *PMPTHREAT_STATS_DATA;
```



## <a name="members"></a><span data-ttu-id="4ca3e-108">Membros</span><span class="sxs-lookup"><span data-stu-id="4ca3e-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="4ca3e-109">**dwThreatCount**</span><span class="sxs-lookup"><span data-stu-id="4ca3e-109">**dwThreatCount**</span></span>
</dt> <dd>

<span data-ttu-id="4ca3e-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="4ca3e-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="4ca3e-111">Número de ameaças.</span><span class="sxs-lookup"><span data-stu-id="4ca3e-111">Number of threats.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4ca3e-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ca3e-112">Requirements</span></span>



| <span data-ttu-id="4ca3e-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ca3e-113">Requirement</span></span> | <span data-ttu-id="4ca3e-114">Valor</span><span class="sxs-lookup"><span data-stu-id="4ca3e-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4ca3e-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ca3e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="4ca3e-116">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="4ca3e-116">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="4ca3e-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4ca3e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="4ca3e-118">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="4ca3e-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4ca3e-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4ca3e-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="4ca3e-120"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="4ca3e-120"><dt>MpClient.h</dt></span></span> </dl> |



 

 





