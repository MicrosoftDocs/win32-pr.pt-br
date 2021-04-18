---
title: Estrutura de WMDRMNET_POLICY_MINIMUM_ENVIRONMENT (wmdrmsdk. h)
description: A \_ estrutura de \_ ambiente mínima da política WMDRMNET \_ contém os requisitos mínimos de segurança para o Windows Media DRM para dispositivos de rede.
ms.assetid: b1bc9a8d-197e-45fe-a152-0b81add977eb
keywords:
- Formato de mídia do Windows de estrutura de WMDRMNET_POLICY_MINIMUM_ENVIRONMENT
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_MINIMUM_ENVIRONMENT
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf53fdec186a44eff375dd2e9cf9badfe0ba715
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105781410"
---
# <a name="wmdrmnet_policy_minimum_environment-structure"></a><span data-ttu-id="2f463-105">\_Estrutura de \_ ambiente mínima da política de WMDRMNET \_</span><span class="sxs-lookup"><span data-stu-id="2f463-105">WMDRMNET\_POLICY\_MINIMUM\_ENVIRONMENT structure</span></span>

<span data-ttu-id="2f463-106">A estrutura de **\_ \_ \_ ambiente mínima da política WMDRMNET** contém os requisitos mínimos de segurança para o Windows Media DRM para dispositivos de rede.</span><span class="sxs-lookup"><span data-stu-id="2f463-106">The **WMDRMNET\_POLICY\_MINIMUM\_ENVIRONMENT** structure contains the minimum security requirements for Windows Media DRM for Network Devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f463-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f463-107">Syntax</span></span>


```C++
typedef struct WMDRMNET_POLICY_MINIMUM_ENVIRONMENT {
  WORD  wMinimumSecurityLevel;
  DWORD dwMinimumAppRevocationListVersion;
  DWORD dwMinimumDeviceRevocationListVersion;
} ;
```



## <a name="members"></a><span data-ttu-id="2f463-108">Membros</span><span class="sxs-lookup"><span data-stu-id="2f463-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="2f463-109">**wMinimumSecurityLevel**</span><span class="sxs-lookup"><span data-stu-id="2f463-109">**wMinimumSecurityLevel**</span></span>
</dt> <dd>

<span data-ttu-id="2f463-110">Nível mínimo de segurança do aplicativo necessário.</span><span class="sxs-lookup"><span data-stu-id="2f463-110">Minimum application security level required.</span></span>

</dd> <dt>

<span data-ttu-id="2f463-111">**dwMinimumAppRevocationListVersion**</span><span class="sxs-lookup"><span data-stu-id="2f463-111">**dwMinimumAppRevocationListVersion**</span></span>
</dt> <dd>

<span data-ttu-id="2f463-112">A versão mínima da lista de certificados revogados do aplicativo é necessária.</span><span class="sxs-lookup"><span data-stu-id="2f463-112">Minimum application certificate revocation list version required.</span></span>

</dd> <dt>

<span data-ttu-id="2f463-113">**dwMinimumDeviceRevocationListVersion**</span><span class="sxs-lookup"><span data-stu-id="2f463-113">**dwMinimumDeviceRevocationListVersion**</span></span>
</dt> <dd>

<span data-ttu-id="2f463-114">Lista mínima de revogação de certificados de dispositivo necessária.</span><span class="sxs-lookup"><span data-stu-id="2f463-114">Minimum device certificate revocation list required.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2f463-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f463-115">Remarks</span></span>

<span data-ttu-id="2f463-116">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="2f463-116">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f463-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f463-117">Requirements</span></span>



| <span data-ttu-id="2f463-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f463-118">Requirement</span></span> | <span data-ttu-id="2f463-119">Valor</span><span class="sxs-lookup"><span data-stu-id="2f463-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f463-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2f463-120">Header</span></span><br/> | <dl> <span data-ttu-id="2f463-121"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f463-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f463-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f463-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f463-123">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="2f463-123">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="2f463-124">**política de WMDRMNET \_**</span><span class="sxs-lookup"><span data-stu-id="2f463-124">**WMDRMNET\_POLICY**</span></span>](wmdrmnet-policy.md)
</dt> </dl>

 

 





