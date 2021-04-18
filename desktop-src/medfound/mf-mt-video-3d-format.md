---
description: Para um tipo de mídia de vídeo, especifica como os quadros de vídeo 3D são armazenados na memória.
ms.assetid: 880DF017-5841-4C0A-82AF-F092DEF5406B
title: Atributo MF_MT_VIDEO_3D_FORMAT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66f2b12f907edb2875b3b121607509288787c8e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757268"
---
# <a name="mf_mt_video_3d_format-attribute"></a><span data-ttu-id="2a3c5-103">\_Atributo de \_ \_ formato 3D de vídeo MF MT \_</span><span class="sxs-lookup"><span data-stu-id="2a3c5-103">MF\_MT\_VIDEO\_3D\_FORMAT attribute</span></span>

<span data-ttu-id="2a3c5-104">Para um tipo de mídia de vídeo, especifica como os quadros de vídeo 3D são armazenados na memória.</span><span class="sxs-lookup"><span data-stu-id="2a3c5-104">For a video media type, specifies how 3D video frames are stored in memory.</span></span>

## <a name="data-type"></a><span data-ttu-id="2a3c5-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="2a3c5-105">Data type</span></span>

<span data-ttu-id="2a3c5-106">**MFVideo3DFormat** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="2a3c5-106">**MFVideo3DFormat** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2a3c5-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a3c5-107">Remarks</span></span>

<span data-ttu-id="2a3c5-108">O valor desse atributo é um membro da enumeração [**MFVideo3DFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dformat) .</span><span class="sxs-lookup"><span data-stu-id="2a3c5-108">The value of this attribute is a member of the [**MFVideo3DFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dformat) enumeration.</span></span> <span data-ttu-id="2a3c5-109">O atributo se aplicará somente se o atributo [ \_ \_ \_ 3D de vídeo MF MT](mf-mt-video-3d.md) for **true**.</span><span class="sxs-lookup"><span data-stu-id="2a3c5-109">The attribute applies only if the [MF\_MT\_VIDEO\_3D](mf-mt-video-3d.md) attribute is **TRUE**.</span></span>

<span data-ttu-id="2a3c5-110">Esse atributo é necessário para formatos de vídeo 3D não compactados.</span><span class="sxs-lookup"><span data-stu-id="2a3c5-110">This attribute is required for uncompressed 3D video formats.</span></span> <span data-ttu-id="2a3c5-111">É opcional para vídeo 3D compactado.</span><span class="sxs-lookup"><span data-stu-id="2a3c5-111">It is optional for compressed 3D video.</span></span> <span data-ttu-id="2a3c5-112">Uma fonte de mídia que fornece quadros codificados pode ser capaz de definir o atributo, com base nas informações no contêiner de arquivo.</span><span class="sxs-lookup"><span data-stu-id="2a3c5-112">A media source that delivers encoded frames might be able to set the attribute, based on information in the file container.</span></span> <span data-ttu-id="2a3c5-113">Caso contrário, o atributo deve ser definido pelo decodificador no tipo de mídia de saída do decodificador.</span><span class="sxs-lookup"><span data-stu-id="2a3c5-113">Otherwise, the attribute should be set by the decoder in the decoder's output media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a3c5-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a3c5-114">Requirements</span></span>



| <span data-ttu-id="2a3c5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a3c5-115">Requirement</span></span> | <span data-ttu-id="2a3c5-116">Valor</span><span class="sxs-lookup"><span data-stu-id="2a3c5-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2a3c5-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a3c5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2a3c5-118">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2a3c5-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="2a3c5-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2a3c5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2a3c5-120">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2a3c5-120">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="2a3c5-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2a3c5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a3c5-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a3c5-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a3c5-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="2a3c5-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a3c5-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2a3c5-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




