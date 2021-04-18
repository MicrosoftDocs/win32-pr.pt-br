---
description: Define algoritmos para o processador de vídeo que é usado pelo \_ algoritmo do processador de vídeo MF \_ \_ .
ms.assetid: 3BB0836E-39E6-40FA-9BA0-C986EB587CF1
title: Enumeração de MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_VIDEO_PROCESSOR_ALGORITHM_TYPE
api_type:
- HeaderDef
api_location:
- mfidl.h
ms.openlocfilehash: 604fee61ae4b6a34d876de8c2863ee6dddad73d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105781236"
---
# <a name="mf_video_processor_algorithm_type-enumeration"></a><span data-ttu-id="e2da3-103">\_Enumeração de \_ tipo de algoritmo do processador de vídeo MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="e2da3-103">MF\_VIDEO\_PROCESSOR\_ALGORITHM\_TYPE enumeration</span></span>

<span data-ttu-id="e2da3-104">Define algoritmos para o processador de vídeo que é usado pelo [ \_ algoritmo do \_ processador \_ de vídeo MF](mf-video-processor-algorithm.md).</span><span class="sxs-lookup"><span data-stu-id="e2da3-104">Defines algorithms for the video processor which is use by [MF\_VIDEO\_PROCESSOR\_ALGORITHM](mf-video-processor-algorithm.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e2da3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2da3-105">Syntax</span></span>


```C++
typedef enum _MF_VIDEO_PROCESSOR_ALGORITHM_TYPE { 
  MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT      = 0,
  MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444  = 1
} MF_VIDEO_PROCESSOR_ALGORITHM_TYPE;
```



## <a name="constants"></a><span data-ttu-id="e2da3-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="e2da3-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e2da3-107"><span id="MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT"></span><span id="mf_video_processor_algorithm_default"></span>**\_padrão de \_ algoritmo do processador de vídeo MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e2da3-107"><span id="MF_VIDEO_PROCESSOR_ALGORITHM_DEFAULT"></span><span id="mf_video_processor_algorithm_default"></span>**MF\_VIDEO\_PROCESSOR\_ALGORITHM\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="e2da3-108">o modo padrão favorece um equilíbrio entre qualidade e velocidade</span><span class="sxs-lookup"><span data-stu-id="e2da3-108">default mode favors a balance of quality and speed</span></span>

</dd> <dt>

<span data-ttu-id="e2da3-109"><span id="MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444"></span><span id="mf_video_processor_algorithm_mrf_crf_444"></span>**\_Algoritmo do processador de vídeo MF \_ \_ \_ MRF \_ CRF \_ 444**</span><span class="sxs-lookup"><span data-stu-id="e2da3-109"><span id="MF_VIDEO_PROCESSOR_ALGORITHM_MRF_CRF_444"></span><span id="mf_video_processor_algorithm_mrf_crf_444"></span>**MF\_VIDEO\_PROCESSOR\_ALGORITHM\_MRF\_CRF\_444**</span></span>
</dt> <dd>

<span data-ttu-id="e2da3-110">O processador de vídeo sempre será processado internamente no AYUV e usará filtros de alta qualidade.</span><span class="sxs-lookup"><span data-stu-id="e2da3-110">The video processor will always internally process in AYUV and use high quality filters.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e2da3-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2da3-111">Requirements</span></span>



| <span data-ttu-id="e2da3-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2da3-112">Requirement</span></span> | <span data-ttu-id="e2da3-113">Valor</span><span class="sxs-lookup"><span data-stu-id="e2da3-113">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e2da3-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2da3-114">Minimum supported client</span></span><br/> | <span data-ttu-id="e2da3-115">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e2da3-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e2da3-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e2da3-116">Minimum supported server</span></span><br/> | <span data-ttu-id="e2da3-117">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="e2da3-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e2da3-118">INSERI</span><span class="sxs-lookup"><span data-stu-id="e2da3-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e2da3-119"><dt>Mfidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e2da3-119"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2da3-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2da3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2da3-121">Enumerações de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e2da3-121">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




