---
description: Especifica o tamanho do buffer usado durante a codificação. Essa propriedade só se aplica a constantes de taxa de bits constante (CBR) e a taxa de bits variável (VBR).
ms.assetid: 3315785e-306f-44d6-ac39-796025a2da3a
title: Propriedade AVEncCommonBufferSize (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c677c483c320c9dceef391f45c5d8bf163eece0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087849"
---
# <a name="avenccommonbuffersize-property"></a><span data-ttu-id="c05de-104">Propriedade AVEncCommonBufferSize</span><span class="sxs-lookup"><span data-stu-id="c05de-104">AVEncCommonBufferSize property</span></span>

<span data-ttu-id="c05de-105">Especifica o tamanho do buffer usado durante a codificação.</span><span class="sxs-lookup"><span data-stu-id="c05de-105">Specifies the size of the buffer used during encoding.</span></span> <span data-ttu-id="c05de-106">Essa propriedade só se aplica a constantes de taxa de bits constante (CBR) e a taxa de bits variável (VBR).</span><span class="sxs-lookup"><span data-stu-id="c05de-106">This property applies only to constant bit rate (CBR) and variable bit rate (VBR) encoding modes.</span></span>

<span data-ttu-id="c05de-107">Esta propriedade é de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c05de-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="c05de-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="c05de-108">Data type</span></span>

<span data-ttu-id="c05de-109">**UINT32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="c05de-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="c05de-110">GUID da propriedade</span><span class="sxs-lookup"><span data-stu-id="c05de-110">Property GUID</span></span>

<span data-ttu-id="c05de-111">**CODECAPI \_ AVEncCommonBufferSize**</span><span class="sxs-lookup"><span data-stu-id="c05de-111">**CODECAPI\_AVEncCommonBufferSize**</span></span>

## <a name="property-value"></a><span data-ttu-id="c05de-112">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="c05de-112">Property value</span></span>

<span data-ttu-id="c05de-113">Esta propriedade tem um intervalo linear de valores.</span><span class="sxs-lookup"><span data-stu-id="c05de-113">This property has a linear range of values.</span></span> <span data-ttu-id="c05de-114">Para obter o intervalo com suporte, chame [**ICodecAPI:: GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="c05de-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span> <span data-ttu-id="c05de-115">Os intervalos de parâmetros não têm suporte para codificadores de câmera H. 264 UVC 1,5.</span><span class="sxs-lookup"><span data-stu-id="c05de-115">Parameter ranges are not supported for H.264 UVC 1.5 camera encoders.</span></span>

## <a name="remarks"></a><span data-ttu-id="c05de-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c05de-116">Remarks</span></span>

<span data-ttu-id="c05de-117">Para alguns formatos de vídeo, o tamanho do buffer é especificado em bits e para outros, ele é especificado em bytes.</span><span class="sxs-lookup"><span data-stu-id="c05de-117">For some video formats the buffer size is specified in bits and for others it is specified in bytes.</span></span> <span data-ttu-id="c05de-118">Consulte os comentários abaixo para obter informações específicas.</span><span class="sxs-lookup"><span data-stu-id="c05de-118">See the remarks below for specific information.</span></span>

<span data-ttu-id="c05de-119">Para o vídeo MPEG, essa propriedade define o tamanho do buffer do verificador de buffer de vídeo (VBV).</span><span class="sxs-lookup"><span data-stu-id="c05de-119">For MPEG video, this property defines the video buffer verifier (VBV) buffer size.</span></span> <span data-ttu-id="c05de-120">O tamanho do buffer está em bits.</span><span class="sxs-lookup"><span data-stu-id="c05de-120">The size of the buffer is in bits.</span></span>

<span data-ttu-id="c05de-121">Para vídeos H. 264 e vídeo de mídia do Windows, a propriedade define o tamanho do decodificador de referência hipotética (HRD).</span><span class="sxs-lookup"><span data-stu-id="c05de-121">For H.264 video and Windows Media Video, the property defines the hypothetical reference decoder (HRD) size.</span></span> <span data-ttu-id="c05de-122">O tamanho do buffer está em bytes.</span><span class="sxs-lookup"><span data-stu-id="c05de-122">The size of the buffer is in bytes.</span></span>

<span data-ttu-id="c05de-123">Para câmeras de codificação UVC 1,5 H264, o valor de CPB enviado para o codificador de câmera deve ser alinhado em 16 bits.</span><span class="sxs-lookup"><span data-stu-id="c05de-123">For UVC 1.5 H264 encoding cameras, the CPB value sent to the camera encoder must be 16-bit aligned.</span></span> <span data-ttu-id="c05de-124">O tamanho do buffer está em bytes.</span><span class="sxs-lookup"><span data-stu-id="c05de-124">The size of the buffer is in bytes.</span></span>

<span data-ttu-id="c05de-125">Essa propriedade também é usada com [codificadores de câmera H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span><span class="sxs-lookup"><span data-stu-id="c05de-125">This property is also used with [H.264 UVC 1.5 camera encoders](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).</span></span>

## <a name="requirements"></a><span data-ttu-id="c05de-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c05de-126">Requirements</span></span>



| <span data-ttu-id="c05de-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c05de-127">Requirement</span></span> | <span data-ttu-id="c05de-128">Valor</span><span class="sxs-lookup"><span data-stu-id="c05de-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c05de-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c05de-129">Minimum supported client</span></span><br/> | <span data-ttu-id="c05de-130">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c05de-130">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="c05de-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c05de-131">Minimum supported server</span></span><br/> | <span data-ttu-id="c05de-132">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c05de-132">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="c05de-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c05de-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c05de-134"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="c05de-134"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c05de-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="c05de-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c05de-136">Propriedades da API do codec</span><span class="sxs-lookup"><span data-stu-id="c05de-136">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="c05de-137">**Interface ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="c05de-137">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

