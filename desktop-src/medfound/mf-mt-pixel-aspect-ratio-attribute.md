---
description: Taxa de proporção de pixel para um tipo de mídia de vídeo.
ms.assetid: e82cdd22-7d3f-4858-befd-43fa6f9f915e
title: Atributo MF_MT_PIXEL_ASPECT_RATIO (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50c0d28ea11ba664208fcfe5fc356f1f57f2878e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501838"
---
# <a name="mf_mt_pixel_aspect_ratio-attribute"></a><span data-ttu-id="bb246-103">\_Atributo de \_ \_ taxa de proporção MF MT pixel \_</span><span class="sxs-lookup"><span data-stu-id="bb246-103">MF\_MT\_PIXEL\_ASPECT\_RATIO attribute</span></span>

<span data-ttu-id="bb246-104">Taxa de proporção de pixel para um tipo de mídia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="bb246-104">Pixel aspect ratio for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="bb246-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="bb246-105">Data type</span></span>

<span data-ttu-id="bb246-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="bb246-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="bb246-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb246-107">Remarks</span></span>

<span data-ttu-id="bb246-108">Os bits superiores de 32 contêm o numerador da taxa de proporção de pixel e os bits inferiores de 32 contêm o denominador.</span><span class="sxs-lookup"><span data-stu-id="bb246-108">The upper 32 bits contain the numerator of the pixel aspect ratio and the lower 32 bits contain the denominator.</span></span> <span data-ttu-id="bb246-109">O numerador é o componente horizontal da taxa de proporção; o denominador é o componente vertical.</span><span class="sxs-lookup"><span data-stu-id="bb246-109">The numerator is the horizontal component of the aspect ratio; the denominator is the vertical component.</span></span>

<span data-ttu-id="bb246-110">Para definir esse atributo, use a função [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) .</span><span class="sxs-lookup"><span data-stu-id="bb246-110">To set this attribute, use the [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio) function.</span></span> <span data-ttu-id="bb246-111">Para obter esse atributo, use a função [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) .</span><span class="sxs-lookup"><span data-stu-id="bb246-111">To get this attribute, use the [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio) function.</span></span>

<span data-ttu-id="bb246-112">A taxa de proporção de pixel descreve a forma dos pixels na imagem de vídeo exibida.</span><span class="sxs-lookup"><span data-stu-id="bb246-112">The pixel aspect ratio describes the shape of the pixels in the displayed video image.</span></span> <span data-ttu-id="bb246-113">Defina esse atributo se a imagem tiver pixels não quadrados.</span><span class="sxs-lookup"><span data-stu-id="bb246-113">Set this attribute if the image has non-square pixels.</span></span> <span data-ttu-id="bb246-114">Para exibir corretamente em um dispositivo de vídeo com pixels quadrados, a imagem deve ser dimensionada pelo inverso da taxa de proporção de pixel da imagem.</span><span class="sxs-lookup"><span data-stu-id="bb246-114">To display correctly on a display device with square pixels, the image must be scaled by the inverse of the image's pixel aspect ratio.</span></span>

<span data-ttu-id="bb246-115">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="bb246-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb246-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb246-116">Requirements</span></span>



| <span data-ttu-id="bb246-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb246-117">Requirement</span></span> | <span data-ttu-id="bb246-118">Valor</span><span class="sxs-lookup"><span data-stu-id="bb246-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bb246-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb246-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bb246-120">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="bb246-120">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="bb246-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bb246-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bb246-122">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="bb246-122">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="bb246-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bb246-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb246-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb246-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb246-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="bb246-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb246-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bb246-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bb246-127">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="bb246-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="bb246-128">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="bb246-128">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bb246-129">Taxa de proporção da imagem</span><span class="sxs-lookup"><span data-stu-id="bb246-129">Picture Aspect Ratio</span></span>](picture-aspect-ratio.md)
</dt> </dl>

 

 




