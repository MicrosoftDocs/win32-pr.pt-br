---
title: Estrutura de DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS (wmdrmsdk. h)
description: A \_ estrutura de níveis de proteção de saída mínima de DRM \_ \_ \_ contém os níveis mínimos de proteção de saída (OPLs) para reprodução de vários tipos de conteúdo. Um dispositivo deve dar suporte ao mínimo de OPL para um tipo de dados para receber esse tipo de dados do leitor.
ms.assetid: 6232ecd4-9829-4de3-9810-70e3d3c129a9
keywords:
- Formato de mídia do Windows de estrutura de DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS
- estruturar formato de mídia do Windows
topic_type:
- apiref
api_name:
- DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 060fdda4cd1c3cc665e396a72d46ac05e721abe4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786131"
---
# <a name="drm_minimum_output_protection_levels-structure"></a><span data-ttu-id="ca02e-106">\_Estrutura de \_ \_ níveis de proteção de saída mínima do DRM \_</span><span class="sxs-lookup"><span data-stu-id="ca02e-106">DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS structure</span></span>

<span data-ttu-id="ca02e-107">A estrutura de **\_ níveis de \_ \_ proteção \_ de saída mínima de DRM** contém os níveis mínimos de proteção de saída (OPLs) para reprodução de vários tipos de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ca02e-107">The **DRM\_MINIMUM\_OUTPUT\_PROTECTION\_LEVELS** structure holds the minimum output protection levels (OPLs) for playback of various types of content.</span></span> <span data-ttu-id="ca02e-108">Um dispositivo deve dar suporte ao mínimo de OPL para um tipo de dados para receber esse tipo de dados do leitor.</span><span class="sxs-lookup"><span data-stu-id="ca02e-108">A device must support the minimum OPL for a type of data to receive that type of data from the reader.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca02e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca02e-109">Syntax</span></span>


```C++
typedef struct DRM_MINIMUM_OUTPUT_PROTECTION_LEVELS {
  WORD wCompressedDigitalVideo;
  WORD wUncompressedDigitalVideo;
  WORD wAnalogVideo;
  WORD wCompressedDigitalAudio;
  WORD wUncompressedDigitalAudio;
} ;
```



## <a name="members"></a><span data-ttu-id="ca02e-110">Membros</span><span class="sxs-lookup"><span data-stu-id="ca02e-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="ca02e-111">**wCompressedDigitalVideo**</span><span class="sxs-lookup"><span data-stu-id="ca02e-111">**wCompressedDigitalVideo**</span></span>
</dt> <dd>

<span data-ttu-id="ca02e-112">OPL mínimo necessário para receber vídeo digital compactado.</span><span class="sxs-lookup"><span data-stu-id="ca02e-112">Minimum OPL required to receive compressed digital video.</span></span>

</dd> <dt>

<span data-ttu-id="ca02e-113">**wUncompressedDigitalVideo**</span><span class="sxs-lookup"><span data-stu-id="ca02e-113">**wUncompressedDigitalVideo**</span></span>
</dt> <dd>

<span data-ttu-id="ca02e-114">OPL mínimo necessário para receber vídeo digital não compactado.</span><span class="sxs-lookup"><span data-stu-id="ca02e-114">Minimum OPL required to receive uncompressed digital video.</span></span>

</dd> <dt>

<span data-ttu-id="ca02e-115">**wAnalogVideo**</span><span class="sxs-lookup"><span data-stu-id="ca02e-115">**wAnalogVideo**</span></span>
</dt> <dd>

<span data-ttu-id="ca02e-116">OPL mínimo necessário para receber vídeo analógico.</span><span class="sxs-lookup"><span data-stu-id="ca02e-116">Minimum OPL required to receive analog video.</span></span>

</dd> <dt>

<span data-ttu-id="ca02e-117">**wCompressedDigitalAudio**</span><span class="sxs-lookup"><span data-stu-id="ca02e-117">**wCompressedDigitalAudio**</span></span>
</dt> <dd>

<span data-ttu-id="ca02e-118">OPL mínimo necessário para receber áudio digital compactado.</span><span class="sxs-lookup"><span data-stu-id="ca02e-118">Minimum OPL required to receive compressed digital audio.</span></span>

</dd> <dt>

<span data-ttu-id="ca02e-119">**wUncompressedDigitalAudio**</span><span class="sxs-lookup"><span data-stu-id="ca02e-119">**wUncompressedDigitalAudio**</span></span>
</dt> <dd>

<span data-ttu-id="ca02e-120">OPL mínimo necessário para receber áudio digital descompactado.</span><span class="sxs-lookup"><span data-stu-id="ca02e-120">Minimum OPL required to receive uncompressed digital audio.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ca02e-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca02e-121">Remarks</span></span>

<span data-ttu-id="ca02e-122">Essa estrutura é usada como um membro da estrutura [**\_ \_ OPL de reprodução DRM**](drmdrm-play-opl.md) .</span><span class="sxs-lookup"><span data-stu-id="ca02e-122">This structure is used as a member of the [**DRM\_PLAY\_OPL**](drmdrm-play-opl.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca02e-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca02e-123">Requirements</span></span>



| <span data-ttu-id="ca02e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca02e-124">Requirement</span></span> | <span data-ttu-id="ca02e-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ca02e-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ca02e-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ca02e-126">Header</span></span><br/> | <dl> <span data-ttu-id="ca02e-127"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca02e-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca02e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca02e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca02e-129">**Estruturas**</span><span class="sxs-lookup"><span data-stu-id="ca02e-129">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





