---
description: Especifica primárias de cores personalizadas para um tipo de mídia de vídeo.
ms.assetid: dc5df755-53cf-4910-af42-309f1f46b1ed
title: Atributo MF_MT_CUSTOM_VIDEO_PRIMARIES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3286d63e39638f74cacafa1b4376b28c7703f7c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782379"
---
# <a name="mf_mt_custom_video_primaries-attribute"></a><span data-ttu-id="5eba2-103">\_Atributo de \_ \_ \_ primários de vídeo de MF MT</span><span class="sxs-lookup"><span data-stu-id="5eba2-103">MF\_MT\_CUSTOM\_VIDEO\_PRIMARIES attribute</span></span>

<span data-ttu-id="5eba2-104">Especifica primárias de cores personalizadas para um tipo de mídia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5eba2-104">Specifies custom color primaries for a video media type.</span></span>

## <a name="data-type"></a><span data-ttu-id="5eba2-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="5eba2-105">Data type</span></span>

<span data-ttu-id="5eba2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="5eba2-106">**UINT32**</span></span>

<span data-ttu-id="5eba2-107">Matriz de bytes</span><span class="sxs-lookup"><span data-stu-id="5eba2-107">Byte array</span></span>

## <a name="remarks"></a><span data-ttu-id="5eba2-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="5eba2-108">Remarks</span></span>

<span data-ttu-id="5eba2-109">Os dados de atributo são uma estrutura [**\_ primária de \_ vídeo \_ de MT personalizado**](/windows/desktop/api/mfapi/ns-mfapi-mt_custom_video_primaries) .</span><span class="sxs-lookup"><span data-stu-id="5eba2-109">The attribute data is an [**MT\_CUSTOM\_VIDEO\_PRIMARIES**](/windows/desktop/api/mfapi/ns-mfapi-mt_custom_video_primaries) structure.</span></span>

<span data-ttu-id="5eba2-110">Esse atributo especifica o volume de cor real de conteúdo ou uma exibição.</span><span class="sxs-lookup"><span data-stu-id="5eba2-110">This attribute specifies the actual color volume of content or a display.</span></span> <span data-ttu-id="5eba2-111">As informações de Master volume de cores CEA-861,3/SMPTE ST. 2086 são armazenadas nesse atributo por decodificadores.</span><span class="sxs-lookup"><span data-stu-id="5eba2-111">CEA-861.3 / SMPTE ST.2086 color volume mastering information is stored in this attribute by decoders.</span></span> <span data-ttu-id="5eba2-112">Observe que esse atributo não substitui o atributo [**de \_ \_ \_ primárias de vídeo MF MT**](mf-mt-video-primaries-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="5eba2-112">Note that this attribute does not replace the [**MF\_MT\_VIDEO\_PRIMARIES**](mf-mt-video-primaries-attribute.md)attribute.</span></span> <span data-ttu-id="5eba2-113">Esse atributo descreve uma dica sobre o volume de cores do conteúdo, enquanto **os \_ \_ \_ primários de vídeo MF MT** descrevem os primários de cor nos quais o conteúdo é realmente codificado (por exemplo: o significado de 1,0 nos canais R/g/B de uma representação de ponto flutuante).</span><span class="sxs-lookup"><span data-stu-id="5eba2-113">This attribute describes a hint about the color volume of the content, whereas **MF\_MT\_VIDEO\_PRIMARIES** describes the color primaries in which the content is actually coded (e.g: the meaning of 1.0 in the R/G/B channels of a floating point representation).</span></span>

<span data-ttu-id="5eba2-114">A constante de GUID para esse atributo é exportada de mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="5eba2-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="5eba2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5eba2-115">Requirements</span></span>



| <span data-ttu-id="5eba2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5eba2-116">Requirement</span></span> | <span data-ttu-id="5eba2-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5eba2-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5eba2-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5eba2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5eba2-119">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5eba2-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5eba2-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5eba2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5eba2-121">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5eba2-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5eba2-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5eba2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5eba2-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5eba2-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5eba2-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="5eba2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5eba2-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5eba2-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="5eba2-126">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="5eba2-126">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="5eba2-127">**IMFAttributes:: getBlob**</span><span class="sxs-lookup"><span data-stu-id="5eba2-127">**IMFAttributes::GetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[<span data-ttu-id="5eba2-128">**IMFAttributes:: setBlob**</span><span class="sxs-lookup"><span data-stu-id="5eba2-128">**IMFAttributes::SetBlob**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[<span data-ttu-id="5eba2-129">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="5eba2-129">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

 




