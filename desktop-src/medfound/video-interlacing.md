---
description: Entrelaçamento de vídeo
ms.assetid: 2911ae57-1703-4a9d-bd33-94af1e0f8804
title: Entrelaçamento de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec10f49ef21f3701f85467a3f4a1c4b08d69df72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813654"
---
# <a name="video-interlacing"></a><span data-ttu-id="8f458-103">Entrelaçamento de vídeo</span><span class="sxs-lookup"><span data-stu-id="8f458-103">Video Interlacing</span></span>

<span data-ttu-id="8f458-104">Este tópico descreve como as fontes de mídia e os decodificadores devem lidar com conteúdo de vídeo entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="8f458-104">This topic describes how media sources and decoders should handle interlaced video content.</span></span>

<span data-ttu-id="8f458-105">Para decodificar e renderizar o vídeo entrelaçado corretamente, as seguintes informações são necessárias:</span><span class="sxs-lookup"><span data-stu-id="8f458-105">To decode and render interlaced video correctly, the following information is needed:</span></span>

-   <span data-ttu-id="8f458-106">Progressivo ou entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="8f458-106">Progressive or interlaced.</span></span> <span data-ttu-id="8f458-107">Um fluxo de vídeo pode conter quadros progressivos, quadros entrelaçados ou uma mistura de ambos.</span><span class="sxs-lookup"><span data-stu-id="8f458-107">A video stream can contain progressive frames, interlaced frames, or a mix of both.</span></span>

-   <span data-ttu-id="8f458-108">Campo predominância.</span><span class="sxs-lookup"><span data-stu-id="8f458-108">Field dominance.</span></span> <span data-ttu-id="8f458-109">O campo predominância descreve qual campo aparece primeiro, o campo superior ou o campo inferior.</span><span class="sxs-lookup"><span data-stu-id="8f458-109">Field dominance describes which field appears first, the upper field or the lower field.</span></span>

-   <span data-ttu-id="8f458-110">Repita o primeiro campo.</span><span class="sxs-lookup"><span data-stu-id="8f458-110">Repeat first field.</span></span> <span data-ttu-id="8f458-111">Esse sinalizador é usado na reestruturação de 3:2, quando o quadro é progressivo, mas o fluxo é entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="8f458-111">This flag is used in 3:2 pulldown, when the frame is progressive but the stream is interlaced.</span></span> <span data-ttu-id="8f458-112">Nesse contexto, o primeiro campo pode ser o campo superior ou inferior.</span><span class="sxs-lookup"><span data-stu-id="8f458-112">In this context, the first field can be the upper or lower field.</span></span>

-   <span data-ttu-id="8f458-113">Campos intercalados ou campo único.</span><span class="sxs-lookup"><span data-stu-id="8f458-113">Interleaved fields or single field.</span></span> <span data-ttu-id="8f458-114">Um exemplo pode conter um único campo ou dois campos intercalados.</span><span class="sxs-lookup"><span data-stu-id="8f458-114">A sample can hold either a single field, or two interleaved fields.</span></span> <span data-ttu-id="8f458-115">Se um exemplo contiver um único campo, a altura de amostra será metade da altura do quadro, pois o exemplo contém apenas metade das linhas de varredura de um quadro.</span><span class="sxs-lookup"><span data-stu-id="8f458-115">If a sample contains a single field, the sample height is half the frame height, because the sample contains only half of the scan lines for a frame.</span></span> <span data-ttu-id="8f458-116">Os campos intercalados são recomendados, a menos que as características do conteúdo de origem ditem de outra forma.</span><span class="sxs-lookup"><span data-stu-id="8f458-116">Interleaved fields are recommended unless the characteristics of the source content dictate otherwise.</span></span>

<span data-ttu-id="8f458-117">Qualquer uma dessas características pode mudar de uma amostra para a próxima.</span><span class="sxs-lookup"><span data-stu-id="8f458-117">Any of these characteristics can change from one sample to the next.</span></span> <span data-ttu-id="8f458-118">No entanto, os componentes de vídeo precisam saber algo sobre o conteúdo geral antes de o streaming começar.</span><span class="sxs-lookup"><span data-stu-id="8f458-118">However, video components need to know something about the overall content before streaming begins.</span></span> <span data-ttu-id="8f458-119">Por exemplo, se o vídeo estiver entrelaçado, o processador de vídeo avançado (EVR) precisa reservar memória de vídeo para o desentrelaçamento.</span><span class="sxs-lookup"><span data-stu-id="8f458-119">For example, if the video is interlaced, the enhanced video renderer (EVR) needs to reserve video memory for the deinterlacing.</span></span> <span data-ttu-id="8f458-120">Se o vídeo for totalmente progressivo, por outro lado, o EVR poderá otimizar o pipeline de renderização.</span><span class="sxs-lookup"><span data-stu-id="8f458-120">If the video is entirely progressive frames, on the other hand, the EVR can optimize the rendering pipeline.</span></span> <span data-ttu-id="8f458-121">Adicionar uma etapa de desentrelaçamento ao pipeline aumenta a latência de renderização.</span><span class="sxs-lookup"><span data-stu-id="8f458-121">Adding a deinterlacing step to the pipeline increases the rendering latency.</span></span>

<span data-ttu-id="8f458-122">As informações sobre o entrelaçamento são armazenadas em dois locais:</span><span class="sxs-lookup"><span data-stu-id="8f458-122">Information about interlacing is stored in two places:</span></span>

-   <span data-ttu-id="8f458-123">As informações gerais sobre o entrelaçamento em um fluxo são colocadas no tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="8f458-123">General information about the interlacing in a stream is placed in the media type.</span></span> <span data-ttu-id="8f458-124">Para obter mais informações sobre tipos de mídia, consulte [tipos de mídia](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="8f458-124">For more information about media types, see [Media Types](media-types.md).</span></span>

-   <span data-ttu-id="8f458-125">As informações que podem ser alteradas com cada exemplo são colocadas no exemplo como um atributo.</span><span class="sxs-lookup"><span data-stu-id="8f458-125">Information that can change with each sample is placed on the sample as an attribute.</span></span> <span data-ttu-id="8f458-126">Para obter mais informações sobre exemplos, consulte [amostras de mídia](media-samples.md).</span><span class="sxs-lookup"><span data-stu-id="8f458-126">For more information about samples, see [Media Samples](media-samples.md).</span></span>

## <a name="interlace-information-in-the-media-type"></a><span data-ttu-id="8f458-127">Entrelaçar informações no tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="8f458-127">Interlace Information in the Media Type</span></span>

<span data-ttu-id="8f458-128">O atributo do [**\_ \_ \_ modo de entrelaçamento MF MT**](mf-mt-interlace-mode-attribute.md) no tipo de mídia descreve como o fluxo como um todo é entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="8f458-128">The [**MF\_MT\_INTERLACE\_MODE**](mf-mt-interlace-mode-attribute.md) attribute on the media type describes how the stream as a whole is interlaced.</span></span> <span data-ttu-id="8f458-129">O valor desse atributo é um membro da enumeração [**MFVideoInterlaceMode**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode) .</span><span class="sxs-lookup"><span data-stu-id="8f458-129">The value of this attribute is a member of the [**MFVideoInterlaceMode**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode) enumeration.</span></span> <span data-ttu-id="8f458-130">Um tipo de mídia de vídeo sempre deve ter esse atributo.</span><span class="sxs-lookup"><span data-stu-id="8f458-130">A video media type should always have this attribute.</span></span>

-   <span data-ttu-id="8f458-131">Se o fluxo contiver apenas quadros progressivos, sem quadros entrelaçados, use MFVideoInterlace \_ progressivo.</span><span class="sxs-lookup"><span data-stu-id="8f458-131">If the stream contains only progressive frames, with no interlaced frames, use MFVideoInterlace\_Progressive.</span></span>
-   <span data-ttu-id="8f458-132">Se o fluxo contiver apenas quadros entrelaçados e cada amostra contiver dois campos intercalados, use MFVideoInterlace \_ FieldInterleavedUpperFirst ou MFVideoInterlace \_ FieldInterleavedLowerFirst.</span><span class="sxs-lookup"><span data-stu-id="8f458-132">If the stream contains only interlaced frames, and every sample contains two interleaved fields, use MFVideoInterlace\_FieldInterleavedUpperFirst or MFVideoInterlace\_FieldInterleavedLowerFirst.</span></span>
-   <span data-ttu-id="8f458-133">Se o fluxo contiver apenas quadros entrelaçados e cada amostra contiver um único campo, use MFVideoInterlace \_ FieldSingleUpper ou MFVideoInterlace \_ FieldSingleLower.</span><span class="sxs-lookup"><span data-stu-id="8f458-133">If the stream contains only interlaced frames, and every sample contains a single field, use MFVideoInterlace\_FieldSingleUpper or MFVideoInterlace\_FieldSingleLower.</span></span> <span data-ttu-id="8f458-134">Se os campos forem alternados entre superior e inferior, não importa quais desses dois valores são usados.</span><span class="sxs-lookup"><span data-stu-id="8f458-134">If the fields alternate between upper and lower, then it does not matter which of these two values is used.</span></span> <span data-ttu-id="8f458-135">Se o formato contiver apenas campos maiúsculos ou apenas campos inferiores, defina o valor que corresponde ao conteúdo.</span><span class="sxs-lookup"><span data-stu-id="8f458-135">If the format contains just upper fields, or just lower fields, then set the value that corresponds to the content.</span></span>
-   <span data-ttu-id="8f458-136">Se o fluxo contiver uma combinação de quadros entrelaçados e progressivos, ou se o campo predominância alternar, defina o tipo de mídia como MFVideoInterlace \_ MixedInterlaceOrProgressive.</span><span class="sxs-lookup"><span data-stu-id="8f458-136">If the stream contains a mix of interlaced and progressive frames, or if the field dominance switches, set the media type to MFVideoInterlace\_MixedInterlaceOrProgressive.</span></span> <span data-ttu-id="8f458-137">Use atributos de exemplo para descrever cada quadro.</span><span class="sxs-lookup"><span data-stu-id="8f458-137">Use sample attributes to describe each frame.</span></span>

<span data-ttu-id="8f458-138">A tabela a seguir resume esse atributo.</span><span class="sxs-lookup"><span data-stu-id="8f458-138">The following table summarizes this attribute.</span></span>



| <span data-ttu-id="8f458-139">\_modo de \_ entrelaçamento do MF MT \_</span><span class="sxs-lookup"><span data-stu-id="8f458-139">MF\_MT\_INTERLACE\_MODE</span></span>                       | <span data-ttu-id="8f458-140">Entrelaçadas?</span><span class="sxs-lookup"><span data-stu-id="8f458-140">Interlaced?</span></span> | <span data-ttu-id="8f458-141">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8f458-141">Samples</span></span>                                  | <span data-ttu-id="8f458-142">Primeiro campo</span><span class="sxs-lookup"><span data-stu-id="8f458-142">First field</span></span>    |
|-----------------------------------------------|-------------|------------------------------------------|----------------|
| <span data-ttu-id="8f458-143">MFVideoInterlace \_ progressivo</span><span class="sxs-lookup"><span data-stu-id="8f458-143">MFVideoInterlace\_Progressive</span></span>                 | <span data-ttu-id="8f458-144">No</span><span class="sxs-lookup"><span data-stu-id="8f458-144">No</span></span>          | <span data-ttu-id="8f458-145">Quadro progressivo</span><span class="sxs-lookup"><span data-stu-id="8f458-145">Progressive frame</span></span>                        | <span data-ttu-id="8f458-146">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="8f458-146">Not applicable</span></span> |
| <span data-ttu-id="8f458-147">MFVideoInterlace \_ FieldInterleavedUpperFirst</span><span class="sxs-lookup"><span data-stu-id="8f458-147">MFVideoInterlace\_FieldInterleavedUpperFirst</span></span>  | <span data-ttu-id="8f458-148">Yes</span><span class="sxs-lookup"><span data-stu-id="8f458-148">Yes</span></span>         | <span data-ttu-id="8f458-149">Campos intercalados</span><span class="sxs-lookup"><span data-stu-id="8f458-149">Interleaved fields</span></span>                       | <span data-ttu-id="8f458-150">Primeiro superior</span><span class="sxs-lookup"><span data-stu-id="8f458-150">Upper first</span></span>    |
| <span data-ttu-id="8f458-151">MFVideoInterlace \_ FieldInterleavedLowerFirst</span><span class="sxs-lookup"><span data-stu-id="8f458-151">MFVideoInterlace\_FieldInterleavedLowerFirst</span></span>  | <span data-ttu-id="8f458-152">Yes</span><span class="sxs-lookup"><span data-stu-id="8f458-152">Yes</span></span>         | <span data-ttu-id="8f458-153">Campos intercalados</span><span class="sxs-lookup"><span data-stu-id="8f458-153">Interleaved fields</span></span>                       | <span data-ttu-id="8f458-154">Primeiro abaixo</span><span class="sxs-lookup"><span data-stu-id="8f458-154">Lower first</span></span>    |
| <span data-ttu-id="8f458-155">MFVideoInterlace \_ FieldSingleUpper</span><span class="sxs-lookup"><span data-stu-id="8f458-155">MFVideoInterlace\_FieldSingleUpper</span></span>            | <span data-ttu-id="8f458-156">Yes</span><span class="sxs-lookup"><span data-stu-id="8f458-156">Yes</span></span>         | <span data-ttu-id="8f458-157">Campo único</span><span class="sxs-lookup"><span data-stu-id="8f458-157">Single field</span></span>                             | <span data-ttu-id="8f458-158">Primeiro superior</span><span class="sxs-lookup"><span data-stu-id="8f458-158">Upper first</span></span>    |
| <span data-ttu-id="8f458-159">MFVideoInterlace \_ FieldSingleLower</span><span class="sxs-lookup"><span data-stu-id="8f458-159">MFVideoInterlace\_FieldSingleLower</span></span>            | <span data-ttu-id="8f458-160">Yes</span><span class="sxs-lookup"><span data-stu-id="8f458-160">Yes</span></span>         | <span data-ttu-id="8f458-161">Campo único</span><span class="sxs-lookup"><span data-stu-id="8f458-161">Single field</span></span>                             | <span data-ttu-id="8f458-162">Primeiro abaixo</span><span class="sxs-lookup"><span data-stu-id="8f458-162">Lower first</span></span>    |
| <span data-ttu-id="8f458-163">MFVideoInterlace \_ MixedInterlaceOrProgressive</span><span class="sxs-lookup"><span data-stu-id="8f458-163">MFVideoInterlace\_MixedInterlaceOrProgressive</span></span> | <span data-ttu-id="8f458-164">Pode variar</span><span class="sxs-lookup"><span data-stu-id="8f458-164">Can vary</span></span>    | <span data-ttu-id="8f458-165">Campos intercalados ou quadros progressivos</span><span class="sxs-lookup"><span data-stu-id="8f458-165">Interleaved fields or progressive frames</span></span> | <span data-ttu-id="8f458-166">Pode variar</span><span class="sxs-lookup"><span data-stu-id="8f458-166">Can vary</span></span>       |



 

<span data-ttu-id="8f458-167">Campos intercalados e campos únicos não podem ser misturados.</span><span class="sxs-lookup"><span data-stu-id="8f458-167">Interleaved fields and single fields cannot be mixed.</span></span> <span data-ttu-id="8f458-168">Alternar de um para outro requer uma alteração de tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="8f458-168">Switching from one to another requires a media type change.</span></span>

## <a name="interlace-flags-on-samples"></a><span data-ttu-id="8f458-169">Sinalizadores de entrelaçamento em exemplos</span><span class="sxs-lookup"><span data-stu-id="8f458-169">Interlace Flags on Samples</span></span>

<span data-ttu-id="8f458-170">As informações que podem mudar de uma amostra para a próxima são indicadas usando atributos de exemplo.</span><span class="sxs-lookup"><span data-stu-id="8f458-170">Information that can change from one sample to the next is indicated using sample attributes.</span></span> <span data-ttu-id="8f458-171">Use a interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) para obter ou definir esses atributos.</span><span class="sxs-lookup"><span data-stu-id="8f458-171">Use the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface to get or set these attributes.</span></span>

<span data-ttu-id="8f458-172">Todos os atributos de entrelaçamento listados nesta seção têm valores Boolianos.</span><span class="sxs-lookup"><span data-stu-id="8f458-172">All of the interlacing attributes listed in this section have Boolean values.</span></span> <span data-ttu-id="8f458-173">Efetivamente, cada um desses atributos pode ter três valores: **true**, **false** ou não definido.</span><span class="sxs-lookup"><span data-stu-id="8f458-173">Effectively, each of these attributes can have three values: either **TRUE**, **FALSE**, or not set.</span></span> <span data-ttu-id="8f458-174">Se um atributo não estiver definido, o valor será obtido do tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="8f458-174">If an attribute is not set, the value is taken from the media type.</span></span> <span data-ttu-id="8f458-175">Se um atributo for definido, o valor substituirá o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="8f458-175">If an attribute is set, the value overrides the media type.</span></span> <span data-ttu-id="8f458-176">Algumas combinações de sinalizadores e tipos de mídia não são válidas.</span><span class="sxs-lookup"><span data-stu-id="8f458-176">Some combinations of flags and media types are not valid.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8f458-177">Atributo</span><span class="sxs-lookup"><span data-stu-id="8f458-177">Attribute</span></span></th>
<th><span data-ttu-id="8f458-178">Descrição</span><span class="sxs-lookup"><span data-stu-id="8f458-178">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8f458-179"><a href="mfsampleextension-interlaced-attribute.md">MFSampleExtension_Interlaced</a></span><span class="sxs-lookup"><span data-stu-id="8f458-179"><a href="mfsampleextension-interlaced-attribute.md">MFSampleExtension_Interlaced</a></span></span></td>
<td><span data-ttu-id="8f458-180">Se for <strong>true</strong>, o quadro será entrelaçado.</span><span class="sxs-lookup"><span data-stu-id="8f458-180">If <strong>TRUE</strong>, the frame is interlaced.</span></span> <span data-ttu-id="8f458-181">Se for <strong>false</strong>, o quadro será progressivo.</span><span class="sxs-lookup"><span data-stu-id="8f458-181">If <strong>FALSE</strong>, the frame is progressive.</span></span><br/> <span data-ttu-id="8f458-182">Defina esse atributo em cada exemplo se o tipo de mídia for MFVideoInterlace_MixedInterlaceOrProgressive.</span><span class="sxs-lookup"><span data-stu-id="8f458-182">Set this attribute on every sample if the media type is MFVideoInterlace_MixedInterlaceOrProgressive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f458-183"><a href="mfsampleextension-bottomfieldfirst-attribute.md">MFSampleExtension_BottomFieldFirst</a></span><span class="sxs-lookup"><span data-stu-id="8f458-183"><a href="mfsampleextension-bottomfieldfirst-attribute.md">MFSampleExtension_BottomFieldFirst</a></span></span></td>
<td><span data-ttu-id="8f458-184">O significado desse sinalizador depende se os exemplos contêm campos intercalados ou campos únicos.</span><span class="sxs-lookup"><span data-stu-id="8f458-184">The meaning of this flag depends on whether the samples contain interleaved fields or single fields.</span></span><br/>
<ul>
<li><span data-ttu-id="8f458-185">Campos intercalados: se <strong>for verdadeiro</strong>, o campo inferior será o primeiro.</span><span class="sxs-lookup"><span data-stu-id="8f458-185">Interleaved fields: If <strong>TRUE</strong>, the lower field is first.</span></span> <span data-ttu-id="8f458-186">Se for <strong>false</strong>, o campo superior será primeiro.</span><span class="sxs-lookup"><span data-stu-id="8f458-186">If <strong>FALSE</strong>, the upper field is first.</span></span><br/></li>
<li><span data-ttu-id="8f458-187">Campos únicos: se <strong>for true</strong>, o exemplo conterá um campo inferior.</span><span class="sxs-lookup"><span data-stu-id="8f458-187">Single fields: If <strong>TRUE</strong>, the sample contains a lower field.</span></span> <span data-ttu-id="8f458-188">Se <strong>for false</strong>, o exemplo conterá um campo superior.</span><span class="sxs-lookup"><span data-stu-id="8f458-188">If <strong>FALSE</strong>, the sample contains an upper field.</span></span><br/></li>
</ul>
<span data-ttu-id="8f458-189">Defina esse atributo em cada amostra de entrelaçamento se o tipo de mídia for MFVideoInterlace_FieldSingleUpper, MFVideoInterlace_FieldSingleLower ou MFVideoInterlace_MixedInterlaceOrProgressive.</span><span class="sxs-lookup"><span data-stu-id="8f458-189">Set this attribute on every interlace sample if the media type is MFVideoInterlace_FieldSingleUpper, MFVideoInterlace_FieldSingleLower, or MFVideoInterlace_MixedInterlaceOrProgressive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8f458-190"><a href="mfsampleextension-repeatfirstfield-attribute.md">MFSampleExtension_RepeatFirstField</a></span><span class="sxs-lookup"><span data-stu-id="8f458-190"><a href="mfsampleextension-repeatfirstfield-attribute.md">MFSampleExtension_RepeatFirstField</a></span></span></td>
<td><span data-ttu-id="8f458-191">Se <strong>for true</strong>, o primeiro campo será repetido.</span><span class="sxs-lookup"><span data-stu-id="8f458-191">If <strong>TRUE</strong>, the first field is repeated.</span></span> <span data-ttu-id="8f458-192">Se for <strong>false</strong> ou not set, o primeiro campo não será repetido.</span><span class="sxs-lookup"><span data-stu-id="8f458-192">If <strong>FALSE</strong> or not set, the first field is not repeated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8f458-193"><a href="mfsampleextension-singlefield-attribute.md">MFSampleExtension_SingleField</a></span><span class="sxs-lookup"><span data-stu-id="8f458-193"><a href="mfsampleextension-singlefield-attribute.md">MFSampleExtension_SingleField</a></span></span></td>
<td><span data-ttu-id="8f458-194">Se <strong>for true</strong>, o exemplo conterá um único campo.</span><span class="sxs-lookup"><span data-stu-id="8f458-194">If <strong>TRUE</strong>, the sample contains a single field.</span></span> <span data-ttu-id="8f458-195">Se <strong>for false</strong>, o exemplo conterá campos intercalados.</span><span class="sxs-lookup"><span data-stu-id="8f458-195">If <strong>FALSE</strong>, the sample contains interleaved fields.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="8f458-196">A tabela a seguir mostra quais sinalizadores são necessários, opcionais ou proibidos, com base no tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="8f458-196">The following table shows which flags are required, optional, or prohibited, based on the media type.</span></span>



| <span data-ttu-id="8f458-197">Tipo de Mídia</span><span class="sxs-lookup"><span data-stu-id="8f458-197">Media Type</span></span>         | <span data-ttu-id="8f458-198">Sinalizador entrelaçado</span><span class="sxs-lookup"><span data-stu-id="8f458-198">Interlaced Flag</span></span>                      | <span data-ttu-id="8f458-199">Sinalizador BottomFieldFirst</span><span class="sxs-lookup"><span data-stu-id="8f458-199">BottomFieldFirst Flag</span></span>                    | <span data-ttu-id="8f458-200">Sinalizador RepeatFirstField</span><span class="sxs-lookup"><span data-stu-id="8f458-200">RepeatFirstField Flag</span></span> | <span data-ttu-id="8f458-201">Sinalizador de únicofield</span><span class="sxs-lookup"><span data-stu-id="8f458-201">SingleField Flag</span></span>                     |
|--------------------|--------------------------------------|------------------------------------------|-----------------------|--------------------------------------|
| <span data-ttu-id="8f458-202">Progressivo</span><span class="sxs-lookup"><span data-stu-id="8f458-202">Progressive</span></span>        | <span data-ttu-id="8f458-203">Adicional Se definido, deve ser **false**.</span><span class="sxs-lookup"><span data-stu-id="8f458-203">Optional; if set, must be **FALSE**.</span></span> | <span data-ttu-id="8f458-204">Não definir.</span><span class="sxs-lookup"><span data-stu-id="8f458-204">Do not set.</span></span>                              | <span data-ttu-id="8f458-205">Não definir.</span><span class="sxs-lookup"><span data-stu-id="8f458-205">Do not set.</span></span>           | <span data-ttu-id="8f458-206">Não definir.</span><span class="sxs-lookup"><span data-stu-id="8f458-206">Do not set.</span></span>                          |
| <span data-ttu-id="8f458-207">Campos intercalados</span><span class="sxs-lookup"><span data-stu-id="8f458-207">Interleaved fields</span></span> | <span data-ttu-id="8f458-208">Adicional Se definido, deve ser **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="8f458-208">Optional; if set, must be **TRUE**.</span></span>  | <span data-ttu-id="8f458-209">Adicional Se definido, deve corresponder ao tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="8f458-209">Optional; if set, must match media type.</span></span> | <span data-ttu-id="8f458-210">Não definir.</span><span class="sxs-lookup"><span data-stu-id="8f458-210">Do not set.</span></span>           | <span data-ttu-id="8f458-211">Adicional Se definido, deve ser **false**.</span><span class="sxs-lookup"><span data-stu-id="8f458-211">Optional; if set, must be **FALSE**.</span></span> |
| <span data-ttu-id="8f458-212">Campos únicos</span><span class="sxs-lookup"><span data-stu-id="8f458-212">Single fields</span></span>      | <span data-ttu-id="8f458-213">Adicional Se definido, deve ser **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="8f458-213">Optional; if set, must be **TRUE**.</span></span>  | <span data-ttu-id="8f458-214">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="8f458-214">Required.</span></span>                                | <span data-ttu-id="8f458-215">Não definir.</span><span class="sxs-lookup"><span data-stu-id="8f458-215">Do not set.</span></span>           | <span data-ttu-id="8f458-216">Defina como **true**.</span><span class="sxs-lookup"><span data-stu-id="8f458-216">Set to **TRUE**.</span></span>                     |
| <span data-ttu-id="8f458-217">Mixed</span><span class="sxs-lookup"><span data-stu-id="8f458-217">Mixed</span></span>              | <span data-ttu-id="8f458-218">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="8f458-218">Required.</span></span>                            | <span data-ttu-id="8f458-219">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="8f458-219">Required.</span></span>                                | <span data-ttu-id="8f458-220">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="8f458-220">Required.</span></span>             | <span data-ttu-id="8f458-221">Adicional Se definido, deve ser **false**.</span><span class="sxs-lookup"><span data-stu-id="8f458-221">Optional; if set, must be **FALSE**.</span></span> |



 

<span data-ttu-id="8f458-222">Nos casos em que o atributo é opcional, o tipo de mídia já define as informações.</span><span class="sxs-lookup"><span data-stu-id="8f458-222">In the cases where the attribute is optional, the media type already defines the information.</span></span> <span data-ttu-id="8f458-223">É válido definir o atributo para corresponder, mas não obrigatório.</span><span class="sxs-lookup"><span data-stu-id="8f458-223">It is valid to set the attribute to match, but not required.</span></span>

<span data-ttu-id="8f458-224">Por exemplo, se o tipo de mídia for MFVideoInterlace \_ progressivo, ele implica que todos os quadros no fluxo são progressivos.</span><span class="sxs-lookup"><span data-stu-id="8f458-224">For example, if the media type is MFVideoInterlace\_Progressive, it implies that all frames in the stream are progressive.</span></span> <span data-ttu-id="8f458-225">Portanto, você pode definir o atributo **\_ entrelaçado MFSampleExtension** como **false** ou deixar a definição do atributo.</span><span class="sxs-lookup"><span data-stu-id="8f458-225">Therefore, you can either set the **MFSampleExtension\_Interlaced** attribute to **FALSE**, or leave the attribute unset.</span></span>

## <a name="recommendations"></a><span data-ttu-id="8f458-226">Recomendações</span><span class="sxs-lookup"><span data-stu-id="8f458-226">Recommendations</span></span>

<span data-ttu-id="8f458-227">Esta seção contém recomendações para vários tipos de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="8f458-227">This section contains recommendations for various types of content.</span></span>

1. <span data-ttu-id="8f458-228">O vídeo é todos os quadros progressivos.</span><span class="sxs-lookup"><span data-stu-id="8f458-228">The video is all progressive frames.</span></span>

-   <span data-ttu-id="8f458-229">Defina o tipo de mídia como MFVideoInterlace \_ progressivo.</span><span class="sxs-lookup"><span data-stu-id="8f458-229">Set the media type to MFVideoInterlace\_Progressive.</span></span>

-   <span data-ttu-id="8f458-230">Não defina o atributo **\_ entrelaçado MFSampleExtension** ou defina-o como **false** em todos os quadros.</span><span class="sxs-lookup"><span data-stu-id="8f458-230">Do not set the **MFSampleExtension\_Interlaced** attribute, or set it to **FALSE** on every frame.</span></span>

-   <span data-ttu-id="8f458-231">Não defina os atributos **MFSampleExtension \_ BottomFieldFirst**, **MFSampleExtension \_ RepeatFirstField** ou **MFSampleExtension \_ singlefield** .</span><span class="sxs-lookup"><span data-stu-id="8f458-231">Do not set the **MFSampleExtension\_BottomFieldFirst**, **MFSampleExtension\_RepeatFirstField**, or **MFSampleExtension\_SingleField** attributes.</span></span>

2. <span data-ttu-id="8f458-232">O vídeo é todos os campos entrelaçados com o mesmo campo predominância.</span><span class="sxs-lookup"><span data-stu-id="8f458-232">The video is all interlaced fields with the same field dominance.</span></span> <span data-ttu-id="8f458-233">Os exemplos contêm campos intercalados.</span><span class="sxs-lookup"><span data-stu-id="8f458-233">Samples contain interleaved fields.</span></span>

-   <span data-ttu-id="8f458-234">Defina o tipo de mídia como MFVideoInterlace \_ FieldInterleavedUpperFirst ou MFVideoInterlace \_ FieldInterleavedLowerFirst.</span><span class="sxs-lookup"><span data-stu-id="8f458-234">Set the media type to MFVideoInterlace\_FieldInterleavedUpperFirst or MFVideoInterlace\_FieldInterleavedLowerFirst.</span></span>

-   <span data-ttu-id="8f458-235">Não defina o atributo **\_ entrelaçado MFSampleExtension** ou defina-o como **true** em todos os quadros.</span><span class="sxs-lookup"><span data-stu-id="8f458-235">Do not set the **MFSampleExtension\_Interlaced** attribute, or set it to **TRUE** on every frame.</span></span>

-   <span data-ttu-id="8f458-236">Não defina o atributo **MFSampleExtension \_ BottomFieldFirst** ou defina o valor em cada quadro para corresponder ao tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="8f458-236">Do not set the **MFSampleExtension\_BottomFieldFirst** attribute, or set the value on every frame to match the media type.</span></span>

-   <span data-ttu-id="8f458-237">Não defina o atributo **MFSampleExtension \_ RepeatFirstField** ou defina-o como **false** em todos os quadros.</span><span class="sxs-lookup"><span data-stu-id="8f458-237">Do not set the **MFSampleExtension\_RepeatFirstField** attribute, or set it to **FALSE** on every frame.</span></span>

-   <span data-ttu-id="8f458-238">Não defina o atributo **MFSampleExtension \_ únicofield** ou defina-o como **false** em todos os quadros.</span><span class="sxs-lookup"><span data-stu-id="8f458-238">Do not set the **MFSampleExtension\_SingleField** attribute, or set it to **FALSE** on every frame.</span></span>

3. <span data-ttu-id="8f458-239">O vídeo contém uma mistura de quadros entrelaçados e progressivos, com campos repetidos e predominância de campo variável (por exemplo, vídeo de DVD).</span><span class="sxs-lookup"><span data-stu-id="8f458-239">The video contains a mix of interlaced and progressive frames, with repeated fields and varying field dominance (for example, DVD video).</span></span>

-   <span data-ttu-id="8f458-240">Defina o tipo de mídia como MFVideoInterlace \_ MixedInterlaceOrProgressive.</span><span class="sxs-lookup"><span data-stu-id="8f458-240">Set the media type to MFVideoInterlace\_MixedInterlaceOrProgressive.</span></span>

-   <span data-ttu-id="8f458-241">Em cada quadro, defina os atributos **MFSampleExtension \_ entrelaçado**, **MFSampleExtension \_ BottomFieldFirst** e **MFSampleExtension \_ RepeatFirstField** .</span><span class="sxs-lookup"><span data-stu-id="8f458-241">On every frame, set the **MFSampleExtension\_Interlaced**, **MFSampleExtension\_BottomFieldFirst**, and **MFSampleExtension\_RepeatFirstField** attributes.</span></span>

-   <span data-ttu-id="8f458-242">Não defina o atributo **MFSampleExtension \_ únicofield** ou defina-o como **false** em todos os quadros.</span><span class="sxs-lookup"><span data-stu-id="8f458-242">Do not set the **MFSampleExtension\_SingleField** attribute, or set it to **FALSE** on every frame.</span></span>

4. <span data-ttu-id="8f458-243">O vídeo é entrelaçado e os exemplos contêm campos únicos.</span><span class="sxs-lookup"><span data-stu-id="8f458-243">The video is interlaced and samples contain single fields.</span></span>

-   <span data-ttu-id="8f458-244">Defina o tipo de mídia como MFVideoInterlace \_ FieldSingleUpper ou MFVideoInterlace \_ FieldSingleLower.</span><span class="sxs-lookup"><span data-stu-id="8f458-244">Set the media type to MFVideoInterlace\_FieldSingleUpper or MFVideoInterlace\_FieldSingleLower.</span></span>

-   <span data-ttu-id="8f458-245">Em cada quadro, defina o atributo **MFSampleExtension \_ BottomFieldFirst** .</span><span class="sxs-lookup"><span data-stu-id="8f458-245">On every frame, set the **MFSampleExtension\_BottomFieldFirst** attribute.</span></span>

-   <span data-ttu-id="8f458-246">Não defina o atributo **\_ entrelaçado MFSampleExtension** ou defina-o como **true** em todos os quadros.</span><span class="sxs-lookup"><span data-stu-id="8f458-246">Do not set the **MFSampleExtension\_Interlaced** attribute, or set it to **TRUE** on every frame.</span></span>

-   <span data-ttu-id="8f458-247">Não defina o atributo **MFSampleExtension \_ RepeatFirstField** ou defina-o como **false** em todos os quadros.</span><span class="sxs-lookup"><span data-stu-id="8f458-247">Do not set the **MFSampleExtension\_RepeatFirstField** attribute, or set it to **FALSE** on every frame.</span></span>

-   <span data-ttu-id="8f458-248">Não defina o atributo **MFSampleExtension \_ únicofield** ou defina-o como **true** em todos os quadros.</span><span class="sxs-lookup"><span data-stu-id="8f458-248">Do not set the **MFSampleExtension\_SingleField** attribute, or set it to **TRUE** on every frame.</span></span>

<span data-ttu-id="8f458-249">A maior parte do conteúdo de vídeo se encaixa em uma dessas categorias.</span><span class="sxs-lookup"><span data-stu-id="8f458-249">Most video content falls into one of these categories.</span></span>

## <a name="mpeg-2-mappings"></a><span data-ttu-id="8f458-250">Mapeamentos MPEG-2</span><span class="sxs-lookup"><span data-stu-id="8f458-250">MPEG-2 Mappings</span></span>

<span data-ttu-id="8f458-251">Para conteúdo MPEG-2, use os seguintes mapeamentos para converter os sinalizadores MPEG-2 em Media Foundation atributos de exemplo.</span><span class="sxs-lookup"><span data-stu-id="8f458-251">For MPEG-2 content, use the following mappings to convert the MPEG-2 flags to Media Foundation sample attributes.</span></span>

<span data-ttu-id="8f458-252">**estrutura da imagem \_**</span><span class="sxs-lookup"><span data-stu-id="8f458-252">**picture\_structure**</span></span>



| <span data-ttu-id="8f458-253">Valor</span><span class="sxs-lookup"><span data-stu-id="8f458-253">Value</span></span>         | <span data-ttu-id="8f458-254">Atributo de exemplo</span><span class="sxs-lookup"><span data-stu-id="8f458-254">Sample Attribute</span></span>                                                                                                        |
|---------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f458-255">frame</span><span class="sxs-lookup"><span data-stu-id="8f458-255">frame</span></span>         | <span data-ttu-id="8f458-256">**MFSampleExtension \_ Únicofield**  =  **falso**</span><span class="sxs-lookup"><span data-stu-id="8f458-256">**MFSampleExtension\_SingleField** = **FALSE**</span></span>                                                                          |
| <span data-ttu-id="8f458-257">\_campo superior</span><span class="sxs-lookup"><span data-stu-id="8f458-257">top\_field</span></span>    | <span data-ttu-id="8f458-258">**MFSampleExtension \_ Únicofield**  =  **verdadeiro**</span><span class="sxs-lookup"><span data-stu-id="8f458-258">**MFSampleExtension\_SingleField** = **TRUE**</span></span><br/> <span data-ttu-id="8f458-259">**MFSampleExtension \_ BottomFieldFirst**  =  **false**</span><span class="sxs-lookup"><span data-stu-id="8f458-259">**MFSampleExtension\_BottomFieldFirst** = **FALSE**</span></span><br/> |
| <span data-ttu-id="8f458-260">\_campo inferior</span><span class="sxs-lookup"><span data-stu-id="8f458-260">bottom\_field</span></span> | <span data-ttu-id="8f458-261">**MFSampleExtension \_ Únicofield**  =  **verdadeiro**</span><span class="sxs-lookup"><span data-stu-id="8f458-261">**MFSampleExtension\_SingleField** = **TRUE**</span></span><br/> <span data-ttu-id="8f458-262">**MFSampleExtension \_ BottomFieldFirst**  =  **true**</span><span class="sxs-lookup"><span data-stu-id="8f458-262">**MFSampleExtension\_BottomFieldFirst** = **TRUE**</span></span><br/>  |



 

<span data-ttu-id="8f458-263">**quadro progressivo \_**</span><span class="sxs-lookup"><span data-stu-id="8f458-263">**progressive\_frame**</span></span>



| <span data-ttu-id="8f458-264">Valor</span><span class="sxs-lookup"><span data-stu-id="8f458-264">Value</span></span> | <span data-ttu-id="8f458-265">Atributo de exemplo</span><span class="sxs-lookup"><span data-stu-id="8f458-265">Sample Attribute</span></span>                              |
|-------|-----------------------------------------------|
| <span data-ttu-id="8f458-266">0</span><span class="sxs-lookup"><span data-stu-id="8f458-266">0</span></span>     | <span data-ttu-id="8f458-267">**MFSampleExtension \_ Entrelaçado**  =  **verdadeiro**</span><span class="sxs-lookup"><span data-stu-id="8f458-267">**MFSampleExtension\_Interlaced** = **TRUE**</span></span>  |
| <span data-ttu-id="8f458-268">1</span><span class="sxs-lookup"><span data-stu-id="8f458-268">1</span></span>     | <span data-ttu-id="8f458-269">**MFSampleExtension \_ Falso entrelaçado**  =  </span><span class="sxs-lookup"><span data-stu-id="8f458-269">**MFSampleExtension\_Interlaced** = **FALSE**</span></span> |



 

<span data-ttu-id="8f458-270">**\_primeiro campo \_ principal**</span><span class="sxs-lookup"><span data-stu-id="8f458-270">**top\_field\_first**</span></span>



| <span data-ttu-id="8f458-271">Valor</span><span class="sxs-lookup"><span data-stu-id="8f458-271">Value</span></span> | <span data-ttu-id="8f458-272">Atributo de exemplo</span><span class="sxs-lookup"><span data-stu-id="8f458-272">Sample Attribute</span></span>                                    |
|-------|-----------------------------------------------------|
| <span data-ttu-id="8f458-273">0</span><span class="sxs-lookup"><span data-stu-id="8f458-273">0</span></span>     | <span data-ttu-id="8f458-274">**MFSampleExtension \_ BottomFieldFirst**  =  **true**</span><span class="sxs-lookup"><span data-stu-id="8f458-274">**MFSampleExtension\_BottomFieldFirst** = **TRUE**</span></span>  |
| <span data-ttu-id="8f458-275">1</span><span class="sxs-lookup"><span data-stu-id="8f458-275">1</span></span>     | <span data-ttu-id="8f458-276">**MFSampleExtension \_ BottomFieldFirst**  =  **false**</span><span class="sxs-lookup"><span data-stu-id="8f458-276">**MFSampleExtension\_BottomFieldFirst** = **FALSE**</span></span> |



 

<span data-ttu-id="8f458-277">**repetir \_ primeiro \_ campo**</span><span class="sxs-lookup"><span data-stu-id="8f458-277">**repeat\_first\_field**</span></span>



| <span data-ttu-id="8f458-278">Valor</span><span class="sxs-lookup"><span data-stu-id="8f458-278">Value</span></span> | <span data-ttu-id="8f458-279">Atributo de exemplo</span><span class="sxs-lookup"><span data-stu-id="8f458-279">Sample Attribute</span></span>                                    |
|-------|-----------------------------------------------------|
| <span data-ttu-id="8f458-280">0</span><span class="sxs-lookup"><span data-stu-id="8f458-280">0</span></span>     | <span data-ttu-id="8f458-281">**MFSampleExtension \_ RepeatFirstField**  =  **false**</span><span class="sxs-lookup"><span data-stu-id="8f458-281">**MFSampleExtension\_RepeatFirstField** = **FALSE**</span></span> |
| <span data-ttu-id="8f458-282">1</span><span class="sxs-lookup"><span data-stu-id="8f458-282">1</span></span>     | <span data-ttu-id="8f458-283">**MFSampleExtension \_ RepeatFirstField**  =  **true**</span><span class="sxs-lookup"><span data-stu-id="8f458-283">**MFSampleExtension\_RepeatFirstField** = **TRUE**</span></span>  |



 

## <a name="single-field-samples"></a><span data-ttu-id="8f458-284">Exemplos de Single-Field</span><span class="sxs-lookup"><span data-stu-id="8f458-284">Single-Field Samples</span></span>

<span data-ttu-id="8f458-285">Se o tipo de mídia for MFVideoInterlace \_ FieldSingleUpper ou MFVideoInterlace \_ FieldSingleLower, significa que cada exemplo contém um único campo.</span><span class="sxs-lookup"><span data-stu-id="8f458-285">If the media type is MFVideoInterlace\_FieldSingleUpper or MFVideoInterlace\_FieldSingleLower, it means that each sample contains a single field.</span></span> <span data-ttu-id="8f458-286">No entanto, o tipo de mídia descreve o quadro inteiro.</span><span class="sxs-lookup"><span data-stu-id="8f458-286">However, the media type describes the entire frame.</span></span> <span data-ttu-id="8f458-287">Portanto, cada buffer contém apenas metade do número de linhas de campo fornecidas no tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="8f458-287">Therefore, each buffer contains only half the number of field lines given in the media type.</span></span> <span data-ttu-id="8f458-288">Por exemplo, se o tipo de mídia descrever o vídeo como 720 × 480, cada campo conterá 240 linhas de varredura e, portanto, cada buffer conterá apenas 240 linhas de pixels.</span><span class="sxs-lookup"><span data-stu-id="8f458-288">For example, if the media type describes the video as 720 × 480, each field contains 240 scan lines, and therefore each buffer contains only 240 rows of pixels.</span></span> <span data-ttu-id="8f458-289">Se você escrever um componente que aceite tipos de mídia com exemplos de campo único, deverá levar esse fato em conta ao acessar os dados no buffer.</span><span class="sxs-lookup"><span data-stu-id="8f458-289">If you write a component that accepts media types with single-field samples, you must take this fact into account when you access the data in the buffer.</span></span>

<span data-ttu-id="8f458-290">A mesma regra se aplica à abertura geométrica (atributo de[ \_ \_ \_ abertura geométrica MF MT](mf-mt-geometric-aperture-attribute.md) ) e à abertura de exibição mínima (atributo de[ \_ \_ \_ \_ abertura de exibição mínima de MF MT](mf-mt-minimum-display-aperture-attribute.md) ).</span><span class="sxs-lookup"><span data-stu-id="8f458-290">The same rule applies to the geometric aperture ([MF\_MT\_GEOMETRIC\_APERTURE](mf-mt-geometric-aperture-attribute.md) attribute) and minimum display aperture ([MF\_MT\_MINIMUM\_DISPLAY\_APERTURE](mf-mt-minimum-display-aperture-attribute.md) attribute).</span></span> <span data-ttu-id="8f458-291">Essas regiões são especificadas em termos de todo o quadro, não dos campos individuais.</span><span class="sxs-lookup"><span data-stu-id="8f458-291">These regions are specified in terms of the entire frame, not the individual fields.</span></span>

## <a name="directshow-mappings"></a><span data-ttu-id="8f458-292">Mapeamentos do DirectShow</span><span class="sxs-lookup"><span data-stu-id="8f458-292">DirectShow Mappings</span></span>

<span data-ttu-id="8f458-293">No DirectShow, as informações de entrelaçamento por amostra estão contidas no membro **dwTypeSpecificFlags** da estrutura de **\_ \_ Propriedades am SAMPLE2** .</span><span class="sxs-lookup"><span data-stu-id="8f458-293">In DirectShow, per-sample interlacing information is contained in the **dwTypeSpecificFlags** member of the **AM\_SAMPLE2\_PROPERTIES** structure.</span></span> <span data-ttu-id="8f458-294">A tabela a seguir mostra os atributos equivalentes para Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8f458-294">The following table shows the equivalent attributes for Media Foundation.</span></span>



| <span data-ttu-id="8f458-295">Sinalizador de exemplo do DirectShow</span><span class="sxs-lookup"><span data-stu-id="8f458-295">DirectShow sample flag</span></span>              | <span data-ttu-id="8f458-296">Media Foundation atributo de exemplo</span><span class="sxs-lookup"><span data-stu-id="8f458-296">Media Foundation sample attribute</span></span>                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8f458-297">\_ \_ \_ quadro intercalado do sinalizador de vídeo am \_</span><span class="sxs-lookup"><span data-stu-id="8f458-297">AM\_VIDEO\_FLAG\_INTERLEAVED\_FRAME</span></span> | <span data-ttu-id="8f458-298">**MFSampleExtension \_ Únicofield**  =  **falso**.</span><span class="sxs-lookup"><span data-stu-id="8f458-298">**MFSampleExtension\_SingleField** = **FALSE**.</span></span>                                                                                                                                    |
| <span data-ttu-id="8f458-299">\_Campo1 do \_ sinalizador de vídeo am \_</span><span class="sxs-lookup"><span data-stu-id="8f458-299">AM\_VIDEO\_FLAG\_FIELD1</span></span>             | <span data-ttu-id="8f458-300">**MFSampleExtension \_ Entrelaçado**  =  **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="8f458-300">**MFSampleExtension\_Interlaced** = **TRUE**.</span></span><br/> <span data-ttu-id="8f458-301">**MFSampleExtension \_ Singlefield**  =  **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="8f458-301">**MFSampleExtension\_SingleField** = **TRUE**.</span></span><br/> <span data-ttu-id="8f458-302">**MFSampleExtension \_ BottomFieldFirst**  =  **false**.</span><span class="sxs-lookup"><span data-stu-id="8f458-302">**MFSampleExtension\_BottomFieldFirst** = **FALSE**.</span></span><br/> |
| <span data-ttu-id="8f458-303">\_Sinalizador de vídeo am \_ \_ campo2</span><span class="sxs-lookup"><span data-stu-id="8f458-303">AM\_VIDEO\_FLAG\_FIELD2</span></span>             | <span data-ttu-id="8f458-304">**MFSampleExtension \_ Entrelaçado**  =  **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="8f458-304">**MFSampleExtension\_Interlaced** = **TRUE**.</span></span><br/> <span data-ttu-id="8f458-305">**MFSampleExtension \_ Singlefield**  =  **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="8f458-305">**MFSampleExtension\_SingleField** = **TRUE**.</span></span><br/> <span data-ttu-id="8f458-306">**MFSampleExtension \_ BottomFieldFirst**  =  **true**.</span><span class="sxs-lookup"><span data-stu-id="8f458-306">**MFSampleExtension\_BottomFieldFirst** = **TRUE**.</span></span><br/>  |
| <span data-ttu-id="8f458-307">\_sinalizador de vídeo am \_ \_ trançado</span><span class="sxs-lookup"><span data-stu-id="8f458-307">AM\_VIDEO\_FLAG\_WEAVE</span></span>              | <span data-ttu-id="8f458-308">**MFSampleExtension \_ Falso entrelaçado**  =  .</span><span class="sxs-lookup"><span data-stu-id="8f458-308">**MFSampleExtension\_Interlaced** = **FALSE**.</span></span> <span data-ttu-id="8f458-309">(Esse sinalizador indica que o driver não deve desentrelaçar os dois campos.)</span><span class="sxs-lookup"><span data-stu-id="8f458-309">(This flag indicates that the driver should not deinterlace the two fields.)</span></span>                                                        |
| <span data-ttu-id="8f458-310">\_Sinalizador de vídeo am \_ \_ FIELD1FIRST</span><span class="sxs-lookup"><span data-stu-id="8f458-310">AM\_VIDEO\_FLAG\_FIELD1FIRST</span></span>        | <span data-ttu-id="8f458-311">**MFSampleExtension \_ BottomFieldFirst**  =  **false**.</span><span class="sxs-lookup"><span data-stu-id="8f458-311">**MFSampleExtension\_BottomFieldFirst** = **FALSE**.</span></span> <span data-ttu-id="8f458-312">Se o conteúdo for entrelaçado e o \_ sinalizador FIELD1FIRST do sinalizador de vídeo am \_ \_ não estiver presente, defina esse atributo como **true**.</span><span class="sxs-lookup"><span data-stu-id="8f458-312">If the content is interlaced and the AM\_VIDEO\_FLAG\_FIELD1FIRST flag is not present, set this attribute to **TRUE**.</span></span>        |
| <span data-ttu-id="8f458-313">\_campo de \_ repetição do sinalizador de vídeo am \_ \_</span><span class="sxs-lookup"><span data-stu-id="8f458-313">AM\_VIDEO\_FLAG\_REPEAT\_FIELD</span></span>      | <span data-ttu-id="8f458-314">**MFSampleExtension \_ RepeatFirstField**  =  **true**.</span><span class="sxs-lookup"><span data-stu-id="8f458-314">**MFSampleExtension\_RepeatFirstField** = **TRUE**.</span></span> <span data-ttu-id="8f458-315">Se o \_ sinalizador de campo de repetição do sinalizador de vídeo am \_ \_ \_ não estiver presente, defina esse atributo como **false**.</span><span class="sxs-lookup"><span data-stu-id="8f458-315">If the AM\_VIDEO\_FLAG\_REPEAT\_FIELD flag is not present, set this attribute to **FALSE**.</span></span>                                    |



 

<span data-ttu-id="8f458-316">Se o exemplo do DirectShow não contiver sinalizadores de exemplo, use o valor de **dwInterlaceFlags** da estrutura **VIDEOINFOHEADER2** :</span><span class="sxs-lookup"><span data-stu-id="8f458-316">If the DirectShow sample does not contain sample flags, use the value of **dwInterlaceFlags** from the **VIDEOINFOHEADER2** structure:</span></span>



| <span data-ttu-id="8f458-317">Sinalizador de entrelaçamento do DirectShow</span><span class="sxs-lookup"><span data-stu-id="8f458-317">DirectShow interlace flag</span></span>    | <span data-ttu-id="8f458-318">Media Foundation atributo de exemplo</span><span class="sxs-lookup"><span data-stu-id="8f458-318">Media Foundation sample attribute</span></span>                    |
|------------------------------|------------------------------------------------------|
| <span data-ttu-id="8f458-319">\_Isentrelaçado AMINTERLACE</span><span class="sxs-lookup"><span data-stu-id="8f458-319">AMINTERLACE\_IsInterlaced</span></span>    | <span data-ttu-id="8f458-320">**MFSampleExtension \_ Entrelaçado**  =  **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="8f458-320">**MFSampleExtension\_Interlaced** = **TRUE**.</span></span>        |
| <span data-ttu-id="8f458-321">AMINTERLACE \_ 1FieldPerSample</span><span class="sxs-lookup"><span data-stu-id="8f458-321">AMINTERLACE\_1FieldPerSample</span></span> | <span data-ttu-id="8f458-322">**MFSampleExtension \_ Singlefield**  =  **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="8f458-322">**MFSampleExtension\_SingleField** = **TRUE**.</span></span>       |
| <span data-ttu-id="8f458-323">AMINTERLACE \_ Field1First</span><span class="sxs-lookup"><span data-stu-id="8f458-323">AMINTERLACE\_Field1First</span></span>     | <span data-ttu-id="8f458-324">**MFSampleExtension \_ BottomFieldFirst**  =  **false**.</span><span class="sxs-lookup"><span data-stu-id="8f458-324">**MFSampleExtension\_BottomFieldFirst** = **FALSE**.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8f458-325">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8f458-325">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8f458-326">Tipos de mídia de vídeo</span><span class="sxs-lookup"><span data-stu-id="8f458-326">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="8f458-327">Tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="8f458-327">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 




