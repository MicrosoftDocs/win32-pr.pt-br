---
description: Especifica os cantos esquerdo e superior do retângulo de recorte, se o vídeo for cortado.
ms.assetid: 8ce8b3b8-dd91-41e1-a4ba-b0c2d9d0edd2
title: Propriedade AVEncVideoEncodeOffsetOrigin (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7db4d685942b8c21f2d5047003f2172c54b1d50d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087508"
---
# <a name="avencvideoencodeoffsetorigin-property"></a><span data-ttu-id="8b848-103">Propriedade AVEncVideoEncodeOffsetOrigin</span><span class="sxs-lookup"><span data-stu-id="8b848-103">AVEncVideoEncodeOffsetOrigin property</span></span>

<span data-ttu-id="8b848-104">Especifica os cantos esquerdo e superior do retângulo de recorte, se o vídeo for cortado.</span><span class="sxs-lookup"><span data-stu-id="8b848-104">Specifies the left and top corners of the clipping rectangle, if the video is cropped.</span></span>

<span data-ttu-id="8b848-105">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="8b848-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="8b848-106">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="8b848-106">Data type</span></span>

<span data-ttu-id="8b848-107">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="8b848-107">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="8b848-108">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="8b848-108">Property GUID</span></span>

<span data-ttu-id="8b848-109">**CODECAPI \_ AVEncVideoEncodeOffsetOrigin**</span><span class="sxs-lookup"><span data-stu-id="8b848-109">**CODECAPI\_AVEncVideoEncodeOffsetOrigin**</span></span>

## <a name="property-value"></a><span data-ttu-id="8b848-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="8b848-110">Property value</span></span>

<span data-ttu-id="8b848-111">Os 16 bits superiores do valor contêm o deslocamento da borda esquerda do quadro de entrada, em pixels.</span><span class="sxs-lookup"><span data-stu-id="8b848-111">The upper 16 bits of the value contain the offset from the left edge of the input frame, in pixels.</span></span> <span data-ttu-id="8b848-112">Os 16 bits inferiores contêm o deslocamento da borda superior do quadro de entrada, em pixels.</span><span class="sxs-lookup"><span data-stu-id="8b848-112">The lower 16 bits contain the offset from the top edge of the input frame, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b848-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b848-113">Remarks</span></span>

<span data-ttu-id="8b848-114">Os aplicativos podem definir essa propriedade para cortar o vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="8b848-114">Applications can set this property to crop the input video.</span></span> <span data-ttu-id="8b848-115">Use a propriedade [**AVEncVideoEncodeDimension**](avencvideoencodedimension-property.md) para especificar a largura e a altura do retângulo de recorte.</span><span class="sxs-lookup"><span data-stu-id="8b848-115">Use the [**AVEncVideoEncodeDimension**](avencvideoencodedimension-property.md) property to specify the width and height of the clipping rectangle.</span></span>

## <a name="requirements"></a><span data-ttu-id="8b848-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b848-116">Requirements</span></span>



| <span data-ttu-id="8b848-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b848-117">Requirement</span></span> | <span data-ttu-id="8b848-118">Valor</span><span class="sxs-lookup"><span data-stu-id="8b848-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8b848-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b848-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8b848-120">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8b848-120">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="8b848-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b848-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8b848-122">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="8b848-122">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="8b848-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8b848-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b848-124"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b848-124"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b848-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b848-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b848-126">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="8b848-126">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="8b848-127">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="8b848-127">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




