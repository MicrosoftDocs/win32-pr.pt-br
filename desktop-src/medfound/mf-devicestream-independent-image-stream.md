---
description: Especifica se o fluxo de imagem em uma origem de captura de vídeo é independente do fluxo de vídeo.
ms.assetid: DC4ED612-593B-40BF-BB42-946149042D1F
title: Atributo MF_DEVICESTREAM_INDEPENDENT_IMAGE_STREAM (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 174e62a1bdd178ad2d8dce7fab5bf9ce3104d834
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105751336"
---
# <a name="mf_devicestream_independent_image_stream-attribute"></a><span data-ttu-id="46d71-103">\_Atributo de \_ \_ fluxo de imagem independente MF DEVICESTREAM \_</span><span class="sxs-lookup"><span data-stu-id="46d71-103">MF\_DEVICESTREAM\_INDEPENDENT\_IMAGE\_STREAM attribute</span></span>

<span data-ttu-id="46d71-104">Especifica se o fluxo de imagem em uma origem de captura de vídeo é independente do fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="46d71-104">Specifies whether the image stream on a video capture source is independent of the video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="46d71-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="46d71-105">Data type</span></span>

<span data-ttu-id="46d71-106">**Bool** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="46d71-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="46d71-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="46d71-107">Remarks</span></span>

<span data-ttu-id="46d71-108">Algumas câmeras de vídeo USB expõem um fluxo que produz imagens ainda.</span><span class="sxs-lookup"><span data-stu-id="46d71-108">Some USB video cameras expose a stream that produces still images.</span></span> <span data-ttu-id="46d71-109">Em algumas câmeras, o fluxo de imagem simplesmente retorna o próximo quadro do fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="46d71-109">In some cameras, the image stream simply returns the next frame from the video stream.</span></span> <span data-ttu-id="46d71-110">Em outras câmeras, o fluxo de imagens funciona independentemente do fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="46d71-110">In other cameras, the image stream functions independently of the video stream.</span></span> <span data-ttu-id="46d71-111">Se a câmera tiver um fluxo de imagem independente, a origem da mídia para o dispositivo de captura definirá esse atributo como **true** no fluxo da imagem.</span><span class="sxs-lookup"><span data-stu-id="46d71-111">If the camera has an independent image stream, the media source for the capture device sets this attribute to **TRUE** on the image stream.</span></span>

<span data-ttu-id="46d71-112">Para obter esse atributo, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="46d71-112">To get this attribute, do the following:</span></span>

1.  <span data-ttu-id="46d71-113">Consulte a origem da mídia para a interface [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) .</span><span class="sxs-lookup"><span data-stu-id="46d71-113">Query the media source for the [**IMFMediaSourceEx**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourceex) interface.</span></span>
2.  <span data-ttu-id="46d71-114">Chame [**IMFMediaSourceEx:: Getstreamattributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) para obter um ponteiro [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="46d71-114">Call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes) to get an [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer for the stream.</span></span>
3.  <span data-ttu-id="46d71-115">Chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) para obter o atributo.</span><span class="sxs-lookup"><span data-stu-id="46d71-115">Call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) to get the attribute.</span></span>

<span data-ttu-id="46d71-116">Esse atributo se aplica somente quando o atributo de [ \_ \_ \_ fluxo de imagem DEVICESTREAM MF](mf-devicestream-image-stream.md) é **true**.</span><span class="sxs-lookup"><span data-stu-id="46d71-116">This attribute applies only when the [MF\_DEVICESTREAM\_IMAGE\_STREAM](mf-devicestream-image-stream.md) attribute is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="46d71-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="46d71-117">Requirements</span></span>



| <span data-ttu-id="46d71-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="46d71-118">Requirement</span></span> | <span data-ttu-id="46d71-119">Valor</span><span class="sxs-lookup"><span data-stu-id="46d71-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="46d71-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46d71-120">Minimum supported client</span></span><br/> | <span data-ttu-id="46d71-121">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="46d71-121">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="46d71-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="46d71-122">Minimum supported server</span></span><br/> | <span data-ttu-id="46d71-123">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="46d71-123">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="46d71-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="46d71-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="46d71-125"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="46d71-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46d71-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="46d71-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46d71-127">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="46d71-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




