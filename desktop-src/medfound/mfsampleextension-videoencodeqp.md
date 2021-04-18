---
description: Especifica o parâmetro de quantificação (QP) que foi usado para codificar uma amostra de vídeo.
ms.assetid: F7C4FEFC-FEE7-4614-BC90-4F9D5D878F49
title: Atributo MFSampleExtension_VideoEncodeQP (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 721f5df00ff24b307daed2ccbcbf61a04b129db2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791291"
---
# <a name="mfsampleextension_videoencodeqp-attribute"></a><span data-ttu-id="b10e4-103">\_Atributo MFSampleExtension VideoEncodeQP</span><span class="sxs-lookup"><span data-stu-id="b10e4-103">MFSampleExtension\_VideoEncodeQP attribute</span></span>

<span data-ttu-id="b10e4-104">Especifica o parâmetro de quantificação (QP) que foi usado para codificar uma amostra de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b10e4-104">Specifies the quantization parameter (QP) that was used to encode a video sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="b10e4-105">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="b10e4-105">Data type</span></span>

<span data-ttu-id="b10e4-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="b10e4-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="b10e4-107">Obter/definir</span><span class="sxs-lookup"><span data-stu-id="b10e4-107">Get/set</span></span>

<span data-ttu-id="b10e4-108">Para obter esse atributo, chame [**IMFAttributes:: getuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="b10e4-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="b10e4-109">Para definir esse atributo, chame [**IMFAttributes:: setuint64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="b10e4-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="b10e4-110">Aplica-se a</span><span class="sxs-lookup"><span data-stu-id="b10e4-110">Applies to</span></span>

[<span data-ttu-id="b10e4-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="b10e4-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="b10e4-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="b10e4-112">Remarks</span></span>

<span data-ttu-id="b10e4-113">O [**codificador de vídeo H. 264**](h-264-video-encoder.md) define esse atributo nos exemplos de saída que ele gera.</span><span class="sxs-lookup"><span data-stu-id="b10e4-113">The [**H.264 Video Encoder**](h-264-video-encoder.md) sets this attribute on the output samples that it generates.</span></span>

## <a name="requirements"></a><span data-ttu-id="b10e4-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b10e4-114">Requirements</span></span>



| <span data-ttu-id="b10e4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b10e4-115">Requirement</span></span> | <span data-ttu-id="b10e4-116">Valor</span><span class="sxs-lookup"><span data-stu-id="b10e4-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b10e4-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b10e4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b10e4-118">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="b10e4-118">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="b10e4-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b10e4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b10e4-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="b10e4-120">None supported</span></span><br/>                                                          |
| <span data-ttu-id="b10e4-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b10e4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b10e4-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b10e4-122"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b10e4-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="b10e4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b10e4-124">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b10e4-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b10e4-125">**Codificador de vídeo H. 264**</span><span class="sxs-lookup"><span data-stu-id="b10e4-125">**H.264 Video Encoder**</span></span>](h-264-video-encoder.md)
</dt> <dt>

[<span data-ttu-id="b10e4-126">Atributos de exemplo</span><span class="sxs-lookup"><span data-stu-id="b10e4-126">Sample Attributes</span></span>](sample-attributes.md)
</dt> <dt>

[<span data-ttu-id="b10e4-127">Amostras de mídia</span><span class="sxs-lookup"><span data-stu-id="b10e4-127">Media Samples</span></span>](media-samples.md)
</dt> </dl>

 

 




