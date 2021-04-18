---
description: A enumeração EXPERTSTATUSENUMERATION contém valores de status. Ele é usado pelo membro de status da estrutura EXPERTSTATUS e o parâmetro status em ExpertIndicateStatus.
ms.assetid: 217dce5a-3698-45a9-bb13-8379bcbdd762
title: Enumeração EXPERTSTATUSENUMERATION (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERT_STATUS_ENUMERATION
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b634d4dad2e024c3c995216b5af7de23b14b7da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764643"
---
# <a name="expertstatusenumeration-enumeration"></a><span data-ttu-id="8fd44-104">Enumeração EXPERTSTATUSENUMERATION</span><span class="sxs-lookup"><span data-stu-id="8fd44-104">EXPERTSTATUSENUMERATION enumeration</span></span>

<span data-ttu-id="8fd44-105">A enumeração **EXPERTSTATUSENUMERATION** contém valores de status.</span><span class="sxs-lookup"><span data-stu-id="8fd44-105">The **EXPERTSTATUSENUMERATION** enumeration contains status values.</span></span> <span data-ttu-id="8fd44-106">Ele é usado pelo membro de **status** da estrutura [EXPERTSTATUS](expertstatus.md) e o parâmetro *status* em [ExpertIndicateStatus](expertindicatestatus.md).</span><span class="sxs-lookup"><span data-stu-id="8fd44-106">It is used by the **Status** member of [EXPERTSTATUS](expertstatus.md) structure and the *Status* parameter in [ExpertIndicateStatus](expertindicatestatus.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8fd44-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8fd44-107">Syntax</span></span>


```C++
typedef enum  { 
  EXPERTSTATUS_INACTIVE  = 0,
  EXPERTSTATUS_STARTING,
  EXPERTSTATUS_RUNNING,
  EXPERTSTATUS_PROBLEM,
  EXPERTSTATUS_ABORTED,
  EXPERTSTATUS_DONE
} EXPERT_STATUS_ENUMERATION;
```



## <a name="constants"></a><span data-ttu-id="8fd44-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="8fd44-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="8fd44-109"><span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span>**EXPERTSTATUS \_ INativo**</span><span class="sxs-lookup"><span data-stu-id="8fd44-109"><span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span>**EXPERTSTATUS\_INACTIVE**</span></span>
</dt> <dd>

<span data-ttu-id="8fd44-110">O especialista nunca começou.</span><span class="sxs-lookup"><span data-stu-id="8fd44-110">The expert never started.</span></span>

</dd> <dt>

<span data-ttu-id="8fd44-111"><span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span>**EXPERTSTATUS \_ iniciando**</span><span class="sxs-lookup"><span data-stu-id="8fd44-111"><span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span>**EXPERTSTATUS\_STARTING**</span></span>
</dt> <dd>

<span data-ttu-id="8fd44-112">O especialista está sendo iniciado.</span><span class="sxs-lookup"><span data-stu-id="8fd44-112">The expert is starting.</span></span>

</dd> <dt>

<span data-ttu-id="8fd44-113"><span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span>**EXPERTSTATUS \_ em execução**</span><span class="sxs-lookup"><span data-stu-id="8fd44-113"><span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span>**EXPERTSTATUS\_RUNNING**</span></span>
</dt> <dd>

<span data-ttu-id="8fd44-114">O especialista está em execução normalmente.</span><span class="sxs-lookup"><span data-stu-id="8fd44-114">The expert is running normally.</span></span>

</dd> <dt>

<span data-ttu-id="8fd44-115"><span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span>**problema de EXPERTSTATUS \_**</span><span class="sxs-lookup"><span data-stu-id="8fd44-115"><span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span>**EXPERTSTATUS\_PROBLEM**</span></span>
</dt> <dd>

<span data-ttu-id="8fd44-116">Um problema especificado no *substatus* interrompeu o especialista.</span><span class="sxs-lookup"><span data-stu-id="8fd44-116">A problem specified in *SubStatus* stopped the expert.</span></span>

</dd> <dt>

<span data-ttu-id="8fd44-117"><span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span>**EXPERTSTATUS \_ anulado**</span><span class="sxs-lookup"><span data-stu-id="8fd44-117"><span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span>**EXPERTSTATUS\_ABORTED**</span></span>
</dt> <dd>

<span data-ttu-id="8fd44-118">Monitor de Rede parou o especialista.</span><span class="sxs-lookup"><span data-stu-id="8fd44-118">Network Monitor stopped the expert.</span></span>

</dd> <dt>

<span data-ttu-id="8fd44-119"><span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span>**EXPERTSTATUS \_ concluído**</span><span class="sxs-lookup"><span data-stu-id="8fd44-119"><span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span>**EXPERTSTATUS\_DONE**</span></span>
</dt> <dd>

<span data-ttu-id="8fd44-120">O especialista foi concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="8fd44-120">The expert finished successfully.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8fd44-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8fd44-121">Requirements</span></span>



| <span data-ttu-id="8fd44-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="8fd44-122">Requirement</span></span> | <span data-ttu-id="8fd44-123">Valor</span><span class="sxs-lookup"><span data-stu-id="8fd44-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8fd44-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8fd44-124">Minimum supported client</span></span><br/> | <span data-ttu-id="8fd44-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8fd44-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8fd44-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8fd44-126">Minimum supported server</span></span><br/> | <span data-ttu-id="8fd44-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8fd44-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8fd44-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8fd44-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fd44-129"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fd44-129"><dt>Netmon.h</dt></span></span> </dl> |



 

 




