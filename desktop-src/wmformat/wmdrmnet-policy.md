---
title: Estrutura de WMDRMNET_POLICY (wmdrmsdk. h)
description: A \_ estrutura da política WMDRMNET contém a política a ser usada para operações do Windows Media DRM para dispositivos de rede.
ms.assetid: 11eaaeb2-3470-4f58-ae1c-53ee0f60bdce
keywords:
- Formato de mídia do Windows de estrutura de WMDRMNET_POLICY
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574e37a8c5ee7f68291012b86cda3a89e25949ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747274"
---
# <a name="wmdrmnet_policy-structure"></a><span data-ttu-id="d69d7-105">Estrutura de política do WMDRMNET \_</span><span class="sxs-lookup"><span data-stu-id="d69d7-105">WMDRMNET\_POLICY structure</span></span>

<span data-ttu-id="d69d7-106">A estrutura da **\_ política WMDRMNET** contém a política a ser usada para operações do Windows Media DRM para dispositivos de rede.</span><span class="sxs-lookup"><span data-stu-id="d69d7-106">The **WMDRMNET\_POLICY** structure contains the policy to be used for Windows Media DRM for Network Devices operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="d69d7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d69d7-107">Syntax</span></span>


```C++
typedef struct WMDRMNET_POLICY {
  WMDRMNET_POLICY_TYPE ePolicyType;
  BYTE                 *pbPolicy;
} ;
```



## <a name="members"></a><span data-ttu-id="d69d7-108">Membros</span><span class="sxs-lookup"><span data-stu-id="d69d7-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="d69d7-109">**ePolicyType**</span><span class="sxs-lookup"><span data-stu-id="d69d7-109">**ePolicyType**</span></span>
</dt> <dd>

<span data-ttu-id="d69d7-110">Membro da enumeração [**de \_ \_ tipo de política WMDRMNET**](wmdrmnet-policy-type.md) que especifica o tipo de política.</span><span class="sxs-lookup"><span data-stu-id="d69d7-110">Member of the [**WMDRMNET\_POLICY\_TYPE**](wmdrmnet-policy-type.md) enumeration that specifies the type of policy.</span></span>

</dd> <dt>

<span data-ttu-id="d69d7-111">**pbPolicy**</span><span class="sxs-lookup"><span data-stu-id="d69d7-111">**pbPolicy**</span></span>
</dt> <dd>

<span data-ttu-id="d69d7-112">Buffer que contém a política.</span><span class="sxs-lookup"><span data-stu-id="d69d7-112">Buffer containing the policy.</span></span> <span data-ttu-id="d69d7-113">O único tipo de política com suporte no momento é o **\_ tipo de política WMDRMNET \_ \_ TRANSCRYPTPLAY**.</span><span class="sxs-lookup"><span data-stu-id="d69d7-113">The only type of policy currently supported is **WMDRMNET\_POLICY\_TYPE\_TRANSCRYPTPLAY**.</span></span> <span data-ttu-id="d69d7-114">Este membro é um ponteiro para uma **estrutura \_ \_ TRANSCRYPTPLAY da política WMDRMNET** .</span><span class="sxs-lookup"><span data-stu-id="d69d7-114">This member is a pointer to a **WMDRMNET\_POLICY\_TRANSCRYPTPLAY** structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d69d7-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d69d7-115">Remarks</span></span>

<span data-ttu-id="d69d7-116">Essa estrutura é usada como um parâmetro para o método [**IWMDRMNetTransmitter:: GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="d69d7-116">This structure is used as a parameter for the [**IWMDRMNetTransmitter::GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d69d7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d69d7-117">Requirements</span></span>



| <span data-ttu-id="d69d7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d69d7-118">Requirement</span></span> | <span data-ttu-id="d69d7-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d69d7-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d69d7-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d69d7-120">Header</span></span><br/> | <dl> <span data-ttu-id="d69d7-121"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="d69d7-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d69d7-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="d69d7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d69d7-123">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="d69d7-123">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="d69d7-124">**\_ \_ requisitos globais da política de WMDRMNET \_**</span><span class="sxs-lookup"><span data-stu-id="d69d7-124">**WMDRMNET\_POLICY\_GLOBAL\_REQUIREMENTS**</span></span>](wmdrmnet-policy-global-requirements.md)
</dt> <dt>

[<span data-ttu-id="d69d7-125">**\_ \_ ambiente mínimo da política de WMDRMNET \_**</span><span class="sxs-lookup"><span data-stu-id="d69d7-125">**WMDRMNET\_POLICY\_MINIMUM\_ENVIRONMENT**</span></span>](wmdrmnet-policy-minimum-environment.md)
</dt> <dt>

[<span data-ttu-id="d69d7-126">**política de WMDRMNET \_ \_ TRANSCRYPTPLAY**</span><span class="sxs-lookup"><span data-stu-id="d69d7-126">**WMDRMNET\_POLICY\_TRANSCRYPTPLAY**</span></span>](wmdrmnet-policy-transcryptplay.md)
</dt> <dt>

[<span data-ttu-id="d69d7-127">**\_tipo de política WMDRMNET \_**</span><span class="sxs-lookup"><span data-stu-id="d69d7-127">**WMDRMNET\_POLICY\_TYPE**</span></span>](wmdrmnet-policy-type.md)
</dt> </dl>

 

 





