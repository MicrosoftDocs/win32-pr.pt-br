---
title: Estrutura de DRM_VIDEO_OUTPUT_PROTECTION_IDS (wmdrmsdk. h)
description: A \_ \_ estrutura de IDs da proteção de saída de vídeo DRM \_ \_ contém uma matriz de \_ estruturas de proteção de saída de vídeo DRM \_ \_ .
ms.assetid: 9f206a7e-c92b-4f29-a591-72784086d1db
keywords:
- Formato de mídia do Windows de estrutura de DRM_VIDEO_OUTPUT_PROTECTION_IDS
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51af3ccebec52ab6f6863aeb376ed27f8c8e2467
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788996"
---
# <a name="drm_video_output_protection_ids-structure"></a><span data-ttu-id="00bc8-105">\_Estrutura de \_ IDs de proteção de saída de vídeo DRM \_ \_</span><span class="sxs-lookup"><span data-stu-id="00bc8-105">DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS structure</span></span>

<span data-ttu-id="00bc8-106">A estrutura de **IDs da proteção de \_ saída de vídeo \_ \_ \_ DRM** contém uma matriz de estruturas de **proteção de \_ \_ saída \_ de vídeo DRM** .</span><span class="sxs-lookup"><span data-stu-id="00bc8-106">The **DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS** structure holds an array of **DRM\_VIDEO\_OUTPUT\_PROTECTION** structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="00bc8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00bc8-107">Syntax</span></span>


```C++
typedef struct DRM_VIDEO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_VIDEO_OUTPUT_PROTECTION *rgVop;
} ;
```



## <a name="members"></a><span data-ttu-id="00bc8-108">Membros</span><span class="sxs-lookup"><span data-stu-id="00bc8-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="00bc8-109">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="00bc8-109">**cEntries**</span></span>
</dt> <dd>

<span data-ttu-id="00bc8-110">Número de elementos na matriz referenciados por **rgVop**.</span><span class="sxs-lookup"><span data-stu-id="00bc8-110">Number of elements in the array referenced by **rgVop**.</span></span>

</dd> <dt>

<span data-ttu-id="00bc8-111">**rgVop**</span><span class="sxs-lookup"><span data-stu-id="00bc8-111">**rgVop**</span></span>
</dt> <dd>

<span data-ttu-id="00bc8-112">Endereço de uma matriz de estruturas de **\_ proteção de \_ saída \_ de vídeo DRM** .</span><span class="sxs-lookup"><span data-stu-id="00bc8-112">Address of an array of **DRM\_VIDEO\_OUTPUT\_PROTECTION** structures.</span></span> <span data-ttu-id="00bc8-113">**DRM \_ A \_ \_ proteção de saída de vídeo** é um tipo definido como [**\_ \_ proteção de saída DRM**](drm-output-protection.md).</span><span class="sxs-lookup"><span data-stu-id="00bc8-113">**DRM\_VIDEO\_OUTPUT\_PROTECTION** is a type defined as [**DRM\_OUTPUT\_PROTECTION**](drm-output-protection.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00bc8-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="00bc8-114">Remarks</span></span>

<span data-ttu-id="00bc8-115">Essa estrutura é usada como um membro da estrutura [**\_ \_ OPL de reprodução DRM**](drmdrm-play-opl.md) .</span><span class="sxs-lookup"><span data-stu-id="00bc8-115">This structure is used as a member of the [**DRM\_PLAY\_OPL**](drmdrm-play-opl.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="00bc8-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00bc8-116">Requirements</span></span>



| <span data-ttu-id="00bc8-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="00bc8-117">Requirement</span></span> | <span data-ttu-id="00bc8-118">Valor</span><span class="sxs-lookup"><span data-stu-id="00bc8-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="00bc8-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="00bc8-119">Header</span></span><br/> | <dl> <span data-ttu-id="00bc8-120"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="00bc8-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00bc8-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="00bc8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00bc8-122">**\_IDs de \_ proteção de saída de áudio DRM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="00bc8-122">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS**</span></span>](drm-audio-output-protection-ids.md)
</dt> <dt>

[<span data-ttu-id="00bc8-123">**\_IDs de proteção de saída de vídeo DRM \_ \_ \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="00bc8-123">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS\_EX**</span></span>](drm-video-output-protection-ids-ex.md)
</dt> <dt>

[<span data-ttu-id="00bc8-124">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="00bc8-124">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





