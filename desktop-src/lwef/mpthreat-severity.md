---
title: Enumeração de MPTHREAT_SEVERITY (MpClient. h)
description: Possíveis severidades de ameaça.
ms.assetid: 7C50AC74-16CB-4198-ABB2-D6999429F2EA
keywords:
- Recursos do ambiente Windows herdado de enumeração de MPTHREAT_SEVERITY
- PMPTHREAT_SEVERITY recursos de ambiente herdados do ponteiro de enumeração do Windows
topic_type:
- apiref
api_name:
- MPTHREAT_SEVERITY
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eec7bff3b23a89ce8187798d8a69a9968cbc2bf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105763874"
---
# <a name="mpthreat_severity-enumeration"></a><span data-ttu-id="886dc-105">\_Enumeração de severidade MPTHREAT</span><span class="sxs-lookup"><span data-stu-id="886dc-105">MPTHREAT\_SEVERITY enumeration</span></span>

<span data-ttu-id="886dc-106">Possíveis severidades de ameaça.</span><span class="sxs-lookup"><span data-stu-id="886dc-106">Possible threat severities.</span></span>

## <a name="syntax"></a><span data-ttu-id="886dc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="886dc-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_SEVERITY { 
  MP_THREAT_SEVERITY_UNKNOWN   = 0,
  MP_THREAT_SEVERITY_LOW       = 1,
  MP_THREAT_SEVERITY_MODERATE  = 2,
  MP_THREAT_SEVERITY_HIGH      = 4,
  MP_THREAT_SEVERITY_SEVERE    = 5,
  MP_THREAT_SEVERITY_MAXVALUE  = 5
} MPTHREAT_SEVERITY, *PMPTHREAT_SEVERITY;
```



## <a name="constants"></a><span data-ttu-id="886dc-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="886dc-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="886dc-109"><span id="MP_THREAT_SEVERITY_UNKNOWN"></span><span id="mp_threat_severity_unknown"></span>**severidade de ameaça de MP \_ \_ \_ desconhecida**</span><span class="sxs-lookup"><span data-stu-id="886dc-109"><span id="MP_THREAT_SEVERITY_UNKNOWN"></span><span id="mp_threat_severity_unknown"></span>**MP\_THREAT\_SEVERITY\_UNKNOWN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="886dc-110"><span id="MP_THREAT_SEVERITY_LOW"></span><span id="mp_threat_severity_low"></span>**severidade de ameaça de MP \_ \_ \_ baixa**</span><span class="sxs-lookup"><span data-stu-id="886dc-110"><span id="MP_THREAT_SEVERITY_LOW"></span><span id="mp_threat_severity_low"></span>**MP\_THREAT\_SEVERITY\_LOW**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="886dc-111"><span id="MP_THREAT_SEVERITY_MODERATE"></span><span id="mp_threat_severity_moderate"></span>**severidade de ameaça de MP \_ \_ \_ moderada**</span><span class="sxs-lookup"><span data-stu-id="886dc-111"><span id="MP_THREAT_SEVERITY_MODERATE"></span><span id="mp_threat_severity_moderate"></span>**MP\_THREAT\_SEVERITY\_MODERATE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="886dc-112"><span id="MP_THREAT_SEVERITY_HIGH"></span><span id="mp_threat_severity_high"></span>**\_ \_ severidade alta da ameaça MP \_**</span><span class="sxs-lookup"><span data-stu-id="886dc-112"><span id="MP_THREAT_SEVERITY_HIGH"></span><span id="mp_threat_severity_high"></span>**MP\_THREAT\_SEVERITY\_HIGH**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="886dc-113"><span id="MP_THREAT_SEVERITY_SEVERE"></span><span id="mp_threat_severity_severe"></span>**severidade de ameaça de MP \_ \_ \_ grave**</span><span class="sxs-lookup"><span data-stu-id="886dc-113"><span id="MP_THREAT_SEVERITY_SEVERE"></span><span id="mp_threat_severity_severe"></span>**MP\_THREAT\_SEVERITY\_SEVERE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="886dc-114"><span id="MP_THREAT_SEVERITY_MAXVALUE"></span><span id="mp_threat_severity_maxvalue"></span>**severidade da ameaça de MP \_ \_ \_ MaxValue**</span><span class="sxs-lookup"><span data-stu-id="886dc-114"><span id="MP_THREAT_SEVERITY_MAXVALUE"></span><span id="mp_threat_severity_maxvalue"></span>**MP\_THREAT\_SEVERITY\_MAXVALUE**</span></span>
<span data-ttu-id="886dc-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="886dc-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="886dc-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="886dc-116">Requirements</span></span>



| <span data-ttu-id="886dc-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="886dc-117">Requirement</span></span> | <span data-ttu-id="886dc-118">Valor</span><span class="sxs-lookup"><span data-stu-id="886dc-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="886dc-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="886dc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="886dc-120">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="886dc-120">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="886dc-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="886dc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="886dc-122">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="886dc-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="886dc-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="886dc-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="886dc-124"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="886dc-124"><dt>MpClient.h</dt></span></span> </dl> |



 

 





