---
title: Estrutura de WINBIO_ANTI_SPOOF_POLICY (WinBio \_ Types. h)
description: Representa a política de antifalsificação para um usuário.
ms.assetid: 2B433AE8-21A0-4AF1-853C-9074527DB2E4
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_ANTI_SPOOF_POLICY
- Ponteiro de estrutura de PWINBIO_ANTI_SPOOF_POLICY Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_ANTI_SPOOF_POLICY
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3da8b7811afb1de1ad464675125f125ef0ceab73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455407"
---
# <a name="winbio_anti_spoof_policy-structure"></a><span data-ttu-id="a38a3-105">\_Estrutura de \_ política antifalsificação do WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="a38a3-105">WINBIO\_ANTI\_SPOOF\_POLICY structure</span></span>

<span data-ttu-id="a38a3-106">Representa a política de antifalsificação para um usuário.</span><span class="sxs-lookup"><span data-stu-id="a38a3-106">Represents the antispoofing policy for a user.</span></span>

## <a name="syntax"></a><span data-ttu-id="a38a3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a38a3-107">Syntax</span></span>


```C++
typedef struct _WINBIO_ANTI_SPOOF_POLICY {
  WINBIO_ANTI_SPOOF_POLICY_ACTION Action;
  WINBIO_POLICY_SOURCE            Source;
} WINBIO_ANTI_SPOOF_POLICY, *PWINBIO_ANTI_SPOOF_POLICY;
```



## <a name="members"></a><span data-ttu-id="a38a3-108">Membros</span><span class="sxs-lookup"><span data-stu-id="a38a3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a38a3-109">**Ação**</span><span class="sxs-lookup"><span data-stu-id="a38a3-109">**Action**</span></span>
</dt> <dd>

<span data-ttu-id="a38a3-110">O tipo de ação a ser tomada para a política de antifalsificação.</span><span class="sxs-lookup"><span data-stu-id="a38a3-110">The type of action to take for the antispoofing policy.</span></span>

</dd> <dt>

<span data-ttu-id="a38a3-111">**Origem**</span><span class="sxs-lookup"><span data-stu-id="a38a3-111">**Source**</span></span>
</dt> <dd>

<span data-ttu-id="a38a3-112">A origem da política de antifalsificação.</span><span class="sxs-lookup"><span data-stu-id="a38a3-112">The source for the antispoofing policy.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a38a3-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a38a3-113">Requirements</span></span>



| <span data-ttu-id="a38a3-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a38a3-114">Requirement</span></span> | <span data-ttu-id="a38a3-115">Valor</span><span class="sxs-lookup"><span data-stu-id="a38a3-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a38a3-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a38a3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a38a3-117">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="a38a3-117">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="a38a3-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a38a3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a38a3-119">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="a38a3-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="a38a3-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a38a3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a38a3-121"><dt>WinBio \_ Types. h (inclui WinBio. h para aplicativos cliente ou WinBio \_ Adapters. h para adaptadores)</dt></span><span class="sxs-lookup"><span data-stu-id="a38a3-121"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a38a3-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="a38a3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a38a3-123">**\_ação da \_ política antifalsificação do \_ WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="a38a3-123">**WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION**</span></span>](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[<span data-ttu-id="a38a3-124">**\_origem da política de WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="a38a3-124">**WINBIO\_POLICY\_SOURCE**</span></span>](winbio-policy-source.md)
</dt> <dt>

[<span data-ttu-id="a38a3-125">**\_resultado assíncrono do WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="a38a3-125">**WINBIO\_ASYNC\_RESULT**</span></span>](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)
</dt> <dt>

[<span data-ttu-id="a38a3-126">**WinBioGetProperty**</span><span class="sxs-lookup"><span data-stu-id="a38a3-126">**WinBioGetProperty**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)
</dt> <dt>

[<span data-ttu-id="a38a3-127">**WinBioSetProperty**</span><span class="sxs-lookup"><span data-stu-id="a38a3-127">**WinBioSetProperty**</span></span>](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty)
</dt> </dl>

 

 





