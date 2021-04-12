---
title: Enumeração de MP_SIGNATURE_TYPE (MpClient. h)
description: Tipos de assinatura possíveis.
ms.assetid: 44B195A8-866D-4B87-9576-54E00658F9B3
keywords:
- Recursos do ambiente Windows herdado de enumeração de MP_SIGNATURE_TYPE
- PMP_SIGNATURE_TYPE recursos de ambiente herdados do ponteiro de enumeração do Windows
topic_type:
- apiref
api_name:
- MP_SIGNATURE_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b99f7140706e9a6d3fa32e7eb346ef6478f3f26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455075"
---
# <a name="mp_signature_type-enumeration"></a><span data-ttu-id="a59c2-105">Enumeração de tipo de \_ assinatura MP \_</span><span class="sxs-lookup"><span data-stu-id="a59c2-105">MP\_SIGNATURE\_TYPE enumeration</span></span>

<span data-ttu-id="a59c2-106">Tipos de assinatura possíveis.</span><span class="sxs-lookup"><span data-stu-id="a59c2-106">Possible signature types.</span></span>

## <a name="syntax"></a><span data-ttu-id="a59c2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a59c2-107">Syntax</span></span>


```C++
typedef enum tagMP_SIGNATURE_TYPE { 
  MP_SIGNATURE_ANTIMALWARE     = 0,
  MP_SIGNATURE_ANTIVIRUS       = 1,
  MP_SIGNATURE_ANTISPYWARE     = 2,
  MP_SIGNATURE_NIS             = 3,
  MP_SIGNATURE_TYPES_MAXVALUE  = 3
} MP_SIGNATURE_TYPE, *PMP_SIGNATURE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="a59c2-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="a59c2-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a59c2-109"><span id="MP_SIGNATURE_ANTIMALWARE"></span><span id="mp_signature_antimalware"></span>**AntiMalware de \_ assinatura MP \_**</span><span class="sxs-lookup"><span data-stu-id="a59c2-109"><span id="MP_SIGNATURE_ANTIMALWARE"></span><span id="mp_signature_antimalware"></span>**MP\_SIGNATURE\_ANTIMALWARE**</span></span>
</dt> <dd>

<span data-ttu-id="a59c2-110">Assinaturas antivírus e antispyware.</span><span class="sxs-lookup"><span data-stu-id="a59c2-110">Both antivirus and antispyware signatures.</span></span>

</dd> <dt>

<span data-ttu-id="a59c2-111"><span id="MP_SIGNATURE_ANTIVIRUS"></span><span id="mp_signature_antivirus"></span>**\_antivírus de assinatura MP \_**</span><span class="sxs-lookup"><span data-stu-id="a59c2-111"><span id="MP_SIGNATURE_ANTIVIRUS"></span><span id="mp_signature_antivirus"></span>**MP\_SIGNATURE\_ANTIVIRUS**</span></span>
</dt> <dd>

<span data-ttu-id="a59c2-112">Somente assinaturas de antivírus.</span><span class="sxs-lookup"><span data-stu-id="a59c2-112">Only antivirus signatures.</span></span>

</dd> <dt>

<span data-ttu-id="a59c2-113"><span id="MP_SIGNATURE_ANTISPYWARE"></span><span id="mp_signature_antispyware"></span>**ANTI-SPYWARE de \_ assinatura MP \_**</span><span class="sxs-lookup"><span data-stu-id="a59c2-113"><span id="MP_SIGNATURE_ANTISPYWARE"></span><span id="mp_signature_antispyware"></span>**MP\_SIGNATURE\_ANTISPYWARE**</span></span>
</dt> <dd>

<span data-ttu-id="a59c2-114">Somente assinaturas de AntiSpyware.</span><span class="sxs-lookup"><span data-stu-id="a59c2-114">Only antispyware signatures.</span></span>

</dd> <dt>

<span data-ttu-id="a59c2-115"><span id="MP_SIGNATURE_NIS"></span><span id="mp_signature_nis"></span>**\_NIS de assinatura do MP \_**</span><span class="sxs-lookup"><span data-stu-id="a59c2-115"><span id="MP_SIGNATURE_NIS"></span><span id="mp_signature_nis"></span>**MP\_SIGNATURE\_NIS**</span></span>
</dt> <dd>

<span data-ttu-id="a59c2-116">Assinaturas NIS.</span><span class="sxs-lookup"><span data-stu-id="a59c2-116">NIS signatures.</span></span>

</dd> <dt>

<span data-ttu-id="a59c2-117"><span id="MP_SIGNATURE_TYPES_MAXVALUE"></span><span id="mp_signature_types_maxvalue"></span>**tipos de assinatura do MP \_ \_ \_ MaxValue**</span><span class="sxs-lookup"><span data-stu-id="a59c2-117"><span id="MP_SIGNATURE_TYPES_MAXVALUE"></span><span id="mp_signature_types_maxvalue"></span>**MP\_SIGNATURE\_TYPES\_MAXVALUE**</span></span>
<span data-ttu-id="a59c2-118"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a59c2-118"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="a59c2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a59c2-119">Requirements</span></span>



| <span data-ttu-id="a59c2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="a59c2-120">Requirement</span></span> | <span data-ttu-id="a59c2-121">Valor</span><span class="sxs-lookup"><span data-stu-id="a59c2-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a59c2-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a59c2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a59c2-123">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a59c2-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a59c2-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a59c2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a59c2-125">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a59c2-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a59c2-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a59c2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="a59c2-127"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="a59c2-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





