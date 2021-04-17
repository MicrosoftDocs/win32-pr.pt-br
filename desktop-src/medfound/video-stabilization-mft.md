---
description: O MFT de estabilização de vídeo é uma Microsoft Media Foundation transformação (MFT) que executa a estabilização de imagem em um fluxo de vídeo.
ms.assetid: BBC42190-08E4-4C3B-972A-FD30621A6CC1
title: MFT Estabilização de Vídeo (Camerauicontrol. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65eb64b05e41842b1f7b3ad2e49a6c064be08f0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769366"
---
# <a name="video-stabilization-mft"></a><span data-ttu-id="99815-103">Estabilização de Vídeo MFT</span><span class="sxs-lookup"><span data-stu-id="99815-103">Video Stabilization MFT</span></span>

<span data-ttu-id="99815-104">O MFT de estabilização de vídeo é uma Microsoft Media Foundation transformação (MFT) que executa a estabilização de imagem em um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="99815-104">The video stabilization MFT is a Microsoft Media Foundation transform (MFT) that performs image stabilization on a video stream.</span></span>

## <a name="clsid"></a><span data-ttu-id="99815-105">CLSID</span><span class="sxs-lookup"><span data-stu-id="99815-105">CLSID</span></span>

<span data-ttu-id="99815-106">\_CMSVIDEODSPMFT CLSID</span><span class="sxs-lookup"><span data-stu-id="99815-106">CLSID\_CMSVideoDSPMFT</span></span>

## <a name="interfaces"></a><span data-ttu-id="99815-107">Interfaces</span><span class="sxs-lookup"><span data-stu-id="99815-107">Interfaces</span></span>

-   [<span data-ttu-id="99815-108">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="99815-108">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="99815-109">**IMFAttributes**</span><span class="sxs-lookup"><span data-stu-id="99815-109">**IMFAttributes**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [<span data-ttu-id="99815-110">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="99815-110">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="99815-111">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="99815-111">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="99815-112">**IMediaExtension**</span><span class="sxs-lookup"><span data-stu-id="99815-112">**IMediaExtension**</span></span>](/uwp/api/Windows.Media.IMediaExtension?view=winrt-19041)

## <a name="input-formats"></a><span data-ttu-id="99815-113">Formatos de entrada</span><span class="sxs-lookup"><span data-stu-id="99815-113">Input Formats</span></span>

<span data-ttu-id="99815-114">As combinações de tipo de mídia de entrada e subtipo aceitas pelo MFT de estabilização de vídeo para vídeo descompactado são:</span><span class="sxs-lookup"><span data-stu-id="99815-114">The input media type and sub-type combinations accepted by the video stabilization MFT for uncompressed video are:</span></span>

-   <span data-ttu-id="99815-115">**vídeo de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="99815-115">**MEDIATYPE\_VIDEO**</span></span>
-   <span data-ttu-id="99815-116">**MEDIASUBTYPE \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="99815-116">**MEDIASUBTYPE\_NV12**</span></span>
-   <span data-ttu-id="99815-117">**MEDIASUBTYPE \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="99815-117">**MEDIASUBTYPE\_YUY2**</span></span>

## <a name="output-formats"></a><span data-ttu-id="99815-118">Formatos de saída</span><span class="sxs-lookup"><span data-stu-id="99815-118">Output Formats</span></span>

<span data-ttu-id="99815-119">As combinações de tipo e subtipo de mídia de saída aceitas pelo MFT de estabilização de vídeo são:</span><span class="sxs-lookup"><span data-stu-id="99815-119">The output media type and sub-type combinations accepted by the video stabilization MFT are:</span></span>

-   <span data-ttu-id="99815-120">**vídeo de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="99815-120">**MEDIATYPE\_VIDEO**</span></span>
-   <span data-ttu-id="99815-121">**MEDIASUBTYPE \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="99815-121">**MEDIASUBTYPE\_NV12**</span></span>

<span data-ttu-id="99815-122">O tipo de mídia de entrada deve ser definido antes do tipo de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="99815-122">The input media type must be set before the output media type.</span></span> <span data-ttu-id="99815-123">Na maioria das situações, o suporte a formato limitado não é um problema porque o pipeline insere automaticamente as conversões de cor necessárias.</span><span class="sxs-lookup"><span data-stu-id="99815-123">In most situations, the limited format support is not an issue because the pipeline automatically inserts the necessary color conversions.</span></span>

<span data-ttu-id="99815-124">O componente MFT de estabilização de vídeo é capaz de alterar o formato dinâmico quando a entrada é alterada.</span><span class="sxs-lookup"><span data-stu-id="99815-124">The video stabilization MFT component is capable of dynamic format change when input changes.</span></span> <span data-ttu-id="99815-125">Quando o tamanho da imagem de entrada for alterado ou o subtipo for alterado, ele irá disparar uma alteração de formato dinâmico no fluxo de saída.</span><span class="sxs-lookup"><span data-stu-id="99815-125">When the input picture size changes or the subtype changes, it will trigger a dynamic format change on the output stream.</span></span>

<span data-ttu-id="99815-126">A MFT de estabilização de vídeo fará a conversão de cores nos seguintes casos:</span><span class="sxs-lookup"><span data-stu-id="99815-126">The video stabilization MFT will do color conversion in the following cases:</span></span>

-   <span data-ttu-id="99815-127">Quando o formato de entrada é **MEDIASUBTYPE \_ YUY2**.</span><span class="sxs-lookup"><span data-stu-id="99815-127">When the input format is **MEDIASUBTYPE\_YUY2**.</span></span>
-   <span data-ttu-id="99815-128">Quando o modo de compatibilidade do Microsoft DirectX 9,0 é usado.</span><span class="sxs-lookup"><span data-stu-id="99815-128">When Microsoft DirectX 9.0 compatibility mode is used.</span></span>

### <a name="attributes"></a><span data-ttu-id="99815-129">Atributos</span><span class="sxs-lookup"><span data-stu-id="99815-129">Attributes</span></span>

<span data-ttu-id="99815-130">Os atributos a seguir têm suporte pelo MFT de estabilização de vídeo por meio da interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="99815-130">The following attributes are supported by the video stabilization MFT through the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

-   <span data-ttu-id="99815-131">O [modo MF \_ VIDEODSP \_ ](mf-videodsp-mode.md) do atributo coloca a MFT de estabilização de vídeo no modo de estabilização ou no modo de passagem.</span><span class="sxs-lookup"><span data-stu-id="99815-131">The attribute [MF\_VIDEODSP\_MODE](mf-videodsp-mode.md) puts the video stabilization MFT into either stabilization mode or pass-through mode.</span></span> <span data-ttu-id="99815-132">O aplicativo deve chamar [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) no **\_ \_ tipo VIDEODSP** do GUID MF com um inteiro correspondente a um dos seguintes valores válidos: **MFVideoDSPMode \_ estabilization** = 4, **MFVideoDSPMode \_ PassThrough** = 1.</span><span class="sxs-lookup"><span data-stu-id="99815-132">The application should call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) on the GUID **MF\_VIDEODSP\_TYPE** with an integer corresponding to one of the following valid values: **MFVideoDSPMode\_Stabilization** = 4, **MFVideoDSPMode\_Passthrough** = 1.</span></span> <span data-ttu-id="99815-133">O \_ modo MF VIDEODSP \_ pode ser alterado a qualquer momento durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="99815-133">MF\_VIDEODSP\_MODE can be changed at any time during playback.</span></span> <span data-ttu-id="99815-134">Isso causa uma alteração no modo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="99815-134">This causes a dynamic mode change.</span></span> <span data-ttu-id="99815-135">A saída mudará para estabilizada ou passará após 16 ou 2 quadros (dependendo do modo de latência) depois que o atributo for alterado.</span><span class="sxs-lookup"><span data-stu-id="99815-135">The output will switch to either stabilized or pass through after either 16 or 2 frames (depending on the latency mode) after the attribute is changed.</span></span>
-   <span data-ttu-id="99815-136">O atributo [MF de \_ baixa \_ LATÊNCIA](mf-low-latency.md) coloca o MFT de estabilização de vídeo no modo de baixa latência ou no modo de alta qualidade.</span><span class="sxs-lookup"><span data-stu-id="99815-136">The attribute [MF\_LOW\_LATENCY](mf-low-latency.md) puts the video stabilization MFT into either low latency mode or high quality mode.</span></span> <span data-ttu-id="99815-137">O aplicativo deve chamar [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) na **\_ baixa \_ latência de MF** de GUID com um inteiro correspondente a um dos seguintes valores válidos: baixa latência = 1 alta qualidade = 0</span><span class="sxs-lookup"><span data-stu-id="99815-137">The application should call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) on the GUID **MF\_LOW\_LATENCY** with an integer corresponding to one of the following valid values: Low latency = 1 High Quality = 0</span></span>
-   <span data-ttu-id="99815-138">O atributo [MF \_ SA \_ D3D11 \_ BINDFLAGS](mf-sa-d3d11-bindflags.md) é usado pelo pipeline para especificar os sinalizadores de associação de D3D11 para criar os exemplos de saída com.</span><span class="sxs-lookup"><span data-stu-id="99815-138">The attribute [MF\_SA\_D3D11\_BINDFLAGS](mf-sa-d3d11-bindflags.md) is used by the pipeline to specify the D3D11 bind flags to create the output samples with.</span></span> <span data-ttu-id="99815-139">Qualquer combinação de valores da enumeração [**\_ \_ sinalizador de associação D3D11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) é válida.</span><span class="sxs-lookup"><span data-stu-id="99815-139">Any combination of values from the [**D3D11\_BIND\_FLAG**](/windows/win32/api/d3d11/ne-d3d11-d3d11_bind_flag) enumeration is valid.</span></span>
-   <span data-ttu-id="99815-140">A **contagem de \_ \_ amostra de \_ saída \_ \_ mínima do atributo MF SA** é usada pelo pipeline para especificar o número mínimo de amostras para as quais esse componente deve dar suporte na saída.</span><span class="sxs-lookup"><span data-stu-id="99815-140">The attribute **MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT** is used by the pipeline to specify the minimum number of samples that this component must support on output.</span></span>
-   <span data-ttu-id="99815-141">O atributo [MFSampleExtension \_ VideoDSPMode](mfsampleextension-videodspmode.md) é definido em cada exemplo produzido por estabilização para indicar o [ \_ \_ modo de VIDEODSP de MF](mf-videodsp-mode.md) em vigor aplicado a esse exemplo (se a amostra foi estabilizada ou não).</span><span class="sxs-lookup"><span data-stu-id="99815-141">The attribute [MFSampleExtension\_VideoDSPMode](mfsampleextension-videodspmode.md) is set on every sample produced by stabilization to indicate the effective [MF\_VIDEODSP\_MODE](mf-videodsp-mode.md) applied to that sample (whether or not the sample was stabilized).</span></span> <span data-ttu-id="99815-142">Em determinadas condições, os exemplos não podem ser estabilizados (devido à alta carga do sistema ou solicitações pelo usuário).</span><span class="sxs-lookup"><span data-stu-id="99815-142">Under certain conditions, samples may not be stabilized (due to high system load, or requests by the user).</span></span> <span data-ttu-id="99815-143">Esse atributo tem os mesmos valores que o \_ atributo de modo MF VIDEODSP \_ (**\_ estabilização de MFVideoDSPMode** e **\_ passagem de MFVideoDSPMode**).</span><span class="sxs-lookup"><span data-stu-id="99815-143">This attribute has the same values as the MF\_VIDEODSP\_MODE attribute (**MFVideoDSPMode\_Stabilization** and **MFVideoDSPMode\_Passthrough**).</span></span> <span data-ttu-id="99815-144">Para obter o valor deste atributo, os aplicativos devem chamar [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) no GUID **MFSampleExtension \_ VideoDSPMode**.</span><span class="sxs-lookup"><span data-stu-id="99815-144">To get the value of this attribute applications should call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) on GUID **MFSampleExtension\_VideoDSPMode**.</span></span>

## <a name="remarks"></a><span data-ttu-id="99815-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="99815-145">Remarks</span></span>

<span data-ttu-id="99815-146">Uma instância do DSP de estabilização de vídeo pode ser criada de uma das seguintes maneiras:</span><span class="sxs-lookup"><span data-stu-id="99815-146">An instance of the video stabilization DSP can be created in one of the following ways:</span></span>

-   <span data-ttu-id="99815-147">Chamando [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span><span class="sxs-lookup"><span data-stu-id="99815-147">By calling [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span> <span data-ttu-id="99815-148">O DSP de estabilização de vídeo é registrado na categoria de **\_ efeito de \_ vídeo \_ da categoria MFT** .</span><span class="sxs-lookup"><span data-stu-id="99815-148">The video stabilization DSP is registered under the **MFT\_CATEGORY\_VIDEO\_EFFECT** category.</span></span>
-   <span data-ttu-id="99815-149">Chamando a função COM **CoCreateInstance** passando-a para o CLSID **CLSID \_ CMSVideoDSPMFT**.</span><span class="sxs-lookup"><span data-stu-id="99815-149">By calling the COM function **CoCreateInstance** passing it the CLSID **CLSID\_CMSVideoDSPMFT**.</span></span> <span data-ttu-id="99815-150">Para usar esse método, você deve incluir wmcodecdsp. h e vincular em wmcodecdspuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="99815-150">To use this method, you must include wmcodecdsp.h and link against wmcodecdspuuid.lib.</span></span>

<span data-ttu-id="99815-151">Além disso, o DSP de estabilização de vídeo dá suporte à instanciação usando Windows Runtime como uma extensão de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="99815-151">Additionally, the video stabilization DSP supports instantiation using Windows Runtime as a Windows Media Extension.</span></span> <span data-ttu-id="99815-152">Ele é definido no [**Windows. Media. VideoEffects**](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041), e seu nome completo é "Windows. Media. VideoEffects. VideoStabilization".</span><span class="sxs-lookup"><span data-stu-id="99815-152">It is defined on the [**Windows.Media.VideoEffects**](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041), and its full name is "Windows.Media.VideoEffects.VideoStabilization".</span></span>

## <a name="requirements"></a><span data-ttu-id="99815-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99815-153">Requirements</span></span>



| <span data-ttu-id="99815-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="99815-154">Requirement</span></span> | <span data-ttu-id="99815-155">Valor</span><span class="sxs-lookup"><span data-stu-id="99815-155">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="99815-156">parâmetro</span><span class="sxs-lookup"><span data-stu-id="99815-156">Header</span></span><br/> | <dl> <span data-ttu-id="99815-157"><dt>Camerauicontrol. h</dt></span><span class="sxs-lookup"><span data-stu-id="99815-157"><dt>Camerauicontrol.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99815-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="99815-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99815-159">Processadores de sinais digitais</span><span class="sxs-lookup"><span data-stu-id="99815-159">Digital Signal Processors</span></span>](windowsmediadigitalsignalprocessors.md)
</dt> <dt>

[<span data-ttu-id="99815-160">**Windows.Media.VideoEffects**</span><span class="sxs-lookup"><span data-stu-id="99815-160">**Windows.Media.VideoEffects**</span></span>](/uwp/api/Windows.Media.VideoEffects?view=winrt-19041)
</dt> </dl>

 

 
