---
title: Estrutura de DRM_COPY_OPL (wmdrmsdk. h)
description: A \_ estrutura OPL de cópia do DRM \_ contém informações sobre os níveis de proteção de saída (OPLs) especificados em uma licença para ações de cópia.
ms.assetid: 439cbd56-05c1-46f8-86b9-ac1341902a40
keywords:
- Formato de mídia do Windows de estrutura de DRM_COPY_OPL
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_COPY_OPL
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28655e220588bb704567de033e1117dd569d3ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782690"
---
# <a name="drm_copy_opl-structure"></a><span data-ttu-id="39787-105">\_Estrutura OPL de cópia DRM \_</span><span class="sxs-lookup"><span data-stu-id="39787-105">DRM\_COPY\_OPL structure</span></span>

<span data-ttu-id="39787-106">A **estrutura \_ \_ OPL de cópia do DRM** contém informações sobre os níveis de proteção de saída (OPLs) especificados em uma licença para ações de cópia.</span><span class="sxs-lookup"><span data-stu-id="39787-106">The **DRM\_COPY\_OPL** structure holds information about the output protection levels (OPLs) specified in a license for copy actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="39787-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39787-107">Syntax</span></span>


```C++
typedef struct DRM_COPY_OPL {
  WORD               wMinimumCopyLevel;
  DRM_OPL_OUTPUT_IDS oplIdIncludes;
  DRM_OPL_OUTPUT_IDS oplIdExcludes;
} ;
```



## <a name="members"></a><span data-ttu-id="39787-108">Membros</span><span class="sxs-lookup"><span data-stu-id="39787-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="39787-109">**wMinimumCopyLevel**</span><span class="sxs-lookup"><span data-stu-id="39787-109">**wMinimumCopyLevel**</span></span>
</dt> <dd>

<span data-ttu-id="39787-110">OPL mínimo para ações de cópia.</span><span class="sxs-lookup"><span data-stu-id="39787-110">Minimum OPL for copy actions.</span></span>

</dd> <dt>

<span data-ttu-id="39787-111">**oplIdIncludes**</span><span class="sxs-lookup"><span data-stu-id="39787-111">**oplIdIncludes**</span></span>
</dt> <dd>

<span data-ttu-id="39787-112">[**DRM \_ OPL \_ \_**](drmdrm-opl-output-ids.md) a estrutura de IDs de saída que contém os identificadores de tecnologias a permitir.</span><span class="sxs-lookup"><span data-stu-id="39787-112">[**DRM\_OPL\_OUTPUT\_IDS**](drmdrm-opl-output-ids.md) structure containing the identifiers of technologies to allow.</span></span> <span data-ttu-id="39787-113">Esse membro é usado para tecnologias de saída atribuídas OPLs menor do que o nível de cópia mínimo, mas para o qual o conteúdo pode ser copiado.</span><span class="sxs-lookup"><span data-stu-id="39787-113">This member is used for output technologies that are assigned OPLs lower than the minimum copy level, but to which the content may be copied.</span></span>

</dd> <dt>

<span data-ttu-id="39787-114">**oplIdExcludes**</span><span class="sxs-lookup"><span data-stu-id="39787-114">**oplIdExcludes**</span></span>
</dt> <dd>

<span data-ttu-id="39787-115">[**DRM \_ OPL \_ \_**](drmdrm-opl-output-ids.md) a estrutura de IDs de saída que contém os identificadores de saída de tecnologias para restringir.</span><span class="sxs-lookup"><span data-stu-id="39787-115">[**DRM\_OPL\_OUTPUT\_IDS**](drmdrm-opl-output-ids.md) structure containing the output identifiers of technologies to restrict.</span></span> <span data-ttu-id="39787-116">Esse membro é usado para tecnologias de saída que recebem OPLs que excedem o nível de cópia mínimo, mas que o emissor da licença não concede direitos para copiar para o.</span><span class="sxs-lookup"><span data-stu-id="39787-116">This member is used for output technologies that are assigned OPLs that exceed the minimum copy level, but that the license issuer does not grant rights for copying to.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="39787-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39787-117">Requirements</span></span>



| <span data-ttu-id="39787-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="39787-118">Requirement</span></span> | <span data-ttu-id="39787-119">Valor</span><span class="sxs-lookup"><span data-stu-id="39787-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39787-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="39787-120">Header</span></span><br/> | <dl> <span data-ttu-id="39787-121"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="39787-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39787-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="39787-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39787-123">**\_OPL de reprodução DRM \_**</span><span class="sxs-lookup"><span data-stu-id="39787-123">**DRM\_PLAY\_OPL**</span></span>](drmdrm-play-opl.md)
</dt> <dt>

[<span data-ttu-id="39787-124">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="39787-124">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





