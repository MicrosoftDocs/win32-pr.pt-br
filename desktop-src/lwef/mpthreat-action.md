---
title: Enumeração de MPTHREAT_ACTION (MpClient. h)
description: Possíveis ações de ameaça.
ms.assetid: 142249A5-4C9D-4E3A-A06E-70C040F9C14F
keywords:
- Recursos do ambiente Windows herdado de enumeração de MPTHREAT_ACTION
- PMPTHREAT_ACTION recursos de ambiente herdados do ponteiro de enumeração do Windows
topic_type:
- apiref
api_name:
- MPTHREAT_ACTION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae0377517af590072b797a57c051ad062842ea9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085504"
---
# <a name="mpthreat_action-enumeration"></a><span data-ttu-id="43f02-105">\_Enumeração de ação MPTHREAT</span><span class="sxs-lookup"><span data-stu-id="43f02-105">MPTHREAT\_ACTION enumeration</span></span>

<span data-ttu-id="43f02-106">Possíveis ações de ameaça.</span><span class="sxs-lookup"><span data-stu-id="43f02-106">Possible threat actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="43f02-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="43f02-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_ACTION { 
  MP_THREAT_ACTION_UNKNOWN      = 0,
  MP_THREAT_ACTION_CLEAN        = 1,
  MP_THREAT_ACTION_QUARANTINE   = 2,
  MP_THREAT_ACTION_REMOVE       = 3,
  MP_THREAT_ACTION_ALLOW        = 6,
  MP_THREAT_ACTION_USERDEFINED  = 8,
  MP_THREAT_ACTION_NOACTION     = 9,
  MP_THREAT_ACTION_BLOCK        = 10,
  MP_THREAT_ACTION_MAX_VALUE    = 10
} MPTHREAT_ACTION, *PMPTHREAT_ACTION;
```



## <a name="constants"></a><span data-ttu-id="43f02-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="43f02-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="43f02-109"><span id="MP_THREAT_ACTION_UNKNOWN"></span><span id="mp_threat_action_unknown"></span>**\_ação de ameaça MP \_ \_ desconhecida**</span><span class="sxs-lookup"><span data-stu-id="43f02-109"><span id="MP_THREAT_ACTION_UNKNOWN"></span><span id="mp_threat_action_unknown"></span>**MP\_THREAT\_ACTION\_UNKNOWN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="43f02-110"><span id="MP_THREAT_ACTION_CLEAN"></span><span id="mp_threat_action_clean"></span>**\_limpeza de \_ ação de ameaça MP \_**</span><span class="sxs-lookup"><span data-stu-id="43f02-110"><span id="MP_THREAT_ACTION_CLEAN"></span><span id="mp_threat_action_clean"></span>**MP\_THREAT\_ACTION\_CLEAN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="43f02-111"><span id="MP_THREAT_ACTION_QUARANTINE"></span><span id="mp_threat_action_quarantine"></span>**\_quarentena da \_ ação de ameaça de MP \_**</span><span class="sxs-lookup"><span data-stu-id="43f02-111"><span id="MP_THREAT_ACTION_QUARANTINE"></span><span id="mp_threat_action_quarantine"></span>**MP\_THREAT\_ACTION\_QUARANTINE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="43f02-112"><span id="MP_THREAT_ACTION_REMOVE"></span><span id="mp_threat_action_remove"></span>**\_remoção de \_ ação de ameaça MP \_**</span><span class="sxs-lookup"><span data-stu-id="43f02-112"><span id="MP_THREAT_ACTION_REMOVE"></span><span id="mp_threat_action_remove"></span>**MP\_THREAT\_ACTION\_REMOVE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="43f02-113"><span id="MP_THREAT_ACTION_ALLOW"></span><span id="mp_threat_action_allow"></span>**\_permissão de \_ ação de ameaça MP \_**</span><span class="sxs-lookup"><span data-stu-id="43f02-113"><span id="MP_THREAT_ACTION_ALLOW"></span><span id="mp_threat_action_allow"></span>**MP\_THREAT\_ACTION\_ALLOW**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="43f02-114"><span id="MP_THREAT_ACTION_USERDEFINED"></span><span id="mp_threat_action_userdefined"></span>**\_ação de ameaça MP \_ \_ UserDefined**</span><span class="sxs-lookup"><span data-stu-id="43f02-114"><span id="MP_THREAT_ACTION_USERDEFINED"></span><span id="mp_threat_action_userdefined"></span>**MP\_THREAT\_ACTION\_USERDEFINED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="43f02-115"><span id="MP_THREAT_ACTION_NOACTION"></span><span id="mp_threat_action_noaction"></span>**ação de ameaça de MP \_ \_ \_ NoAction**</span><span class="sxs-lookup"><span data-stu-id="43f02-115"><span id="MP_THREAT_ACTION_NOACTION"></span><span id="mp_threat_action_noaction"></span>**MP\_THREAT\_ACTION\_NOACTION**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="43f02-116"><span id="MP_THREAT_ACTION_BLOCK"></span><span id="mp_threat_action_block"></span>**\_bloco de \_ ação de ameaça MP \_**</span><span class="sxs-lookup"><span data-stu-id="43f02-116"><span id="MP_THREAT_ACTION_BLOCK"></span><span id="mp_threat_action_block"></span>**MP\_THREAT\_ACTION\_BLOCK**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="43f02-117"><span id="MP_THREAT_ACTION_MAX_VALUE"></span><span id="mp_threat_action_max_value"></span>**\_ \_ valor máximo de ação de ameaça MP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="43f02-117"><span id="MP_THREAT_ACTION_MAX_VALUE"></span><span id="mp_threat_action_max_value"></span>**MP\_THREAT\_ACTION\_MAX\_VALUE**</span></span>
<span data-ttu-id="43f02-118"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="43f02-118"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="43f02-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43f02-119">Requirements</span></span>



| <span data-ttu-id="43f02-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="43f02-120">Requirement</span></span> | <span data-ttu-id="43f02-121">Valor</span><span class="sxs-lookup"><span data-stu-id="43f02-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43f02-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43f02-122">Minimum supported client</span></span><br/> | <span data-ttu-id="43f02-123">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="43f02-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="43f02-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43f02-124">Minimum supported server</span></span><br/> | <span data-ttu-id="43f02-125">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="43f02-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="43f02-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="43f02-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="43f02-127"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="43f02-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





