---
title: Enumeração de WINBIO_ANTI_SPOOF_POLICY_ACTION (WinBio \_ Types. h)
description: Especifica os tipos de ações que você assume para a política de antifalsificação de um usuário.
ms.assetid: 846C0725-1796-49E4-883C-44AC7D618317
keywords:
- API de Windows Biometric Framework de enumeração de WINBIO_ANTI_SPOOF_POLICY_ACTION
- PWINBIO_ANTI_SPOOF_POLICY Windows Biometric Framework API do ponteiro de enumeração
topic_type:
- apiref
api_name:
- WINBIO_ANTI_SPOOF_POLICY_ACTION
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5905624bad252475cdde12c003f31a734e64dd2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918672"
---
# <a name="winbio_anti_spoof_policy_action-enumeration"></a><span data-ttu-id="e3068-105">\_Enumeração de \_ ação de política de antifalsificação WINBIO \_ \_</span><span class="sxs-lookup"><span data-stu-id="e3068-105">WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION enumeration</span></span>

<span data-ttu-id="e3068-106">Especifica os tipos de ações que você assume para a política de antifalsificação de um usuário.</span><span class="sxs-lookup"><span data-stu-id="e3068-106">Specifies the types of actions you take for the antispoofing policy of a user.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3068-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3068-107">Syntax</span></span>


```C++
typedef enum _WINBIO_ANTI_SPOOF_POLICY_ACTION { 
  WINBIO_ANTI_SPOOF_DISABLE  = 0x00000000,
  WINBIO_ANTI_SPOOF_ENABLE   = 0x00000001,
  WINBIO_ANTI_SPOOF_REMOVE   = 0x00000002
} WINBIO_ANTI_SPOOF_POLICY_ACTION, *PWINBIO_ANTI_SPOOF_POLICY;
```



## <a name="constants"></a><span data-ttu-id="e3068-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="e3068-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e3068-109"><span id="WINBIO_ANTI_SPOOF_DISABLE"></span><span id="winbio_anti_spoof_disable"></span>**\_ \_ desabilitar antifalsificação do WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="e3068-109"><span id="WINBIO_ANTI_SPOOF_DISABLE"></span><span id="winbio_anti_spoof_disable"></span>**WINBIO\_ANTI\_SPOOF\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="e3068-110">Desativa a detecção de falsificação para um fator biométrico.</span><span class="sxs-lookup"><span data-stu-id="e3068-110">Turns off the detection of spoofing for a biometric factor.</span></span>

</dd> <dt>

<span data-ttu-id="e3068-111"><span id="WINBIO_ANTI_SPOOF_ENABLE"></span><span id="winbio_anti_spoof_enable"></span>**\_ \_ habilitar antifalsificação do WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="e3068-111"><span id="WINBIO_ANTI_SPOOF_ENABLE"></span><span id="winbio_anti_spoof_enable"></span>**WINBIO\_ANTI\_SPOOF\_ENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="e3068-112">Ativa a detecção de falsificação para um fator biométrico.</span><span class="sxs-lookup"><span data-stu-id="e3068-112">Turns on the detection of spoofing for a biometric factor.</span></span>

</dd> <dt>

<span data-ttu-id="e3068-113"><span id="WINBIO_ANTI_SPOOF_REMOVE"></span><span id="winbio_anti_spoof_remove"></span>**\_remoção de \_ antifalsificação do WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="e3068-113"><span id="WINBIO_ANTI_SPOOF_REMOVE"></span><span id="winbio_anti_spoof_remove"></span>**WINBIO\_ANTI\_SPOOF\_REMOVE**</span></span>
</dt> <dd>

<span data-ttu-id="e3068-114">Remove toda a política antifalsificação para o fator biométrico da conta.</span><span class="sxs-lookup"><span data-stu-id="e3068-114">Removes the entire antispoofing policy for the biometric factor from the account.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e3068-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3068-115">Requirements</span></span>



| <span data-ttu-id="e3068-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3068-116">Requirement</span></span> | <span data-ttu-id="e3068-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e3068-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3068-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3068-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e3068-119">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e3068-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="e3068-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3068-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e3068-121">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="e3068-121">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="e3068-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e3068-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3068-123"><dt>WinBio \_ Types. h (inclui WinBio. h para aplicativos cliente ou WinBio \_ Adapters. h para adaptadores)</dt></span><span class="sxs-lookup"><span data-stu-id="e3068-123"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3068-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3068-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3068-125">**\_ação da \_ política antifalsificação do \_ WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="e3068-125">**WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION**</span></span>](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[<span data-ttu-id="e3068-126">**\_origem da política de WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="e3068-126">**WINBIO\_POLICY\_SOURCE**</span></span>](winbio-policy-source.md)
</dt> </dl>

 

 





