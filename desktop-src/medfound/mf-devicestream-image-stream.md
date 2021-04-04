---
description: Especifica se um fluxo em uma origem de captura de vídeo é um fluxo de imagem ainda.
ms.assetid: 52251A45-3603-41C7-A869-7F6319BD337F
title: Atributo MF_DEVICESTREAM_IMAGE_STREAM (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 382ce587574d6ec46509a460dfb964e23dd416d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647386"
---
# <a name="mf_devicestream_image_stream-attribute"></a><span data-ttu-id="f52fe-103">\_Atributo de \_ fluxo de imagem DEVICESTREAM MF \_</span><span class="sxs-lookup"><span data-stu-id="f52fe-103">MF\_DEVICESTREAM\_IMAGE\_STREAM attribute</span></span>

<span data-ttu-id="f52fe-104">Especifica se um fluxo em uma origem de captura de vídeo é um fluxo de imagem ainda.</span><span class="sxs-lookup"><span data-stu-id="f52fe-104">Specifies whether a stream on a video capture source is a still-image stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="f52fe-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="f52fe-105">Data type</span></span>

<span data-ttu-id="f52fe-106">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="f52fe-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f52fe-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="f52fe-107">Remarks</span></span>

<span data-ttu-id="f52fe-108">Algumas câmeras de vídeo expõem um fluxo de imagem ainda que produz imagens de alta resolução.</span><span class="sxs-lookup"><span data-stu-id="f52fe-108">Some video cameras expose a still-image stream that produces high-resolution images.</span></span> <span data-ttu-id="f52fe-109">O fluxo de imagem pode produzir imagens descompactadas ou imagens JPEG.</span><span class="sxs-lookup"><span data-stu-id="f52fe-109">The image stream might produce uncompressed images or JPEG images.</span></span> <span data-ttu-id="f52fe-110">Se a câmera tiver um fluxo de imagem, a origem da mídia para o dispositivo de captura definirá esse atributo como **true** no fluxo da imagem.</span><span class="sxs-lookup"><span data-stu-id="f52fe-110">If the camera has an image stream, the media source for the capture device sets this attribute to **TRUE** on the image stream.</span></span>

<span data-ttu-id="f52fe-111">Para obter esse atributo, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f52fe-111">To get this attribute, do the following:</span></span>

1.  <span data-ttu-id="f52fe-112">Consulte a origem da mídia para a interface [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .</span><span class="sxs-lookup"><span data-stu-id="f52fe-112">Query the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span>
2.  <span data-ttu-id="f52fe-113">Chame [**IMFMediaSourceEx:: Getstreamattributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) para obter um ponteiro [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="f52fe-113">Call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer for the stream.</span></span>
3.  <span data-ttu-id="f52fe-114">Chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) para obter o atributo.</span><span class="sxs-lookup"><span data-stu-id="f52fe-114">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="f52fe-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f52fe-115">Requirements</span></span>



| <span data-ttu-id="f52fe-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f52fe-116">Requirement</span></span> | <span data-ttu-id="f52fe-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f52fe-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f52fe-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f52fe-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f52fe-119">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f52fe-119">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f52fe-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f52fe-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f52fe-121">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f52fe-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f52fe-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f52fe-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f52fe-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f52fe-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f52fe-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="f52fe-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f52fe-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f52fe-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




