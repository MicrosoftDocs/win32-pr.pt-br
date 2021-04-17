---
title: Enumeração de WMDRMNET_POLICY_TYPE (wmdrmsdk. h)
description: O \_ tipo de \_ enumeração tipo de política WMDRMNET lista os tipos de políticas que estão disponíveis para operações do Windows Media DRM para dispositivos de rede.
ms.assetid: 83e9e247-3bd8-4857-97b6-95b3cd5ad25c
keywords:
- Formato de mídia do Windows de enumeração de WMDRMNET_POLICY_TYPE
- Formato de mídia do Windows de enumeração
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_TYPE
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 964a3e938caa312f02f21074f046f3cf88d72de6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751306"
---
# <a name="wmdrmnet_policy_type-enumeration"></a><span data-ttu-id="006b0-105">Enumeração de tipo de \_ política WMDRMNET \_</span><span class="sxs-lookup"><span data-stu-id="006b0-105">WMDRMNET\_POLICY\_TYPE enumeration</span></span>

<span data-ttu-id="006b0-106">O tipo de enumeração **\_ \_ tipo de política WMDRMNET** lista os tipos de políticas que estão disponíveis para operações do Windows Media DRM para dispositivos de rede.</span><span class="sxs-lookup"><span data-stu-id="006b0-106">The **WMDRMNET\_POLICY\_TYPE** enumeration type lists the types of policies that are available for Windows Media DRM for Network Devices operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="006b0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="006b0-107">Syntax</span></span>


```C++
typedef enum WMDRMNET_POLICY_TYPE { 
  WMDRMNET_POLICY_TYPE_UNDEFINED       = 0x0000,
  WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY  = 0x0001
} ;
```



## <a name="constants"></a><span data-ttu-id="006b0-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="006b0-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="006b0-109"><span id="WMDRMNET_POLICY_TYPE_UNDEFINED"></span><span id="wmdrmnet_policy_type_undefined"></span>**\_tipo de política WMDRMNET \_ \_ indefinido**</span><span class="sxs-lookup"><span data-stu-id="006b0-109"><span id="WMDRMNET_POLICY_TYPE_UNDEFINED"></span><span id="wmdrmnet_policy_type_undefined"></span>**WMDRMNET\_POLICY\_TYPE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="006b0-110">Não há suporte para tipos de política indefinidos.</span><span class="sxs-lookup"><span data-stu-id="006b0-110">Undefined policy types are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="006b0-111"><span id="WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY"></span><span id="wmdrmnet_policy_type_transcryptplay"></span>**\_tipo de política WMDRMNET \_ \_ TRANSCRYPTPLAY**</span><span class="sxs-lookup"><span data-stu-id="006b0-111"><span id="WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY"></span><span id="wmdrmnet_policy_type_transcryptplay"></span>**WMDRMNET\_POLICY\_TYPE\_TRANSCRYPTPLAY**</span></span>
</dt> <dd>

<span data-ttu-id="006b0-112">A política rege a capacidade de converter o conteúdo protegido pelo Windows Media DRM em dados protegidos do Windows Media DRM para dispositivos de rede e reproduzi-los novamente em um dispositivo Networked.</span><span class="sxs-lookup"><span data-stu-id="006b0-112">The policy governs the ability to convert content protected by Windows Media DRM into protected Windows Media DRM for Network Devices data and play it back on a networked device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="006b0-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="006b0-113">Remarks</span></span>

<span data-ttu-id="006b0-114">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="006b0-114">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="006b0-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="006b0-115">Requirements</span></span>



| <span data-ttu-id="006b0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="006b0-116">Requirement</span></span> | <span data-ttu-id="006b0-117">Valor</span><span class="sxs-lookup"><span data-stu-id="006b0-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="006b0-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="006b0-118">Header</span></span><br/> | <dl> <span data-ttu-id="006b0-119"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="006b0-119"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="006b0-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="006b0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="006b0-121">**Tipos de enumeração**</span><span class="sxs-lookup"><span data-stu-id="006b0-121">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> <dt>

[<span data-ttu-id="006b0-122">**política de WMDRMNET \_**</span><span class="sxs-lookup"><span data-stu-id="006b0-122">**WMDRMNET\_POLICY**</span></span>](wmdrmnet-policy.md)
</dt> </dl>

 

 





