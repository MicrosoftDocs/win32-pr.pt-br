---
title: Estrutura de DRM_PLAY_OPL (wmdrmsdk. h)
description: A \_ estrutura OPL de reprodução do DRM \_ contém informações sobre os níveis de proteção de saída (OPLs) especificados em uma licença para ações de reprodução.
ms.assetid: 10703893-630c-4cbe-a0b0-d2890905daba
keywords:
- Formato de mídia do Windows de estrutura de DRM_PLAY_OPL
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_PLAY_OPL
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a40d8fe4e8b3c820f9d7bcb405b5c0806040182
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810655"
---
# <a name="drm_play_opl-structure"></a><span data-ttu-id="e2ed3-105">\_Estrutura OPL de reprodução DRM \_</span><span class="sxs-lookup"><span data-stu-id="e2ed3-105">DRM\_PLAY\_OPL structure</span></span>

<span data-ttu-id="e2ed3-106">A **estrutura \_ \_ OPL de reprodução do DRM** contém informações sobre os níveis de proteção de saída (OPLs) especificados em uma licença para ações de reprodução.</span><span class="sxs-lookup"><span data-stu-id="e2ed3-106">The **DRM\_PLAY\_OPL** structure holds information about the output protection levels (OPLs) specified in a license for play actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2ed3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e2ed3-107">Syntax</span></span>


```C++
typedef struct DRM_PLAY_OPL {
  DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS minOPL;
  DRM_OPL_OUTPUT_IDS                   oplIdReserved;
  DRM_VIDEO_OUTPUT_PROTECTION_IDS      vopi;
} ;
```



## <a name="members"></a><span data-ttu-id="e2ed3-108">Membros</span><span class="sxs-lookup"><span data-stu-id="e2ed3-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e2ed3-109">**minOPL**</span><span class="sxs-lookup"><span data-stu-id="e2ed3-109">**minOPL**</span></span>
</dt> <dd>

<span data-ttu-id="e2ed3-110">[**DRM \_ A estrutura de \_ \_ \_ níveis de proteção de saída mínima**](drmdrm-minimum-output-protection-levels.md) que contém o OPL mínimo necessário para reproduzir o conteúdo em formatos diferentes.</span><span class="sxs-lookup"><span data-stu-id="e2ed3-110">[**DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS**](drmdrm-minimum-output-protection-levels.md) structure containing the minimum OPL required to play content in different formats.</span></span>

</dd> <dt>

<span data-ttu-id="e2ed3-111">**oplIdReserved**</span><span class="sxs-lookup"><span data-stu-id="e2ed3-111">**oplIdReserved**</span></span>
</dt> <dd>

<span data-ttu-id="e2ed3-112">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="e2ed3-112">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="e2ed3-113">**vopi**</span><span class="sxs-lookup"><span data-stu-id="e2ed3-113">**vopi**</span></span>
</dt> <dd>

<span data-ttu-id="e2ed3-114">[**DRM \_ A \_ proteção de saída de vídeo \_ \_ identifica**](drmdrm-video-output-protection-ids.md) a estrutura que contém os identificadores de proteção de saída de vídeo que se aplicam à reprodução do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="e2ed3-114">[**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS**](drmdrm-video-output-protection-ids.md) structure containing the video output protection identifiers that apply to playback of the content.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e2ed3-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2ed3-115">Requirements</span></span>



| <span data-ttu-id="e2ed3-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2ed3-116">Requirement</span></span> | <span data-ttu-id="e2ed3-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e2ed3-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e2ed3-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e2ed3-118">Header</span></span><br/> | <dl> <span data-ttu-id="e2ed3-119"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2ed3-119"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2ed3-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2ed3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2ed3-121">**\_OPL de cópia DRM \_**</span><span class="sxs-lookup"><span data-stu-id="e2ed3-121">**DRM\_COPY\_OPL**</span></span>](drmdrm-copy-opl.md)
</dt> <dt>

[<span data-ttu-id="e2ed3-122">**execução do DRM \_ \_ OPL \_ ex**</span><span class="sxs-lookup"><span data-stu-id="e2ed3-122">**DRM\_PLAY\_OPL\_EX**</span></span>](drm-play-opl-ex.md)
</dt> <dt>

[<span data-ttu-id="e2ed3-123">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="e2ed3-123">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





