---
description: Especifica o tipo de imagem que é a saída de um codificador de vídeo.
ms.assetid: 18A47033-3EAC-46C3-94AB-6ED20732F63C
title: Atributo MFSampleExtension_VideoEncodePictureType (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bfe0df0e4f3163e7c8c0581c5c7c2a854555eec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105811032"
---
# <a name="mfsampleextension_videoencodepicturetype-attribute"></a><span data-ttu-id="b9518-103">\_Atributo MFSampleExtension VideoEncodePictureType</span><span class="sxs-lookup"><span data-stu-id="b9518-103">MFSampleExtension\_VideoEncodePictureType attribute</span></span>

<span data-ttu-id="b9518-104">Especifica o tipo de imagem que é a saída de um codificador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b9518-104">Specifies the type of picture that is output by a video encoder.</span></span>

## <a name="data-type"></a><span data-ttu-id="b9518-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b9518-105">Data type</span></span>

<span data-ttu-id="b9518-106">**eAVEncH264PictureType \_ B** armazenado como **UINT32**</span><span class="sxs-lookup"><span data-stu-id="b9518-106">**eAVEncH264PictureType\_B** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="b9518-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="b9518-107">Get/set</span></span>

<span data-ttu-id="b9518-108">Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="b9518-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="b9518-109">Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="b9518-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="b9518-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="b9518-110">Applies to</span></span>

[<span data-ttu-id="b9518-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="b9518-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="b9518-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9518-112">Remarks</span></span>

<span data-ttu-id="b9518-113">O [**codificador de vídeo H. 264**](h-264-video-encoder.md) define esse atributo nos exemplos de saída que ele gera.</span><span class="sxs-lookup"><span data-stu-id="b9518-113">The [**H.264 Video Encoder**](h-264-video-encoder.md) sets this attribute on the output samples that it generates.</span></span> <span data-ttu-id="b9518-114">O valor do atributo é um membro da enumeração [**eAVEncH264PictureType**](/windows/desktop/api/codecapi/ne-codecapi-eavench264picturetype) .</span><span class="sxs-lookup"><span data-stu-id="b9518-114">The value of the attribute is a member of the [**eAVEncH264PictureType**](/windows/desktop/api/codecapi/ne-codecapi-eavench264picturetype) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9518-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9518-115">Requirements</span></span>



| <span data-ttu-id="b9518-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9518-116">Requirement</span></span> | <span data-ttu-id="b9518-117">Valor</span><span class="sxs-lookup"><span data-stu-id="b9518-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b9518-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9518-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b9518-119">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b9518-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="b9518-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9518-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b9518-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b9518-121">None supported</span></span><br/>                                                          |
| <span data-ttu-id="b9518-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b9518-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9518-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9518-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9518-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9518-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9518-125">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b9518-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b9518-126">**Codificador de vídeo H. 264**</span><span class="sxs-lookup"><span data-stu-id="b9518-126">**H.264 Video Encoder**</span></span>](h-264-video-encoder.md)
</dt> <dt>

[<span data-ttu-id="b9518-127">Atributos de exemplo</span><span class="sxs-lookup"><span data-stu-id="b9518-127">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="b9518-128">Amostras de mídia</span><span class="sxs-lookup"><span data-stu-id="b9518-128">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




