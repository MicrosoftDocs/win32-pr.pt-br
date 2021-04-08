---
title: Enumeração de BG_JOB_PRIORITY (Deliveryoptimization. h)
description: A enumeração BG_JOB_PRIORITY define os valores constantes que especificam o nível de prioridade de um trabalho.
ms.assetid: AF1F1F6D-473A-49E5-B24D-644A70DF304C
keywords:
- Enumeração de BG_JOB_PRIORITY
- Enumeração de BG_JOB_PRIORITY
topic_type:
- apiref
api_name:
- BG_JOB_PRIORITY
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 45b1f0f3029cc6157f2f100b3324165cfac1b03b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009233"
---
# <a name="bg_job_priority-enumeration"></a><span data-ttu-id="f87f7-105">Enumeração de BG_JOB_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="f87f7-105">BG_JOB_PRIORITY enumeration</span></span>

<span data-ttu-id="f87f7-106">A enumeração **BG_JOB_PRIORITY** define os valores constantes que especificam o nível de prioridade de um trabalho.</span><span class="sxs-lookup"><span data-stu-id="f87f7-106">The **BG_JOB_PRIORITY** enumeration defines the constant values that specify the priority level of a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="f87f7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f87f7-107">Syntax</span></span>


```C++
typedef enum  { 
  BG_JOB_PRIORITY_FOREGROUND,
  BG_JOB_PRIORITY_HIGH,
  BG_JOB_PRIORITY_NORMAL,
  BG_JOB_PRIORITY_LOW
} BG_JOB_PRIORITY;
```



## <a name="constants"></a><span data-ttu-id="f87f7-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="f87f7-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f87f7-109"><span id="BG_JOB_PRIORITY_FOREGROUND"></span><span id="bg_job_priority_foreground"></span>**BG_JOB_PRIORITY_FOREGROUND**</span><span class="sxs-lookup"><span data-stu-id="f87f7-109"><span id="BG_JOB_PRIORITY_FOREGROUND"></span><span id="bg_job_priority_foreground"></span>**BG_JOB_PRIORITY_FOREGROUND**</span></span>
</dt> <dd>

<span data-ttu-id="f87f7-110">Transfere o trabalho em primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="f87f7-110">Transfers the job in the foreground.</span></span> <span data-ttu-id="f87f7-111">As transferências de primeiro plano competem pela largura de banda da rede com outros aplicativos, o que pode impedir a experiência de rede do usuário.</span><span class="sxs-lookup"><span data-stu-id="f87f7-111">Foreground transfers compete for network bandwidth with other applications, which can impede the user's network experience.</span></span> <span data-ttu-id="f87f7-112">Esse é o nível de prioridade mais alto.</span><span class="sxs-lookup"><span data-stu-id="f87f7-112">This is the highest priority level.</span></span>

</dd> <dt>

<span data-ttu-id="f87f7-113"><span id="BG_JOB_PRIORITY_HIGH"></span><span id="bg_job_priority_high"></span>**BG_JOB_PRIORITY_HIGH**</span><span class="sxs-lookup"><span data-stu-id="f87f7-113"><span id="BG_JOB_PRIORITY_HIGH"></span><span id="bg_job_priority_high"></span>**BG_JOB_PRIORITY_HIGH**</span></span>
</dt> <dd>

<span data-ttu-id="f87f7-114">Transfere o trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="f87f7-114">Transfers the job in the background.</span></span> <span data-ttu-id="f87f7-115">As transferências em segundo plano usam uma pequena porcentagem da largura de banda da rede.</span><span class="sxs-lookup"><span data-stu-id="f87f7-115">Background transfers use a small percentage of network bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="f87f7-116"><span id="BG_JOB_PRIORITY_NORMAL"></span><span id="bg_job_priority_normal"></span>**BG_JOB_PRIORITY_NORMAL**</span><span class="sxs-lookup"><span data-stu-id="f87f7-116"><span id="BG_JOB_PRIORITY_NORMAL"></span><span id="bg_job_priority_normal"></span>**BG_JOB_PRIORITY_NORMAL**</span></span>
</dt> <dd>

<span data-ttu-id="f87f7-117">O comportamento DO é o mesmo para todos os trabalhos que não sejam de primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="f87f7-117">DO behavior is same for all non foreground job.</span></span> <span data-ttu-id="f87f7-118">Consulte os comentários em BG_JOB_PRIORITY_HIGH para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="f87f7-118">See comments in BG_JOB_PRIORITY_HIGH for details.</span></span>

</dd> <dt>

<span data-ttu-id="f87f7-119"><span id="BG_JOB_PRIORITY_LOW"></span><span id="bg_job_priority_low"></span>**BG_JOB_PRIORITY_LOW**</span><span class="sxs-lookup"><span data-stu-id="f87f7-119"><span id="BG_JOB_PRIORITY_LOW"></span><span id="bg_job_priority_low"></span>**BG_JOB_PRIORITY_LOW**</span></span>
</dt> <dd>

<span data-ttu-id="f87f7-120">O comportamento DO é o mesmo para todos os trabalhos que não sejam de primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="f87f7-120">DO behavior is same for all non foreground job.</span></span> <span data-ttu-id="f87f7-121">Consulte os comentários em BG_JOB_PRIORITY_HIGH para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="f87f7-121">See comments in BG_JOB_PRIORITY_HIGH for details.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f87f7-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="f87f7-122">Remarks</span></span>

<span data-ttu-id="f87f7-123">Várias transferências de primeiro e segundo plano podem ocorrer simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="f87f7-123">Multiple foreground and background transfers can take place simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="f87f7-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f87f7-124">Requirements</span></span>



| <span data-ttu-id="f87f7-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f87f7-125">Requirement</span></span> | <span data-ttu-id="f87f7-126">Valor</span><span class="sxs-lookup"><span data-stu-id="f87f7-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f87f7-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f87f7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f87f7-128">\[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="f87f7-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f87f7-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f87f7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f87f7-130">Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]</span><span class="sxs-lookup"><span data-stu-id="f87f7-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f87f7-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f87f7-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f87f7-132"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="f87f7-132"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f87f7-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="f87f7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f87f7-134">**Método ibackgroundcopyjob:: getanteriority**</span><span class="sxs-lookup"><span data-stu-id="f87f7-134">**IBackgroundCopyJob::GetPriority**</span></span>](ibackgroundcopyjob-getpriority.md)
</dt> <dt>

[<span data-ttu-id="f87f7-135">**Método ibackgroundcopyjob:: setanteriority**</span><span class="sxs-lookup"><span data-stu-id="f87f7-135">**IBackgroundCopyJob::SetPriority**</span></span>](ibackgroundcopyjob-setpriority.md)
</dt> </dl>

 

 





