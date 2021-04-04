---
description: O decodificador de vídeo DV Media Foundation é uma transformação Media Foundation que decodifica vídeo DV.
ms.assetid: 97e5ba52-92fc-49e4-9c22-6f61bfda2003
title: Decodificador de vídeo DV
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed277c3e4dd1aaa031d4dcf4694c7c3051fe37ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646589"
---
# <a name="dv-video-decoder"></a><span data-ttu-id="52fb6-103">Decodificador de vídeo DV</span><span class="sxs-lookup"><span data-stu-id="52fb6-103">DV Video Decoder</span></span>

<span data-ttu-id="52fb6-104">O decodificador de vídeo DV Media Foundation é uma [transformação Media Foundation](media-foundation-transforms.md) que DECODIFICA vídeo DV.</span><span class="sxs-lookup"><span data-stu-id="52fb6-104">The Media Foundation DV video decoder is a [Media Foundation Transform](media-foundation-transforms.md) that decodes DV video.</span></span>

<span data-ttu-id="52fb6-105">O decodificador de vídeo DV dá suporte aos seguintes tipos de entrada:</span><span class="sxs-lookup"><span data-stu-id="52fb6-105">The DV video decoder supports the following input types:</span></span>



| <span data-ttu-id="52fb6-106">Subtype</span><span class="sxs-lookup"><span data-stu-id="52fb6-106">Subtype</span></span>                 | <span data-ttu-id="52fb6-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="52fb6-107">Description</span></span>                  |
|-------------------------|------------------------------|
| <span data-ttu-id="52fb6-108">**MFVideoFormat \_ DVC**</span><span class="sxs-lookup"><span data-stu-id="52fb6-108">**MFVideoFormat\_DVC**</span></span>  | <span data-ttu-id="52fb6-109">Vídeo de DVC/DV</span><span class="sxs-lookup"><span data-stu-id="52fb6-109">DVC/DV Video</span></span>                 |
| <span data-ttu-id="52fb6-110">**MFVideoFormat \_ DVHD**</span><span class="sxs-lookup"><span data-stu-id="52fb6-110">**MFVideoFormat\_DVHD**</span></span> | <span data-ttu-id="52fb6-111">HD-DVCR (1125-60 ou 1250-50)</span><span class="sxs-lookup"><span data-stu-id="52fb6-111">HD-DVCR (1125-60 or 1250-50)</span></span> |
| <span data-ttu-id="52fb6-112">**MFVideoFormat \_ DVSD**</span><span class="sxs-lookup"><span data-stu-id="52fb6-112">**MFVideoFormat\_DVSD**</span></span> | <span data-ttu-id="52fb6-113">SDL-DVCR (525-60 ou 625-50)</span><span class="sxs-lookup"><span data-stu-id="52fb6-113">SDL-DVCR (525-60 or 625-50)</span></span>  |
| <span data-ttu-id="52fb6-114">**MFVideoFormat \_ DVSL**</span><span class="sxs-lookup"><span data-stu-id="52fb6-114">**MFVideoFormat\_DVSL**</span></span> | <span data-ttu-id="52fb6-115">SD-DVCR (525-60 ou 625-50)</span><span class="sxs-lookup"><span data-stu-id="52fb6-115">SD-DVCR (525-60 or 625-50)</span></span>   |



 

<span data-ttu-id="52fb6-116">Ele dá suporte a um único tipo de saída:</span><span class="sxs-lookup"><span data-stu-id="52fb6-116">It supports a single output type:</span></span>



| <span data-ttu-id="52fb6-117">Subtype</span><span class="sxs-lookup"><span data-stu-id="52fb6-117">Subtype</span></span>             | <span data-ttu-id="52fb6-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="52fb6-118">Description</span></span> |
|---------------------|-------------|
| <span data-ttu-id="52fb6-119">MFVideoFormat \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="52fb6-119">MFVideoFormat\_YUY2</span></span> | <span data-ttu-id="52fb6-120">Vídeo do YUY2</span><span class="sxs-lookup"><span data-stu-id="52fb6-120">YUY2 video</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="52fb6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52fb6-121">Requirements</span></span>



| <span data-ttu-id="52fb6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="52fb6-122">Requirement</span></span> | <span data-ttu-id="52fb6-123">Valor</span><span class="sxs-lookup"><span data-stu-id="52fb6-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="52fb6-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52fb6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="52fb6-125">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="52fb6-125">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="52fb6-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="52fb6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="52fb6-127">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="52fb6-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="52fb6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="52fb6-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52fb6-129"><dt>Mfdvdec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52fb6-129"><dt>Mfdvdec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52fb6-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="52fb6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52fb6-131">Objetos de codec</span><span class="sxs-lookup"><span data-stu-id="52fb6-131">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="52fb6-132">Formatos de mídia compatíveis com o Media Foundation</span><span class="sxs-lookup"><span data-stu-id="52fb6-132">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="52fb6-133">Tipos de mídia de vídeo</span><span class="sxs-lookup"><span data-stu-id="52fb6-133">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 




