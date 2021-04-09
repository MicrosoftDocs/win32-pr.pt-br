---
title: Enumeração de MP_PERSISTENCE_LIMIT_TYPE (MpClient. h)
description: Tipo de limite de persistência.
ms.assetid: 57423110-7966-4240-8B15-1859D3D9EA4C
keywords:
- Recursos do ambiente Windows herdado de enumeração de MP_PERSISTENCE_LIMIT_TYPE
- PMP_PERSISTENCE_LIMIT_TYPE recursos de ambiente herdados do ponteiro de enumeração do Windows
topic_type:
- apiref
api_name:
- MP_PERSISTENCE_LIMIT_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fb52bc6ee630590ca189b88c1fdde5a30e17747
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009680"
---
# <a name="mp_persistence_limit_type-enumeration"></a><span data-ttu-id="6b430-105">\_Enumeração de \_ tipo de limite de persistência MP \_</span><span class="sxs-lookup"><span data-stu-id="6b430-105">MP\_PERSISTENCE\_LIMIT\_TYPE enumeration</span></span>

<span data-ttu-id="6b430-106">Tipo de limite de persistência.</span><span class="sxs-lookup"><span data-stu-id="6b430-106">Persistence limit type.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b430-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b430-107">Syntax</span></span>


```C++
typedef enum tagMP_PERSISTENCE_LIMIT_TYPE { 
  MP_PERSISTENCE_UNKNOWN      = 0,
  MP_PERSISTENCE_NO_LIMIT     = 1,
  MP_PERSISTENCE_DURATION     = 2,
  MP_PERSISTENCE_VDM_VERSION  = 3,
  MP_PERSISTENCE_TIMESTAMP    = 4,
  MP_PERSISTENCE_FORCED       = 5
} MP_PERSISTENCE_LIMIT_TYPE, *PMP_PERSISTENCE_LIMIT_TYPE;
```



## <a name="constants"></a><span data-ttu-id="6b430-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="6b430-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6b430-109"><span id="MP_PERSISTENCE_UNKNOWN"></span><span id="mp_persistence_unknown"></span>**persistência de MP \_ \_ desconhecida**</span><span class="sxs-lookup"><span data-stu-id="6b430-109"><span id="MP_PERSISTENCE_UNKNOWN"></span><span id="mp_persistence_unknown"></span>**MP\_PERSISTENCE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="6b430-110">Desconhecido.</span><span class="sxs-lookup"><span data-stu-id="6b430-110">Unknown.</span></span>

</dd> <dt>

<span data-ttu-id="6b430-111"><span id="MP_PERSISTENCE_NO_LIMIT"></span><span id="mp_persistence_no_limit"></span>**persistência de MP \_ \_ sem \_ limite**</span><span class="sxs-lookup"><span data-stu-id="6b430-111"><span id="MP_PERSISTENCE_NO_LIMIT"></span><span id="mp_persistence_no_limit"></span>**MP\_PERSISTENCE\_NO\_LIMIT**</span></span>
</dt> <dd>

<span data-ttu-id="6b430-112">Não há limite.</span><span class="sxs-lookup"><span data-stu-id="6b430-112">No limit.</span></span>

</dd> <dt>

<span data-ttu-id="6b430-113"><span id="MP_PERSISTENCE_DURATION"></span><span id="mp_persistence_duration"></span>**\_duração da persistência MP \_**</span><span class="sxs-lookup"><span data-stu-id="6b430-113"><span id="MP_PERSISTENCE_DURATION"></span><span id="mp_persistence_duration"></span>**MP\_PERSISTENCE\_DURATION**</span></span>
</dt> <dd>

<span data-ttu-id="6b430-114">Permanência.</span><span class="sxs-lookup"><span data-stu-id="6b430-114">Duration.</span></span>

</dd> <dt>

<span data-ttu-id="6b430-115"><span id="MP_PERSISTENCE_VDM_VERSION"></span><span id="mp_persistence_vdm_version"></span>**\_versão do \_ VDM \_ persistência do MP**</span><span class="sxs-lookup"><span data-stu-id="6b430-115"><span id="MP_PERSISTENCE_VDM_VERSION"></span><span id="mp_persistence_vdm_version"></span>**MP\_PERSISTENCE\_VDM\_VERSION**</span></span>
</dt> <dd>

<span data-ttu-id="6b430-116">Versão do VDM.</span><span class="sxs-lookup"><span data-stu-id="6b430-116">VDM version.</span></span>

</dd> <dt>

<span data-ttu-id="6b430-117"><span id="MP_PERSISTENCE_TIMESTAMP"></span><span id="mp_persistence_timestamp"></span>**\_carimbo de \_ data/hora de persistência MP**</span><span class="sxs-lookup"><span data-stu-id="6b430-117"><span id="MP_PERSISTENCE_TIMESTAMP"></span><span id="mp_persistence_timestamp"></span>**MP\_PERSISTENCE\_TIMESTAMP**</span></span>
</dt> <dd>

<span data-ttu-id="6b430-118">Estampa.</span><span class="sxs-lookup"><span data-stu-id="6b430-118">Timestamp.</span></span>

</dd> <dt>

<span data-ttu-id="6b430-119"><span id="MP_PERSISTENCE_FORCED"></span><span id="mp_persistence_forced"></span>**persistência de MP \_ \_ forçada**</span><span class="sxs-lookup"><span data-stu-id="6b430-119"><span id="MP_PERSISTENCE_FORCED"></span><span id="mp_persistence_forced"></span>**MP\_PERSISTENCE\_FORCED**</span></span>
</dt> <dd>

<span data-ttu-id="6b430-120">Exigir.</span><span class="sxs-lookup"><span data-stu-id="6b430-120">Forced.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6b430-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b430-121">Requirements</span></span>



| <span data-ttu-id="6b430-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b430-122">Requirement</span></span> | <span data-ttu-id="6b430-123">Valor</span><span class="sxs-lookup"><span data-stu-id="6b430-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b430-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b430-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6b430-125">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="6b430-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="6b430-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6b430-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6b430-127">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="6b430-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6b430-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6b430-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b430-129"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b430-129"><dt>MpClient.h</dt></span></span> </dl> |



 

 





