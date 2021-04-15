---
description: Este tópico descreve a diferença entre os tipos de mídia completa e os tipos de mídia parcial.
ms.assetid: 59b3f0b5-f378-41e6-9b49-85a16bb6e008
title: Tipos de mídia completos e parciais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac772c09668ee3db96e42d25b3089fa74be104af
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104506351"
---
# <a name="complete-and-partial-media-types"></a><span data-ttu-id="fadbd-103">Tipos de mídia completos e parciais</span><span class="sxs-lookup"><span data-stu-id="fadbd-103">Complete and Partial Media Types</span></span>

<span data-ttu-id="fadbd-104">Este tópico descreve a diferença entre os tipos de mídia completa e os tipos de mídia parcial.</span><span class="sxs-lookup"><span data-stu-id="fadbd-104">This topic describes the difference between complete media types and partial media types.</span></span>

## <a name="complete-media-types"></a><span data-ttu-id="fadbd-105">Tipos de mídia completos</span><span class="sxs-lookup"><span data-stu-id="fadbd-105">Complete Media Types</span></span>

<span data-ttu-id="fadbd-106">Um tipo de mídia *completo* é aquele que define totalmente o formato do fluxo de mídia.</span><span class="sxs-lookup"><span data-stu-id="fadbd-106">A *complete* media type is one that fully defines the format of the media stream.</span></span> <span data-ttu-id="fadbd-107">Dado um tipo de mídia completo, um componente de pipeline pode analisar os dados de fluxo associados ao tipo de mídia, sem ambiguidade.</span><span class="sxs-lookup"><span data-stu-id="fadbd-107">Given a complete media type, a pipeline component can parse the stream data associated with the media type, with no ambiguity.</span></span>

<span data-ttu-id="fadbd-108">Para formatos descompactados, os tópicos a seguir definem os atributos necessários para um tipo de mídia completo:</span><span class="sxs-lookup"><span data-stu-id="fadbd-108">For uncompressed formats, the following topics define the attributes that are required for a complete media type:</span></span>

-   <span data-ttu-id="fadbd-109">Áudio: [tipos de mídia de áudio não compactados](uncompressed-audio-media-types.md)</span><span class="sxs-lookup"><span data-stu-id="fadbd-109">Audio: [Uncompressed Audio Media Types](uncompressed-audio-media-types.md)</span></span>
-   <span data-ttu-id="fadbd-110">Vídeo: [tipos de mídia de vídeo descompactados](uncompressed-video-media-types.md)</span><span class="sxs-lookup"><span data-stu-id="fadbd-110">Video: [Uncompressed Video Media Types](uncompressed-video-media-types.md)</span></span>

<span data-ttu-id="fadbd-111">Para fluxos compactados (ou *codificados*), a definição de um tipo de mídia completo é definida pelo codec.</span><span class="sxs-lookup"><span data-stu-id="fadbd-111">For compressed (or *encoded*) streams, the definition of a complete media type is defined by the codec.</span></span> <span data-ttu-id="fadbd-112">No entanto, se algum atributo de tipo descompactado for conhecido para o fluxo compactado, esses valores deverão ser incluídos no tipo de mídia para o fluxo compactado.</span><span class="sxs-lookup"><span data-stu-id="fadbd-112">However, if any uncompressed type attributes are known for the compressed stream, these values should be included in the media type for the compressed stream.</span></span> <span data-ttu-id="fadbd-113">Por exemplo, se o tamanho do quadro for conhecido, defina o atributo de [**\_ tamanho do \_ quadro \_ MF MT**](mf-mt-frame-size-attribute.md) no tipo de mídia, embora tecnicamente um fluxo compactado não tenha um tamanho de quadro.</span><span class="sxs-lookup"><span data-stu-id="fadbd-113">For example, if the frame size is known, set the [**MF\_MT\_FRAME\_SIZE**](mf-mt-frame-size-attribute.md) attribute on the media type, even though technically a compressed stream does not have a frame size.</span></span>

## <a name="partial-media-types"></a><span data-ttu-id="fadbd-114">Tipos de mídia parciais</span><span class="sxs-lookup"><span data-stu-id="fadbd-114">Partial Media Types</span></span>

<span data-ttu-id="fadbd-115">Um tipo de mídia *parcial* não tem um ou mais dos atributos necessários para um tipo de mídia completo.</span><span class="sxs-lookup"><span data-stu-id="fadbd-115">A *partial* media type is lacks one or more of the attributes needed for a complete media type.</span></span> <span data-ttu-id="fadbd-116">Ao enumerar possíveis tipos de mídia, um componente Microsoft Media Foundation pode deixar um valor definido, para indicar que ele pode lidar com qualquer valor.</span><span class="sxs-lookup"><span data-stu-id="fadbd-116">When enumerating possible media types, a Microsoft Media Foundation component may leave a value unset, to indicate that it can handle any value.</span></span> <span data-ttu-id="fadbd-117">Por exemplo, um processador de vídeo pode deixar a desdefinição do atributo de [**\_ taxa de \_ quadros \_ MF MT**](mf-mt-frame-rate-attribute.md) , para indicar que ele pode lidar com qualquer taxa de quadros e executará uma conversão de taxa de quadros, se necessário.</span><span class="sxs-lookup"><span data-stu-id="fadbd-117">For example, a video processor might leave the [**MF\_MT\_FRAME\_RATE**](mf-mt-frame-rate-attribute.md) attribute unset, to indicate that it can handle any frame rate, and will perform a frame-rate conversion if necessary.</span></span>

<span data-ttu-id="fadbd-118">Se você criar um tipo de mídia parcial, ainda deverá incluir tantas informações quantas forem conhecidas.</span><span class="sxs-lookup"><span data-stu-id="fadbd-118">If you create a partial media type, you should still include as much information as you know.</span></span> <span data-ttu-id="fadbd-119">No entanto, um tipo de mídia não deve incluir informações incertas.</span><span class="sxs-lookup"><span data-stu-id="fadbd-119">However, a media type must not include information that is uncertain.</span></span> <span data-ttu-id="fadbd-120">É melhor que as informações estejam ausentes do que incorreto.</span><span class="sxs-lookup"><span data-stu-id="fadbd-120">It is better for information to be missing than wrong.</span></span>

<span data-ttu-id="fadbd-121">No mínimo, um tipo de mídia parcial deve incluir apenas dois atributos: [**\_ \_ \_ tipo principal MF MT**](mf-mt-major-type-attribute.md) e [**\_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="fadbd-121">At a minimum, a partial media type should include just two attributes: [**MF\_MT\_MAJOR\_TYPE**](mf-mt-major-type-attribute.md) and [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md).</span></span>

<span data-ttu-id="fadbd-122">Às vezes Media Foundation componentes devem fornecer tipos de mídia completos:</span><span class="sxs-lookup"><span data-stu-id="fadbd-122">Sometimes Media Foundation components must provide complete media types:</span></span>

-   <span data-ttu-id="fadbd-123">As fontes de mídia devem fornecer tipos de saída completos.</span><span class="sxs-lookup"><span data-stu-id="fadbd-123">Media sources must provide complete output types.</span></span>
-   <span data-ttu-id="fadbd-124">Os decodificadores devem fornecer tipos de saída completos, depois que o tipo de entrada é definido.</span><span class="sxs-lookup"><span data-stu-id="fadbd-124">Decoders must provide complete output types, after the input type is set.</span></span> <span data-ttu-id="fadbd-125">Antes que o tipo de entrada seja definido, um decodificador pode fornecer um tipo de saída parcial.</span><span class="sxs-lookup"><span data-stu-id="fadbd-125">Before the input type is set, a decoder might provide a partial output type.</span></span>
-   <span data-ttu-id="fadbd-126">Os codificadores devem fornecer tipos de entrada completos, depois que o tipo de saída for definido.</span><span class="sxs-lookup"><span data-stu-id="fadbd-126">Encoders must provide complete input types, after the output type is set.</span></span> <span data-ttu-id="fadbd-127">Antes de o tipo de saída ser definido, um codificador pode fornecer um tipo de entrada parcial.</span><span class="sxs-lookup"><span data-stu-id="fadbd-127">Before the output type is set, an encoder might provide a partial input type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fadbd-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fadbd-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fadbd-129">Tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="fadbd-129">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 



