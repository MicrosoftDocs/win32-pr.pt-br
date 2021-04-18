---
title: Estrutura de DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX (wmdrmsdk. h)
description: A \_ \_ estrutura ex de proteção de saída de áudio DRM \_ \_ \_ contém uma lista de identificadores de proteção de saída de áudio. Essa estrutura estende as \_ \_ \_ IDs de proteção de saída de áudio DRM \_ adicionando um número de versão.
ms.assetid: e650ddeb-5e41-4ff8-b872-40c85ab519c1
keywords:
- Formato de mídia do Windows de estrutura de DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb687b5600e75f845c2d980f73f3b8c2eeda970a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793954"
---
# <a name="drm_audio_output_protection_ids_ex-structure"></a><span data-ttu-id="23eba-106">\_ \_ \_ \_ Estrutura ex de proteção de saída de áudio DRM \_</span><span class="sxs-lookup"><span data-stu-id="23eba-106">DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS\_EX structure</span></span>

<span data-ttu-id="23eba-107">A **estrutura \_ \_ \_ \_ \_ ex de proteção de saída de áudio DRM** contém uma lista de identificadores de proteção de saída de áudio.</span><span class="sxs-lookup"><span data-stu-id="23eba-107">The **DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS\_EX** structure contains a list of audio output protection identifiers.</span></span> <span data-ttu-id="23eba-108">Essa estrutura estende **as \_ \_ IDs de \_ proteção \_ de saída de áudio DRM** adicionando um número de versão.</span><span class="sxs-lookup"><span data-stu-id="23eba-108">This structure extends **DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS** by adding a version number.</span></span>

## <a name="syntax"></a><span data-ttu-id="23eba-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="23eba-109">Syntax</span></span>


```C++
typedef struct DRM_AUDIO_OUTPUT_PROTECTION_IDS_EX {
  DWORD                          dwVersion;
  WORD                           cEntries;
  DRM_AUDIO_OUTPUT_PROTECTION_EX *rgAop;
} ;
```



## <a name="members"></a><span data-ttu-id="23eba-110">Membros</span><span class="sxs-lookup"><span data-stu-id="23eba-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="23eba-111">**DW**</span><span class="sxs-lookup"><span data-stu-id="23eba-111">**dwVersion**</span></span>
</dt> <dd>

<span data-ttu-id="23eba-112">Número da versão.</span><span class="sxs-lookup"><span data-stu-id="23eba-112">Version number.</span></span>

</dd> <dt>

<span data-ttu-id="23eba-113">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="23eba-113">**cEntries**</span></span>
</dt> <dd>

<span data-ttu-id="23eba-114">Número de entradas na matriz **rgAop** .</span><span class="sxs-lookup"><span data-stu-id="23eba-114">Number of entries in the **rgAop** array.</span></span>

</dd> <dt>

<span data-ttu-id="23eba-115">**rgAop**</span><span class="sxs-lookup"><span data-stu-id="23eba-115">**rgAop**</span></span>
</dt> <dd>

<span data-ttu-id="23eba-116">Matriz de **estruturas \_ \_ ex de \_ proteção \_ de saída de áudio DRM** .</span><span class="sxs-lookup"><span data-stu-id="23eba-116">Array of **DRM\_AUDIO\_OUTPUT\_PROTECTION\_EX** structures.</span></span> <span data-ttu-id="23eba-117">**DRM \_ Proteção de saída de áudio \_ \_ \_ ex** é um tipo definido como [**proteção de \_ saída DRM \_ \_ ex**](drm-output-protection-ex.md).</span><span class="sxs-lookup"><span data-stu-id="23eba-117">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_EX** is a type defined as [**DRM\_OUTPUT\_PROTECTION\_EX**](drm-output-protection-ex.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="23eba-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="23eba-118">Remarks</span></span>

<span data-ttu-id="23eba-119">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="23eba-119">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="23eba-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23eba-120">Requirements</span></span>



| <span data-ttu-id="23eba-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="23eba-121">Requirement</span></span> | <span data-ttu-id="23eba-122">Valor</span><span class="sxs-lookup"><span data-stu-id="23eba-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="23eba-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="23eba-123">Header</span></span><br/> | <dl> <span data-ttu-id="23eba-124"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="23eba-124"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23eba-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="23eba-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23eba-126">**\_IDs de \_ proteção de saída de áudio DRM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="23eba-126">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS**</span></span>](drm-audio-output-protection-ids.md)
</dt> <dt>

[<span data-ttu-id="23eba-127">**\_IDs de proteção de saída de vídeo DRM \_ \_ \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="23eba-127">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS\_EX**</span></span>](drm-video-output-protection-ids-ex.md)
</dt> <dt>

[<span data-ttu-id="23eba-128">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="23eba-128">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





