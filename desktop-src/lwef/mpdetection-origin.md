---
title: Enumeração de MPDETECTION_ORIGIN (MpClient. h)
description: Origem da detecção.
ms.assetid: 9FEE2FAD-3E44-4134-B968-53E971F6B092
keywords:
- Recursos do ambiente Windows herdado de enumeração de MPDETECTION_ORIGIN
- PMPDETECTION_ORIGIN recursos de ambiente herdados do ponteiro de enumeração do Windows
topic_type:
- apiref
api_name:
- MPDETECTION_ORIGIN
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4224aafef2c72db2a8d3b27f338ca83feaf64f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105771734"
---
# <a name="mpdetection_origin-enumeration"></a><span data-ttu-id="63749-105">\_Enumeração de origem MPDETECTION</span><span class="sxs-lookup"><span data-stu-id="63749-105">MPDETECTION\_ORIGIN enumeration</span></span>

<span data-ttu-id="63749-106">Origem da detecção.</span><span class="sxs-lookup"><span data-stu-id="63749-106">Detection origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="63749-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="63749-107">Syntax</span></span>


```C++
typedef enum tagMPDETECTION_ORIGIN { 
  MPDETECTION_ORIGIN_UNKNOWN        = 0,
  MPDETECTION_ORIGIN_LOCAL_MACHINE  = 1 << 0,
  MPDETECTION_ORIGIN_NETWORKSHARE   = 1 << 1,
  MPDETECTION_ORIGIN_INTERNET       = 1 << 2,
  MPDETECTION_ORIGIN_OUTBOUND       = 1 << 3,
  MPDETECTION_ORIGIN_INBOUND        = 1 << 4
} MPDETECTION_ORIGIN, *PMPDETECTION_ORIGIN;
```



## <a name="constants"></a><span data-ttu-id="63749-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="63749-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="63749-109"><span id="MPDETECTION_ORIGIN_UNKNOWN"></span><span id="mpdetection_origin_unknown"></span>**\_origem MPDETECTION \_ desconhecida**</span><span class="sxs-lookup"><span data-stu-id="63749-109"><span id="MPDETECTION_ORIGIN_UNKNOWN"></span><span id="mpdetection_origin_unknown"></span>**MPDETECTION\_ORIGIN\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="63749-110">A origem detectada era desconhecida.</span><span class="sxs-lookup"><span data-stu-id="63749-110">Threat detected origin unknown.</span></span>

</dd> <dt>

<span data-ttu-id="63749-111"><span id="MPDETECTION_ORIGIN_LOCAL_MACHINE"></span><span id="mpdetection_origin_local_machine"></span>**\_ \_ máquina local de origem do MPDETECTION \_**</span><span class="sxs-lookup"><span data-stu-id="63749-111"><span id="MPDETECTION_ORIGIN_LOCAL_MACHINE"></span><span id="mpdetection_origin_local_machine"></span>**MPDETECTION\_ORIGIN\_LOCAL\_MACHINE**</span></span>
</dt> <dd>

<span data-ttu-id="63749-112">Ameaça detectada no computador local.</span><span class="sxs-lookup"><span data-stu-id="63749-112">Threat detected on local machine.</span></span>

</dd> <dt>

<span data-ttu-id="63749-113"><span id="MPDETECTION_ORIGIN_NETWORKSHARE"></span><span id="mpdetection_origin_networkshare"></span>**MPDETECTION \_ Origin \_ NETWORKSHARE**</span><span class="sxs-lookup"><span data-stu-id="63749-113"><span id="MPDETECTION_ORIGIN_NETWORKSHARE"></span><span id="mpdetection_origin_networkshare"></span>**MPDETECTION\_ORIGIN\_NETWORKSHARE**</span></span>
</dt> <dd>

<span data-ttu-id="63749-114">Ameaça detectada no compartilhamento de rede.</span><span class="sxs-lookup"><span data-stu-id="63749-114">Threat detected on network share.</span></span>

</dd> <dt>

<span data-ttu-id="63749-115"><span id="MPDETECTION_ORIGIN_INTERNET"></span><span id="mpdetection_origin_internet"></span>**\_Internet de origem MPDETECTION \_**</span><span class="sxs-lookup"><span data-stu-id="63749-115"><span id="MPDETECTION_ORIGIN_INTERNET"></span><span id="mpdetection_origin_internet"></span>**MPDETECTION\_ORIGIN\_INTERNET**</span></span>
</dt> <dd>

<span data-ttu-id="63749-116">Ameaça detectada na Internet.</span><span class="sxs-lookup"><span data-stu-id="63749-116">Threat detected on internet.</span></span>

</dd> <dt>

<span data-ttu-id="63749-117"><span id="MPDETECTION_ORIGIN_OUTBOUND"></span><span id="mpdetection_origin_outbound"></span>**\_saída de origem MPDETECTION \_**</span><span class="sxs-lookup"><span data-stu-id="63749-117"><span id="MPDETECTION_ORIGIN_OUTBOUND"></span><span id="mpdetection_origin_outbound"></span>**MPDETECTION\_ORIGIN\_OUTBOUND**</span></span>
</dt> <dd>

<span data-ttu-id="63749-118">Ameaça detectada em uma conexão de saída.</span><span class="sxs-lookup"><span data-stu-id="63749-118">Threat detected on an outbound connection.</span></span>

</dd> <dt>

<span data-ttu-id="63749-119"><span id="MPDETECTION_ORIGIN_INBOUND"></span><span id="mpdetection_origin_inbound"></span>**\_entrada de origem MPDETECTION \_**</span><span class="sxs-lookup"><span data-stu-id="63749-119"><span id="MPDETECTION_ORIGIN_INBOUND"></span><span id="mpdetection_origin_inbound"></span>**MPDETECTION\_ORIGIN\_INBOUND**</span></span>
</dt> <dd>

<span data-ttu-id="63749-120">Ameaça detectada em uma conexão de entrada.</span><span class="sxs-lookup"><span data-stu-id="63749-120">Threat detected on an inbound connection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="63749-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63749-121">Requirements</span></span>



| <span data-ttu-id="63749-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="63749-122">Requirement</span></span> | <span data-ttu-id="63749-123">Valor</span><span class="sxs-lookup"><span data-stu-id="63749-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63749-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63749-124">Minimum supported client</span></span><br/> | <span data-ttu-id="63749-125">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="63749-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="63749-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="63749-126">Minimum supported server</span></span><br/> | <span data-ttu-id="63749-127">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="63749-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="63749-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="63749-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="63749-129"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="63749-129"><dt>MpClient.h</dt></span></span> </dl> |



 

 





