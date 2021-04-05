---
description: Especifica o número de pontos de extremidade de streaming e o número de fluxos com suporte para um codificador UVC H. 264.
ms.assetid: 343EC59E-30E5-4F37-8B05-60EF51717835
title: Atributo MF_MT_H264_SIMULCAST_SUPPORT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 879490c6984186cf45971d2b122f0c2217b0f164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827205"
---
# <a name="mf_mt_h264_simulcast_support-attribute"></a><span data-ttu-id="e20da-103">Atributo de suporte do MF \_ MT \_ H264 \_ simulcast \_</span><span class="sxs-lookup"><span data-stu-id="e20da-103">MF\_MT\_H264\_SIMULCAST\_SUPPORT attribute</span></span>

<span data-ttu-id="e20da-104">Especifica o número de pontos de extremidade de streaming e o número de fluxos com suporte para um codificador UVC H. 264.</span><span class="sxs-lookup"><span data-stu-id="e20da-104">Specifies the number of streaming endpoints and the number of supported streams for a UVC H.264 encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="e20da-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e20da-105">Data type</span></span>

<span data-ttu-id="e20da-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e20da-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="e20da-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="e20da-107">Get/set</span></span>

<span data-ttu-id="e20da-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="e20da-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="e20da-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="e20da-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="e20da-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="e20da-110">Applies to</span></span>

[<span data-ttu-id="e20da-111">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="e20da-111">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a><span data-ttu-id="e20da-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="e20da-112">Remarks</span></span>

<span data-ttu-id="e20da-113">Esse atributo se aplica aos tipos de mídia para os fluxos H. 264 transmitidos por USB.</span><span class="sxs-lookup"><span data-stu-id="e20da-113">This attribute applies to media types for H.264 streams transmitted over USB.</span></span> <span data-ttu-id="e20da-114">O valor corresponde ao campo **bSimulcastSupport** no descritor de formato de vídeo UVC 1,5 H. 264.</span><span class="sxs-lookup"><span data-stu-id="e20da-114">The value corresponds to the **bSimulcastSupport** field in the UVC 1.5 H.264 video format descriptor.</span></span>

<span data-ttu-id="e20da-115">Esse atributo também é usado com [codificadores de câmera H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).</span><span class="sxs-lookup"><span data-stu-id="e20da-115">This attribute is also used with [H.264 UVC 1.5 camera encoders](camera-encoder-h264-uvc-1-5.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e20da-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e20da-116">Requirements</span></span>



| <span data-ttu-id="e20da-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e20da-117">Requirement</span></span> | <span data-ttu-id="e20da-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e20da-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e20da-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e20da-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e20da-120">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e20da-120">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="e20da-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e20da-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e20da-122">Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e20da-122">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="e20da-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e20da-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e20da-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e20da-124"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e20da-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="e20da-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e20da-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e20da-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="e20da-127">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="e20da-127">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




