---
title: Enumeração de WINBIO_POLICY_SOURCE (WinBio \_ Types. h)
description: Lista as possíveis fontes de informações de política para a detecção de falsificação para fatores biométricos.
ms.assetid: 3DC3BB0B-1FD7-473C-8E0B-B7E0A4A44E9E
keywords:
- API de Windows Biometric Framework de enumeração de WINBIO_POLICY_SOURCE
- PWINBIO_POLICY_SOURCE Windows Biometric Framework API do ponteiro de enumeração
topic_type:
- apiref
api_name:
- WINBIO_POLICY_SOURCE
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866d1d82d939f143c4385caa5d94c68ffe3758f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295901"
---
# <a name="winbio_policy_source-enumeration"></a><span data-ttu-id="3c0df-105">Enumeração de origem de \_ política WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="3c0df-105">WINBIO\_POLICY\_SOURCE enumeration</span></span>

<span data-ttu-id="3c0df-106">Lista as possíveis fontes de informações de política para a detecção de falsificação para fatores biométricos.</span><span class="sxs-lookup"><span data-stu-id="3c0df-106">Lists the possible sources of policy information for the detection of spoofing for biometric factors.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c0df-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c0df-107">Syntax</span></span>


```C++
typedef enum _WINBIO_POLICY_SOURCE { 
  WINBIO_POLICY_UNKNOWN  = 0x00000000,
  WINBIO_POLICY_DEFAULT  = 0x00000001,
  WINBIO_POLICY_LOCAL    = 0x00000002,
  WINBIO_POLICY_ADMIN    = 0x00000003
} WINBIO_POLICY_SOURCE, *PWINBIO_POLICY_SOURCE;
```



## <a name="constants"></a><span data-ttu-id="3c0df-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="3c0df-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3c0df-109"><span id="WINBIO_POLICY_UNKNOWN"></span><span id="winbio_policy_unknown"></span>**política de WINBIO \_ \_ desconhecida**</span><span class="sxs-lookup"><span data-stu-id="3c0df-109"><span id="WINBIO_POLICY_UNKNOWN"></span><span id="winbio_policy_unknown"></span>**WINBIO\_POLICY\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="3c0df-110">A origem da política é desconhecida.</span><span class="sxs-lookup"><span data-stu-id="3c0df-110">The source of the policy is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="3c0df-111"><span id="WINBIO_POLICY_DEFAULT"></span><span id="winbio_policy_default"></span>**\_padrão de política WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="3c0df-111"><span id="WINBIO_POLICY_DEFAULT"></span><span id="winbio_policy_default"></span>**WINBIO\_POLICY\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="3c0df-112">A política é a política padrão que o Windows Biometric Framework fornece.</span><span class="sxs-lookup"><span data-stu-id="3c0df-112">The policy is the default policy that the Windows Biometric Framework provides.</span></span>

</dd> <dt>

<span data-ttu-id="3c0df-113"><span id="WINBIO_POLICY_LOCAL"></span><span id="winbio_policy_local"></span>**WINBIO \_ política \_ local**</span><span class="sxs-lookup"><span data-stu-id="3c0df-113"><span id="WINBIO_POLICY_LOCAL"></span><span id="winbio_policy_local"></span>**WINBIO\_POLICY\_LOCAL**</span></span>
</dt> <dd>

<span data-ttu-id="3c0df-114">A política que o usuário individual definiu para sua conta usando o aplicativo **configurações** .</span><span class="sxs-lookup"><span data-stu-id="3c0df-114">The policy that the individual user set for their account by using the **Settings** app.</span></span> <span data-ttu-id="3c0df-115">Essa política substitui a política padrão.</span><span class="sxs-lookup"><span data-stu-id="3c0df-115">This policy overrides the default policy.</span></span>

</dd> <dt>

<span data-ttu-id="3c0df-116"><span id="WINBIO_POLICY_ADMIN"></span><span id="winbio_policy_admin"></span>**\_administrador da política do WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="3c0df-116"><span id="WINBIO_POLICY_ADMIN"></span><span id="winbio_policy_admin"></span>**WINBIO\_POLICY\_ADMIN**</span></span>
</dt> <dd>

<span data-ttu-id="3c0df-117">Uma política de grupo que o administrador de ti definiu para a empresa.</span><span class="sxs-lookup"><span data-stu-id="3c0df-117">A group policy that the IT administrator set for the enterprise.</span></span> <span data-ttu-id="3c0df-118">Os usuários individuais não podem substituir essa política.</span><span class="sxs-lookup"><span data-stu-id="3c0df-118">Individual users cannot override this policy.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3c0df-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c0df-119">Requirements</span></span>



| <span data-ttu-id="3c0df-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c0df-120">Requirement</span></span> | <span data-ttu-id="3c0df-121">Valor</span><span class="sxs-lookup"><span data-stu-id="3c0df-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c0df-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c0df-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3c0df-123">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="3c0df-123">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="3c0df-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3c0df-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3c0df-125">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="3c0df-125">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="3c0df-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3c0df-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c0df-127"><dt>WinBio \_ Types. h (inclui WinBio. h para aplicativos cliente ou WinBio \_ Adapters. h para adaptadores)</dt></span><span class="sxs-lookup"><span data-stu-id="3c0df-127"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c0df-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="3c0df-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c0df-129">**\_ação da \_ política antifalsificação do \_ WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="3c0df-129">**WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION**</span></span>](winbio-anti-spoof-policy-action.md)
</dt> </dl>

 

 





