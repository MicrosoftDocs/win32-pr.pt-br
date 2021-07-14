---
description: Relata os metadados e o buffer de máscara para uma máscara de segmentação em segundo plano que distingue entre o plano de fundo e o primeiro plano de um quadro de vídeo.
title: MF_CAPTURE_METADATA_FRAME_BACKGROUND_MASK atributo (Mfapi.h)
ms.topic: reference
ms.date: 06/01/2021
ms.openlocfilehash: 3dc28d92566b14a44f61fe84bd3f68688c464d4a
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691835"
---
# <a name="mf_capture_metadata_frame_background_mask-attribute"></a><span data-ttu-id="6feb5-103">Atributo MF \_ CAPTURE \_ METADATA \_ FRAME BACKGROUND \_ \_ MASK</span><span class="sxs-lookup"><span data-stu-id="6feb5-103">MF\_CAPTURE\_METADATA\_FRAME\_BACKGROUND\_MASK attribute</span></span>

<span data-ttu-id="6feb5-104">Relata os metadados e o buffer de máscara para uma máscara de segmentação em segundo plano que distingue entre o plano de fundo e o primeiro plano de um quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6feb5-104">Reports the metadata and mask buffer for a background segmentation mask that distinguishes between the background and foreground of a video frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="6feb5-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="6feb5-105">Data type</span></span>

<span data-ttu-id="6feb5-106">**Blob**</span><span class="sxs-lookup"><span data-stu-id="6feb5-106">**BLOB**</span></span>

## <a name="remarks"></a><span data-ttu-id="6feb5-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="6feb5-107">Remarks</span></span>

<span data-ttu-id="6feb5-108">Os dados carregados por esse atributo são uma estrutura KSCAMERA_METADATA_BACKGROUNDSEGMENTATIONMASK que contém informações sobre as dimensões da máscara em segundo plano, bem como sua cobertura do quadro do qual ele é inferido, que é [o](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-kscamera_metadata_backgroundsegmentationmask) quadro que é produzido pelo fluxo.</span><span class="sxs-lookup"><span data-stu-id="6feb5-108">The data carried by this attribute is a [KSCAMERA_METADATA_BACKGROUNDSEGMENTATIONMASK](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-kscamera_metadata_backgroundsegmentationmask) structure that contains information about the dimensions of the background mask as well as its coverage of the frame it is inferred from, which is the frame that is outputted by the stream.</span></span> <span data-ttu-id="6feb5-109">Ele também carrega um buffer contíguo que representa a máscara a ser aproveitada pelo aplicativo consumidor para definir quais pixels são considerados parte do primeiro plano ou da tela de fundo.</span><span class="sxs-lookup"><span data-stu-id="6feb5-109">It also carries a contiguous buffer representing the mask to be leveraged by the consuming app to define which pixels are considered part of the foreground or background.</span></span> <span data-ttu-id="6feb5-110">O dimensionamento e a correlação de coordenadas de imagem da máscara em relação ao quadro são tratados pelo aplicativo consumidor.</span><span class="sxs-lookup"><span data-stu-id="6feb5-110">The scaling and image coordinate correlation of the mask regarding the frame is handled by the consuming app.</span></span> 

## <a name="requirements"></a><span data-ttu-id="6feb5-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6feb5-111">Requirements</span></span>



| <span data-ttu-id="6feb5-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="6feb5-112">Requirement</span></span> | <span data-ttu-id="6feb5-113">Valor</span><span class="sxs-lookup"><span data-stu-id="6feb5-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6feb5-114">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6feb5-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6feb5-115">Windows Build 22000t</span><span class="sxs-lookup"><span data-stu-id="6feb5-115">Windows Build 22000t</span></span><br/>                          |
| <span data-ttu-id="6feb5-116">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6feb5-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6feb5-117">Windows Build 22000</span><span class="sxs-lookup"><span data-stu-id="6feb5-117">Windows Build 22000</span></span><br/>                      |
| <span data-ttu-id="6feb5-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6feb5-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="6feb5-119"><dt>Mfapi.h</dt></span><span class="sxs-lookup"><span data-stu-id="6feb5-119"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6feb5-120">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6feb5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6feb5-121">Lista alfabética de Media Foundation atributos</span><span class="sxs-lookup"><span data-stu-id="6feb5-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6feb5-122">**IMFAttributes::GetBlob**</span><span class="sxs-lookup"><span data-stu-id="6feb5-122">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="6feb5-123">**IMFAttributes::SetBlob**</span><span class="sxs-lookup"><span data-stu-id="6feb5-123">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="6feb5-124">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="6feb5-124">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="6feb5-125">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="6feb5-125">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 




