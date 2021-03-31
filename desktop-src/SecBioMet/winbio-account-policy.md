---
title: Estrutura de WINBIO_ACCOUNT_POLICY ( \_ adaptador WINBIO. h)
description: Contém uma política de antifalsificação padrão ou específica da conta.
ms.assetid: 7098FC53-E487-42B2-8B4B-EB7E2D296CB6
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_ACCOUNT_POLICY
- Ponteiro de estrutura de PWINBIO_ACCOUNT_POLICY Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_ACCOUNT_POLICY
api_location:
- Winbio_adapter.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c734fa6d98615b7708a65ebad1dddc47cdc77cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918444"
---
# <a name="winbio_account_policy-structure"></a><span data-ttu-id="20643-105">Estrutura de política de \_ conta do WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="20643-105">WINBIO\_ACCOUNT\_POLICY structure</span></span>

<span data-ttu-id="20643-106">A estrutura de **\_ \_ política de conta do WINBIO** contém uma política de antifalsificação padrão ou específica da conta.</span><span class="sxs-lookup"><span data-stu-id="20643-106">The **WINBIO\_ACCOUNT\_POLICY** structure contains either a default or account-specific antispoofing policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="20643-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20643-107">Syntax</span></span>


```C++
typedef struct _WINBIO_ACCOUNT_POLICY {
  WINBIO_IDENTITY                 Identity;
  WINBIO_ANTI_SPOOF_POLICY_ACTION AntiSpoofBehavior;
} WINBIO_ACCOUNT_POLICY, *PWINBIO_ACCOUNT_POLICY;
```



## <a name="members"></a><span data-ttu-id="20643-108">Membros</span><span class="sxs-lookup"><span data-stu-id="20643-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="20643-109">**Identidade**</span><span class="sxs-lookup"><span data-stu-id="20643-109">**Identity**</span></span>
</dt> <dd>

<span data-ttu-id="20643-110">Uma estrutura de [**\_ identidade WINBIO**](winbio-identity.md) que especifica as informações da conta.</span><span class="sxs-lookup"><span data-stu-id="20643-110">A [**WINBIO\_IDENTITY**](winbio-identity.md) structure that specifies the account information.</span></span>

</dd> <dt>

<span data-ttu-id="20643-111">**AntiSpoofBehavior**</span><span class="sxs-lookup"><span data-stu-id="20643-111">**AntiSpoofBehavior**</span></span>
</dt> <dd>

<span data-ttu-id="20643-112">Um dos valores de enumeração da [**\_ \_ \_ \_ ação da política antifalsificação WINBIO**](winbio-anti-spoof-policy-action.md) que especifica qual ação de política de antifalsificação deve ser usada para a conta.</span><span class="sxs-lookup"><span data-stu-id="20643-112">One of the [**WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION**](winbio-anti-spoof-policy-action.md) enumeration values that specifies what antispoofing policy action to use for the account.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="20643-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="20643-113">Remarks</span></span>

<span data-ttu-id="20643-114">Consulte a discussão do método [**EngineAdapterSetAccountPolicy**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn) para obter uma descrição de como essa estrutura é usada.</span><span class="sxs-lookup"><span data-stu-id="20643-114">See the discussion of the [**EngineAdapterSetAccountPolicy**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn) method for a description of how this structure is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="20643-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="20643-115">Requirements</span></span>



| <span data-ttu-id="20643-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="20643-116">Requirement</span></span> | <span data-ttu-id="20643-117">Valor</span><span class="sxs-lookup"><span data-stu-id="20643-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20643-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20643-118">Minimum supported client</span></span><br/> | <span data-ttu-id="20643-119">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="20643-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="20643-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="20643-120">Minimum supported server</span></span><br/> | <span data-ttu-id="20643-121">\[Somente aplicativos da área de trabalho do Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="20643-121">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="20643-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="20643-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="20643-123"><dt>\_Adaptador WinBio. h (inclui o \_ adaptador WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="20643-123"><dt>Winbio\_adapter.h (include Winbio\_adapter.h)</dt></span></span> </dl> |



 

 





