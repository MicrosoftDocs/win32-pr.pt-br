---
description: A interface IMediaDet recupera informações sobre um arquivo de mídia, como o número de fluxos, o tipo de mídia, a duração e a taxa de quadros de cada fluxo.
ms.assetid: 596fc84e-a88a-4e1b-aa48-b6dc9031db31
title: Interface IMediaDet (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ca5c87a1424872491aba5dcf4e01011872e9ff36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782231"
---
# <a name="imediadet-interface"></a><span data-ttu-id="58862-103">Interface IMediaDet</span><span class="sxs-lookup"><span data-stu-id="58862-103">IMediaDet interface</span></span>

> [!Note]  
> <span data-ttu-id="58862-104">\[Preterido.</span><span class="sxs-lookup"><span data-stu-id="58862-104">\[Deprecated.</span></span> <span data-ttu-id="58862-105">Essa API pode ser removida de versões futuras do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="58862-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="58862-106">A `IMediaDet` interface recupera informações sobre um arquivo de mídia, como o número de fluxos, o tipo de mídia, a duração e a taxa de quadros de cada fluxo.</span><span class="sxs-lookup"><span data-stu-id="58862-106">The `IMediaDet` interface retrieves information about a media file, such as the number of streams, and the media type, duration, and frame rate of each stream.</span></span> <span data-ttu-id="58862-107">Ele também contém métodos para recuperar quadros individuais de um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="58862-107">It also contains methods for retrieving individual frames from a video stream.</span></span> <span data-ttu-id="58862-108">O objeto do [detector de mídia (MediaDet)](media-detector--mediadet.md) expõe essa interface.</span><span class="sxs-lookup"><span data-stu-id="58862-108">The [Media Detector (MediaDet)](media-detector--mediadet.md) object exposes this interface.</span></span>

<span data-ttu-id="58862-109">Para obter informações sobre um arquivo usando essa interface, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="58862-109">To obtain information about a file using this interface, perform the following steps:</span></span>

1.  <span data-ttu-id="58862-110">Crie uma instância do objeto MediaDet chamando **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="58862-110">Create an instance of the MediaDet object by calling **CoCreateInstance**.</span></span> <span data-ttu-id="58862-111">A ID de classe é CLSID \_ MediaDet.</span><span class="sxs-lookup"><span data-stu-id="58862-111">The class ID is CLSID\_MediaDet.</span></span>
2.  <span data-ttu-id="58862-112">Chame [**IMediaDet::p \_ nome**](imediadet-put-filename.md) do arquivo UT para especificar o nome do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="58862-112">Call [**IMediaDet::put\_Filename**](imediadet-put-filename.md) to specify the name of the source file.</span></span>
3.  <span data-ttu-id="58862-113">Chame [**IMediaDet:: get \_ OutputStreams**](imediadet-get-outputstreams.md) para obter o número de fluxos de saída na origem.</span><span class="sxs-lookup"><span data-stu-id="58862-113">Call [**IMediaDet::get\_OutputStreams**](imediadet-get-outputstreams.md) to obtain the number of output streams in the source.</span></span>
4.  <span data-ttu-id="58862-114">Chame [**IMediaDet::p UT \_ CurrentStream**](imediadet-put-currentstream.md) para especificar um fluxo específico.</span><span class="sxs-lookup"><span data-stu-id="58862-114">Call [**IMediaDet::put\_CurrentStream**](imediadet-put-currentstream.md) to specify a particular stream.</span></span>
5.  <span data-ttu-id="58862-115">Chame qualquer um dos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="58862-115">Call any of the following methods:</span></span>
    -   [<span data-ttu-id="58862-116">**IMediaDet:: obter a \_ taxa de quadros**</span><span class="sxs-lookup"><span data-stu-id="58862-116">**IMediaDet::get\_FrameRate**</span></span>](imediadet-get-framerate.md)
    -   [<span data-ttu-id="58862-117">**IMediaDet:: obter \_ streamLength**</span><span class="sxs-lookup"><span data-stu-id="58862-117">**IMediaDet::get\_StreamLength**</span></span>](imediadet-get-streamlength.md)
    -   [<span data-ttu-id="58862-118">**IMediaDet:: obter \_ StreamMediaType**</span><span class="sxs-lookup"><span data-stu-id="58862-118">**IMediaDet::get\_StreamMediaType**</span></span>](imediadet-get-streammediatype.md)
    -   [<span data-ttu-id="58862-119">**IMediaDet:: obter \_ streamtype**</span><span class="sxs-lookup"><span data-stu-id="58862-119">**IMediaDet::get\_StreamType**</span></span>](imediadet-get-streamtype.md)

<span data-ttu-id="58862-120">Para recuperar um quadro de vídeo, chame [**IMediaDet:: GetBitmapBits**](imediadet-getbitmapbits.md) ou [**IMediaDet:: WriteBitmapBits**](imediadet-writebitmapbits.md).</span><span class="sxs-lookup"><span data-stu-id="58862-120">To retrieve a video frame, call [**IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) or [**IMediaDet::WriteBitmapBits**](imediadet-writebitmapbits.md).</span></span> <span data-ttu-id="58862-121">O quadro retornado sempre está no formato RGB de 24 bits.</span><span class="sxs-lookup"><span data-stu-id="58862-121">The returned frame is always in 24-bit RGB format.</span></span>

> [!Note]  
> <span data-ttu-id="58862-122">Não use o mesmo objeto MediaDet com vários arquivos.</span><span class="sxs-lookup"><span data-stu-id="58862-122">Do not use the same MediaDet object with multiple files.</span></span> <span data-ttu-id="58862-123">Para obter informações ou quadros de vídeo de mais de um arquivo, use instâncias MediaDet separadas.</span><span class="sxs-lookup"><span data-stu-id="58862-123">To get information or video frames from more than one file, use separate MediaDet instances.</span></span>

 

<span data-ttu-id="58862-124">A interface **IMediaDet** não dá suporte a formatos [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , portanto, você não pode usar essa interface para obter campos entrelaçados ou informações sobre entrelaçamento.</span><span class="sxs-lookup"><span data-stu-id="58862-124">The **IMediaDet** interface does not support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) formats, so you cannot use this interface to get interlaced fields or information about interlacing.</span></span> <span data-ttu-id="58862-125">Além disso, se o decodificador upstream der suporte apenas a **VIDEOINFOHEADER2**, você não poderá usar `IMediaDet` .</span><span class="sxs-lookup"><span data-stu-id="58862-125">Also, if the upstream decoder supports only **VIDEOINFOHEADER2**, you cannot use `IMediaDet`.</span></span> <span data-ttu-id="58862-126">Esse pode ser o caso com um decodificador MPEG-2, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="58862-126">This might be the case with an MPEG-2 decoder, for example.</span></span> <span data-ttu-id="58862-127">Além disso, a `IMediaDet` interface ignora todos os fluxos no arquivo que não são de vídeo ou áudio.</span><span class="sxs-lookup"><span data-stu-id="58862-127">Also, the `IMediaDet` interface ignores any streams in the file that are not video or audio.</span></span> <span data-ttu-id="58862-128">Por exemplo, se o arquivo contiver um fluxo de áudio, um fluxo de dados e um fluxo de vídeo, o método **Get \_ OutputStreams** relatará apenas dois fluxos (o áudio e o vídeo).</span><span class="sxs-lookup"><span data-stu-id="58862-128">For example, if the file contains an audio stream, a data stream, and a video stream, the **get\_OutputStreams** method will report only two streams (the audio and video).</span></span>

## <a name="members"></a><span data-ttu-id="58862-129">Membros</span><span class="sxs-lookup"><span data-stu-id="58862-129">Members</span></span>

<span data-ttu-id="58862-130">A interface **IMediaDet** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="58862-130">The **IMediaDet** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="58862-131">**IMediaDet** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="58862-131">**IMediaDet** also has these types of members:</span></span>

-   [<span data-ttu-id="58862-132">Métodos</span><span class="sxs-lookup"><span data-stu-id="58862-132">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="58862-133">Métodos</span><span class="sxs-lookup"><span data-stu-id="58862-133">Methods</span></span>

<span data-ttu-id="58862-134">A interface **IMediaDet** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="58862-134">The **IMediaDet** interface has these methods.</span></span>



| <span data-ttu-id="58862-135">Método</span><span class="sxs-lookup"><span data-stu-id="58862-135">Method</span></span>                                                        | <span data-ttu-id="58862-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="58862-136">Description</span></span>                                                                                                |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="58862-137">**EnterBitmapGrabMode**</span><span class="sxs-lookup"><span data-stu-id="58862-137">**EnterBitmapGrabMode**</span></span>](imediadet-enterbitmapgrabmode.md)  | <span data-ttu-id="58862-138">Alterna o detector de mídia para o modo de captura de bitmap e procura o grafo de filtro em um horário especificado.</span><span class="sxs-lookup"><span data-stu-id="58862-138">Switches the media detector to bitmap grab mode and seeks the filter graph to a specified time.</span></span><br/> |
| [<span data-ttu-id="58862-139">**obter \_ CurrentStream**</span><span class="sxs-lookup"><span data-stu-id="58862-139">**get\_CurrentStream**</span></span>](imediadet-get-currentstream.md)     | <span data-ttu-id="58862-140">Recupera o número de fluxo usado atualmente pelo detector de mídia.</span><span class="sxs-lookup"><span data-stu-id="58862-140">Retrieves the stream number currently used by the media detector.</span></span><br/>                               |
| [<span data-ttu-id="58862-141">**obter \_ nome de arquivo**</span><span class="sxs-lookup"><span data-stu-id="58862-141">**get\_Filename**</span></span>](imediadet-get-filename.md)               | <span data-ttu-id="58862-142">Recupera o nome do arquivo de origem usado atualmente pelo detector de mídia.</span><span class="sxs-lookup"><span data-stu-id="58862-142">Retrieves the name of the source file currently used by the media detector.</span></span><br/>                     |
| [<span data-ttu-id="58862-143">**obter \_ filtro**</span><span class="sxs-lookup"><span data-stu-id="58862-143">**get\_Filter**</span></span>](imediadet-get-filter.md)                   | <span data-ttu-id="58862-144">Recupera um ponteiro para o filtro de origem usado atualmente pelo detector de mídia.</span><span class="sxs-lookup"><span data-stu-id="58862-144">Retrieves a pointer to the source filter currently used by the media detector.</span></span><br/>                  |
| [<span data-ttu-id="58862-145">**obter \_ taxa de quadros**</span><span class="sxs-lookup"><span data-stu-id="58862-145">**get\_FrameRate**</span></span>](imediadet-get-framerate.md)             | <span data-ttu-id="58862-146">Recupera a taxa de quadros do fluxo atual.</span><span class="sxs-lookup"><span data-stu-id="58862-146">Retrieves the frame rate of the current stream.</span></span><br/>                                                 |
| [<span data-ttu-id="58862-147">**obter \_ OutputStreams**</span><span class="sxs-lookup"><span data-stu-id="58862-147">**get\_OutputStreams**</span></span>](imediadet-get-outputstreams.md)     | <span data-ttu-id="58862-148">Recupera o número de fluxos de áudio e vídeo contidos na origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="58862-148">Retrieves the number of audio and video streams contained in the media source.</span></span><br/>                  |
| [<span data-ttu-id="58862-149">**obter \_ streamLength**</span><span class="sxs-lookup"><span data-stu-id="58862-149">**get\_StreamLength**</span></span>](imediadet-get-streamlength.md)       | <span data-ttu-id="58862-150">Recupera a duração do fluxo atual.</span><span class="sxs-lookup"><span data-stu-id="58862-150">Retrieves the duration of the current stream.</span></span><br/>                                                   |
| [<span data-ttu-id="58862-151">**obter \_ StreamMediaType**</span><span class="sxs-lookup"><span data-stu-id="58862-151">**get\_StreamMediaType**</span></span>](imediadet-get-streammediatype.md) | <span data-ttu-id="58862-152">Recupera o tipo de mídia do fluxo atual.</span><span class="sxs-lookup"><span data-stu-id="58862-152">Retrieves the media type of the current stream.</span></span><br/>                                                 |
| [<span data-ttu-id="58862-153">**obter \_ streamtype**</span><span class="sxs-lookup"><span data-stu-id="58862-153">**get\_StreamType**</span></span>](imediadet-get-streamtype.md)           | <span data-ttu-id="58862-154">Recupera o identificador global exclusivo (GUID) para o tipo de mídia do fluxo atual.</span><span class="sxs-lookup"><span data-stu-id="58862-154">Retrieves the globally unique identifier (GUID) for the media type of the current stream.</span></span><br/>       |
| [<span data-ttu-id="58862-155">**obter \_ StreamTypeB**</span><span class="sxs-lookup"><span data-stu-id="58862-155">**get\_StreamTypeB**</span></span>](imediadet-get-streamtypeb.md)         | <span data-ttu-id="58862-156">Recupera uma cadeia de caracteres que representa o GUID do tipo de mídia para o fluxo atual.</span><span class="sxs-lookup"><span data-stu-id="58862-156">Retrieves a string representing the GUID of the media type for the current stream.</span></span><br/>              |
| [<span data-ttu-id="58862-157">**GetBitmapBits**</span><span class="sxs-lookup"><span data-stu-id="58862-157">**GetBitmapBits**</span></span>](imediadet-getbitmapbits.md)              | <span data-ttu-id="58862-158">Recupera um quadro de vídeo no tempo de mídia especificado.</span><span class="sxs-lookup"><span data-stu-id="58862-158">Retrieves a video frame at the specified media time.</span></span><br/>                                            |
| [<span data-ttu-id="58862-159">**GetSampleGrabber**</span><span class="sxs-lookup"><span data-stu-id="58862-159">**GetSampleGrabber**</span></span>](imediadet-getsamplegrabber.md)        | <span data-ttu-id="58862-160">Recupera um ponteiro para a interface [**ISampleGrabber**](isamplegrabber.md) .</span><span class="sxs-lookup"><span data-stu-id="58862-160">Retrieves a pointer to the [**ISampleGrabber**](isamplegrabber.md) interface.</span></span><br/>                  |
| [<span data-ttu-id="58862-161">**colocar \_ CurrentStream**</span><span class="sxs-lookup"><span data-stu-id="58862-161">**put\_CurrentStream**</span></span>](imediadet-put-currentstream.md)     | <span data-ttu-id="58862-162">Especifica o número de fluxo para o detector de mídia a ser usado.</span><span class="sxs-lookup"><span data-stu-id="58862-162">Specifies the stream number for the media detector to use.</span></span><br/>                                      |
| [<span data-ttu-id="58862-163">**colocar \_ nome do arquivo**</span><span class="sxs-lookup"><span data-stu-id="58862-163">**put\_Filename**</span></span>](imediadet-put-filename.md)               | <span data-ttu-id="58862-164">Especifica o nome do arquivo de origem para o detector de mídia a ser usado.</span><span class="sxs-lookup"><span data-stu-id="58862-164">Specifies the name of the source file for the media detector to use.</span></span><br/>                            |
| [<span data-ttu-id="58862-165">**colocar \_ filtro**</span><span class="sxs-lookup"><span data-stu-id="58862-165">**put\_Filter**</span></span>](imediadet-put-filter.md)                   | <span data-ttu-id="58862-166">Especifica um filtro de origem para o detector de mídia a ser usado.</span><span class="sxs-lookup"><span data-stu-id="58862-166">Specifies a source filter for the media detector to use.</span></span><br/>                                        |
| [<span data-ttu-id="58862-167">**WriteBitmapBits**</span><span class="sxs-lookup"><span data-stu-id="58862-167">**WriteBitmapBits**</span></span>](imediadet-writebitmapbits.md)          | <span data-ttu-id="58862-168">Recupera um quadro de vídeo no tempo de mídia especificado e grava-o em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="58862-168">Retrieves a video frame at the specified media time and writes it to a file.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="58862-169">Comentários</span><span class="sxs-lookup"><span data-stu-id="58862-169">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="58862-170">O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.</span><span class="sxs-lookup"><span data-stu-id="58862-170">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="58862-171">Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="58862-171">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="58862-172">O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.</span><span class="sxs-lookup"><span data-stu-id="58862-172">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="58862-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="58862-173">Requirements</span></span>



| <span data-ttu-id="58862-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="58862-174">Requirement</span></span> | <span data-ttu-id="58862-175">Valor</span><span class="sxs-lookup"><span data-stu-id="58862-175">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58862-176">parâmetro</span><span class="sxs-lookup"><span data-stu-id="58862-176">Header</span></span><br/>  | <dl> <span data-ttu-id="58862-177"><dt>QEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="58862-177"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="58862-178">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="58862-178">Library</span></span><br/> | <dl> <span data-ttu-id="58862-179"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58862-179"><dt>Strmiids.lib</dt></span></span> </dl> |



 

 
