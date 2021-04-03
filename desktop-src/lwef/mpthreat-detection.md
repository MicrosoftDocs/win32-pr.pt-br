---
title: Enumeração de MPTHREAT_DETECTION (MpClient. h)
description: Possíveis tipos conhecidos de detecção de ameaças inválidas.
ms.assetid: 14FCA9BD-A9A1-488B-B8E8-88DE0DF18F27
keywords:
- Recursos do ambiente Windows herdado de enumeração de MPTHREAT_DETECTION
- PMPTHREAT_DETECTION recursos de ambiente herdados do ponteiro de enumeração do Windows
topic_type:
- apiref
api_name:
- MPTHREAT_DETECTION
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86edc0e1ca4ee130f2a2a4a678447771f1ae40ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644526"
---
# <a name="mpthreat_detection-enumeration"></a><span data-ttu-id="7be83-105">Enumeração de detecção de MPTHREAT \_</span><span class="sxs-lookup"><span data-stu-id="7be83-105">MPTHREAT\_DETECTION enumeration</span></span>

<span data-ttu-id="7be83-106">Possíveis tipos conhecidos de detecção de ameaças inválidas.</span><span class="sxs-lookup"><span data-stu-id="7be83-106">Possible known bad threat detection types.</span></span>

## <a name="syntax"></a><span data-ttu-id="7be83-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7be83-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_DETECTION { 
  MP_THREAT_DETECTION_CONCRETE    = 0,
  MP_THREAT_DETECTION_HEURISTIC   = 1,
  MP_THREAT_DETECTION_GENERIC     = 2,
  MP_THREAT_DETECTION_SUSPICIOUS  = 4,
  MP_THREAT_DETECTION_FASTPATH    = 8
} MPTHREAT_DETECTION, *PMPTHREAT_DETECTION;
```



## <a name="constants"></a><span data-ttu-id="7be83-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="7be83-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="7be83-109"><span id="MP_THREAT_DETECTION_CONCRETE"></span><span id="mp_threat_detection_concrete"></span>**\_ \_ concreta detecção de ameaças do MP \_**</span><span class="sxs-lookup"><span data-stu-id="7be83-109"><span id="MP_THREAT_DETECTION_CONCRETE"></span><span id="mp_threat_detection_concrete"></span>**MP\_THREAT\_DETECTION\_CONCRETE**</span></span>
</dt> <dd>

<span data-ttu-id="7be83-110">A ameaça foi detectada por meio de assinaturas concretas.</span><span class="sxs-lookup"><span data-stu-id="7be83-110">Threat was detected via concrete signatures.</span></span>

</dd> <dt>

<span data-ttu-id="7be83-111"><span id="MP_THREAT_DETECTION_HEURISTIC"></span><span id="mp_threat_detection_heuristic"></span>**\_heurística de \_ detecção de ameaças MP \_**</span><span class="sxs-lookup"><span data-stu-id="7be83-111"><span id="MP_THREAT_DETECTION_HEURISTIC"></span><span id="mp_threat_detection_heuristic"></span>**MP\_THREAT\_DETECTION\_HEURISTIC**</span></span>
</dt> <dd>

<span data-ttu-id="7be83-112">A ameaça foi detectada por meio de heurística.</span><span class="sxs-lookup"><span data-stu-id="7be83-112">Threat was detected via heuristic.</span></span>

</dd> <dt>

<span data-ttu-id="7be83-113"><span id="MP_THREAT_DETECTION_GENERIC"></span><span id="mp_threat_detection_generic"></span>**detecção de ameaças do MP \_ \_ \_ genérica**</span><span class="sxs-lookup"><span data-stu-id="7be83-113"><span id="MP_THREAT_DETECTION_GENERIC"></span><span id="mp_threat_detection_generic"></span>**MP\_THREAT\_DETECTION\_GENERIC**</span></span>
</dt> <dd>

<span data-ttu-id="7be83-114">A ameaça foi detectada por meio de assinaturas genéricas.</span><span class="sxs-lookup"><span data-stu-id="7be83-114">Threat was detected via generic signatures.</span></span>

</dd> <dt>

<span data-ttu-id="7be83-115"><span id="MP_THREAT_DETECTION_SUSPICIOUS"></span><span id="mp_threat_detection_suspicious"></span>**detecção de ameaças do MP \_ \_ \_ suspeita**</span><span class="sxs-lookup"><span data-stu-id="7be83-115"><span id="MP_THREAT_DETECTION_SUSPICIOUS"></span><span id="mp_threat_detection_suspicious"></span>**MP\_THREAT\_DETECTION\_SUSPICIOUS**</span></span>
</dt> <dd>

<span data-ttu-id="7be83-116">A ameaça foi detectada por meio do monitoramento de comportamento.</span><span class="sxs-lookup"><span data-stu-id="7be83-116">Threat was detected via behavior monitoring.</span></span>

</dd> <dt>

<span data-ttu-id="7be83-117"><span id="MP_THREAT_DETECTION_FASTPATH"></span><span id="mp_threat_detection_fastpath"></span>**\_FASTPATH de \_ detecção de ameaças MP \_**</span><span class="sxs-lookup"><span data-stu-id="7be83-117"><span id="MP_THREAT_DETECTION_FASTPATH"></span><span id="mp_threat_detection_fastpath"></span>**MP\_THREAT\_DETECTION\_FASTPATH**</span></span>
</dt> <dd>

<span data-ttu-id="7be83-118">A ameaça foi detectada via FastPath.</span><span class="sxs-lookup"><span data-stu-id="7be83-118">Threat was detected via fastpath.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7be83-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7be83-119">Requirements</span></span>



| <span data-ttu-id="7be83-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="7be83-120">Requirement</span></span> | <span data-ttu-id="7be83-121">Valor</span><span class="sxs-lookup"><span data-stu-id="7be83-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7be83-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7be83-122">Minimum supported client</span></span><br/> | <span data-ttu-id="7be83-123">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7be83-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="7be83-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7be83-124">Minimum supported server</span></span><br/> | <span data-ttu-id="7be83-125">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7be83-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7be83-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7be83-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="7be83-127"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="7be83-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





