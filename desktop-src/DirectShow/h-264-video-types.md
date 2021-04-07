---
description: Tipos de vídeo H. 264
ms.assetid: aa3166b2-6b04-44fa-bc9d-c8ff46f99201
title: Tipos de vídeo H. 264
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dcd33703798e305947cdcd663c7a86c7c494683
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103919685"
---
# <a name="h264-video-types"></a><span data-ttu-id="feda0-103">Tipos de vídeo H. 264</span><span class="sxs-lookup"><span data-stu-id="feda0-103">H.264 Video Types</span></span>

<span data-ttu-id="feda0-104">Os subtipos de mídia a seguir são definidos para o vídeo H. 264.</span><span class="sxs-lookup"><span data-stu-id="feda0-104">The following media subtypes are defined for H.264 video.</span></span>



| <span data-ttu-id="feda0-105">Subtype</span><span class="sxs-lookup"><span data-stu-id="feda0-105">Subtype</span></span>                | <span data-ttu-id="feda0-106">FOURCC</span><span class="sxs-lookup"><span data-stu-id="feda0-106">FOURCC</span></span> | <span data-ttu-id="feda0-107">Description</span><span class="sxs-lookup"><span data-stu-id="feda0-107">Description</span></span>                                                    |
|------------------------|--------|----------------------------------------------------------------|
| <span data-ttu-id="feda0-108">**MEDIASUBTYPE \_ AVC1**</span><span class="sxs-lookup"><span data-stu-id="feda0-108">**MEDIASUBTYPE\_AVC1**</span></span> | <span data-ttu-id="feda0-109">'AVC1'</span><span class="sxs-lookup"><span data-stu-id="feda0-109">'AVC1'</span></span> | <span data-ttu-id="feda0-110">H. 264 fragmentado sem códigos de início.</span><span class="sxs-lookup"><span data-stu-id="feda0-110">H.264 bitstream without start codes.</span></span>                           |
| <span data-ttu-id="feda0-111">**MEDIASUBTYPE \_ H264**</span><span class="sxs-lookup"><span data-stu-id="feda0-111">**MEDIASUBTYPE\_H264**</span></span> | <span data-ttu-id="feda0-112">Taxas</span><span class="sxs-lookup"><span data-stu-id="feda0-112">'H264'</span></span> | <span data-ttu-id="feda0-113">H. 264 fragmentado com códigos de início.</span><span class="sxs-lookup"><span data-stu-id="feda0-113">H.264 bitstream with start codes.</span></span>                              |
| <span data-ttu-id="feda0-114">**MEDIASUBTYPE \_ H264**</span><span class="sxs-lookup"><span data-stu-id="feda0-114">**MEDIASUBTYPE\_h264**</span></span> | <span data-ttu-id="feda0-115">Taxas</span><span class="sxs-lookup"><span data-stu-id="feda0-115">'h264'</span></span> | <span data-ttu-id="feda0-116">Equivalente a **MEDIASUBTYPE \_ H264**, com um FOURCC diferente.</span><span class="sxs-lookup"><span data-stu-id="feda0-116">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |
| <span data-ttu-id="feda0-117">**MEDIASUBTYPE \_ x264**</span><span class="sxs-lookup"><span data-stu-id="feda0-117">**MEDIASUBTYPE\_X264**</span></span> | <span data-ttu-id="feda0-118">'X264'</span><span class="sxs-lookup"><span data-stu-id="feda0-118">'X264'</span></span> | <span data-ttu-id="feda0-119">Equivalente a **MEDIASUBTYPE \_ H264**, com um FOURCC diferente.</span><span class="sxs-lookup"><span data-stu-id="feda0-119">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |
| <span data-ttu-id="feda0-120">**MEDIASUBTYPE \_ x264**</span><span class="sxs-lookup"><span data-stu-id="feda0-120">**MEDIASUBTYPE\_x264**</span></span> | <span data-ttu-id="feda0-121">'x264'</span><span class="sxs-lookup"><span data-stu-id="feda0-121">'x264'</span></span> | <span data-ttu-id="feda0-122">Equivalente a **MEDIASUBTYPE \_ H264**, com um FOURCC diferente.</span><span class="sxs-lookup"><span data-stu-id="feda0-122">Equivalent to **MEDIASUBTYPE\_H264**, with a different FOURCC.</span></span> |



 

<span data-ttu-id="feda0-123">Esses GUIDs de subtipo são declarados em wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="feda0-123">These subtype GUIDs are declared in wmcodecdsp.h.</span></span>

<span data-ttu-id="feda0-124">A principal diferença entre esses tipos de mídia é a presença de códigos de início no fragmentado.</span><span class="sxs-lookup"><span data-stu-id="feda0-124">The main difference between these media types is the presence of start codes in the bitstream.</span></span> <span data-ttu-id="feda0-125">Se o subtipo for **MEDIASUBTYPE \_ AVC1**, o fragmentado não conterá códigos de início.</span><span class="sxs-lookup"><span data-stu-id="feda0-125">If the subtype is **MEDIASUBTYPE\_AVC1**, the bitstream does not contain start codes.</span></span>

### <a name="h264-bitstream-with-start-codes"></a><span data-ttu-id="feda0-126">H. 264 fragmentado com códigos de início</span><span class="sxs-lookup"><span data-stu-id="feda0-126">H.264 Bitstream with Start Codes</span></span>

<span data-ttu-id="feda0-127">H. 264 fragmentado que são transmitidas pelo ar ou que estão contidas no programa MPEG-2 ou fluxos de transporte, ou gravados em HD-DVD, são formatados conforme descrito em anexo B do ITU-T Rec. H. 264.</span><span class="sxs-lookup"><span data-stu-id="feda0-127">H.264 bitstreams that are transmitted over the air, or contained in MPEG-2 program or transport streams, or recorded on HD-DVD, are formatted as described in Annex B of ITU-T Rec. H.264.</span></span> <span data-ttu-id="feda0-128">De acordo com essa especificação, o fragmentado consiste em uma sequência de NALUs (unidades de camada de abstração de rede), cada uma das quais é prefixada com um código de início igual a 0x000001 ou 0x00000001.</span><span class="sxs-lookup"><span data-stu-id="feda0-128">According to this specification, the bitstream consists of a sequence of network abstraction layer units (NALUs), each of which is prefixed with a start code equal to 0x000001 or 0x00000001.</span></span>

<span data-ttu-id="feda0-129">Quando os códigos de início estão presentes no fragmentado, o seguinte tipo de mídia é usado:</span><span class="sxs-lookup"><span data-stu-id="feda0-129">When start codes are present in the bitstream, the following media type is used:</span></span>



|             |                                                                                                   |
|-------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="feda0-130">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="feda0-130">Major type</span></span>  | <span data-ttu-id="feda0-131">**Vídeo de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="feda0-131">**MEDIATYPE\_Video**</span></span>                                                                              |
| <span data-ttu-id="feda0-132">Subtipos</span><span class="sxs-lookup"><span data-stu-id="feda0-132">Subtypes</span></span>    | <span data-ttu-id="feda0-133">**MEDIASUBTYPE \_ H264**, **MEDIASUBTYPE \_ H264**, **MEDIASUBTYPE \_ x264** ou **MEDIASUBTYPE \_ x264**</span><span class="sxs-lookup"><span data-stu-id="feda0-133">**MEDIASUBTYPE\_H264**, **MEDIASUBTYPE\_h264**, **MEDIASUBTYPE\_X264**, or **MEDIASUBTYPE\_x264**</span></span> |
| <span data-ttu-id="feda0-134">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="feda0-134">Format type</span></span> | <span data-ttu-id="feda0-135">**Formato \_ VideoInfo**, **Format \_ VideoInfo2**, **Format \_ MPEG2Video** ou **GUID \_ NULL**</span><span class="sxs-lookup"><span data-stu-id="feda0-135">**FORMAT\_VideoInfo**, **FORMAT\_VideoInfo2**, **FORMAT\_MPEG2Video**, or **GUID\_NULL**</span></span>          |



 

<span data-ttu-id="feda0-136">Se o tipo de formato for **GUID \_ NULL**, nenhuma estrutura de formato estará presente.</span><span class="sxs-lookup"><span data-stu-id="feda0-136">If the format type is **GUID\_NULL**, no format structure is present.</span></span>

<span data-ttu-id="feda0-137">Quando o fragmentado contém códigos de início, qualquer um dos tipos de formato listados aqui é suficiente, porque o decodificador não requer informações adicionais para analisar o fluxo.</span><span class="sxs-lookup"><span data-stu-id="feda0-137">When the bitstream contains start codes, any of the format types listed here is sufficient, because the decoder does not require any additional information to parse the stream.</span></span> <span data-ttu-id="feda0-138">O fragmentado já contém todas as informações necessárias para o decodificador e os códigos de início permitem que o decodificador localize o início de cada NALU.</span><span class="sxs-lookup"><span data-stu-id="feda0-138">The bitstream already contains all of the information needed by the decoder, and the start codes enable the decoder to locate the start of each NALU.</span></span>

<span data-ttu-id="feda0-139">Os seguintes subtipos são equivalentes:</span><span class="sxs-lookup"><span data-stu-id="feda0-139">The following subtypes are equivalent:</span></span>

### <a name="h264-bitstream-without-start-codes"></a><span data-ttu-id="feda0-140">H. 264 fragmentado sem códigos de início</span><span class="sxs-lookup"><span data-stu-id="feda0-140">H.264 Bitstream Without Start Codes</span></span>

<span data-ttu-id="feda0-141">O formato de contêiner MP4 armazena dados H. 264 sem códigos de início.</span><span class="sxs-lookup"><span data-stu-id="feda0-141">The MP4 container format stores H.264 data without start codes.</span></span> <span data-ttu-id="feda0-142">Em vez disso, cada NALU é prefixado por um campo de comprimento, que fornece o comprimento do NALU em bytes.</span><span class="sxs-lookup"><span data-stu-id="feda0-142">Instead, each NALU is prefixed by a length field, which gives the length of the NALU in bytes.</span></span> <span data-ttu-id="feda0-143">O tamanho do campo de comprimento pode variar, mas geralmente é 1, 2 ou 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="feda0-143">The size of the length field can vary, but is typically 1, 2, or 4 bytes.</span></span>

<span data-ttu-id="feda0-144">Quando os códigos de início não estão presentes no fragmentado, o tipo de mídia a seguir é usado.</span><span class="sxs-lookup"><span data-stu-id="feda0-144">When start codes are not present in the bitstream, the following media type is used.</span></span>



|             |                        |
|-------------|------------------------|
| <span data-ttu-id="feda0-145">Tipo principal</span><span class="sxs-lookup"><span data-stu-id="feda0-145">Major type</span></span>  | <span data-ttu-id="feda0-146">**Vídeo de MEDIATYPE \_**</span><span class="sxs-lookup"><span data-stu-id="feda0-146">**MEDIATYPE\_Video**</span></span>   |
| <span data-ttu-id="feda0-147">Subtype</span><span class="sxs-lookup"><span data-stu-id="feda0-147">Subtype</span></span>     | <span data-ttu-id="feda0-148">**MEDIASUBTYPE \_ AVC1**</span><span class="sxs-lookup"><span data-stu-id="feda0-148">**MEDIASUBTYPE\_AVC1**</span></span> |
| <span data-ttu-id="feda0-149">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="feda0-149">Format type</span></span> | <span data-ttu-id="feda0-150">**MPEG2Video de formato \_**</span><span class="sxs-lookup"><span data-stu-id="feda0-150">**FORMAT\_MPEG2Video**</span></span> |



 

<span data-ttu-id="feda0-151">O bloco de formato é uma estrutura [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) .</span><span class="sxs-lookup"><span data-stu-id="feda0-151">The format block is an [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure.</span></span> <span data-ttu-id="feda0-152">Essa estrutura deve ser preenchida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="feda0-152">This structure should be filled in as follows:</span></span>

-   <span data-ttu-id="feda0-153">**HDR**: uma estrutura [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) que descreve o fragmentado.</span><span class="sxs-lookup"><span data-stu-id="feda0-153">**hdr**: A [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure that describes the bitstream.</span></span> <span data-ttu-id="feda0-154">Nenhuma tabela de cores está presente após a parte [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) da estrutura e **biClrUsed** deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="feda0-154">No color table is present after the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) portion of the structure, and **biClrUsed** must be zero.</span></span>
-   <span data-ttu-id="feda0-155">**dwStartTimeCode**: não usado.</span><span class="sxs-lookup"><span data-stu-id="feda0-155">**dwStartTimeCode**: Not used.</span></span> <span data-ttu-id="feda0-156">Definido como zero.</span><span class="sxs-lookup"><span data-stu-id="feda0-156">Set to zero.</span></span>
-   <span data-ttu-id="feda0-157">**cbSequenceHeader**: o comprimento da matriz **dwSequenceHeader** em bytes.</span><span class="sxs-lookup"><span data-stu-id="feda0-157">**cbSequenceHeader**: The length of the **dwSequenceHeader** array in bytes.</span></span>
-   <span data-ttu-id="feda0-158">**dwProfile**: especifica o perfil H. 264.</span><span class="sxs-lookup"><span data-stu-id="feda0-158">**dwProfile**: Specifies the H.264 profile.</span></span>
-   <span data-ttu-id="feda0-159">**dwLevel**: especifica o nível H. 264.</span><span class="sxs-lookup"><span data-stu-id="feda0-159">**dwLevel**: Specifies the H.264 level.</span></span>
-   <span data-ttu-id="feda0-160">**dwFlags**: o número de bytes usados para o campo de comprimento que aparece antes de cada **NALU**.</span><span class="sxs-lookup"><span data-stu-id="feda0-160">**dwFlags**: The number of bytes used for the length field that appears before each **NALU**.</span></span> <span data-ttu-id="feda0-161">O campo comprimento indica o tamanho dos seguintes NALU em bytes.</span><span class="sxs-lookup"><span data-stu-id="feda0-161">The length field indicates the size of the following NALU in bytes.</span></span> <span data-ttu-id="feda0-162">Por exemplo, se **dwFlags** for 4, cada NALU será precedido por um campo de comprimento de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="feda0-162">For example, if **dwFlags** is 4, each NALU is preceded by a 4-byte length field.</span></span> <span data-ttu-id="feda0-163">Os valores válidos são 1, 2 e 4.</span><span class="sxs-lookup"><span data-stu-id="feda0-163">The valid values are 1, 2, and 4.</span></span>
-   <span data-ttu-id="feda0-164">**dwSequenceHeader**: uma matriz de bytes que pode conter o conjunto de parâmetros de sequência (SPS) e o conjunto de parâmetros de imagem (PPS) NALUs.</span><span class="sxs-lookup"><span data-stu-id="feda0-164">**dwSequenceHeader**: A byte array that may contain sequence parameter set (SPS) and picture parameter set (PPS) NALUs.</span></span>

<span data-ttu-id="feda0-165">O contêiner MP4 pode conter conjuntos de parâmetros de sequência (SPS) ou conjuntos de parâmetros de imagem (PPS) como unidades NAL especiais em cabeçalhos de arquivo ou em um fluxo separado (distinto do fluxo de vídeo).</span><span class="sxs-lookup"><span data-stu-id="feda0-165">The MP4 container might contain sequence parameter sets (SPS) or picture parameter sets (PPS) as special NAL units in file headers or in a separate stream (distinct from the video stream).</span></span> <span data-ttu-id="feda0-166">Quando o formato é estabelecido, o tipo de mídia pode especificar as unidades do SPS e do PPS NAL na matriz **dwSequenceHeader** .</span><span class="sxs-lookup"><span data-stu-id="feda0-166">When the format is established, the media type can specify SPS and PPS NAL units in the **dwSequenceHeader** array.</span></span> <span data-ttu-id="feda0-167">Se **cbSequenceHeader** for maior que zero, **dwSequenceHeader** será o início de uma matriz de bytes que contém o SPS e o PPS NALUs, delimitados por campos de comprimento de 2 bytes, todos em ordem de bytes de rede (big-endian).</span><span class="sxs-lookup"><span data-stu-id="feda0-167">If **cbSequenceHeader** is greater than zero, **dwSequenceHeader** is the start of a byte array containing SPS and PPS NALUs, delimited by 2-byte length fields, all in network byte order (big-endian).</span></span> <span data-ttu-id="feda0-168">É possível ter tanto o SPS quanto o PPS, apenas um desses tipos ou nenhum.</span><span class="sxs-lookup"><span data-stu-id="feda0-168">It is possible to have both SPS and PPS, only one of these types, or none.</span></span> <span data-ttu-id="feda0-169">O tipo real de cada NALU pode ser determinado examinando o campo de **\_ \_ tipo de unidade nal** do NALU em si.</span><span class="sxs-lookup"><span data-stu-id="feda0-169">The actual type of each NALU can be determined by examining the **nal\_unit\_type** field of the NALU itself.</span></span>

<span data-ttu-id="feda0-170">Quando esse tipo de mídia é usado, cada exemplo de mídia começa no início de um NALU e as unidades NAL não abrangem amostras.</span><span class="sxs-lookup"><span data-stu-id="feda0-170">When this media type is used, each media sample starts at the beginning of a NALU, and NAL units do not span samples.</span></span> <span data-ttu-id="feda0-171">Isso permite que o decodificador se recupere de dados corrompidos ou amostras descartadas.</span><span class="sxs-lookup"><span data-stu-id="feda0-171">This enables the decoder to recover from data corruption or dropped samples.</span></span>

 

 



