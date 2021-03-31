---
title: Enumeração de MPTHREAT_TYPE (MpClient. h)
description: Tipos de ameaça possíveis.
ms.assetid: 56061F12-AA89-4203-BED4-99613E24002A
keywords:
- Recursos do ambiente Windows herdado de enumeração de MPTHREAT_TYPE
- PMPTHREAT_TYPE recursos de ambiente herdados do ponteiro de enumeração do Windows
topic_type:
- apiref
api_name:
- MPTHREAT_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed823b100c91f259252d7cad71e554099caf6a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369490"
---
# <a name="mpthreat_type-enumeration"></a><span data-ttu-id="91bc4-105">\_Enumeração de tipo MPTHREAT</span><span class="sxs-lookup"><span data-stu-id="91bc4-105">MPTHREAT\_TYPE enumeration</span></span>

<span data-ttu-id="91bc4-106">Tipos de ameaça possíveis.</span><span class="sxs-lookup"><span data-stu-id="91bc4-106">Possible threat types.</span></span>

## <a name="syntax"></a><span data-ttu-id="91bc4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="91bc4-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_TYPE { 
  MPTHREAT_TYPE_KNOWNBAD   = 0,
  MPTHREAT_TYPE_BEHAVIOR   = 1,
  MPTHREAT_TYPE_UNKNOWN    = 2,
  MPTHREAT_TYPE_KNOWNGOOD  = 3,
  MPTHREAT_TYPE_NIS        = 4,
  MPTHREAT_TYPE_MAXVALUE   = 4
} MPTHREAT_TYPE, *PMPTHREAT_TYPE;
```



## <a name="constants"></a><span data-ttu-id="91bc4-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="91bc4-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="91bc4-109"><span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span>**MPTHREAT \_ tipo \_ KNOWNBAD**</span><span class="sxs-lookup"><span data-stu-id="91bc4-109"><span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span>**MPTHREAT\_TYPE\_KNOWNBAD**</span></span>
</dt> <dd>

<span data-ttu-id="91bc4-110">Ameaça inválida conhecida detectada por assinatura.</span><span class="sxs-lookup"><span data-stu-id="91bc4-110">Known bad threat detected via signature.</span></span>

</dd> <dt>

<span data-ttu-id="91bc4-111"><span id="MPTHREAT_TYPE_BEHAVIOR"></span><span id="mpthreat_type_behavior"></span>**\_comportamento do tipo MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="91bc4-111"><span id="MPTHREAT_TYPE_BEHAVIOR"></span><span id="mpthreat_type_behavior"></span>**MPTHREAT\_TYPE\_BEHAVIOR**</span></span>
</dt> <dd>

<span data-ttu-id="91bc4-112">Ameaça suspeita detectada por meio do monitoramento de comportamento.</span><span class="sxs-lookup"><span data-stu-id="91bc4-112">Suspicious threat detected via behavior monitoring.</span></span>

</dd> <dt>

<span data-ttu-id="91bc4-113"><span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span>**tipo de MPTHREAT \_ \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="91bc4-113"><span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span>**MPTHREAT\_TYPE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="91bc4-114">Ameaças desconhecidas (não classificadas).</span><span class="sxs-lookup"><span data-stu-id="91bc4-114">Unknown threats (unclassified).</span></span>

</dd> <dt>

<span data-ttu-id="91bc4-115"><span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span>**MPTHREAT \_ tipo \_ KNOWNGOOD**</span><span class="sxs-lookup"><span data-stu-id="91bc4-115"><span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span>**MPTHREAT\_TYPE\_KNOWNGOOD**</span></span>
</dt> <dd>

<span data-ttu-id="91bc4-116">Boa ameaça conhecida.</span><span class="sxs-lookup"><span data-stu-id="91bc4-116">Known good threat.</span></span>

</dd> <dt>

<span data-ttu-id="91bc4-117"><span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span>**MPTHREAT \_ tipo \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="91bc4-117"><span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span>**MPTHREAT\_TYPE\_NIS**</span></span>
</dt> <dd>

<span data-ttu-id="91bc4-118">Detecção de ameaças NIS.</span><span class="sxs-lookup"><span data-stu-id="91bc4-118">NIS threat detection.</span></span>

</dd> <dt>

<span data-ttu-id="91bc4-119"><span id="MPTHREAT_TYPE_MAXVALUE"></span><span id="mpthreat_type_maxvalue"></span>**tipo de MPTHREAT \_ \_ MaxValue**</span><span class="sxs-lookup"><span data-stu-id="91bc4-119"><span id="MPTHREAT_TYPE_MAXVALUE"></span><span id="mpthreat_type_maxvalue"></span>**MPTHREAT\_TYPE\_MAXVALUE**</span></span>
</dt> <dd>

<span data-ttu-id="91bc4-120">Valor máximo possível.</span><span class="sxs-lookup"><span data-stu-id="91bc4-120">Maximum value possible.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="91bc4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91bc4-121">Requirements</span></span>



| <span data-ttu-id="91bc4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="91bc4-122">Requirement</span></span> | <span data-ttu-id="91bc4-123">Valor</span><span class="sxs-lookup"><span data-stu-id="91bc4-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="91bc4-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91bc4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="91bc4-125">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="91bc4-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="91bc4-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="91bc4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="91bc4-127">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="91bc4-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="91bc4-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="91bc4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="91bc4-129"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="91bc4-129"><dt>MpClient.h</dt></span></span> </dl> |



 

 





