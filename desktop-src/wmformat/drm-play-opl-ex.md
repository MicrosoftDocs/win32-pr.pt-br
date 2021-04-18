---
title: Estrutura de DRM_PLAY_OPL_EX (wmdrmsdk. h)
description: A \_ estrutura DRM Play \_ OPL \_ ex contém informações sobre os níveis de proteção de saída (OPLs) especificados em uma licença para ações de reprodução.
ms.assetid: 287f6681-f12e-4ef3-b802-24ee7b94bc7f
keywords:
- Formato de mídia do Windows de estrutura de DRM_PLAY_OPL_EX
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_PLAY_OPL_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edf85ee664b33df9c63c390a870401b100327f53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788998"
---
# <a name="drm_play_opl_ex-structure"></a><span data-ttu-id="442dc-105">Estrutura de exemplo do DRM \_ Play \_ OPL \_</span><span class="sxs-lookup"><span data-stu-id="442dc-105">DRM\_PLAY\_OPL\_EX structure</span></span>

<span data-ttu-id="442dc-106">A estrutura **DRM \_ Play \_ OPL \_ ex** contém informações sobre os níveis de proteção de saída (OPLs) especificados em uma licença para ações de reprodução.</span><span class="sxs-lookup"><span data-stu-id="442dc-106">The **DRM\_PLAY\_OPL\_EX** structure holds information about the output protection levels (OPLs) specified in a license for play actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="442dc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="442dc-107">Syntax</span></span>


```C++
typedef struct DRM_PLAY_OPL_EX {
  DWORD                                dwVersion;
  DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS minOPL;
  DRM_OPL_OUTPUT_IDS                   oplIdReserved;
  DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX   vopi;
} ;
```



## <a name="members"></a><span data-ttu-id="442dc-108">Membros</span><span class="sxs-lookup"><span data-stu-id="442dc-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="442dc-109">**DW**</span><span class="sxs-lookup"><span data-stu-id="442dc-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="442dc-110">Número da versão.</span><span class="sxs-lookup"><span data-stu-id="442dc-110">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="442dc-111">**minOPL**</span><span class="sxs-lookup"><span data-stu-id="442dc-111">**minOPL**</span></span>
</dt> <dd>

<span data-ttu-id="442dc-112">[**DRM \_ A estrutura de \_ \_ \_ níveis de proteção de saída mínima**](drmdrm-minimum-output-protection-levels.md) que contém o OPL mínimo necessário para reproduzir o conteúdo em formatos diferentes.</span><span class="sxs-lookup"><span data-stu-id="442dc-112">[**DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS**](drmdrm-minimum-output-protection-levels.md) structure containing the minimum OPL required to play content in different formats.</span></span>

</dd> <dt>

<span data-ttu-id="442dc-113">**oplIdReserved**</span><span class="sxs-lookup"><span data-stu-id="442dc-113">**oplIdReserved**</span></span>
</dt> <dd>

<span data-ttu-id="442dc-114">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="442dc-114">Reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="442dc-115">**vopi**</span><span class="sxs-lookup"><span data-stu-id="442dc-115">**vopi**</span></span>
</dt> <dd>

<span data-ttu-id="442dc-116">[**DRM \_ A \_ proteção de saída de vídeo \_ \_ identifica**](drmdrm-video-output-protection-ids.md) a estrutura que contém os identificadores de proteção de saída de vídeo que se aplicam à reprodução do conteúdo.</span><span class="sxs-lookup"><span data-stu-id="442dc-116">[**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS**](drmdrm-video-output-protection-ids.md) structure containing the video output protection identifiers that apply to playback of the content.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="442dc-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="442dc-117">Remarks</span></span>

<span data-ttu-id="442dc-118">Essa estrutura é idêntica à estrutura **\_ \_ OPL de reprodução DRM** , exceto pelo fato de que ela inclui um número de versão.</span><span class="sxs-lookup"><span data-stu-id="442dc-118">This structure is identical to the **DRM\_PLAY\_OPL** structure, except that it includes a version number.</span></span>

## <a name="requirements"></a><span data-ttu-id="442dc-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="442dc-119">Requirements</span></span>



| <span data-ttu-id="442dc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="442dc-120">Requirement</span></span> | <span data-ttu-id="442dc-121">Valor</span><span class="sxs-lookup"><span data-stu-id="442dc-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="442dc-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="442dc-122">Header</span></span><br/> | <dl> <span data-ttu-id="442dc-123"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="442dc-123"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="442dc-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="442dc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="442dc-125">**\_OPL de reprodução DRM \_**</span><span class="sxs-lookup"><span data-stu-id="442dc-125">**DRM\_PLAY\_OPL**</span></span>](drmdrm-play-opl.md)
</dt> <dt>

[<span data-ttu-id="442dc-126">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="442dc-126">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





