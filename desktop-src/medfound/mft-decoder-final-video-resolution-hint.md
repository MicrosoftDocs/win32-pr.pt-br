---
description: Especifica a resolução final de saída da imagem decodificada, após o processamento do vídeo.
ms.assetid: 067867D8-155C-4406-BE07-720016B2AEBC
title: Atributo MFT_DECODER_FINAL_VIDEO_RESOLUTION_HINT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7bbc0f01ef2a1d7062c6ab58c528b015383fc68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164913"
---
# <a name="mft_decoder_final_video_resolution_hint-attribute"></a><span data-ttu-id="e5041-103">\_Atributo de \_ \_ dica de resolução de vídeo final \_ do DEcodificador de MFT \_</span><span class="sxs-lookup"><span data-stu-id="e5041-103">MFT\_DECODER\_FINAL\_VIDEO\_RESOLUTION\_HINT attribute</span></span>

<span data-ttu-id="e5041-104">Especifica a resolução final de saída da imagem decodificada, após o processamento do vídeo.</span><span class="sxs-lookup"><span data-stu-id="e5041-104">Specifies the final output resolution of the decoded image, after video processing.</span></span>

## <a name="data-type"></a><span data-ttu-id="e5041-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e5041-105">Data type</span></span>

<span data-ttu-id="e5041-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="e5041-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="e5041-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="e5041-107">Remarks</span></span>

<span data-ttu-id="e5041-108">Há suporte para esse atributo em alguns decodificadores de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e5041-108">This attribute is supported by some video decoders.</span></span> <span data-ttu-id="e5041-109">Um aplicativo pode definir esse atributo para indicar a largura e a altura da imagem após o processamento do vídeo.</span><span class="sxs-lookup"><span data-stu-id="e5041-109">An application can set this attribute to indicate the width and height of the image after video processing.</span></span> <span data-ttu-id="e5041-110">O decodificador pode usar essas informações para otimizar o processo de decodificação, especialmente se o tamanho final da imagem for muito menor do que o tamanho da imagem nativa.</span><span class="sxs-lookup"><span data-stu-id="e5041-110">The decoder can use this information to optimize the decoding process, especially if the final image size is much smaller than the native image size.</span></span> <span data-ttu-id="e5041-111">Por exemplo, o decodificador pode ignorar um filtro fora de loop.</span><span class="sxs-lookup"><span data-stu-id="e5041-111">For example, the decoder might skip an out-of-loop filter.</span></span>

<span data-ttu-id="e5041-112">Os bits superiores de 32 contêm a largura e os bits de 32 inferiores contêm a altura.</span><span class="sxs-lookup"><span data-stu-id="e5041-112">The upper 32 bits contain the width and the lower 32 bits contain the height.</span></span>

<span data-ttu-id="e5041-113">Para definir este atributo:</span><span class="sxs-lookup"><span data-stu-id="e5041-113">To set this attribute:</span></span>

1.  <span data-ttu-id="e5041-114">Chame [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) no decodificador para obter um ponteiro [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="e5041-114">Call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) on the decoder to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer.</span></span>
2.  <span data-ttu-id="e5041-115">Chame [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) para adicionar o atributo.</span><span class="sxs-lookup"><span data-stu-id="e5041-115">Call [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) to add the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5041-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5041-116">Requirements</span></span>



| <span data-ttu-id="e5041-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5041-117">Requirement</span></span> | <span data-ttu-id="e5041-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e5041-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5041-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5041-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e5041-120">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e5041-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="e5041-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e5041-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e5041-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="e5041-122">None supported</span></span><br/>                                                                |
| <span data-ttu-id="e5041-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e5041-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5041-124"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5041-124"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5041-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="e5041-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5041-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e5041-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e5041-127">Atributos de transformação</span><span class="sxs-lookup"><span data-stu-id="e5041-127">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




