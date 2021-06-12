---
description: Saiba mais sobre os tipos de mídia no DirectShow. O tipo de mídia é uma maneira universal e extensível de descrever formatos de mídia digital.
ms.assetid: 9984ba36-4e43-4886-a073-34b330274c9c
title: Sobre tipos de mídia (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b1489543b33f5eeb2c288add48148b37f31915
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2021
ms.locfileid: "112010889"
---
# <a name="about-media-types-directshow"></a><span data-ttu-id="e90dc-104">Sobre tipos de mídia (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="e90dc-104">About Media Types (DirectShow)</span></span>

<span data-ttu-id="e90dc-105">Como o DirectShow é modular, ele requer uma maneira de descrever o formato dos dados em cada ponto no grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="e90dc-105">Because DirectShow is modular, it requires a way to describe the format of the data at each point in the filter graph.</span></span> <span data-ttu-id="e90dc-106">Por exemplo, considere a reprodução DE AVI.</span><span class="sxs-lookup"><span data-stu-id="e90dc-106">For example, consider AVI playback.</span></span> <span data-ttu-id="e90dc-107">Os dados entram no grafo como um fluxo de partes DE VALOR.</span><span class="sxs-lookup"><span data-stu-id="e90dc-107">Data enters the graph as a stream of RIFF chunks.</span></span> <span data-ttu-id="e90dc-108">Eles são analisados em fluxos de áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="e90dc-108">These are parsed into video and audio streams.</span></span> <span data-ttu-id="e90dc-109">O fluxo de vídeo consiste em quadros de vídeo, que provavelmente são compactados.</span><span class="sxs-lookup"><span data-stu-id="e90dc-109">The video stream consists of video frames, which are probably compressed.</span></span> <span data-ttu-id="e90dc-110">Após a decodificação, o fluxo de vídeo é uma série de bitmaps descompactados.</span><span class="sxs-lookup"><span data-stu-id="e90dc-110">After decoding, the video stream is a series of uncompressed bitmaps.</span></span> <span data-ttu-id="e90dc-111">O fluxo de áudio passa por um processo semelhante.</span><span class="sxs-lookup"><span data-stu-id="e90dc-111">The audio stream goes through a similar process.</span></span>

<span data-ttu-id="e90dc-112">Tipos de mídia: como o DirectShow representa formatos</span><span class="sxs-lookup"><span data-stu-id="e90dc-112">Media Types: How DirectShow Represents Formats</span></span>

<span data-ttu-id="e90dc-113">O *tipo de mídia* é uma maneira universal e extensível de descrever formatos de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="e90dc-113">The *media type* is a universal and extensible way to describe digital media formats.</span></span> <span data-ttu-id="e90dc-114">Quando dois filtros se conectam, eles concordam com um tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="e90dc-114">When two filters connect, they agree on a media type.</span></span> <span data-ttu-id="e90dc-115">O tipo de mídia identifica que tipo de dados o filtro upstream fornecerá ao filtro downstream e o layout físico dos dados.</span><span class="sxs-lookup"><span data-stu-id="e90dc-115">The media type identifies what kind of data the upstream filter will deliver to the downstream filter, and the physical layout of the data.</span></span> <span data-ttu-id="e90dc-116">Se dois filtros não puderem concordar com um tipo de mídia, eles não se conectarão.</span><span class="sxs-lookup"><span data-stu-id="e90dc-116">If two filters cannot agree on a media type, they will not connect.</span></span>

<span data-ttu-id="e90dc-117">Para alguns aplicativos, você nunca terá que se preocupar com tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="e90dc-117">For some applications, you will never have to worry about media types.</span></span> <span data-ttu-id="e90dc-118">Na reprodução de arquivo, por exemplo, o DirectShow trata todos os detalhes.</span><span class="sxs-lookup"><span data-stu-id="e90dc-118">In file playback, for example, DirectShow handles all of the details.</span></span> <span data-ttu-id="e90dc-119">Outros tipos de aplicativos podem precisar trabalhar diretamente com tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="e90dc-119">Other kinds of applications may need to work directly with media types.</span></span>

<span data-ttu-id="e90dc-120">Os tipos de mídia são definidos usando a [**estrutura AM \_ MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)</span><span class="sxs-lookup"><span data-stu-id="e90dc-120">Media types are defined using the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="e90dc-121">Essa estrutura contém as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="e90dc-121">This structure contains the following information:</span></span>

-   <span data-ttu-id="e90dc-122">**Tipo principal:** o tipo principal é um GUID que define a categoria geral dos dados.</span><span class="sxs-lookup"><span data-stu-id="e90dc-122">**Major type**: The major type is a GUID that defines the overall category of the data.</span></span> <span data-ttu-id="e90dc-123">Os principais tipos incluem vídeo, áudio, fluxo de byte não esparso, dados MIDI e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="e90dc-123">Major types include video, audio, unparsed byte stream, MIDI data, and so forth.</span></span>
-   <span data-ttu-id="e90dc-124">**Subtipo**: o subtipo é outro GUID, que define ainda mais o formato.</span><span class="sxs-lookup"><span data-stu-id="e90dc-124">**Subtype**: The subtype is another GUID, which further defines the format.</span></span> <span data-ttu-id="e90dc-125">Por exemplo, dentro do tipo principal de vídeo, há subtipos para RGB-24, RGB-32, UYVY e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="e90dc-125">For example, within the video major type, there are subtypes for RGB-24, RGB-32, UYVY, and so forth.</span></span> <span data-ttu-id="e90dc-126">No áudio, há áudio PCM, conteúdo MPEG-1 e outros.</span><span class="sxs-lookup"><span data-stu-id="e90dc-126">Within audio, there is PCM audio, MPEG-1 payload, and others.</span></span> <span data-ttu-id="e90dc-127">O subtipo fornece mais informações do que o tipo principal, mas não define tudo sobre o formato.</span><span class="sxs-lookup"><span data-stu-id="e90dc-127">The subtype provides more information than the major type, but it does not define everything about the format.</span></span> <span data-ttu-id="e90dc-128">Por exemplo, subtipos de vídeo não definem o tamanho da imagem ou a taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="e90dc-128">For example, video subtypes do not define the image size or the frame rate.</span></span> <span data-ttu-id="e90dc-129">Elas são definidas pelo bloco de formato, descrito abaixo.</span><span class="sxs-lookup"><span data-stu-id="e90dc-129">These are defined by the format block, described below.</span></span>
-   <span data-ttu-id="e90dc-130">**Bloco de** formato: o bloco de formato é um bloco de dados que descreve o formato em detalhes.</span><span class="sxs-lookup"><span data-stu-id="e90dc-130">**Format block**: The format block is a block of data that describes the format in detail.</span></span> <span data-ttu-id="e90dc-131">O bloco de formato é alocado separadamente da estrutura [**AM \_ MEDIA \_ TYPE.**](/windows/win32/api/strmif/ns-strmif-am_media_type)</span><span class="sxs-lookup"><span data-stu-id="e90dc-131">The format block is allocated separately from the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="e90dc-132">O **membro pbFormat** da estrutura **AM MEDIA \_ \_ TYPE** aponta para o bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="e90dc-132">The **pbFormat** member of the **AM\_MEDIA\_TYPE** structure points to the format block.</span></span>

    <span data-ttu-id="e90dc-133">O **membro pbFormat** é digitado \**\* void* _ porque o layout do bloco de formato muda dependendo do tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="e90dc-133">The **pbFormat** member is typed \**void\** _ because the layout of the format block changes depending on the media type.</span></span> <span data-ttu-id="e90dc-134">Por exemplo, o áudio PCM usa uma [estrutura _ *WAVEFORMATEX.* \*](/previous-versions/dd757713(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e90dc-134">For example, PCM audio uses a [_ *WAVEFORMATEX*\*](/previous-versions/dd757713(v=vs.85)) structure.</span></span> <span data-ttu-id="e90dc-135">O vídeo usa várias estruturas, incluindo [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) [**e VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)</span><span class="sxs-lookup"><span data-stu-id="e90dc-135">Video uses various structures, including [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) and [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span></span> <span data-ttu-id="e90dc-136">O **membro formattype** da estrutura [**AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) é um GUID que especifica qual estrutura está contida no bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="e90dc-136">The **formattype** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure is a GUID that specifies which structure is contained in the format block.</span></span> <span data-ttu-id="e90dc-137">Cada estrutura de formato recebe um GUID.</span><span class="sxs-lookup"><span data-stu-id="e90dc-137">Each format structure is assigned a GUID.</span></span> <span data-ttu-id="e90dc-138">O **membro cbFormat** especifica o tamanho do bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="e90dc-138">The **cbFormat** member specifies the size of the format block.</span></span> <span data-ttu-id="e90dc-139">Sempre verifique esses valores antes de desreferenciar o **ponteiro pbFormat.**</span><span class="sxs-lookup"><span data-stu-id="e90dc-139">Always check these values before dereferencing the **pbFormat** pointer.</span></span>

<span data-ttu-id="e90dc-140">Se o bloco de formato for preenchido, o tipo principal e o subtipo conterão informações redundantes.</span><span class="sxs-lookup"><span data-stu-id="e90dc-140">If the format block is filled in, then the major type and subtype contain redundant information.</span></span> <span data-ttu-id="e90dc-141">No entanto, o tipo principal e o subtipo fornecem uma maneira conveniente de identificar formatos sem um bloco de formato completo.</span><span class="sxs-lookup"><span data-stu-id="e90dc-141">The major type and subtype, however, provide a convenient way to identify formats without a complete format block.</span></span> <span data-ttu-id="e90dc-142">Por exemplo, você pode especificar um formato RGB genérico de 24 bits (MEDIASUBTYPE RGB24), sem saber todas as informações exigidas pela estrutura \_ [**VIDEOINFOHEADER,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) como o tamanho da imagem e a taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="e90dc-142">For example, you can specify a generic 24-bit RGB format (MEDIASUBTYPE\_RGB24), without knowing all of the information required by the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure, such as image size and frame rate.</span></span>

<span data-ttu-id="e90dc-143">Por exemplo, um filtro pode usar o seguinte código para verificar um tipo de mídia:</span><span class="sxs-lookup"><span data-stu-id="e90dc-143">For example, a filter might use the following code to check a media type:</span></span>


```C++
HRESULT CheckMediaType(AM_MEDIA_TYPE *pmt)
{
    if (pmt == NULL) return E_POINTER;

    // Check the major type. We're looking for video.
    if (pmt->majortype != MEDIATYPE_Video)
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the subtype. We're looking for 24-bit RGB.
    if (pmt->subtype != MEDIASUBTYPE_RGB24)
    {
        return VFW_E_INVALIDMEDIATYPE;
    }

    // Check the format type and the size of the format block.
    if ((pmt->formattype == FORMAT_VideoInfo) &&
         (pmt->cbFormat >= sizeof(VIDEOINFOHEADER) &&
         (pmt->pbFormat != NULL))
    {
        // Now it's safe to coerce the format block pointer to the
        // correct structure, as defined by the formattype GUID.
        VIDEOINFOHEADER *pVIH = (VIDEOINFOHEADER*)pmt->pbFormat;
    
        // Examine pVIH (not shown). If it looks OK, return S_OK.
        return S_OK;
    }

    return VFW_E_INVALIDMEDIATYPE;
}
```



<span data-ttu-id="e90dc-144">A [**estrutura AM MEDIA \_ \_ TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) também contém alguns campos opcionais.</span><span class="sxs-lookup"><span data-stu-id="e90dc-144">The [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure also contains some optional fields.</span></span> <span data-ttu-id="e90dc-145">Eles podem ser usados para fornecer informações adicionais, mas os filtros não são necessários para usá-los:</span><span class="sxs-lookup"><span data-stu-id="e90dc-145">These can be used to provide additional information, but filters are not required to use them:</span></span>

-   <span data-ttu-id="e90dc-146">**lSampleSize**.</span><span class="sxs-lookup"><span data-stu-id="e90dc-146">**lSampleSize**.</span></span> <span data-ttu-id="e90dc-147">Se esse campo for não zero, ele definirá o tamanho de cada amostra.</span><span class="sxs-lookup"><span data-stu-id="e90dc-147">If this field is non-zero, it defines the size of each sample.</span></span> <span data-ttu-id="e90dc-148">Se for zero, isso indicará que o tamanho da amostra pode mudar de exemplo para exemplo.</span><span class="sxs-lookup"><span data-stu-id="e90dc-148">If it is zero, it indicates that the sample size may change from sample to sample.</span></span>
-   <span data-ttu-id="e90dc-149">**bFixedSizeSamples.**</span><span class="sxs-lookup"><span data-stu-id="e90dc-149">**bFixedSizeSamples**.</span></span> <span data-ttu-id="e90dc-150">Se esse sinalizador booliana **for TRUE,** isso significa que o valor em **lSampleSize** é válido.</span><span class="sxs-lookup"><span data-stu-id="e90dc-150">If this Boolean flag is **TRUE**, it means the value in **lSampleSize** is valid.</span></span> <span data-ttu-id="e90dc-151">Caso contrário, você deve ignorar **lSampleSize**.</span><span class="sxs-lookup"><span data-stu-id="e90dc-151">Otherwise, you should ignore **lSampleSize**.</span></span>
-   <span data-ttu-id="e90dc-152">**bTemporalCompression**.</span><span class="sxs-lookup"><span data-stu-id="e90dc-152">**bTemporalCompression**.</span></span> <span data-ttu-id="e90dc-153">Se esse sinalizador booliana for **FALSE,** isso significa que todos os quadros são quadros-chave.</span><span class="sxs-lookup"><span data-stu-id="e90dc-153">If this Boolean flag is **FALSE**, it means that all frames are key frames.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e90dc-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e90dc-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e90dc-155">O grafo de filtro e seus componentes</span><span class="sxs-lookup"><span data-stu-id="e90dc-155">The Filter Graph and Its Components</span></span>](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 
