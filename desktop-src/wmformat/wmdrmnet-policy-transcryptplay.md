---
title: Estrutura de WMDRMNET_POLICY_TRANSCRYPTPLAY (wmdrmsdk. h)
description: A \_ estrutura TRANSCRYPTPLAY da política WMDRMNET \_ contém as informações de política para reproduzir conteúdo usando o Windows Media DRM para dispositivos de rede.
ms.assetid: 95671c58-a593-40bb-856e-28ad1cba340e
keywords:
- Formato de mídia do Windows de estrutura de WMDRMNET_POLICY_TRANSCRYPTPLAY
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_TRANSCRYPTPLAY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0681251428b87b323c9ad3e73277ec8cdd2b95f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747225"
---
# <a name="wmdrmnet_policy_transcryptplay-structure"></a><span data-ttu-id="706c7-105">\_Estrutura TRANSCRYPTPLAY da política de WMDRMNET \_</span><span class="sxs-lookup"><span data-stu-id="706c7-105">WMDRMNET\_POLICY\_TRANSCRYPTPLAY structure</span></span>

<span data-ttu-id="706c7-106">A **estrutura \_ \_ TRANSCRYPTPLAY da política WMDRMNET** contém as informações de política para reproduzir conteúdo usando o Windows Media DRM para dispositivos de rede.</span><span class="sxs-lookup"><span data-stu-id="706c7-106">The **WMDRMNET\_POLICY\_TRANSCRYPTPLAY** structure holds the policy information for playing content using Windows Media DRM for Network Devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="706c7-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="706c7-107">Syntax</span></span>


```C++
typedef struct WMDRMNET_POLICY_TRANSCRYPTPLAY {
  WMDRMNET_POLICY_GLOBAL_REQUIREMENTS globals;
  WMDRMNET_POLICY_PLAY_OPL            playOPLs;
} ;
```



## <a name="members"></a><span data-ttu-id="706c7-108">Membros</span><span class="sxs-lookup"><span data-stu-id="706c7-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="706c7-109">**Globals**</span><span class="sxs-lookup"><span data-stu-id="706c7-109">**globals**</span></span>
</dt> <dd>

<span data-ttu-id="706c7-110">Estrutura de política global.</span><span class="sxs-lookup"><span data-stu-id="706c7-110">Global policy structure.</span></span>

</dd> <dt>

<span data-ttu-id="706c7-111">**playOPLs**</span><span class="sxs-lookup"><span data-stu-id="706c7-111">**playOPLs**</span></span>
</dt> <dd>

<span data-ttu-id="706c7-112">Níveis de proteção de saída para reprodução.</span><span class="sxs-lookup"><span data-stu-id="706c7-112">Output protection levels for playback.</span></span> <span data-ttu-id="706c7-113">**WMDRMNET \_ A \_ reprodução \_ de política OPL** é um tipo definido como [**DRM \_ Play \_ OPL \_ ex**](drm-play-opl-ex.md).</span><span class="sxs-lookup"><span data-stu-id="706c7-113">**WMDRMNET\_POLICY\_PLAY\_OPL** is a type defined as [**DRM\_PLAY\_OPL\_EX**](drm-play-opl-ex.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="706c7-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="706c7-114">Remarks</span></span>

<span data-ttu-id="706c7-115">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="706c7-115">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="706c7-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="706c7-116">Requirements</span></span>



| <span data-ttu-id="706c7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="706c7-117">Requirement</span></span> | <span data-ttu-id="706c7-118">Valor</span><span class="sxs-lookup"><span data-stu-id="706c7-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="706c7-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="706c7-119">Header</span></span><br/> | <dl> <span data-ttu-id="706c7-120"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="706c7-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="706c7-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="706c7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="706c7-122">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="706c7-122">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="706c7-123">**política de WMDRMNET \_**</span><span class="sxs-lookup"><span data-stu-id="706c7-123">**WMDRMNET\_POLICY**</span></span>](wmdrmnet-policy.md)
</dt> </dl>

 

 





