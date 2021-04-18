---
description: Especifica a largura e a altura do vídeo codificado, se o vídeo for cortado.
ms.assetid: d6217250-63ff-4dff-a357-ff4aaa764695
title: Propriedade AVEncVideoEncodeDimension (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f63d0a5c0d1c6af7c20620c315ad25c16eac528
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105778655"
---
# <a name="avencvideoencodedimension-property"></a><span data-ttu-id="ae6e6-103">Propriedade AVEncVideoEncodeDimension</span><span class="sxs-lookup"><span data-stu-id="ae6e6-103">AVEncVideoEncodeDimension property</span></span>

<span data-ttu-id="ae6e6-104">Especifica a largura e a altura do vídeo codificado, se o vídeo for cortado.</span><span class="sxs-lookup"><span data-stu-id="ae6e6-104">Specifies the width and height of the encoded video, if the video is cropped.</span></span>

<span data-ttu-id="ae6e6-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ae6e6-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="ae6e6-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="ae6e6-106">Data type</span></span>

<span data-ttu-id="ae6e6-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="ae6e6-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="ae6e6-108">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="ae6e6-108">Property GUID</span></span>

<span data-ttu-id="ae6e6-109">**CODECAPI \_ AVEncVideoEncodeDimension**</span><span class="sxs-lookup"><span data-stu-id="ae6e6-109">**CODECAPI\_AVEncVideoEncodeDimension**</span></span>

## <a name="property-value"></a><span data-ttu-id="ae6e6-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="ae6e6-110">Property value</span></span>

<span data-ttu-id="ae6e6-111">Os 16 bits superiores do valor contêm a largura em pixels e os 16 bits inferiores contêm a altura em pixels.</span><span class="sxs-lookup"><span data-stu-id="ae6e6-111">The upper 16 bits of the value contain the width in pixels, and the lower 16 bits contain the height in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae6e6-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="ae6e6-112">Remarks</span></span>

<span data-ttu-id="ae6e6-113">Os aplicativos podem definir essa propriedade para cortar o vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="ae6e6-113">Applications can set this property to crop the input video.</span></span> <span data-ttu-id="ae6e6-114">O tamanho especificado deve ser menor que o tamanho dos quadros de vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="ae6e6-114">The specified size must be less than the size of the input video frames.</span></span> <span data-ttu-id="ae6e6-115">Use a propriedade [**AVEncVideoEncodeOffsetOrigin**](avencvideoencodeoffsetorigin-property.md) para especificar os cantos esquerdo e superior do retângulo de recorte.</span><span class="sxs-lookup"><span data-stu-id="ae6e6-115">Use the [**AVEncVideoEncodeOffsetOrigin**](avencvideoencodeoffsetorigin-property.md) property to specify the left and top corners of the clipping rectangle.</span></span>

<span data-ttu-id="ae6e6-116">Os codificadores podem retornar essa propriedade como um recurso.</span><span class="sxs-lookup"><span data-stu-id="ae6e6-116">Encoders can return this property as a capability.</span></span>

<span data-ttu-id="ae6e6-117">Essa propriedade também é usada com [codificadores de câmera H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span><span class="sxs-lookup"><span data-stu-id="ae6e6-117">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

<span data-ttu-id="ae6e6-118">Para codificadores de câmera UVC 1,5, não há suporte para [AVEncVideoEncodeOffsetOrigin](avencvideoencodeoffsetorigin-property.md) .</span><span class="sxs-lookup"><span data-stu-id="ae6e6-118">For UVC 1.5 camera encoders, [AVEncVideoEncodeOffsetOrigin](avencvideoencodeoffsetorigin-property.md) is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae6e6-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae6e6-119">Requirements</span></span>



| <span data-ttu-id="ae6e6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae6e6-120">Requirement</span></span> | <span data-ttu-id="ae6e6-121">Valor</span><span class="sxs-lookup"><span data-stu-id="ae6e6-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae6e6-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae6e6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ae6e6-123">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ae6e6-123">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="ae6e6-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ae6e6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ae6e6-125">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="ae6e6-125">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="ae6e6-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ae6e6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae6e6-127"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae6e6-127"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae6e6-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae6e6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae6e6-129">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="ae6e6-129">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="ae6e6-130">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="ae6e6-130">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

