---
title: Estrutura de DRM_AUDIO_OUTPUT_PROTECTION_IDS (wmdrmsdk. h)
description: A \_ \_ estrutura de IDs da proteção de saída de áudio DRM \_ \_ contém uma lista de identificadores de proteção de saída de áudio.
ms.assetid: 21972b18-334b-4a4d-812d-21cbfaf7cc58
keywords:
- Formato de mídia do Windows de estrutura de DRM_AUDIO_OUTPUT_PROTECTION_IDS
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_AUDIO_OUTPUT_PROTECTION_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d3c7142f5f575413f72885aa60a0ccb826ecfab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766515"
---
# <a name="drm_audio_output_protection_ids-structure"></a><span data-ttu-id="81c0a-105">\_Estrutura de \_ IDs de proteção de saída de áudio DRM \_ \_</span><span class="sxs-lookup"><span data-stu-id="81c0a-105">DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS structure</span></span>

<span data-ttu-id="81c0a-106">A estrutura de **IDs da proteção de \_ saída de áudio \_ \_ \_ DRM** contém uma lista de identificadores de proteção de saída de áudio.</span><span class="sxs-lookup"><span data-stu-id="81c0a-106">The **DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS** structure contains a list of audio output protection identifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="81c0a-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="81c0a-107">Syntax</span></span>


```C++
typedef struct DRM_AUDIO_OUTPUT_PROTECTION_IDS {
  WORD                        cEntries;
  DRM_AUDIO_OUTPUT_PROTECTION *rgAop;
} ;
```



## <a name="members"></a><span data-ttu-id="81c0a-108">Membros</span><span class="sxs-lookup"><span data-stu-id="81c0a-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="81c0a-109">**cEntries**</span><span class="sxs-lookup"><span data-stu-id="81c0a-109">**cEntries**</span></span>
</dt> <dd>

<span data-ttu-id="81c0a-110">Número de entradas na matriz **rgAop** .</span><span class="sxs-lookup"><span data-stu-id="81c0a-110">Number of entries in the **rgAop** array.</span></span>

</dd> <dt>

<span data-ttu-id="81c0a-111">**rgAop**</span><span class="sxs-lookup"><span data-stu-id="81c0a-111">**rgAop**</span></span>
</dt> <dd>

<span data-ttu-id="81c0a-112">Matriz de estruturas de **\_ proteção de \_ saída \_ de áudio DRM** .</span><span class="sxs-lookup"><span data-stu-id="81c0a-112">Array of **DRM\_AUDIO\_OUTPUT\_PROTECTION** structures.</span></span> <span data-ttu-id="81c0a-113">**DRM \_ A \_ \_ proteção de saída de áudio** é um tipo definido como [**\_ \_ proteção de saída DRM**](drm-output-protection.md).</span><span class="sxs-lookup"><span data-stu-id="81c0a-113">**DRM\_AUDIO\_OUTPUT\_PROTECTION** is a type defined as [**DRM\_OUTPUT\_PROTECTION**](drm-output-protection.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="81c0a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="81c0a-114">Remarks</span></span>

<span data-ttu-id="81c0a-115">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="81c0a-115">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="81c0a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81c0a-116">Requirements</span></span>



| <span data-ttu-id="81c0a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="81c0a-117">Requirement</span></span> | <span data-ttu-id="81c0a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="81c0a-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="81c0a-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="81c0a-119">Header</span></span><br/> | <dl> <span data-ttu-id="81c0a-120"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="81c0a-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81c0a-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="81c0a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81c0a-122">**\_IDs de proteção de saída de áudio DRM \_ \_ \_ \_ ex**</span><span class="sxs-lookup"><span data-stu-id="81c0a-122">**DRM\_AUDIO\_OUTPUT\_PROTECTION\_IDS\_EX**</span></span>](drm-audio-output-protection-ids-ex.md)
</dt> <dt>

[<span data-ttu-id="81c0a-123">**\_IDs de \_ proteção de saída de vídeo DRM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="81c0a-123">**DRM\_VIDEO\_OUTPUT\_PROTECTION\_IDS**</span></span>](drmdrm-video-output-protection-ids.md)
</dt> <dt>

[<span data-ttu-id="81c0a-124">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="81c0a-124">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





