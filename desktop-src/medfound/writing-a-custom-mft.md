---
description: Esta seção descreve como gravar uma Media Foundation de transformação personalizada (MFT).
ms.assetid: a95828d3-afc5-4f6b-aedd-5b6a72621e0e
title: Gravando uma MFT personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d15b9d5ae655ba67d4a526aeb8a82eb9d3912da9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828615"
---
# <a name="writing-a-custom-mft"></a><span data-ttu-id="d82b8-103">Gravando uma MFT personalizada</span><span class="sxs-lookup"><span data-stu-id="d82b8-103">Writing a Custom MFT</span></span>

<span data-ttu-id="d82b8-104">Esta seção descreve como gravar uma Media Foundation de transformação personalizada (MFT).</span><span class="sxs-lookup"><span data-stu-id="d82b8-104">This section describes how to write a custom Media Foundation Transform (MFT).</span></span>

## <a name="mft-checklist"></a><span data-ttu-id="d82b8-105">Lista de verificação de MFT</span><span class="sxs-lookup"><span data-stu-id="d82b8-105">MFT Checklist</span></span>

<span data-ttu-id="d82b8-106">Ao implementar um MFT personalizado, use a seguinte lista de verificação para determinar os requisitos:</span><span class="sxs-lookup"><span data-stu-id="d82b8-106">When you implement a custom MFT, use the following checklist to determine the requirements:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d82b8-107">Todos os MFTs</span><span class="sxs-lookup"><span data-stu-id="d82b8-107">All MFTs</span></span></td>
<td><span data-ttu-id="d82b8-108">Todos os MFTs devem implementar <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>IMFTransform</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d82b8-108">All MFTs must implement <a href="/windows/desktop/api/mftransform/nn-mftransform-imftransform"><strong>IMFTransform</strong></a>.</span></span><br/> <span data-ttu-id="d82b8-109">Os tópicos a seguir fornecem mais informações sobre como implementar essa interface:</span><span class="sxs-lookup"><span data-stu-id="d82b8-109">The following topics give more information about implementing this interface:</span></span>
<ul>
<li><span data-ttu-id="d82b8-110"><a href="basic-mft-processing-model.md">Modelo de processamento de MFT básico</a></span><span class="sxs-lookup"><span data-stu-id="d82b8-110"><a href="basic-mft-processing-model.md">Basic MFT Processing Model</a></span></span></li>
<li><span data-ttu-id="d82b8-111"><a href="time-stamps-and-durations.md">Carimbos de data/hora e durações</a></span><span class="sxs-lookup"><span data-stu-id="d82b8-111"><a href="time-stamps-and-durations.md">Time Stamps and Durations</a></span></span></li>
<li><span data-ttu-id="d82b8-112"><a href="handling-stream-changes.md">Manipulando alterações de fluxo</a></span><span class="sxs-lookup"><span data-stu-id="d82b8-112"><a href="handling-stream-changes.md">Handling Stream Changes</a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d82b8-113">Codificadores e decodificadores</span><span class="sxs-lookup"><span data-stu-id="d82b8-113">Encoders and decoders</span></span></td>
<td><span data-ttu-id="d82b8-114">Requisitos: consulte <a href="implementing-a-codec-mft.md">implementando um codec de MFT</a>.</span><span class="sxs-lookup"><span data-stu-id="d82b8-114">Requirements: See <a href="implementing-a-codec-mft.md">Implementing a Codec MFT</a>.</span></span><br/> <span data-ttu-id="d82b8-115">Recomendado: implemente <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>IMFQualityAdvise</strong></a> ou <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>IMFQualityAdvise2</strong></a>para dar suporte a notificações de QoS (qualidade de serviço).</span><span class="sxs-lookup"><span data-stu-id="d82b8-115">Recommended: Implement <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise"><strong>IMFQualityAdvise</strong></a> or <a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2"><strong>IMFQualityAdvise2</strong></a>, to support quality-of-service (QoS) notifications.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d82b8-116">Decodificadores de vídeo e processadores de vídeo</span><span class="sxs-lookup"><span data-stu-id="d82b8-116">Video decoders and video processors</span></span></td>
<td><span data-ttu-id="d82b8-117">Opcional: suporte para aceleração de vídeo do DirectX.</span><span class="sxs-lookup"><span data-stu-id="d82b8-117">Optional: Support DirectX Video Acceleration.</span></span><br/>
<ul>
<li><span data-ttu-id="d82b8-118"><a href="direct3d-aware-mfts.md">MFTs com reconhecimento de Direct3D</a></span><span class="sxs-lookup"><span data-stu-id="d82b8-118"><a href="direct3d-aware-mfts.md">Direct3D-Aware MFTs</a></span></span></li>
<li><span data-ttu-id="d82b8-119"><a href="supporting-dxva-2-0-in-media-foundation.md">Suporte a DXVA 2,0 no Media Foundation</a></span><span class="sxs-lookup"><span data-stu-id="d82b8-119"><a href="supporting-dxva-2-0-in-media-foundation.md">Supporting DXVA 2.0 in Media Foundation</a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d82b8-120">Codecs de hardware</span><span class="sxs-lookup"><span data-stu-id="d82b8-120">Hardware codecs</span></span></td>
<td><span data-ttu-id="d82b8-121">Consulte <a href="hardware-mfts.md">hardware MFTs</a>.</span><span class="sxs-lookup"><span data-stu-id="d82b8-121">See <a href="hardware-mfts.md">Hardware MFTs</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d82b8-122">Para tornar seu MFT detectável por aplicativos...</span><span class="sxs-lookup"><span data-stu-id="d82b8-122">To make your MFT discoverable by applications...</span></span></td>
<td><span data-ttu-id="d82b8-123">Consulte <a href="registering-and-enumerating-mfts.md">registrando e enumerando MFTs</a>.</span><span class="sxs-lookup"><span data-stu-id="d82b8-123">See <a href="registering-and-enumerating-mfts.md">Registering and Enumerating MFTs</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d82b8-124">Processamento de dados assíncronos</span><span class="sxs-lookup"><span data-stu-id="d82b8-124">Asynchronous data processing</span></span></td>
<td><span data-ttu-id="d82b8-125">O modelo de MFT padrão usa chamadas síncronas (de bloqueio) para processar dados.</span><span class="sxs-lookup"><span data-stu-id="d82b8-125">The default MFT model uses synchronous (blocking) calls to process data.</span></span> <span data-ttu-id="d82b8-126">Para alguns MFTs, o processamento assíncrono pode ser mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="d82b8-126">For some MFTs, asynchronous processing can be more efficient.</span></span> <span data-ttu-id="d82b8-127">No entanto, também é mais complexo implementar.</span><span class="sxs-lookup"><span data-stu-id="d82b8-127">However, it is also more complex to implement.</span></span><br/> <span data-ttu-id="d82b8-128">Para obter mais informações, consulte <a href="asynchronous-mfts.md">assíncrona MFTs</a>.</span><span class="sxs-lookup"><span data-stu-id="d82b8-128">For more information, see <a href="asynchronous-mfts.md">Asynchronous MFTs</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d82b8-129">Controle de taxa, modo de truque ou reprodução reversa</span><span class="sxs-lookup"><span data-stu-id="d82b8-129">Rate control, trick mode, or reverse playback</span></span></td>
<td><span data-ttu-id="d82b8-130">Consulte <a href="implementing-rate-control.md">implementando o controle de taxa</a>.</span><span class="sxs-lookup"><span data-stu-id="d82b8-130">See <a href="implementing-rate-control.md">Implementing Rate Control</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d82b8-131">Se o MFT criar threads...</span><span class="sxs-lookup"><span data-stu-id="d82b8-131">If your MFT creates threads...</span></span></td>
<td><span data-ttu-id="d82b8-132">Implemente a interface <a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>IMFRealTimeClient</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="d82b8-132">Implement the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient"><strong>IMFRealTimeClient</strong></a> interface.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d82b8-133">Se a MFT tiver restrições de licenciamento...</span><span class="sxs-lookup"><span data-stu-id="d82b8-133">If your MFT has licensing restrictions...</span></span></td>
<td><span data-ttu-id="d82b8-134">Considere o uso do mecanismo de campo de uso.</span><span class="sxs-lookup"><span data-stu-id="d82b8-134">Consider using the field-of-use mechanism.</span></span> <span data-ttu-id="d82b8-135">Consulte o <a href="field-of-use-restrictions.md">campo de restrições de uso</a>.</span><span class="sxs-lookup"><span data-stu-id="d82b8-135">See <a href="field-of-use-restrictions.md">Field of Use Restrictions</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d82b8-136">Se você estiver portando um objeto de mídia DirectX existente (DMO)...</span><span class="sxs-lookup"><span data-stu-id="d82b8-136">If you are porting an existing DirectX Media Object (DMO)...</span></span></td>
<td><span data-ttu-id="d82b8-137">Consulte <a href="comparison-of-mfts-and-dmos.md">comparação de MFTs e DMOs</a>.</span><span class="sxs-lookup"><span data-stu-id="d82b8-137">See <a href="comparison-of-mfts-and-dmos.md">Comparison of MFTs and DMOs</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d82b8-138">Esta seção contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="d82b8-138">This section contains the following topics:</span></span>

-   [<span data-ttu-id="d82b8-139">Carimbos de data/hora e durações</span><span class="sxs-lookup"><span data-stu-id="d82b8-139">Time Stamps and Durations</span></span>](time-stamps-and-durations.md)
-   [<span data-ttu-id="d82b8-140">Manipulando alterações de fluxo</span><span class="sxs-lookup"><span data-stu-id="d82b8-140">Handling Stream Changes</span></span>](handling-stream-changes.md)
-   [<span data-ttu-id="d82b8-141">Implementando uma MFT do codec</span><span class="sxs-lookup"><span data-stu-id="d82b8-141">Implementing a Codec MFT</span></span>](implementing-a-codec-mft.md)
-   [<span data-ttu-id="d82b8-142">MFTs com reconhecimento de Direct3D</span><span class="sxs-lookup"><span data-stu-id="d82b8-142">Direct3D-Aware MFTs</span></span>](direct3d-aware-mfts.md)
-   [<span data-ttu-id="d82b8-143">MFTs de hardware</span><span class="sxs-lookup"><span data-stu-id="d82b8-143">Hardware MFTs</span></span>](hardware-mfts.md)
-   [<span data-ttu-id="d82b8-144">Mérito do codec</span><span class="sxs-lookup"><span data-stu-id="d82b8-144">Codec Merit</span></span>](codec-merit.md)

## <a name="related-topics"></a><span data-ttu-id="d82b8-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d82b8-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d82b8-146">Transformações de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d82b8-146">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> </dl>

 

 




