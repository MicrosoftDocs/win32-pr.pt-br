---
title: Estrutura de DRM_OPL_OUTPUT_IDS (wmdrmsdk. h)
description: A estrutura de IDs de saída do DRM \_ OPL \_ \_ contém um número de identificadores de saída de OPL (nível de proteção de saída).
ms.assetid: 3627f2a7-1cea-400b-82e7-678898ccc386
keywords:
- Formato de mídia do Windows de estrutura de DRM_OPL_OUTPUT_IDS
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_OPL_OUTPUT_IDS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 802787c5e373c837d639e0225bf650d80c105970
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105790586"
---
# <a name="drm_opl_output_ids-structure"></a><span data-ttu-id="6fd29-105">\_Estrutura de \_ IDs de saída do DRM OPL \_</span><span class="sxs-lookup"><span data-stu-id="6fd29-105">DRM\_OPL\_OUTPUT\_IDS structure</span></span>

<span data-ttu-id="6fd29-106">A estrutura de **\_ IDs de \_ saída \_ do DRM OPL** contém um número de identificadores de saída de OPL (nível de proteção de saída).</span><span class="sxs-lookup"><span data-stu-id="6fd29-106">The **DRM\_OPL\_OUTPUT\_IDS** structure holds a number of output protection level (OPL) output identifiers.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fd29-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6fd29-107">Syntax</span></span>


```C++
typedef struct DRM_OPL_OUTPUT_IDS {
  WORD cIds;
  GUID *rgIds;
} ;
```



## <a name="members"></a><span data-ttu-id="6fd29-108">Membros</span><span class="sxs-lookup"><span data-stu-id="6fd29-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="6fd29-109">**cIds**</span><span class="sxs-lookup"><span data-stu-id="6fd29-109">**cIds**</span></span>
</dt> <dd>

<span data-ttu-id="6fd29-110">Número de identificadores na matriz referenciados por **rgIds**.</span><span class="sxs-lookup"><span data-stu-id="6fd29-110">Number of identifiers in the array referenced by **rgIds**.</span></span>

</dd> <dt>

<span data-ttu-id="6fd29-111">**rgIds**</span><span class="sxs-lookup"><span data-stu-id="6fd29-111">**rgIds**</span></span>
</dt> <dd>

<span data-ttu-id="6fd29-112">Endereço de uma matriz de GUIDs.</span><span class="sxs-lookup"><span data-stu-id="6fd29-112">Address of an array of GUIDs.</span></span> <span data-ttu-id="6fd29-113">Cada membro da matriz contém um identificador de saída OPL.</span><span class="sxs-lookup"><span data-stu-id="6fd29-113">Each member of the array contains an OPL output identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6fd29-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="6fd29-114">Remarks</span></span>

<span data-ttu-id="6fd29-115">Essa estrutura é usada como membro da [**\_ \_ OPL de cópia DRM**](drmdrm-copy-opl.md) e das estruturas [**\_ \_ OPL de reprodução DRM**](drmdrm-play-opl.md) para identificar grupos de identificadores de saída.</span><span class="sxs-lookup"><span data-stu-id="6fd29-115">This structure is used as a member of the [**DRM\_COPY\_OPL**](drmdrm-copy-opl.md) and [**DRM\_PLAY\_OPL**](drmdrm-play-opl.md) structures to identify groups of output identifiers.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fd29-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fd29-116">Requirements</span></span>



| <span data-ttu-id="6fd29-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fd29-117">Requirement</span></span> | <span data-ttu-id="6fd29-118">Valor</span><span class="sxs-lookup"><span data-stu-id="6fd29-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6fd29-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6fd29-119">Header</span></span><br/> | <dl> <span data-ttu-id="6fd29-120"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fd29-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fd29-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="6fd29-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fd29-122">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="6fd29-122">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





