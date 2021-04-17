---
title: Estrutura de DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX (wmdrmsdk. h)
description: A \_ estrutura ex de proteção de saída de vídeo DRM \_ \_ \_ \_ contém uma matriz de \_ estruturas de proteção de saída de vídeo DRM \_ \_ .
ms.assetid: 89de0ade-fa86-4081-b65b-9c84fb68cf3d
keywords:
- Formato de mídia do Windows de estrutura de DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2e7cc5ec0b4b14d88deb317e62e3e1cd4f92b57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813680"
---
# <a name="drm_video_output_protection_ids_ex-structure"></a><span data-ttu-id="0c730-105">\_ \_ \_ \_ Estrutura ex de proteção de saída de vídeo DRM \_</span><span class="sxs-lookup"><span data-stu-id="0c730-105">DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS\_EX structure</span></span>

<span data-ttu-id="0c730-106">A **estrutura \_ \_ \_ \_ \_ ex de proteção de saída de vídeo DRM** contém uma matriz de estruturas de **\_ \_ \_ proteção de saída de vídeo DRM** .</span><span class="sxs-lookup"><span data-stu-id="0c730-106">The **DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS\_EX** structure holds an array of **DRM\_VIDEO\_OUTPUT\_PROTECTION** structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c730-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0c730-107">Syntax</span></span>


```C++
typedef struct DRM_VIDEO_OUTPUT_PROTECTION_IDS_EX {
  DWORD                          dwVersion;
  WORD                           cEntries;
  DRM_VIDEO_OUTPUT_PROTECTION_EX *rgVop;
} ;
```



## <a name="members"></a><span data-ttu-id="0c730-108">Membros</span><span class="sxs-lookup"><span data-stu-id="0c730-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="0c730-109">**DW**</span><span class="sxs-lookup"><span data-stu-id="0c730-109">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="0c730-110">Número da versão.</span><span class="sxs-lookup"><span data-stu-id="0c730-110">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="0c730-111">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="0c730-111">**cEntries**</span></span>
</dt> <dd>

<span data-ttu-id="0c730-112">Número de elementos na matriz referenciados por **rgVop**.</span><span class="sxs-lookup"><span data-stu-id="0c730-112">Number of elements in the array referenced by **rgVop**.</span></span>

</dd> <dt>

<span data-ttu-id="0c730-113">**rgVop**</span><span class="sxs-lookup"><span data-stu-id="0c730-113">**rgVop**</span></span>
</dt> <dd>

<span data-ttu-id="0c730-114">Endereço de uma matriz de **estruturas \_ \_ ex de \_ proteção \_ de saída de vídeo DRM** .</span><span class="sxs-lookup"><span data-stu-id="0c730-114">Address of an array of **DRM\_VIDEO\_OUTPUT\_PROTECTION\_EX** structures.</span></span> <span data-ttu-id="0c730-115">**DRM \_ Proteção de saída de vídeo \_ \_ \_ ex** é um tipo definido como [**proteção de \_ saída DRM \_ \_ ex**](drm-output-protection-ex.md).</span><span class="sxs-lookup"><span data-stu-id="0c730-115">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_EX** is a type defined as [**DRM\_OUTPUT\_PROTECTION\_EX**](drm-output-protection-ex.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c730-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c730-116">Remarks</span></span>

<span data-ttu-id="0c730-117">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="0c730-117">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c730-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c730-118">Requirements</span></span>



| <span data-ttu-id="0c730-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c730-119">Requirement</span></span> | <span data-ttu-id="0c730-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0c730-120">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0c730-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0c730-121">Header</span></span><br/> | <dl> <span data-ttu-id="0c730-122"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c730-122"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c730-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c730-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c730-124">**\_IDs de proteção de saída de áudio DRM \_ \_ \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="0c730-124">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS\_EX**</span></span>](drm-audio-output-protection-ids-ex.md)
</dt> <dt>

[<span data-ttu-id="0c730-125">**\_IDs de \_ proteção de saída de vídeo DRM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0c730-125">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS**</span></span>](drmdrm-video-output-protection-ids.md)
</dt> <dt>

[<span data-ttu-id="0c730-126">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="0c730-126">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





