---
description: Especifica se um decodificador expõe os tipos de saída IYUV/I420 (adequados para transcodificação) antes de outros formatos.
ms.assetid: 8505CFA1-210A-4DA8-B92A-FCE62F0310E5
title: Atributo MFT_DECODER_EXPOSE_OUTPUT_TYPES_IN_NATIVE_ORDER (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ecf074fa0767552a48e3238374dbd02f077404
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661826"
---
# <a name="mft_decoder_expose_output_types_in_native_order-attribute"></a><span data-ttu-id="2982d-103">O \_ decodificador MFT \_ expõe os \_ \_ tipos \_ de saída no \_ atributo de \_ ordem nativa</span><span class="sxs-lookup"><span data-stu-id="2982d-103">MFT\_DECODER\_EXPOSE\_OUTPUT\_TYPES\_IN\_NATIVE\_ORDER attribute</span></span>

<span data-ttu-id="2982d-104">Especifica se um decodificador expõe os tipos de saída IYUV/I420 (adequados para transcodificação) antes de outros formatos.</span><span class="sxs-lookup"><span data-stu-id="2982d-104">Specifies whether a decoder exposes IYUV/I420 output types (suitable for transcoding) before other formats.</span></span>

## <a name="data-type"></a><span data-ttu-id="2982d-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="2982d-105">Data type</span></span>

<span data-ttu-id="2982d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="2982d-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="2982d-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="2982d-107">Remarks</span></span>

<span data-ttu-id="2982d-108">Esse atributo é uma dica para que o decodificador Organize sua lista de tipos de saída em uma ordem específica, dependendo do uso pretendido, reprodução ou transcodificação.</span><span class="sxs-lookup"><span data-stu-id="2982d-108">This attribute is a hint for the decoder to arrange its list of output types in a particular order, depending on the intended use, either playback or transcode.</span></span>

<span data-ttu-id="2982d-109">Para a maioria dos formatos de codificação (H. 264, MPEG-2, WMV), os decodificadores de vídeo no Microsoft Media Foundation oferecem suporte a várias saídas YUV comuns, incluindo NV12, YV12, YUY2, IYUV e I420.</span><span class="sxs-lookup"><span data-stu-id="2982d-109">For most encoding formats (H.264, MPEG-2, WMV), the video decoders in Microsoft Media Foundation support several common YUV outputs, including NV12, YV12, YUY2, IYUV, and I420.</span></span> <span data-ttu-id="2982d-110">O decodificador oferece uma lista ordenada de tipos de saída por meio de seu método [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) .</span><span class="sxs-lookup"><span data-stu-id="2982d-110">The decoder offers an ordered list of output types through its [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method.</span></span>

<span data-ttu-id="2982d-111">Para reprodução, o NV12 é o formato mais eficiente e com suporte amplo.</span><span class="sxs-lookup"><span data-stu-id="2982d-111">For playback, NV12 is the most efficient and widely supported format.</span></span> <span data-ttu-id="2982d-112">Portanto, por padrão, os decodificadores normalmente oferecem NV12 como o primeiro tipo de saída na lista.</span><span class="sxs-lookup"><span data-stu-id="2982d-112">Therefore, by default, decoders typically offer NV12 as the first output type in the list.</span></span> <span data-ttu-id="2982d-113">Isso minimiza o tempo necessário para resolver o tipo de mídia ao criar uma topologia de reprodução.</span><span class="sxs-lookup"><span data-stu-id="2982d-113">This minimizes the time needed to resolve the media type when building a playback topology.</span></span> <span data-ttu-id="2982d-114">Para transcodificação, no entanto, IYUV ou I420 são mais eficientes para a CPU e normalmente são preferenciais por codificadores.</span><span class="sxs-lookup"><span data-stu-id="2982d-114">For transcoding, however, IYUV or I420 are more efficient for the CPU and are typically preferred by encoders.</span></span>

<span data-ttu-id="2982d-115">Se um decodificador oferecer suporte a esse atributo, o atributo terá o seguinte comportamento:</span><span class="sxs-lookup"><span data-stu-id="2982d-115">If a decoder supports this attribute, the attribute has the following behavior:</span></span>

-   <span data-ttu-id="2982d-116">Se o atributo tiver um valor diferente de zero, IYUV e I420 aparecerão primeiro na lista de tipos de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="2982d-116">If the attribute has a non-zero value, IYUV and I420 appear first in the list of output media types.</span></span> <span data-ttu-id="2982d-117">Essa configuração é mais eficiente para transcodificação.</span><span class="sxs-lookup"><span data-stu-id="2982d-117">This setting is most efficient for transcoding.</span></span>
-   <span data-ttu-id="2982d-118">Se o atributo for zero, NV12 aparecerá primeiro na lista de tipos de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="2982d-118">If the attribute is zero, NV12 appears first in the list of output media types.</span></span> <span data-ttu-id="2982d-119">Essa configuração é mais eficiente para reprodução e é o padrão.</span><span class="sxs-lookup"><span data-stu-id="2982d-119">This setting is most efficient for playback, and is the default.</span></span>

<span data-ttu-id="2982d-120">Para definir este atributo:</span><span class="sxs-lookup"><span data-stu-id="2982d-120">To set this attribute:</span></span>

1.  <span data-ttu-id="2982d-121">Chame [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) no decodificador para obter um ponteiro [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="2982d-121">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the decoder to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="2982d-122">Chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) para adicionar o atributo.</span><span class="sxs-lookup"><span data-stu-id="2982d-122">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to add the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="2982d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2982d-123">Requirements</span></span>



| <span data-ttu-id="2982d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="2982d-124">Requirement</span></span> | <span data-ttu-id="2982d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="2982d-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2982d-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2982d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="2982d-127">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="2982d-127">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="2982d-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2982d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="2982d-129">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2982d-129">None supported</span></span><br/>                                                                |
| <span data-ttu-id="2982d-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2982d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="2982d-131"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="2982d-131"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2982d-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="2982d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2982d-133">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2982d-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




