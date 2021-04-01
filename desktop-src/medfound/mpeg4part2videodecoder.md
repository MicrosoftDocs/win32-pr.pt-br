---
description: O decodificador de vídeo da parte 2 do MPEG4 decodifica fluxos de vídeo que foram codificados de acordo com o padrão da parte 2 do MPEG4.
ms.assetid: 56e32d3c-9bd0-41fe-bb22-e4ff37b7cc5c
title: Decodificador de vídeo MPEG-4 parte 2 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 777e6144684c799eb58f75afd4811ccc8871a46b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164908"
---
# <a name="mpeg-4-part-2-video-decoder"></a><span data-ttu-id="8e9e5-103">Decodificador de vídeo MPEG-4 parte 2</span><span class="sxs-lookup"><span data-stu-id="8e9e5-103">MPEG-4 Part 2 Video Decoder</span></span>

<span data-ttu-id="8e9e5-104">O decodificador de vídeo da parte 2 do MPEG4 decodifica fluxos de vídeo que foram codificados de acordo com o padrão da parte 2 do MPEG4.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-104">The MPEG4 Part 2 Video decoder decodes video streams that were encoded according to the MPEG4 Part 2 standard.</span></span>

<span data-ttu-id="8e9e5-105">Você pode criar uma instância do decodificador de vídeo da parte 2 do MPEG4 chamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-105">You can create an instance of the MPEG4 Part 2 Video decoder by calling **CoCreateInstance**.</span></span> <span data-ttu-id="8e9e5-106">Para criar uma instância do decodificador que se comporta como um objeto de mídia do DirectX (DMO), use o **CLSID \_** do identificador de classe CMpeg4sDecMediaObject.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-106">To create an instance of the decoder that behaves as a DirectX Media Object (DMO), use the class identifier **CLSID\_CMpeg4sDecMediaObject**.</span></span> <span data-ttu-id="8e9e5-107">Para criar um Istance do decodificador que se comporta como uma Media Foundation transformação (MFT), use o CLSID do identificador de classe **\_ CMpeg4sDecMFT**.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-107">To create an istance of the decoder that behaves as a Media Foundation Transform (MFT), use the class identifier **CLSID\_CMpeg4sDecMFT**.</span></span>

## <a name="input-types"></a><span data-ttu-id="8e9e5-108">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="8e9e5-108">Input Types</span></span>

<span data-ttu-id="8e9e5-109">O decodificador de vídeo da parte 2 do MPEG4 dá suporte aos seguintes tipos de mídia de entrada.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-109">The MPEG4 Part 2 Video decoder supports the following input media types.</span></span>

-   <span data-ttu-id="8e9e5-110">MEDIASUBTYPE \_ M4S2</span><span class="sxs-lookup"><span data-stu-id="8e9e5-110">MEDIASUBTYPE\_M4S2</span></span>
-   <span data-ttu-id="8e9e5-111">MEDIASUBTYPE \_ m4s2</span><span class="sxs-lookup"><span data-stu-id="8e9e5-111">MEDIASUBTYPE\_m4s2</span></span>
-   <span data-ttu-id="8e9e5-112">MEDIASUBTYPE \_ MP4V</span><span class="sxs-lookup"><span data-stu-id="8e9e5-112">MEDIASUBTYPE\_MP4V</span></span>
-   <span data-ttu-id="8e9e5-113">MEDIASUBTYPE \_ MP4V</span><span class="sxs-lookup"><span data-stu-id="8e9e5-113">MEDIASUBTYPE\_mp4v</span></span>
-   <span data-ttu-id="8e9e5-114">MEDIASUBTYPE \_ MP4S (preterido)</span><span class="sxs-lookup"><span data-stu-id="8e9e5-114">MEDIASUBTYPE\_MP4S (deprecated)</span></span>
-   <span data-ttu-id="8e9e5-115">MEDIASUBTYPE \_ MP4s (preterido)</span><span class="sxs-lookup"><span data-stu-id="8e9e5-115">MEDIASUBTYPE\_mp4s (deprecated)</span></span>

## <a name="output-types"></a><span data-ttu-id="8e9e5-116">Tipos de saída</span><span class="sxs-lookup"><span data-stu-id="8e9e5-116">Output Types</span></span>

<span data-ttu-id="8e9e5-117">O decodificador de vídeo da parte 2 do MPEG4 dá suporte aos seguintes subtipos de mídia de saída quando ele está agindo como um DMO.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-117">The MPEG4 Part 2 Video decoder supports the following output media subtypes when it is acting as a DMO.</span></span>

-   <span data-ttu-id="8e9e5-118">MEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="8e9e5-118">MEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="8e9e5-119">MEDIASUBTYPE \_ NV12</span><span class="sxs-lookup"><span data-stu-id="8e9e5-119">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="8e9e5-120">MEDIASUBTYPE \_ YUY2</span><span class="sxs-lookup"><span data-stu-id="8e9e5-120">MEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="8e9e5-121">MEDIASUBTYPE \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="8e9e5-121">MEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="8e9e5-122">MEDIASUBTYPE \_ YVYU</span><span class="sxs-lookup"><span data-stu-id="8e9e5-122">MEDIASUBTYPE\_YVYU</span></span>
-   <span data-ttu-id="8e9e5-123">MEDIASUBTYPE \_ NV11</span><span class="sxs-lookup"><span data-stu-id="8e9e5-123">MEDIASUBTYPE\_NV11</span></span>
-   <span data-ttu-id="8e9e5-124">MEDIASUBTYPE \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="8e9e5-124">MEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="8e9e5-125">MEDIASUBTYPE \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="8e9e5-125">MEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="8e9e5-126">MEDIASUBTYPE \_ RGB565</span><span class="sxs-lookup"><span data-stu-id="8e9e5-126">MEDIASUBTYPE\_ RGB565</span></span>
-   <span data-ttu-id="8e9e5-127">MEDIASUBTYPE \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="8e9e5-127">MEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="8e9e5-128">MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="8e9e5-128">MEDIASUBTYPE\_RGB8</span></span>

<span data-ttu-id="8e9e5-129">O decodificador de vídeo da parte 2 do MPEG4 dá suporte aos seguintes subtipos de mídia de saída quando ele está atuando como um MFT.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-129">The MPEG4 Part 2 Video decoder supports the following output media subtypes when it is acting as an MFT.</span></span>

-   <span data-ttu-id="8e9e5-130">MEDIASUBTYPE \_ NV12</span><span class="sxs-lookup"><span data-stu-id="8e9e5-130">MEDIASUBTYPE\_NV12</span></span>
-   <span data-ttu-id="8e9e5-131">MEDIASUBTYPE \_ YV12</span><span class="sxs-lookup"><span data-stu-id="8e9e5-131">MEDIASUBTYPE\_YV12</span></span>

## <a name="formats"></a><span data-ttu-id="8e9e5-132">Formatos</span><span class="sxs-lookup"><span data-stu-id="8e9e5-132">Formats</span></span>

<span data-ttu-id="8e9e5-133">O decodificador de vídeo da parte 2 do MPEG4 aceita os seguintes formatos.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-133">The MPEG4 Part 2 Video decoder accepts the following formats.</span></span>

-   [<span data-ttu-id="8e9e5-134">**VIDEOINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="8e9e5-134">**VIDEOINFOHEADER**</span></span>](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)
-   <span data-ttu-id="8e9e5-135">[**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (VIH2)</span><span class="sxs-lookup"><span data-stu-id="8e9e5-135">[**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) (VIH2)</span></span>
-   [<span data-ttu-id="8e9e5-136">**MFVideoInfo**</span><span class="sxs-lookup"><span data-stu-id="8e9e5-136">**MFVideoInfo**</span></span>](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoinfo)
-   <span data-ttu-id="8e9e5-137">[**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) (somente a parte VIH2 do cabeçalho é usada.)</span><span class="sxs-lookup"><span data-stu-id="8e9e5-137">[**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) (Only the VIH2 portion of the header is used.)</span></span>

## <a name="interfaces-for-the-dmo"></a><span data-ttu-id="8e9e5-138">Interfaces para o DMO</span><span class="sxs-lookup"><span data-stu-id="8e9e5-138">Interfaces for the DMO</span></span>

<span data-ttu-id="8e9e5-139">Se você criar uma instância do decodificador de vídeo MPEG4 parte 2 como um DMO, o decodificador expõe as interfaces a seguir.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-139">If you create an instance of the MPEG4 Part 2 Video decoder as a DMO, the decoder exposes the following interfaces.</span></span>

-   [<span data-ttu-id="8e9e5-140">**IMediaObject**</span><span class="sxs-lookup"><span data-stu-id="8e9e5-140">**IMediaObject**</span></span>](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [<span data-ttu-id="8e9e5-141">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="8e9e5-141">**ICodecAPI**</span></span>](/windows/win32/api/strmif/nn-strmif-icodecapi)

<span data-ttu-id="8e9e5-142">Você pode obter uma interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) chamando **CoCreateInstance** e pode obter uma interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) chamando **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-142">You can obtain an [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) interface by calling **CoCreateInstance**, and you can obtain an [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface by calling **QueryInterface**.</span></span>

## <a name="interfaces-for-the-mft"></a><span data-ttu-id="8e9e5-143">Interfaces para o MFT</span><span class="sxs-lookup"><span data-stu-id="8e9e5-143">Interfaces for the MFT</span></span>

<span data-ttu-id="8e9e5-144">Se você criar uma instância do decodificador de vídeo MPEG2 parte 2 como um MFT, o decodificador exporá as interfaces a seguir.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-144">If you create an instance of the MPEG2 Part 2 Video decoder as an MFT, the decoder exposes the following interfaces.</span></span>

-   [<span data-ttu-id="8e9e5-145">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="8e9e5-145">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [<span data-ttu-id="8e9e5-146">**IMFAttributes**</span><span class="sxs-lookup"><span data-stu-id="8e9e5-146">**IMFAttributes**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [<span data-ttu-id="8e9e5-147">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="8e9e5-147">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="8e9e5-148">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="8e9e5-148">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="8e9e5-149">**IMFRateControl**</span><span class="sxs-lookup"><span data-stu-id="8e9e5-149">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [<span data-ttu-id="8e9e5-150">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="8e9e5-150">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)

<span data-ttu-id="8e9e5-151">Você pode obter um ponteiro para a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) chamando **CoCreateInstance**, e você pode obter um ponteiro para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) chamando [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes).</span><span class="sxs-lookup"><span data-stu-id="8e9e5-151">You can obtain a pointer to the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface by calling **CoCreateInstance**, and you can obtain a pointer to the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface by calling [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes).</span></span> <span data-ttu-id="8e9e5-152">Você pode obter um ponteiro para a interface [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise) ou [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2) chamando **QueryInterface** no MFT.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-152">You can obtain a pointer to the [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise) or [**IMFQualityAdvise2**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2) interface by calling **QueryInterface** on the MFT.</span></span> <span data-ttu-id="8e9e5-153">Você pode obter um ponteiro para a interface [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) ou [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) chamando [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) e passando o serviço de **controle de \_ taxa \_ \_ de MF** do identificador de serviço.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-153">You can obtain a pointer to the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) or [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) interface by calling [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) and passing the service identifier **MF\_RATE\_CONTROL\_SERVICE**.</span></span>

## <a name="profiles-and-levels"></a><span data-ttu-id="8e9e5-154">Perfis e níveis</span><span class="sxs-lookup"><span data-stu-id="8e9e5-154">Profiles and Levels</span></span>

<span data-ttu-id="8e9e5-155">A especificação MPEG4 define vários perfis, cada um deles especifica as ferramentas que um codificador pode usar para gerar um fluxo codificado.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-155">The MPEG4 specification defines several profiles, each of which specifies the tools that an encoder can use to generate an encoded stream.</span></span> <span data-ttu-id="8e9e5-156">O decodificador de vídeo MPEG4 parte 2 dá suporte a dois desses perfis: perfil visual simples e perfil simples avançado.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-156">The MPEG4 Part2 Video Decoder supports two of those profiles: Simple Visual Profile and Advanced Simple Profile.</span></span> <span data-ttu-id="8e9e5-157">Em outras palavras, o decodificador de vídeo da parte 2 do MPEG4 pode decodificar fluxos que foram codificados de acordo com o perfil visual simples ou com o perfil simples avançado.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-157">In other words, the MPEG4 Part 2 Video decoder can decode streams that were encoded according to either the Simple Visual Profile or the Advanced Simple Profile.</span></span>

<span data-ttu-id="8e9e5-158">O perfil visual simples dá suporte à transmissão básica de vídeo de taxa de bits baixa no modo progressivo.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-158">The Simple Visual Profile supports basic transmission of low bit-rate video in progressive mode.</span></span> <span data-ttu-id="8e9e5-159">Ele dá suporte apenas a imagens de intra e de previsão.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-159">It supports only Intra and Prediction pictures.</span></span> <span data-ttu-id="8e9e5-160">Ele também dá suporte ao modo de cabeçalho curto, que é compatível com versões anteriores com o perfil de linha de base H. 263.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-160">It also supports the short header mode, which is backward compatible with the H.263 baseline profile.</span></span> <span data-ttu-id="8e9e5-161">A partir do Windows 10, o decodificador de vídeo da parte 2 MPEG-4 também dá suporte a H. 263v2 (H. 263 +) que oferece suporte a tamanhos de imagem personalizados.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-161">Starting with Windows 10, the MPEG-4 Part 2 Video Decoder also supports H.263v2 (H.263+) which supports custom picture sizes.</span></span>

<span data-ttu-id="8e9e5-162">O perfil simples avançado dá suporte a todas as ferramentas do perfil visual simples e, além disso, dá suporte a vídeo entrelaçado, quadros B, compensação de movimento trimestre-PEL, tabelas de quantificação adicionais e compensação de movimento global.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-162">The Advanced Simple Profile supports all the tools of the Simple Visual Profile and, in addition, supports interlaced video, B-frames, quarter-pel motion compensation, additional quantization tables, and global motion compensation.</span></span>

<span data-ttu-id="8e9e5-163">A especificação MPEG4 também define vários níveis, cada um deles especifica restrições no fluxo de saída gerado por um codificador.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-163">The MPEG4 specification also defines several levels, each of which specifies constraints on the output stream generated by an encoder.</span></span>

<span data-ttu-id="8e9e5-164">A tabela a seguir mostra os perfis e os níveis, juntamente com as resoluções típicas, suportadas pelo decodificador de vídeo da parte 2 do MPEG4.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-164">The following table shows the profiles and levels, along with typical resolutions, supported by the MPEG4 Part 2 Video decoder.</span></span>



| <span data-ttu-id="8e9e5-165">Perfil</span><span class="sxs-lookup"><span data-stu-id="8e9e5-165">Profile</span></span>         | <span data-ttu-id="8e9e5-166">Nível</span><span class="sxs-lookup"><span data-stu-id="8e9e5-166">Level</span></span> | <span data-ttu-id="8e9e5-167">Resolução típica</span><span class="sxs-lookup"><span data-stu-id="8e9e5-167">Typical Resolution</span></span> |
|-----------------|-------|--------------------|
| <span data-ttu-id="8e9e5-168">Visual simples</span><span class="sxs-lookup"><span data-stu-id="8e9e5-168">Simple Visual</span></span>   | <span data-ttu-id="8e9e5-169">0</span><span class="sxs-lookup"><span data-stu-id="8e9e5-169">0</span></span>     | <span data-ttu-id="8e9e5-170">176 x 144</span><span class="sxs-lookup"><span data-stu-id="8e9e5-170">176 x 144</span></span>          |
| <span data-ttu-id="8e9e5-171">Visual simples</span><span class="sxs-lookup"><span data-stu-id="8e9e5-171">Simple Visual</span></span>   | <span data-ttu-id="8e9e5-172">1</span><span class="sxs-lookup"><span data-stu-id="8e9e5-172">1</span></span>     | <span data-ttu-id="8e9e5-173">176 x 144</span><span class="sxs-lookup"><span data-stu-id="8e9e5-173">176 x 144</span></span>          |
| <span data-ttu-id="8e9e5-174">Visual simples</span><span class="sxs-lookup"><span data-stu-id="8e9e5-174">Simple Visual</span></span>   | <span data-ttu-id="8e9e5-175">2</span><span class="sxs-lookup"><span data-stu-id="8e9e5-175">2</span></span>     | <span data-ttu-id="8e9e5-176">352 x 288</span><span class="sxs-lookup"><span data-stu-id="8e9e5-176">352 x 288</span></span>          |
| <span data-ttu-id="8e9e5-177">Visual simples</span><span class="sxs-lookup"><span data-stu-id="8e9e5-177">Simple Visual</span></span>   | <span data-ttu-id="8e9e5-178">3</span><span class="sxs-lookup"><span data-stu-id="8e9e5-178">3</span></span>     | <span data-ttu-id="8e9e5-179">352 x 288</span><span class="sxs-lookup"><span data-stu-id="8e9e5-179">352 x 288</span></span>          |
| <span data-ttu-id="8e9e5-180">SimpleVisual</span><span class="sxs-lookup"><span data-stu-id="8e9e5-180">SimpleVisual</span></span>    | <span data-ttu-id="8e9e5-181">4a</span><span class="sxs-lookup"><span data-stu-id="8e9e5-181">4a</span></span>    | <span data-ttu-id="8e9e5-182">640 x 480</span><span class="sxs-lookup"><span data-stu-id="8e9e5-182">640 x 480</span></span>          |
| <span data-ttu-id="8e9e5-183">Visual simples</span><span class="sxs-lookup"><span data-stu-id="8e9e5-183">Simple Visual</span></span>   | <span data-ttu-id="8e9e5-184">5</span><span class="sxs-lookup"><span data-stu-id="8e9e5-184">5</span></span>     | <span data-ttu-id="8e9e5-185">720 x 576</span><span class="sxs-lookup"><span data-stu-id="8e9e5-185">720 x 576</span></span>          |
| <span data-ttu-id="8e9e5-186">Avançado simples</span><span class="sxs-lookup"><span data-stu-id="8e9e5-186">Advanced Simple</span></span> | <span data-ttu-id="8e9e5-187">0</span><span class="sxs-lookup"><span data-stu-id="8e9e5-187">0</span></span>     | <span data-ttu-id="8e9e5-188">176 x 144</span><span class="sxs-lookup"><span data-stu-id="8e9e5-188">176 x 144</span></span>          |
| <span data-ttu-id="8e9e5-189">Avançado simples</span><span class="sxs-lookup"><span data-stu-id="8e9e5-189">Advanced Simple</span></span> | <span data-ttu-id="8e9e5-190">1</span><span class="sxs-lookup"><span data-stu-id="8e9e5-190">1</span></span>     | <span data-ttu-id="8e9e5-191">176 x 144</span><span class="sxs-lookup"><span data-stu-id="8e9e5-191">176 x 144</span></span>          |
| <span data-ttu-id="8e9e5-192">Avançado simples</span><span class="sxs-lookup"><span data-stu-id="8e9e5-192">Advanced Simple</span></span> | <span data-ttu-id="8e9e5-193">2</span><span class="sxs-lookup"><span data-stu-id="8e9e5-193">2</span></span>     | <span data-ttu-id="8e9e5-194">352 x 288</span><span class="sxs-lookup"><span data-stu-id="8e9e5-194">352 x 288</span></span>          |
| <span data-ttu-id="8e9e5-195">Avançado simples</span><span class="sxs-lookup"><span data-stu-id="8e9e5-195">Advanced Simple</span></span> | <span data-ttu-id="8e9e5-196">3</span><span class="sxs-lookup"><span data-stu-id="8e9e5-196">3</span></span>     | <span data-ttu-id="8e9e5-197">352 x 288</span><span class="sxs-lookup"><span data-stu-id="8e9e5-197">352 x 288</span></span>          |
| <span data-ttu-id="8e9e5-198">Avançado simples</span><span class="sxs-lookup"><span data-stu-id="8e9e5-198">Advanced Simple</span></span> | <span data-ttu-id="8e9e5-199">3b</span><span class="sxs-lookup"><span data-stu-id="8e9e5-199">3b</span></span>    | <span data-ttu-id="8e9e5-200">352 x 288</span><span class="sxs-lookup"><span data-stu-id="8e9e5-200">352 x 288</span></span>          |
| <span data-ttu-id="8e9e5-201">Avançado simples</span><span class="sxs-lookup"><span data-stu-id="8e9e5-201">Advanced Simple</span></span> | <span data-ttu-id="8e9e5-202">4</span><span class="sxs-lookup"><span data-stu-id="8e9e5-202">4</span></span>     | <span data-ttu-id="8e9e5-203">352 x 756</span><span class="sxs-lookup"><span data-stu-id="8e9e5-203">352 x 756</span></span>          |
| <span data-ttu-id="8e9e5-204">Avançado simples</span><span class="sxs-lookup"><span data-stu-id="8e9e5-204">Advanced Simple</span></span> | <span data-ttu-id="8e9e5-205">5</span><span class="sxs-lookup"><span data-stu-id="8e9e5-205">5</span></span>     | <span data-ttu-id="8e9e5-206">720 x 576</span><span class="sxs-lookup"><span data-stu-id="8e9e5-206">720 x 576</span></span>          |



 

<span data-ttu-id="8e9e5-207">Para obter mais informações sobre perfis e níveis, consulte a especificação do MPEG4 parte 2 (ISO/IEC 14496-2): tecnologia da informação – codificação de objetos de áudio-visual--parte 2: Visual.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-207">For more information about profiles and levels, see the MPEG4 Part 2 specification (ISO/IEC 14496-2): Information technology -- Coding of audio-visual objects -- Part 2: Visual.</span></span>

## <a name="decoder-properties"></a><span data-ttu-id="8e9e5-208">Propriedades do decodificador</span><span class="sxs-lookup"><span data-stu-id="8e9e5-208">Decoder Properties</span></span>

<span data-ttu-id="8e9e5-209">Para definir propriedades no decodificador de vídeo do MPEG4 parte 2, use a interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) ou a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="8e9e5-209">To set properties on the MPEG4 Part 2 Video decoder, use the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface or the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="8e9e5-210">O decodificador de vídeo da parte 2 do MPEG4 dá suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-210">The MPEG4 Part 2 Video decoder supports the following properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8e9e5-211">Propriedade</span><span class="sxs-lookup"><span data-stu-id="8e9e5-211">Property</span></span></th>
<th><span data-ttu-id="8e9e5-212">Descrição</span><span class="sxs-lookup"><span data-stu-id="8e9e5-212">Description</span></span></th>
<th><span data-ttu-id="8e9e5-213">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="8e9e5-213">Default Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8e9e5-214"><a href="/windows/desktop/DirectShow/avdecvideoswpowerlevel-property"><strong>CODECAPI_AVDecVideoSWPowerLevel</strong></a></span><span class="sxs-lookup"><span data-stu-id="8e9e5-214"><a href="/windows/desktop/DirectShow/avdecvideoswpowerlevel-property"><strong>CODECAPI_AVDecVideoSWPowerLevel</strong></a></span></span></td>
<td><span data-ttu-id="8e9e5-215">Especifica o nível de energia.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-215">Specifies the power level.</span></span><br/> <dl> <span data-ttu-id="8e9e5-216">Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-216">Windows 7.</span></span><br />
<span data-ttu-id="8e9e5-217">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-217">Write-only.</span></span><br />
</dl></td>
<td><span data-ttu-id="8e9e5-218">100</span><span class="sxs-lookup"><span data-stu-id="8e9e5-218">100</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8e9e5-219"><a href="/windows/desktop/DirectShow/avdecvideothumbnailgenerationmode-property"><strong>CODECAPI_AVDecVideoThumbnailGenerationMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="8e9e5-219"><a href="/windows/desktop/DirectShow/avdecvideothumbnailgenerationmode-property"><strong>CODECAPI_AVDecVideoThumbnailGenerationMode</strong></a></span></span></td>
<td><span data-ttu-id="8e9e5-220">Especifica o modo de geração de miniatura.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-220">Specifies the thumbnail generation mode.</span></span><br/> <dl> <span data-ttu-id="8e9e5-221">Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-221">Windows 7.</span></span><br />
<span data-ttu-id="8e9e5-222">Somente gravação.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-222">Write-only.</span></span><br />
</dl></td>
<td><span data-ttu-id="8e9e5-223"><strong>VARIANT_FALSE</strong></span><span class="sxs-lookup"><span data-stu-id="8e9e5-223"><strong>VARIANT_FALSE</strong></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="8e9e5-224">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e9e5-224">Remarks</span></span>

<span data-ttu-id="8e9e5-225">Os identificadores globalmente exclusivos (GUIDs) para subtipos de mídia RGB diferem dependendo se um decodificador está agindo como um DMO ou um MFT.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-225">The globally unique identifiers (GUIDs) for RGB media subtypes differ depending on whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="8e9e5-226">Os GUIDs para subtipos de mídia não RGB são os mesmos, independentemente de um decodificador estar agindo como um DMO ou um MFT.</span><span class="sxs-lookup"><span data-stu-id="8e9e5-226">The GUIDs for non-RGB media subtypes are the same, regardless of whether a decoder is acting as a DMO or an MFT.</span></span> <span data-ttu-id="8e9e5-227">Para obter informações sobre os GUIDs que representam subtipos de mídia, consulte [tipos de mídia](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="8e9e5-227">For information about the GUIDs that represent media subtypes, see [Media Types](media-types.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8e9e5-228">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e9e5-228">Requirements</span></span>



| <span data-ttu-id="8e9e5-229">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e9e5-229">Requirement</span></span> | <span data-ttu-id="8e9e5-230">Valor</span><span class="sxs-lookup"><span data-stu-id="8e9e5-230">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e9e5-231">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e9e5-231">Minimum supported client</span></span><br/> | <span data-ttu-id="8e9e5-232">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="8e9e5-232">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="8e9e5-233">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8e9e5-233">Minimum supported server</span></span><br/> | <span data-ttu-id="8e9e5-234">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="8e9e5-234">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8e9e5-235">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8e9e5-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e9e5-236"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e9e5-236"><dt>Wmcodecdsp.h</dt></span></span> </dl> |
| <span data-ttu-id="8e9e5-237">DLL</span><span class="sxs-lookup"><span data-stu-id="8e9e5-237">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8e9e5-238"><dt>MP4SDecd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e9e5-238"><dt>MP4SDecd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e9e5-239">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e9e5-239">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e9e5-240">Objetos de codec</span><span class="sxs-lookup"><span data-stu-id="8e9e5-240">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
