---
title: Enumeração de MPTHREAT_STATUS (MpClient. h)
description: Possível status de ameaça.
ms.assetid: 64B57C8B-231B-4A2C-BF2E-45DB62B8350E
keywords:
- Recursos do ambiente Windows herdado de enumeração de MPTHREAT_STATUS
- PMPTHREAT_STATUS recursos de ambiente herdados do ponteiro de enumeração do Windows
topic_type:
- apiref
api_name:
- MPTHREAT_STATUS
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 978a152d6f14d7b3577ece0a2e8bd5a8ba741a3b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756950"
---
# <a name="mpthreat_status-enumeration"></a><span data-ttu-id="295cd-105">\_Enumeração de status MPTHREAT</span><span class="sxs-lookup"><span data-stu-id="295cd-105">MPTHREAT\_STATUS enumeration</span></span>

<span data-ttu-id="295cd-106">Possível status de ameaça.</span><span class="sxs-lookup"><span data-stu-id="295cd-106">Possible threat status.</span></span>

## <a name="syntax"></a><span data-ttu-id="295cd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="295cd-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_STATUS { 
  MP_THREAT_STATUS_UNKNOWN            = 0,
  MP_THREAT_STATUS_DETECTED           = 1,
  MP_THREAT_STATUS_CLEANED            = 2,
  MP_THREAT_STATUS_QUARANTINED        = 3,
  MP_THREAT_STATUS_REMOVED            = 4,
  MP_THREAT_STATUS_ALLOWED            = 5,
  MP_THREAT_STATUS_BLOCKED            = 6,
  MP_THREAT_STATUS_CLEAN_FAILED       = 102,
  MP_THREAT_STATUS_QUARANTINE_FAILED  = 103,
  MP_THREAT_STATUS_REMOVE_FAILED      = 104,
  MP_THREAT_STATUS_ALLOW_FAILED       = 105,
  MP_THREAT_STATUS_ABANDONED          = 106,
  MP_THREAT_STATUS_BLOCK_FAILED       = 107
} MPTHREAT_STATUS, *PMPTHREAT_STATUS;
```



## <a name="constants"></a><span data-ttu-id="295cd-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="295cd-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="295cd-109"><span id="MP_THREAT_STATUS_UNKNOWN"></span><span id="mp_threat_status_unknown"></span>**\_status de ameaça MP \_ \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="295cd-109"><span id="MP_THREAT_STATUS_UNKNOWN"></span><span id="mp_threat_status_unknown"></span>**MP\_THREAT\_STATUS\_UNKNOWN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="295cd-110"><span id="MP_THREAT_STATUS_DETECTED"></span><span id="mp_threat_status_detected"></span>**\_status de ameaça MP \_ \_ detectado**</span><span class="sxs-lookup"><span data-stu-id="295cd-110"><span id="MP_THREAT_STATUS_DETECTED"></span><span id="mp_threat_status_detected"></span>**MP\_THREAT\_STATUS\_DETECTED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="295cd-111"><span id="MP_THREAT_STATUS_CLEANED"></span><span id="mp_threat_status_cleaned"></span>**\_status de ameaça MP \_ \_ limpo**</span><span class="sxs-lookup"><span data-stu-id="295cd-111"><span id="MP_THREAT_STATUS_CLEANED"></span><span id="mp_threat_status_cleaned"></span>**MP\_THREAT\_STATUS\_CLEANED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="295cd-112"><span id="MP_THREAT_STATUS_QUARANTINED"></span><span id="mp_threat_status_quarantined"></span>**STATUS da ameaça MP em \_ \_ \_ quarentena**</span><span class="sxs-lookup"><span data-stu-id="295cd-112"><span id="MP_THREAT_STATUS_QUARANTINED"></span><span id="mp_threat_status_quarantined"></span>**MP\_THREAT\_STATUS\_QUARANTINED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="295cd-113"><span id="MP_THREAT_STATUS_REMOVED"></span><span id="mp_threat_status_removed"></span>**\_status da ameaça MP \_ \_ removido**</span><span class="sxs-lookup"><span data-stu-id="295cd-113"><span id="MP_THREAT_STATUS_REMOVED"></span><span id="mp_threat_status_removed"></span>**MP\_THREAT\_STATUS\_REMOVED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="295cd-114"><span id="MP_THREAT_STATUS_ALLOWED"></span><span id="mp_threat_status_allowed"></span>**\_status de ameaça MP \_ \_ permitido**</span><span class="sxs-lookup"><span data-stu-id="295cd-114"><span id="MP_THREAT_STATUS_ALLOWED"></span><span id="mp_threat_status_allowed"></span>**MP\_THREAT\_STATUS\_ALLOWED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="295cd-115"><span id="MP_THREAT_STATUS_BLOCKED"></span><span id="mp_threat_status_blocked"></span>**\_status de ameaça MP \_ \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="295cd-115"><span id="MP_THREAT_STATUS_BLOCKED"></span><span id="mp_threat_status_blocked"></span>**MP\_THREAT\_STATUS\_BLOCKED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="295cd-116"><span id="MP_THREAT_STATUS_CLEAN_FAILED"></span><span id="mp_threat_status_clean_failed"></span>**\_ \_ \_ falha ao limpar o status da ameaça MP \_**</span><span class="sxs-lookup"><span data-stu-id="295cd-116"><span id="MP_THREAT_STATUS_CLEAN_FAILED"></span><span id="mp_threat_status_clean_failed"></span>**MP\_THREAT\_STATUS\_CLEAN\_FAILED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="295cd-117"><span id="MP_THREAT_STATUS_QUARANTINE_FAILED"></span><span id="mp_threat_status_quarantine_failed"></span>**\_ \_ \_ falha na quarentena do status da ameaça MP \_**</span><span class="sxs-lookup"><span data-stu-id="295cd-117"><span id="MP_THREAT_STATUS_QUARANTINE_FAILED"></span><span id="mp_threat_status_quarantine_failed"></span>**MP\_THREAT\_STATUS\_QUARANTINE\_FAILED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="295cd-118"><span id="MP_THREAT_STATUS_REMOVE_FAILED"></span><span id="mp_threat_status_remove_failed"></span>**\_ \_ \_ falha ao remover o status da ameaça MP \_**</span><span class="sxs-lookup"><span data-stu-id="295cd-118"><span id="MP_THREAT_STATUS_REMOVE_FAILED"></span><span id="mp_threat_status_remove_failed"></span>**MP\_THREAT\_STATUS\_REMOVE\_FAILED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="295cd-119"><span id="MP_THREAT_STATUS_ALLOW_FAILED"></span><span id="mp_threat_status_allow_failed"></span>**\_ \_ \_ falha ao permitir o status da ameaça MP \_**</span><span class="sxs-lookup"><span data-stu-id="295cd-119"><span id="MP_THREAT_STATUS_ALLOW_FAILED"></span><span id="mp_threat_status_allow_failed"></span>**MP\_THREAT\_STATUS\_ALLOW\_FAILED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="295cd-120"><span id="MP_THREAT_STATUS_ABANDONED"></span><span id="mp_threat_status_abandoned"></span>**STATUS de ameaça de MP \_ \_ \_ abandonado**</span><span class="sxs-lookup"><span data-stu-id="295cd-120"><span id="MP_THREAT_STATUS_ABANDONED"></span><span id="mp_threat_status_abandoned"></span>**MP\_THREAT\_STATUS\_ABANDONED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="295cd-121"><span id="MP_THREAT_STATUS_BLOCK_FAILED"></span><span id="mp_threat_status_block_failed"></span>**\_ \_ \_ falha no bloco de status de ameaça MP \_**</span><span class="sxs-lookup"><span data-stu-id="295cd-121"><span id="MP_THREAT_STATUS_BLOCK_FAILED"></span><span id="mp_threat_status_block_failed"></span>**MP\_THREAT\_STATUS\_BLOCK\_FAILED**</span></span>
<span data-ttu-id="295cd-122"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="295cd-122"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="295cd-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="295cd-123">Requirements</span></span>



| <span data-ttu-id="295cd-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="295cd-124">Requirement</span></span> | <span data-ttu-id="295cd-125">Valor</span><span class="sxs-lookup"><span data-stu-id="295cd-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="295cd-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="295cd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="295cd-127">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="295cd-127">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="295cd-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="295cd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="295cd-129">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="295cd-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="295cd-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="295cd-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="295cd-131"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="295cd-131"><dt>MpClient.h</dt></span></span> </dl> |



 

 





