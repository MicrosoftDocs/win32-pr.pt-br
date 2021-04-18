---
title: Estrutura de WMDRM_OUTPUT_PROTECTION_LEVELS (wmdrmsdk. h)
description: A estrutura de níveis de proteção de saída do WMDRM \_ \_ \_ contém os OPLs (níveis de proteções de saída) exigidos por uma licença para executar várias ações.
ms.assetid: 6b284180-1033-4c57-b010-6d4ab4bc593a
keywords:
- Formato de mídia do Windows de estrutura de WMDRM_OUTPUT_PROTECTION_LEVELS
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- WMDRM_OUTPUT_PROTECTION_LEVELS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d720a8aef42178da188b71a1635d97031b138397
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105815428"
---
# <a name="wmdrm_output_protection_levels-structure"></a><span data-ttu-id="2da77-105">\_Estrutura de \_ níveis de proteção de saída WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="2da77-105">WMDRM\_OUTPUT\_PROTECTION\_LEVELS structure</span></span>

<span data-ttu-id="2da77-106">A estrutura de níveis de proteção de saída do WMDRM contém os OPLs (níveis de proteções de saída) exigidos por uma licença para executar várias ações. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2da77-106">The **WMDRM\_OUTPUT\_PROTECTION\_LEVELS** structure contains the output protections levels (OPLs) required by a license to perform various actions.</span></span>

## <a name="syntax"></a><span data-ttu-id="2da77-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2da77-107">Syntax</span></span>


```C++
typedef struct WMDRM_OUTPUT_PROTECTION_LEVELS {
  WORD wCompressedDigitalVideo;
  WORD wUncompressedDigitalVideo;
  WORD wAnalogVideo;
  WORD wCompressedDigitalAudio;
  WORD wUncompressedDigitalAudio;
  WORD wMinimumCopyProtectionLevel;
} ;
```



## <a name="members"></a><span data-ttu-id="2da77-108">Membros</span><span class="sxs-lookup"><span data-stu-id="2da77-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="2da77-109">**wCompressedDigitalVideo**</span><span class="sxs-lookup"><span data-stu-id="2da77-109">**wCompressedDigitalVideo**</span></span>
</dt> <dd>

<span data-ttu-id="2da77-110">OPL mínimo necessário para receber vídeo digital compactado.</span><span class="sxs-lookup"><span data-stu-id="2da77-110">Minimum OPL required to receive compressed digital video.</span></span>

</dd> <dt>

<span data-ttu-id="2da77-111">**wUncompressedDigitalVideo**</span><span class="sxs-lookup"><span data-stu-id="2da77-111">**wUncompressedDigitalVideo**</span></span>
</dt> <dd>

<span data-ttu-id="2da77-112">OPL mínimo necessário para receber vídeo digital não compactado.</span><span class="sxs-lookup"><span data-stu-id="2da77-112">Minimum OPL required to receive uncompressed digital video.</span></span>

</dd> <dt>

<span data-ttu-id="2da77-113">**wAnalogVideo**</span><span class="sxs-lookup"><span data-stu-id="2da77-113">**wAnalogVideo**</span></span>
</dt> <dd>

<span data-ttu-id="2da77-114">OPL mínimo necessário para receber vídeo analógico.</span><span class="sxs-lookup"><span data-stu-id="2da77-114">Minimum OPL required to receive analog video.</span></span>

</dd> <dt>

<span data-ttu-id="2da77-115">**wCompressedDigitalAudio**</span><span class="sxs-lookup"><span data-stu-id="2da77-115">**wCompressedDigitalAudio**</span></span>
</dt> <dd>

<span data-ttu-id="2da77-116">OPL mínimo necessário para receber áudio digital compactado.</span><span class="sxs-lookup"><span data-stu-id="2da77-116">Minimum OPL required to receive compressed digital audio.</span></span>

</dd> <dt>

<span data-ttu-id="2da77-117">**wUncompressedDigitalAudio**</span><span class="sxs-lookup"><span data-stu-id="2da77-117">**wUncompressedDigitalAudio**</span></span>
</dt> <dd>

<span data-ttu-id="2da77-118">OPL mínimo necessário para receber áudio digital descompactado.</span><span class="sxs-lookup"><span data-stu-id="2da77-118">Minimum OPL required to receive uncompressed digital audio.</span></span>

</dd> <dt>

<span data-ttu-id="2da77-119">**wMinimumCopyProtectionLevel**</span><span class="sxs-lookup"><span data-stu-id="2da77-119">**wMinimumCopyProtectionLevel**</span></span>
</dt> <dd>

<span data-ttu-id="2da77-120">OPL mínimo necessário para copiar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="2da77-120">Minimum OPL required to copy the content.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2da77-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="2da77-121">Remarks</span></span>

<span data-ttu-id="2da77-122">Essa estrutura é usada pelo método [**IWMDRMLicense:: GetOutputProtectionLevels**](iwmdrmlicense-getoutputprotectionlevels.md) .</span><span class="sxs-lookup"><span data-stu-id="2da77-122">This structure is used by the [**IWMDRMLicense::GetOutputProtectionLevels**](iwmdrmlicense-getoutputprotectionlevels.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2da77-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2da77-123">Requirements</span></span>



| <span data-ttu-id="2da77-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2da77-124">Requirement</span></span> | <span data-ttu-id="2da77-125">Valor</span><span class="sxs-lookup"><span data-stu-id="2da77-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2da77-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2da77-126">Header</span></span><br/> | <dl> <span data-ttu-id="2da77-127"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="2da77-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2da77-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="2da77-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2da77-129">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="2da77-129">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





