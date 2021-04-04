---
title: Enumeração de MPEXECUTION_STATUS (MpClient. h)
description: Possível status de execução de ameaça.
ms.assetid: 89D6BD9F-4A4C-48F5-BFD1-D09A240EB253
keywords:
- Recursos do ambiente Windows herdado de enumeração de MPEXECUTION_STATUS
- PMPEXECUTION_STATUS recursos de ambiente herdados do ponteiro de enumeração do Windows
topic_type:
- apiref
api_name:
- MPEXECUTION_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5cc21a0d8ec45d0715a7b1af8fb81a25e260711
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824306"
---
# <a name="mpexecution_status-enumeration"></a><span data-ttu-id="5b545-105">\_Enumeração de status MPEXECUTION</span><span class="sxs-lookup"><span data-stu-id="5b545-105">MPEXECUTION\_STATUS enumeration</span></span>

<span data-ttu-id="5b545-106">Possível status de execução de ameaça.</span><span class="sxs-lookup"><span data-stu-id="5b545-106">Possible threat execution status.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b545-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b545-107">Syntax</span></span>


```C++
typedef enum tagMPEXECUTION_STATUS { 
  MP_EXECUTION_STATUS_UNKNOWN        = 0,
  MP_EXECUTION_STATUS_BLOCKED        = 1,
  MP_EXECUTION_STATUS_ALLOWED        = 2,
  MP_EXECUTION_STATUS_EXECUTING      = 3,
  MP_EXECUTION_STATUS_NOT_EXECUTING  = 4
} MPEXECUTION_STATUS, *PMPEXECUTION_STATUS;
```



## <a name="constants"></a><span data-ttu-id="5b545-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="5b545-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="5b545-109"><span id="MP_EXECUTION_STATUS_UNKNOWN"></span><span id="mp_execution_status_unknown"></span>**STATUS de execução do MP \_ \_ \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="5b545-109"><span id="MP_EXECUTION_STATUS_UNKNOWN"></span><span id="mp_execution_status_unknown"></span>**MP\_EXECUTION\_STATUS\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="5b545-110">O status de execução não é conhecido.</span><span class="sxs-lookup"><span data-stu-id="5b545-110">Execution status is not known.</span></span>

</dd> <dt>

<span data-ttu-id="5b545-111"><span id="MP_EXECUTION_STATUS_BLOCKED"></span><span id="mp_execution_status_blocked"></span>**STATUS de execução do MP \_ \_ \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="5b545-111"><span id="MP_EXECUTION_STATUS_BLOCKED"></span><span id="mp_execution_status_blocked"></span>**MP\_EXECUTION\_STATUS\_BLOCKED**</span></span>
</dt> <dd>

<span data-ttu-id="5b545-112">Bloqueado da execução por mini-Filter.</span><span class="sxs-lookup"><span data-stu-id="5b545-112">Blocked from execution by mini-filter.</span></span>

</dd> <dt>

<span data-ttu-id="5b545-113"><span id="MP_EXECUTION_STATUS_ALLOWED"></span><span id="mp_execution_status_allowed"></span>**STATUS de execução do MP \_ \_ \_ permitido**</span><span class="sxs-lookup"><span data-stu-id="5b545-113"><span id="MP_EXECUTION_STATUS_ALLOWED"></span><span id="mp_execution_status_allowed"></span>**MP\_EXECUTION\_STATUS\_ALLOWED**</span></span>
</dt> <dd>

<span data-ttu-id="5b545-114">Permissão para executar por mini-filtro.</span><span class="sxs-lookup"><span data-stu-id="5b545-114">Allowed to execute by mini-filter.</span></span>

</dd> <dt>

<span data-ttu-id="5b545-115"><span id="MP_EXECUTION_STATUS_EXECUTING"></span><span id="mp_execution_status_executing"></span>**execuções do status de execução do MP \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="5b545-115"><span id="MP_EXECUTION_STATUS_EXECUTING"></span><span id="mp_execution_status_executing"></span>**MP\_EXECUTION\_STATUS\_EXECUTING**</span></span>
</dt> <dd>

<span data-ttu-id="5b545-116">A ameaça está em execução.</span><span class="sxs-lookup"><span data-stu-id="5b545-116">Threat is executing.</span></span>

</dd> <dt>

<span data-ttu-id="5b545-117"><span id="MP_EXECUTION_STATUS_NOT_EXECUTING"></span><span id="mp_execution_status_not_executing"></span>**o status de execução do MP não está em \_ \_ \_ \_ execução**</span><span class="sxs-lookup"><span data-stu-id="5b545-117"><span id="MP_EXECUTION_STATUS_NOT_EXECUTING"></span><span id="mp_execution_status_not_executing"></span>**MP\_EXECUTION\_STATUS\_NOT\_EXECUTING**</span></span>
</dt> <dd>

<span data-ttu-id="5b545-118">A ameaça não está em execução e só está disponível no mecanismo durante a correção.</span><span class="sxs-lookup"><span data-stu-id="5b545-118">Threat is not executing, and is only available from the engine during remediation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5b545-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b545-119">Requirements</span></span>



| <span data-ttu-id="5b545-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b545-120">Requirement</span></span> | <span data-ttu-id="5b545-121">Valor</span><span class="sxs-lookup"><span data-stu-id="5b545-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b545-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b545-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5b545-123">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="5b545-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="5b545-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5b545-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5b545-125">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="5b545-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5b545-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5b545-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b545-127"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b545-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





