---
description: Stride de superfície padrão, para um tipo de mídia de vídeo descompactado. Stride é o número de bytes necessários para ir de uma linha de pixels para a próxima.
ms.assetid: 71fda231-3497-49db-b82e-2fd79f6ade66
title: Atributo MF_MT_DEFAULT_STRIDE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b2b9633e14c8d414355ca41be29a9c6c2f8886
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165019"
---
# <a name="mf_mt_default_stride-attribute"></a><span data-ttu-id="d92b0-104">\_ \_ Atributo Stride padrão MF MT \_</span><span class="sxs-lookup"><span data-stu-id="d92b0-104">MF\_MT\_DEFAULT\_STRIDE attribute</span></span>

<span data-ttu-id="d92b0-105">Stride de superfície padrão, para um tipo de mídia de vídeo descompactado.</span><span class="sxs-lookup"><span data-stu-id="d92b0-105">Default surface stride, for an uncompressed video media type.</span></span> <span data-ttu-id="d92b0-106">Stride é o número de bytes necessários para ir de uma linha de pixels para a próxima.</span><span class="sxs-lookup"><span data-stu-id="d92b0-106">Stride is the number of bytes needed to go from one row of pixels to the next.</span></span>

## <a name="data-type"></a><span data-ttu-id="d92b0-107">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d92b0-107">Data type</span></span>

<span data-ttu-id="d92b0-108">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d92b0-108">**UINT32**</span></span>

<span data-ttu-id="d92b0-109">Tratar como um valor **INT32** .</span><span class="sxs-lookup"><span data-stu-id="d92b0-109">Treat as a **INT32** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d92b0-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d92b0-110">Remarks</span></span>

<span data-ttu-id="d92b0-111">O valor do atributo é armazenado como um **UINT32**, mas deve ser convertido em um valor inteiro assinado de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d92b0-111">The attribute value is stored as a **UINT32**, but should be cast to a 32-bit signed integer value.</span></span> <span data-ttu-id="d92b0-112">O stride pode ser negativo.</span><span class="sxs-lookup"><span data-stu-id="d92b0-112">Stride can be negative.</span></span>

<span data-ttu-id="d92b0-113">Stride é positivo para imagens de cima para baixo e negativo para imagens de baixo para cima.</span><span class="sxs-lookup"><span data-stu-id="d92b0-113">Stride is positive for top-down images, and negative for bottom-up images.</span></span>

<span data-ttu-id="d92b0-114">Esse atributo fornece o stride para uma representação *contígua* da imagem na memória; ou seja, uma representação sem nenhum byte de preenchimento adicional após cada linha.</span><span class="sxs-lookup"><span data-stu-id="d92b0-114">This attribute gives the stride for a *contiguous* representation of the image in memory; that is, a representation with no additional padding bytes after each row.</span></span> <span data-ttu-id="d92b0-115">Se um buffer de mídia der suporte à interface [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) , use o método [**IMF2DBuffer:: Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) para obter o stride real da superfície, que pode incluir bytes de preenchimento extras.</span><span class="sxs-lookup"><span data-stu-id="d92b0-115">If a media buffer supports the [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) interface, use the [**IMF2DBuffer::Lock2D**](/windows/desktop/api/mfobjects/nf-mfobjects-imf2dbuffer-lock2d) method to get the actual stride of the surface, which might include extra padding bytes.</span></span>

<span data-ttu-id="d92b0-116">Para obter mais informações sobre o stride de superfície, consulte [Stride de imagem](image-stride.md).</span><span class="sxs-lookup"><span data-stu-id="d92b0-116">For more information about surface stride, see [Image Stride](image-stride.md).</span></span>

<span data-ttu-id="d92b0-117">Para obter um exemplo de como calcular o stride padrão, consulte [buffers de vídeo não compactados](uncompressed-video-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="d92b0-117">For an example of how to calculate the default stride, see [Uncompressed Video Buffers](uncompressed-video-buffers.md).</span></span>

<span data-ttu-id="d92b0-118">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="d92b0-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d92b0-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d92b0-119">Requirements</span></span>



| <span data-ttu-id="d92b0-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d92b0-120">Requirement</span></span> | <span data-ttu-id="d92b0-121">Valor</span><span class="sxs-lookup"><span data-stu-id="d92b0-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d92b0-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d92b0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d92b0-123">Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]</span><span class="sxs-lookup"><span data-stu-id="d92b0-123">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="d92b0-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d92b0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d92b0-125">Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d92b0-125">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="d92b0-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d92b0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d92b0-127"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d92b0-127"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d92b0-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d92b0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d92b0-129">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d92b0-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d92b0-130">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="d92b0-130">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="d92b0-131">**IMFAttributes:: setuint32**</span><span class="sxs-lookup"><span data-stu-id="d92b0-131">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="d92b0-132">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="d92b0-132">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="d92b0-133">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="d92b0-133">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="d92b0-134">Stride da imagem</span><span class="sxs-lookup"><span data-stu-id="d92b0-134">Image Stride</span></span>](image-stride.md)
</dt> </dl>

 

 




