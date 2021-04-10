---
description: Este tópico fornece algumas diretrizes para implementar um decodificador ou um codificador como uma Media Foundation transformação (MFT).
ms.assetid: b15bda0a-0fdd-4601-975d-a71c47c974bf
title: Implementando uma MFT do codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4412db23747e9a6b3468e9e428120d099b2445ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171732"
---
# <a name="implementing-a-codec-mft"></a><span data-ttu-id="f9ac0-103">Implementando uma MFT do codec</span><span class="sxs-lookup"><span data-stu-id="f9ac0-103">Implementing a Codec MFT</span></span>

<span data-ttu-id="f9ac0-104">Este tópico fornece algumas diretrizes para implementar um decodificador ou um codificador como uma Media Foundation transformação (MFT).</span><span class="sxs-lookup"><span data-stu-id="f9ac0-104">This topic provides some guidelines for implementing a decoder or encoder as a Media Foundation Transform (MFT) .</span></span>

-   [<span data-ttu-id="f9ac0-105">Codificadores</span><span class="sxs-lookup"><span data-stu-id="f9ac0-105">Encoders</span></span>](#encoders)
    -   [<span data-ttu-id="f9ac0-106">Negociação de formato do codificador</span><span class="sxs-lookup"><span data-stu-id="f9ac0-106">Encoder Format Negotiation</span></span>](#encoder-format-negotiation)
-   [<span data-ttu-id="f9ac0-107">Decodificadores</span><span class="sxs-lookup"><span data-stu-id="f9ac0-107">Decoders</span></span>](#decoders)
    -   [<span data-ttu-id="f9ac0-108">Decodificadores somente de transcodificação</span><span class="sxs-lookup"><span data-stu-id="f9ac0-108">Transcode-Only Decoders</span></span>](#transcode-only-decoders)
    -   [<span data-ttu-id="f9ac0-109">Atributos de telecineon</span><span class="sxs-lookup"><span data-stu-id="f9ac0-109">Telecine Attributes</span></span>](#telecine-attributes)
-   [<span data-ttu-id="f9ac0-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f9ac0-110">Related topics</span></span>](#related-topics)

## <a name="encoders"></a><span data-ttu-id="f9ac0-111">Codificadores</span><span class="sxs-lookup"><span data-stu-id="f9ac0-111">Encoders</span></span>

### <a name="encoder-format-negotiation"></a><span data-ttu-id="f9ac0-112">Negociação de formato do codificador</span><span class="sxs-lookup"><span data-stu-id="f9ac0-112">Encoder Format Negotiation</span></span>

<span data-ttu-id="f9ac0-113">O procedimento a seguir é usado para inicializar um codificador:</span><span class="sxs-lookup"><span data-stu-id="f9ac0-113">The following procedure is used to initialize an encoder:</span></span>

1.  <span data-ttu-id="f9ac0-114">Consulte o MFT para a interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="f9ac0-114">Query the MFT for the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span>
2.  <span data-ttu-id="f9ac0-115">Chame [**ICodecAPI:: SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) para definir as propriedades de codificação.</span><span class="sxs-lookup"><span data-stu-id="f9ac0-115">Call [**ICodecAPI::SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) to set encoding properties.</span></span>
3.  <span data-ttu-id="f9ac0-116">Chame [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) para definir o formato de codificação.</span><span class="sxs-lookup"><span data-stu-id="f9ac0-116">Call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the encoding format.</span></span>
4.  <span data-ttu-id="f9ac0-117">Chame [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) para obter uma lista de tipos de entrada compatíveis.</span><span class="sxs-lookup"><span data-stu-id="f9ac0-117">Call [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) to get a list of compatible input types.</span></span> <span data-ttu-id="f9ac0-118">(Essa etapa pode ser ignorada.)</span><span class="sxs-lookup"><span data-stu-id="f9ac0-118">(This step might be skipped.)</span></span>
5.  <span data-ttu-id="f9ac0-119">Chame [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) para definir o formato de entrada descompactado.</span><span class="sxs-lookup"><span data-stu-id="f9ac0-119">Call [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) to set the uncompressed input format.</span></span>

<span data-ttu-id="f9ac0-120">Depois que o tipo de saída é definido na etapa 3, o método [**GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) deve retornar uma lista de tipos de entrada que são compatíveis com o tipo de saída atual.</span><span class="sxs-lookup"><span data-stu-id="f9ac0-120">After the output type is set in step 3, the [**GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) method must return a list of input types that are compatible with the current output type.</span></span> <span data-ttu-id="f9ac0-121">Em outras palavras, todos os tipos retornados por **GetInputAvailableType** nesse ponto devem ser válidos para [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span><span class="sxs-lookup"><span data-stu-id="f9ac0-121">In other words, any types returned by **GetInputAvailableType** at this point must be valid for [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span></span>

<span data-ttu-id="f9ac0-122">Para decodificadores, a ordem na qual os tipos são definidos é invertida: o tipo de entrada é definido primeiro, seguido pelo tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="f9ac0-122">For decoders, the order in which types are set is reversed: The input type is set first, followed by the output type.</span></span> <span data-ttu-id="f9ac0-123">Depois que o tipo de entrada é definido, o método [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) deve retornar uma lista de tipos que podem ser passados para o método [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) .</span><span class="sxs-lookup"><span data-stu-id="f9ac0-123">After the input type is set, the [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method must return a list of types that can be passed to the [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) method.</span></span>

<span data-ttu-id="f9ac0-124">Os codificadores e os decodificadores devem dar suporte a NV12 como um formato descompactado comum.</span><span class="sxs-lookup"><span data-stu-id="f9ac0-124">Encoders and decoders should support NV12 as a common uncompressed format.</span></span> <span data-ttu-id="f9ac0-125">Isso garante que os componentes de pipeline possam interoperar com conversões mínimas do colorspace.</span><span class="sxs-lookup"><span data-stu-id="f9ac0-125">This ensures that pipeline components can interoperate with minimal colorspace conversions.</span></span> <span data-ttu-id="f9ac0-126">É claro que outros formatos também podem ter suporte.</span><span class="sxs-lookup"><span data-stu-id="f9ac0-126">Of course, other formats can be supported as well.</span></span>

## <a name="decoders"></a><span data-ttu-id="f9ac0-127">Decodificadores</span><span class="sxs-lookup"><span data-stu-id="f9ac0-127">Decoders</span></span>

### <a name="transcode-only-decoders"></a><span data-ttu-id="f9ac0-128">Decodificadores de Transcode-Only</span><span class="sxs-lookup"><span data-stu-id="f9ac0-128">Transcode-Only Decoders</span></span>

<span data-ttu-id="f9ac0-129">Alguns decodificadores são otimizados para transcodificação (decodificação e, em seguida, codificação de um fluxo) e não são adequados para uso durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="f9ac0-129">Some decoders are optimized for transcoding (decoding and then re-encoding a stream) and are not suitable for use during playback.</span></span>

<span data-ttu-id="f9ac0-130">Se uma MFT do decodificador for destinada apenas para transcodificação, defina o sinalizador de **enumeração de MFT \_ \_ \_ \_ somente transcodificará** ao registrar o MFT.</span><span class="sxs-lookup"><span data-stu-id="f9ac0-130">If a decoder MFT is intended only for transcoding, set the **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY** flag when you register the MFT.</span></span> <span data-ttu-id="f9ac0-131">(Consulte [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister).)</span><span class="sxs-lookup"><span data-stu-id="f9ac0-131">(See [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister).)</span></span>

<span data-ttu-id="f9ac0-132">Por padrão, os decodificadores de transcodificação não são retornados pela função [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="f9ac0-132">By default, transcode decoders are not returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span> <span data-ttu-id="f9ac0-133">Para enumerar os decodificadores de transcodificação, chame **MFTEnumEx** e defina o sinalizador do **sinalizador de enumeração de MFT \_ \_ \_ \_ somente transcodificar** no parâmetro *flags* .</span><span class="sxs-lookup"><span data-stu-id="f9ac0-133">To enumerate transcode decoders, call **MFTEnumEx** and set the **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY** flag in *Flags* parameter.</span></span> <span data-ttu-id="f9ac0-134">Quando usado na função **MFTEnumEx** , esse sinalizador enumerava os decodificadores de transcodificação e outros decodificadores.</span><span class="sxs-lookup"><span data-stu-id="f9ac0-134">When used in the **MFTEnumEx** function, this flag enumerated both transcode decoders and other decoders.</span></span>



| <span data-ttu-id="f9ac0-135">**\_ \_ \_ \_ Somente transcodificação de sinalizador de enumeração de MFT** MFTRegister</span><span class="sxs-lookup"><span data-stu-id="f9ac0-135">MFTRegister **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY**</span></span> | <span data-ttu-id="f9ac0-136">**\_ \_ \_ \_ Somente transcodificação de sinalizador de enumeração de MFT** MFTEnumEx</span><span class="sxs-lookup"><span data-stu-id="f9ac0-136">MFTEnumEx **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY**</span></span> | <span data-ttu-id="f9ac0-137">MFT é enumerado?</span><span class="sxs-lookup"><span data-stu-id="f9ac0-137">Is MFT Enumerated?</span></span> |
|--------------------------------------------------|------------------------------------------------|--------------------|
| <span data-ttu-id="f9ac0-138">1</span><span class="sxs-lookup"><span data-stu-id="f9ac0-138">1</span></span>                                                | <span data-ttu-id="f9ac0-139">1</span><span class="sxs-lookup"><span data-stu-id="f9ac0-139">1</span></span>                                              | <span data-ttu-id="f9ac0-140">Sim</span><span class="sxs-lookup"><span data-stu-id="f9ac0-140">Yes</span></span>                |
| <span data-ttu-id="f9ac0-141">1</span><span class="sxs-lookup"><span data-stu-id="f9ac0-141">1</span></span>                                                | <span data-ttu-id="f9ac0-142">0</span><span class="sxs-lookup"><span data-stu-id="f9ac0-142">0</span></span>                                              | <span data-ttu-id="f9ac0-143">Não</span><span class="sxs-lookup"><span data-stu-id="f9ac0-143">No</span></span>                 |
| <span data-ttu-id="f9ac0-144">0</span><span class="sxs-lookup"><span data-stu-id="f9ac0-144">0</span></span>                                                | <span data-ttu-id="f9ac0-145">1</span><span class="sxs-lookup"><span data-stu-id="f9ac0-145">1</span></span>                                              | <span data-ttu-id="f9ac0-146">Sim</span><span class="sxs-lookup"><span data-stu-id="f9ac0-146">Yes</span></span>                |
| <span data-ttu-id="f9ac0-147">0</span><span class="sxs-lookup"><span data-stu-id="f9ac0-147">0</span></span>                                                | <span data-ttu-id="f9ac0-148">0</span><span class="sxs-lookup"><span data-stu-id="f9ac0-148">0</span></span>                                              | <span data-ttu-id="f9ac0-149">Sim</span><span class="sxs-lookup"><span data-stu-id="f9ac0-149">Yes</span></span>                |



 

### <a name="telecine-attributes"></a><span data-ttu-id="f9ac0-150">Atributos de telecineon</span><span class="sxs-lookup"><span data-stu-id="f9ac0-150">Telecine Attributes</span></span>

<span data-ttu-id="f9ac0-151">A origem da mídia pode anexar os seguintes atributos de telecineon aos exemplos de mídia que ele fornece.</span><span class="sxs-lookup"><span data-stu-id="f9ac0-151">The media source might attach the following telecine attributes to the media samples that it delivers.</span></span>



| <span data-ttu-id="f9ac0-152">Atributo</span><span class="sxs-lookup"><span data-stu-id="f9ac0-152">Attribute</span></span>                                                                                   | <span data-ttu-id="f9ac0-153">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9ac0-153">Description</span></span>                                    |
|---------------------------------------------------------------------------------------------|------------------------------------------------|
| [<span data-ttu-id="f9ac0-154">**MFSampleExtension \_ RepeatFirstField**</span><span class="sxs-lookup"><span data-stu-id="f9ac0-154">**MFSampleExtension\_RepeatFirstField**</span></span>](mfsampleextension-repeatfirstfield-attribute.md) | <span data-ttu-id="f9ac0-155">Equivalente ao sinalizador "repetir primeiro campo" (RFF).</span><span class="sxs-lookup"><span data-stu-id="f9ac0-155">Equivalent to "repeat first field" (RFF) flag.</span></span> |
| [<span data-ttu-id="f9ac0-156">**MFSampleExtension \_ BottomFieldFirst**</span><span class="sxs-lookup"><span data-stu-id="f9ac0-156">**MFSampleExtension\_BottomFieldFirst**</span></span>](mfsampleextension-bottomfieldfirst-attribute.md) | <span data-ttu-id="f9ac0-157">Inverso do sinalizador "Top Field First" (TFF).</span><span class="sxs-lookup"><span data-stu-id="f9ac0-157">Inverse of "top field first" (TFF) flag.</span></span>       |



 

<span data-ttu-id="f9ac0-158">Esses sinalizadores fornecem uma dica para o processador de vídeo avançado (EVR) quando ele executa o desentrelaçamento.</span><span class="sxs-lookup"><span data-stu-id="f9ac0-158">These flags provide a hint to the enhanced video renderer (EVR) when it performs deinterlacing.</span></span> <span data-ttu-id="f9ac0-159">Um decodificador deve propagar esses sinalizadores downstream copiando-os para os exemplos de saída, para que eles cheguem ao EVR.</span><span class="sxs-lookup"><span data-stu-id="f9ac0-159">A decoder should propagate these flags downstream by copying them to the output samples, so that they reach the EVR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9ac0-160">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f9ac0-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9ac0-161">Gravando uma MFT personalizada</span><span class="sxs-lookup"><span data-stu-id="f9ac0-161">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 
