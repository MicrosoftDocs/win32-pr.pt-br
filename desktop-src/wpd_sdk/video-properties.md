---
description: Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de vídeo.
ms.assetid: e6df5b2d-ceb8-4de0-b60b-9102c77143fe
title: Propriedades do vídeo (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Video
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 1f44f32ab19c5ad10cc9c8dd5bdb8816ccc944f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785161"
---
# <a name="video-properties"></a><span data-ttu-id="3b9d0-103">Propriedades do vídeo</span><span class="sxs-lookup"><span data-stu-id="3b9d0-103">Video Properties</span></span>

<span data-ttu-id="3b9d0-104">Os dispositivos portáteis do Windows oferecem suporte às seguintes propriedades de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3b9d0-104">Windows Portable Devices supports the following video properties.</span></span>



| <span data-ttu-id="3b9d0-105">Propriedade</span><span class="sxs-lookup"><span data-stu-id="3b9d0-105">Property</span></span>                                         | <span data-ttu-id="3b9d0-106">VarType</span><span class="sxs-lookup"><span data-stu-id="3b9d0-106">VarType</span></span>        | <span data-ttu-id="3b9d0-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="3b9d0-107">Description</span></span>                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b9d0-108">**\_autor de vídeo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="3b9d0-108">**WPD\_VIDEO\_AUTHOR**</span></span>                           | <span data-ttu-id="3b9d0-109">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="3b9d0-109">**VT\_LPWSTR**</span></span> | <span data-ttu-id="3b9d0-110">O autor do arquivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3b9d0-110">The author of the video file.</span></span>                                                                                                                                                                                                                           |
| <span data-ttu-id="3b9d0-111">**taxa de bits de \_ vídeo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="3b9d0-111">**WPD\_VIDEO\_BITRATE**</span></span>                          | <span data-ttu-id="3b9d0-112">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="3b9d0-112">**VT\_UI4**</span></span>    | <span data-ttu-id="3b9d0-113">A taxa de bits do arquivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3b9d0-113">The bit rate of the video file.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="3b9d0-114">**\_tamanho do \_ buffer de vídeo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="3b9d0-114">**WPD\_VIDEO\_BUFFER\_SIZE**</span></span>                     | <span data-ttu-id="3b9d0-115">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="3b9d0-115">**VT\_UI4**</span></span>    | <span data-ttu-id="3b9d0-116">Um valor que especifica o tamanho de buffer de vídeo necessário para processar esse arquivo.</span><span class="sxs-lookup"><span data-stu-id="3b9d0-116">A value that specifies the required video buffer size to render this file.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="3b9d0-117">**\_créditos de vídeo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="3b9d0-117">**WPD\_VIDEO\_CREDITS**</span></span>                          | <span data-ttu-id="3b9d0-118">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="3b9d0-118">**VT\_LPWSTR**</span></span> | <span data-ttu-id="3b9d0-119">Os créditos que listam a projeção e a equipe do vídeo.</span><span class="sxs-lookup"><span data-stu-id="3b9d0-119">The credits listing the cast and crew for the video.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="3b9d0-120">**\_ \_ código FOURCC de vídeo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="3b9d0-120">**WPD\_VIDEO\_FOURCC\_CODE**</span></span>                     | <span data-ttu-id="3b9d0-121">**VT \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="3b9d0-121">**VT\_DWORD**</span></span>  | <span data-ttu-id="3b9d0-122">O código FourCC registrado que indica o codec que foi usado para o arquivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3b9d0-122">The registered FourCC code that indicates the codec that was used for the video file.</span></span> <span data-ttu-id="3b9d0-123">Para obter uma lista de formatos FourCC, consulte o artigo [registrou códigos FOURCC e formatos de onda](https://msdn2.microsoft.com/library/ms867195.aspx) no site do MSDN.</span><span class="sxs-lookup"><span data-stu-id="3b9d0-123">For a listing of FourCC formats, see the article [Registered FOURCC Codes and WAVE Formats](https://msdn2.microsoft.com/library/ms867195.aspx) on the MSDN Web site.</span></span> |
| <span data-ttu-id="3b9d0-124">**taxa de quadros de \_ vídeo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="3b9d0-124">**WPD\_VIDEO\_FRAMERATE**</span></span>                        | <span data-ttu-id="3b9d0-125">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="3b9d0-125">**VT\_UI4**</span></span>    | <span data-ttu-id="3b9d0-126">A taxa de quadros do arquivo de vídeo, em quadros/segundo x 1.000.</span><span class="sxs-lookup"><span data-stu-id="3b9d0-126">The frame rate of the video file, in frames/second x 1,000.</span></span> <span data-ttu-id="3b9d0-127">Por exemplo, uma taxa de quadros de 29,97 é representada como 29970.</span><span class="sxs-lookup"><span data-stu-id="3b9d0-127">For example, a frame rate of 29.97 is represented as 29970.</span></span>                                                                                                                                 |
| <span data-ttu-id="3b9d0-128">**\_gênero de vídeo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="3b9d0-128">**WPD\_VIDEO\_GENRE**</span></span>                            | <span data-ttu-id="3b9d0-129">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="3b9d0-129">**VT\_LPWSTR**</span></span> | <span data-ttu-id="3b9d0-130">O gênero deste arquivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3b9d0-130">The genre of this video file.</span></span> <span data-ttu-id="3b9d0-131">Não há definições de gênero padrão.</span><span class="sxs-lookup"><span data-stu-id="3b9d0-131">There are no standard genre definitions.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="3b9d0-132">**\_distância do \_ quadro da chave de vídeo WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3b9d0-132">**WPD\_VIDEO\_KEY\_FRAME\_DISTANCE**</span></span>             | <span data-ttu-id="3b9d0-133">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="3b9d0-133">**VT\_UI4**</span></span>    | <span data-ttu-id="3b9d0-134">O intervalo entre os quadros-chave, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="3b9d0-134">The interval between key frames, in milliseconds.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="3b9d0-135">**\_configuração de \_ qualidade de vídeo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="3b9d0-135">**WPD\_VIDEO\_QUALITY\_SETTING**</span></span>                 | <span data-ttu-id="3b9d0-136">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="3b9d0-136">**VT\_UI4**</span></span>    | <span data-ttu-id="3b9d0-137">A configuração de qualidade do arquivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3b9d0-137">The quality setting for the video file.</span></span> <span data-ttu-id="3b9d0-138">Isso depende do codec.</span><span class="sxs-lookup"><span data-stu-id="3b9d0-138">This is codec-dependent.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="3b9d0-139">**\_número de \_ \_ canal RECORDEDTV de vídeo \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="3b9d0-139">**WPD\_VIDEO\_RECORDEDTV\_CHANNEL\_NUMBER**</span></span>      | <span data-ttu-id="3b9d0-140">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="3b9d0-140">**VT\_UI4**</span></span>    | <span data-ttu-id="3b9d0-141">O número do canal de televisão do qual o vídeo foi gravado.</span><span class="sxs-lookup"><span data-stu-id="3b9d0-141">The television channel number the video was recorded from.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="3b9d0-142">**\_Descrição do \_ \_ programa RECORDEDTV de vídeo \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="3b9d0-142">**WPD\_VIDEO\_RECORDEDTV\_PROGRAM\_DESCRIPTION**</span></span> | <span data-ttu-id="3b9d0-143">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="3b9d0-143">**VT\_LPWSTR**</span></span> | <span data-ttu-id="3b9d0-144">Uma descrição do programa de televisão gravado.</span><span class="sxs-lookup"><span data-stu-id="3b9d0-144">A description of the recorded television program.</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="3b9d0-145">**\_repetição de \_ RECORDEDTV de vídeo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="3b9d0-145">**WPD\_VIDEO\_RECORDEDTV\_REPEAT**</span></span>               | <span data-ttu-id="3b9d0-146">**BOOL do VT \_**</span><span class="sxs-lookup"><span data-stu-id="3b9d0-146">**VT\_BOOL**</span></span>   | <span data-ttu-id="3b9d0-147">Um valor booliano que especifica se o programa de televisão foi uma repetição em exibição.</span><span class="sxs-lookup"><span data-stu-id="3b9d0-147">A Boolean value that specifies whether the television program was a repeat showing.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="3b9d0-148">**\_nome da \_ \_ estação RECORDEDTV de vídeo \_ WPD**</span><span class="sxs-lookup"><span data-stu-id="3b9d0-148">**WPD\_VIDEO\_RECORDEDTV\_STATION\_NAME**</span></span>        | <span data-ttu-id="3b9d0-149">**LPWStr do VT \_**</span><span class="sxs-lookup"><span data-stu-id="3b9d0-149">**VT\_LPWSTR**</span></span> | <span data-ttu-id="3b9d0-150">A estação de televisão da qual o vídeo foi gravado.</span><span class="sxs-lookup"><span data-stu-id="3b9d0-150">The television station that the video was recorded from.</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="3b9d0-151">**\_tipo de \_ exame de vídeo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="3b9d0-151">**WPD\_VIDEO\_SCAN\_TYPE**</span></span>                       | <span data-ttu-id="3b9d0-152">**\_UI4 VT**</span><span class="sxs-lookup"><span data-stu-id="3b9d0-152">**VT\_UI4**</span></span>    | <span data-ttu-id="3b9d0-153">Um enumerador de [**\_ tipos de \_ verificação \_ de vídeo WPD**](wpd-video-scan-types.md) que especifica o entrelaçamento do arquivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3b9d0-153">A [**WPD\_VIDEO\_SCAN\_TYPES**](wpd-video-scan-types.md) enumerator that specifies the interlacing of the video file.</span></span>                                                                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="3b9d0-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b9d0-154">Requirements</span></span>



| <span data-ttu-id="3b9d0-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b9d0-155">Requirement</span></span> | <span data-ttu-id="3b9d0-156">Valor</span><span class="sxs-lookup"><span data-stu-id="3b9d0-156">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b9d0-157">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3b9d0-157">Header</span></span><br/> | <dl> <span data-ttu-id="3b9d0-158"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b9d0-158"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b9d0-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b9d0-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b9d0-160">**Propriedades e atributos WPD**</span><span class="sxs-lookup"><span data-stu-id="3b9d0-160">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




