---
description: Sobre os tipos de mídia
ms.assetid: 9984ba36-4e43-4886-a073-34b330274c9c
title: Sobre os tipos de mídia (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3289a37e95bf5dbd1e5c277b5799a2c7c8c90586
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297895"
---
# <a name="about-media-types-directshow"></a><span data-ttu-id="a065e-103">Sobre os tipos de mídia (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="a065e-103">About Media Types (DirectShow)</span></span>

<span data-ttu-id="a065e-104">Como o DirectShow é modular, ele requer uma maneira de descrever o formato dos dados em cada ponto do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="a065e-104">Because DirectShow is modular, it requires a way to describe the format of the data at each point in the filter graph.</span></span> <span data-ttu-id="a065e-105">Por exemplo, considere a reprodução de AVI.</span><span class="sxs-lookup"><span data-stu-id="a065e-105">For example, consider AVI playback.</span></span> <span data-ttu-id="a065e-106">Os dados entram no grafo como um fluxo de partes do RIFF.</span><span class="sxs-lookup"><span data-stu-id="a065e-106">Data enters the graph as a stream of RIFF chunks.</span></span> <span data-ttu-id="a065e-107">Eles são analisados em fluxos de áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="a065e-107">These are parsed into video and audio streams.</span></span> <span data-ttu-id="a065e-108">O fluxo de vídeo consiste em quadros de vídeo, que provavelmente são compactados.</span><span class="sxs-lookup"><span data-stu-id="a065e-108">The video stream consists of video frames, which are probably compressed.</span></span> <span data-ttu-id="a065e-109">Após a decodificação, o fluxo de vídeo é uma série de bitmaps descompactados.</span><span class="sxs-lookup"><span data-stu-id="a065e-109">After decoding, the video stream is a series of uncompressed bitmaps.</span></span> <span data-ttu-id="a065e-110">O fluxo de áudio passa por um processo semelhante.</span><span class="sxs-lookup"><span data-stu-id="a065e-110">The audio stream goes through a similar process.</span></span>

<span data-ttu-id="a065e-111">Tipos de mídia: como o DirectShow representa formatos</span><span class="sxs-lookup"><span data-stu-id="a065e-111">Media Types: How DirectShow Represents Formats</span></span>

<span data-ttu-id="a065e-112">O *tipo de mídia* é uma maneira universal e extensível de descrever formatos de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="a065e-112">The *media type* is a universal and extensible way to describe digital media formats.</span></span> <span data-ttu-id="a065e-113">Quando dois filtros se conectam, eles concordam em um tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="a065e-113">When two filters connect, they agree on a media type.</span></span> <span data-ttu-id="a065e-114">O tipo de mídia identifica o tipo de dados que o filtro upstream fornecerá ao filtro downstream e o layout físico dos dados.</span><span class="sxs-lookup"><span data-stu-id="a065e-114">The media type identifies what kind of data the upstream filter will deliver to the downstream filter, and the physical layout of the data.</span></span> <span data-ttu-id="a065e-115">Se dois filtros não conseguirem concordar em um tipo de mídia, eles não serão conectados.</span><span class="sxs-lookup"><span data-stu-id="a065e-115">If two filters cannot agree on a media type, they will not connect.</span></span>

<span data-ttu-id="a065e-116">Para alguns aplicativos, você nunca precisará se preocupar com os tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="a065e-116">For some applications, you will never have to worry about media types.</span></span> <span data-ttu-id="a065e-117">Na reprodução de arquivo, por exemplo, o DirectShow lida com todos os detalhes.</span><span class="sxs-lookup"><span data-stu-id="a065e-117">In file playback, for example, DirectShow handles all of the details.</span></span> <span data-ttu-id="a065e-118">Outros tipos de aplicativos podem precisar trabalhar diretamente com os tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="a065e-118">Other kinds of applications may need to work directly with media types.</span></span>

<span data-ttu-id="a065e-119">Os tipos de mídia são definidos usando a estrutura [**am \_ Media \_ Type**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="a065e-119">Media types are defined using the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="a065e-120">Essa estrutura contém as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="a065e-120">This structure contains the following information:</span></span>

-   <span data-ttu-id="a065e-121">**Tipo principal**: o tipo principal é um GUID que define a categoria geral dos dados.</span><span class="sxs-lookup"><span data-stu-id="a065e-121">**Major type**: The major type is a GUID that defines the overall category of the data.</span></span> <span data-ttu-id="a065e-122">Os tipos principais incluem vídeo, áudio, fluxo de bytes não analisado, dados MIDI e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="a065e-122">Major types include video, audio, unparsed byte stream, MIDI data, and so forth.</span></span>
-   <span data-ttu-id="a065e-123">**Subtipo**: o subtipo é outro GUID, que define ainda mais o formato.</span><span class="sxs-lookup"><span data-stu-id="a065e-123">**Subtype**: The subtype is another GUID, which further defines the format.</span></span> <span data-ttu-id="a065e-124">Por exemplo, dentro do tipo principal de vídeo, há subtipos para RGB-24, RGB-32, UYVY e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="a065e-124">For example, within the video major type, there are subtypes for RGB-24, RGB-32, UYVY, and so forth.</span></span> <span data-ttu-id="a065e-125">No áudio, há uma carga de áudio PCM, MPEG-1 e outras.</span><span class="sxs-lookup"><span data-stu-id="a065e-125">Within audio, there is PCM audio, MPEG-1 payload, and others.</span></span> <span data-ttu-id="a065e-126">O subtipo fornece mais informações do que o tipo principal, mas não define tudo sobre o formato.</span><span class="sxs-lookup"><span data-stu-id="a065e-126">The subtype provides more information than the major type, but it does not define everything about the format.</span></span> <span data-ttu-id="a065e-127">Por exemplo, os subtipos de vídeo não definem o tamanho da imagem ou a taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="a065e-127">For example, video subtypes do not define the image size or the frame rate.</span></span> <span data-ttu-id="a065e-128">Eles são definidos pelo bloco de formato, descrito abaixo.</span><span class="sxs-lookup"><span data-stu-id="a065e-128">These are defined by the format block, described below.</span></span>
-   <span data-ttu-id="a065e-129">**Bloco de formato**: o bloco de formato é um bloco de dados que descreve o formato em detalhes.</span><span class="sxs-lookup"><span data-stu-id="a065e-129">**Format block**: The format block is a block of data that describes the format in detail.</span></span> <span data-ttu-id="a065e-130">O bloco de formato é alocado separadamente da estrutura do [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="a065e-130">The format block is allocated separately from the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="a065e-131">O membro **pbFormat** da estrutura **do \_ \_ tipo de mídia am** aponta para o bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="a065e-131">The **pbFormat** member of the **AM\_MEDIA\_TYPE** structure points to the format block.</span></span>

    <span data-ttu-id="a065e-132">O membro **pbFormat** é digitado \*\* \* void\* _ porque o layout do bloco de formato muda dependendo do tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="a065e-132">The **pbFormat** member is typed \**void\** _ because the layout of the format block changes depending on the media type.</span></span> <span data-ttu-id="a065e-133">Por exemplo, o áudio PCM usa uma estrutura [_ *WAVEFORMATEX* \*](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a065e-133">For example, PCM audio uses a [_ *WAVEFORMATEX*\*](/previous-versions/dd757713(v=vs.85)) structure.</span></span> <span data-ttu-id="a065e-134">O vídeo usa várias estruturas, incluindo [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) e [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span><span class="sxs-lookup"><span data-stu-id="a065e-134">Video uses various structures, including [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) and [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2).</span></span> <span data-ttu-id="a065e-135">O membro **formatType** da estrutura [**do \_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) é um GUID que especifica qual estrutura está contida no bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="a065e-135">The **formattype** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure is a GUID that specifies which structure is contained in the format block.</span></span> <span data-ttu-id="a065e-136">Cada estrutura de formato é atribuída a um GUID.</span><span class="sxs-lookup"><span data-stu-id="a065e-136">Each format structure is assigned a GUID.</span></span> <span data-ttu-id="a065e-137">O membro **cbFormat** especifica o tamanho do bloco de formato.</span><span class="sxs-lookup"><span data-stu-id="a065e-137">The **cbFormat** member specifies the size of the format block.</span></span> <span data-ttu-id="a065e-138">Sempre verifique esses valores antes de desreferenciar o ponteiro **pbFormat** .</span><span class="sxs-lookup"><span data-stu-id="a065e-138">Always check these values before dereferencing the **pbFormat** pointer.</span></span>

<span data-ttu-id="a065e-139">Se o bloco de formato estiver preenchido, o tipo e subtipo principal contêm informações redundantes.</span><span class="sxs-lookup"><span data-stu-id="a065e-139">If the format block is filled in, then the major type and subtype contain redundant information.</span></span> <span data-ttu-id="a065e-140">O tipo e subtipo principal, no entanto, fornecem uma maneira conveniente de identificar formatos sem um bloco de formato completo.</span><span class="sxs-lookup"><span data-stu-id="a065e-140">The major type and subtype, however, provide a convenient way to identify formats without a complete format block.</span></span> <span data-ttu-id="a065e-141">Por exemplo, você pode especificar um formato RGB genérico de 24 bits (MEDIASUBTYPE \_ RGB24), sem conhecer todas as informações exigidas pela estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , como tamanho da imagem e taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="a065e-141">For example, you can specify a generic 24-bit RGB format (MEDIASUBTYPE\_RGB24), without knowing all of the information required by the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) structure, such as image size and frame rate.</span></span>

<span data-ttu-id="a065e-142">Por exemplo, um filtro pode usar o seguinte código para verificar um tipo de mídia:</span><span class="sxs-lookup"><span data-stu-id="a065e-142">For example, a filter might use the following code to check a media type:</span></span>


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



<span data-ttu-id="a065e-143">A estrutura do [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) também contém alguns campos opcionais.</span><span class="sxs-lookup"><span data-stu-id="a065e-143">The [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure also contains some optional fields.</span></span> <span data-ttu-id="a065e-144">Eles podem ser usados para fornecer informações adicionais, mas não são necessários filtros para usá-los:</span><span class="sxs-lookup"><span data-stu-id="a065e-144">These can be used to provide additional information, but filters are not required to use them:</span></span>

-   <span data-ttu-id="a065e-145">**lSampleSize**.</span><span class="sxs-lookup"><span data-stu-id="a065e-145">**lSampleSize**.</span></span> <span data-ttu-id="a065e-146">Se esse campo for diferente de zero, ele definirá o tamanho de cada exemplo.</span><span class="sxs-lookup"><span data-stu-id="a065e-146">If this field is non-zero, it defines the size of each sample.</span></span> <span data-ttu-id="a065e-147">Se for zero, indica que o tamanho da amostra pode ser alterado de amostra para amostra.</span><span class="sxs-lookup"><span data-stu-id="a065e-147">If it is zero, it indicates that the sample size may change from sample to sample.</span></span>
-   <span data-ttu-id="a065e-148">**bFixedSizeSamples**.</span><span class="sxs-lookup"><span data-stu-id="a065e-148">**bFixedSizeSamples**.</span></span> <span data-ttu-id="a065e-149">Se esse sinalizador booliano for **true**, significa que o valor em **lSampleSize** é válido.</span><span class="sxs-lookup"><span data-stu-id="a065e-149">If this Boolean flag is **TRUE**, it means the value in **lSampleSize** is valid.</span></span> <span data-ttu-id="a065e-150">Caso contrário, você deve ignorar **lSampleSize**.</span><span class="sxs-lookup"><span data-stu-id="a065e-150">Otherwise, you should ignore **lSampleSize**.</span></span>
-   <span data-ttu-id="a065e-151">**bTemporalCompression**.</span><span class="sxs-lookup"><span data-stu-id="a065e-151">**bTemporalCompression**.</span></span> <span data-ttu-id="a065e-152">Se esse sinalizador booliano for **false**, significa que todos os quadros são quadros-chave.</span><span class="sxs-lookup"><span data-stu-id="a065e-152">If this Boolean flag is **FALSE**, it means that all frames are key frames.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a065e-153">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a065e-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a065e-154">O gráfico de filtro e seus componentes</span><span class="sxs-lookup"><span data-stu-id="a065e-154">The Filter Graph and Its Components</span></span>](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 
