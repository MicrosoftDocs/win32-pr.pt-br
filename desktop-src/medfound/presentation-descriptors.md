---
description: Descritores de apresentação
ms.assetid: 714c8bda-5ce1-47e2-ba73-9304e26b3129
title: Descritores de apresentação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44f1581e35fe6d875c691efdd5ef5736c1aa5215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759582"
---
# <a name="presentation-descriptors"></a><span data-ttu-id="b9a58-103">Descritores de apresentação</span><span class="sxs-lookup"><span data-stu-id="b9a58-103">Presentation Descriptors</span></span>

<span data-ttu-id="b9a58-104">Uma *apresentação* é um conjunto de fluxos de mídia relacionados que compartilham um tempo de apresentação comum.</span><span class="sxs-lookup"><span data-stu-id="b9a58-104">A *presentation* is a set of related media streams that share a common presentation time.</span></span> <span data-ttu-id="b9a58-105">Por exemplo, uma apresentação pode consistir em fluxos de áudio e vídeo de um filme.</span><span class="sxs-lookup"><span data-stu-id="b9a58-105">For example, a presentation might consist of the audio and video streams from a movie.</span></span> <span data-ttu-id="b9a58-106">Um *descritor de apresentação* é um objeto que contém a descrição de uma apresentação específica.</span><span class="sxs-lookup"><span data-stu-id="b9a58-106">A *presentation descriptor* is an object that contains the description of a particular presentation.</span></span> <span data-ttu-id="b9a58-107">Os descritores de apresentação são usados para configurar as fontes de mídia e alguns coletores de mídia.</span><span class="sxs-lookup"><span data-stu-id="b9a58-107">Presentation descriptors are used to configure media sources and some media sinks.</span></span>

<span data-ttu-id="b9a58-108">Cada descritor de apresentação contém uma lista de um ou mais *descripdores de fluxo*.</span><span class="sxs-lookup"><span data-stu-id="b9a58-108">Each presentation descriptor contains a list of one or more *stream descriptors*.</span></span> <span data-ttu-id="b9a58-109">Elas descrevem os fluxos na apresentação.</span><span class="sxs-lookup"><span data-stu-id="b9a58-109">These describe the streams in the presentation.</span></span> <span data-ttu-id="b9a58-110">Os fluxos podem ser selecionados ou desmarcados.</span><span class="sxs-lookup"><span data-stu-id="b9a58-110">Streams can be either selected or deselected.</span></span> <span data-ttu-id="b9a58-111">Somente os fluxos selecionados produzem dados.</span><span class="sxs-lookup"><span data-stu-id="b9a58-111">Only the selected streams produce data.</span></span> <span data-ttu-id="b9a58-112">Os fluxos desmarcados não estão ativos e não produzem nenhum dado.</span><span class="sxs-lookup"><span data-stu-id="b9a58-112">Deselected streams are not active and do not produce any data.</span></span> <span data-ttu-id="b9a58-113">Cada descritor de fluxo tem um *manipulador de tipo de mídia*, que é usado para alterar o tipo de mídia do fluxo ou obter o tipo de mídia atual do fluxo.</span><span class="sxs-lookup"><span data-stu-id="b9a58-113">Each stream descriptor has a *media type handler*, which is used to change the stream's media type or get the stream's current media type.</span></span> <span data-ttu-id="b9a58-114">(Para obter mais informações sobre tipos de mídia, consulte [tipos de mídia](media-types.md).)</span><span class="sxs-lookup"><span data-stu-id="b9a58-114">(For more information about media types, see [Media Types](media-types.md).)</span></span>

<span data-ttu-id="b9a58-115">A tabela a seguir mostra as interfaces primárias que cada um desses objetos expõe.</span><span class="sxs-lookup"><span data-stu-id="b9a58-115">The following table shows the primary interfaces that each of these objects exposes.</span></span>



| <span data-ttu-id="b9a58-116">Objeto</span><span class="sxs-lookup"><span data-stu-id="b9a58-116">Object</span></span>                  | <span data-ttu-id="b9a58-117">Interface</span><span class="sxs-lookup"><span data-stu-id="b9a58-117">Interface</span></span>                                                      |
|-------------------------|----------------------------------------------------------------|
| <span data-ttu-id="b9a58-118">Descritor de apresentação</span><span class="sxs-lookup"><span data-stu-id="b9a58-118">Presentation descriptor</span></span> | [<span data-ttu-id="b9a58-119">**IMFPresentationDescriptor**</span><span class="sxs-lookup"><span data-stu-id="b9a58-119">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) |
| <span data-ttu-id="b9a58-120">Descritor de fluxo</span><span class="sxs-lookup"><span data-stu-id="b9a58-120">Stream descriptor</span></span>       | [<span data-ttu-id="b9a58-121">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="b9a58-121">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)             |
| <span data-ttu-id="b9a58-122">Manipulador de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="b9a58-122">Media type handler</span></span>      | [<span data-ttu-id="b9a58-123">**IMFMediaTypeHandler**</span><span class="sxs-lookup"><span data-stu-id="b9a58-123">**IMFMediaTypeHandler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)             |



 

## <a name="media-source-presentations"></a><span data-ttu-id="b9a58-124">Apresentações de origem de mídia</span><span class="sxs-lookup"><span data-stu-id="b9a58-124">Media Source Presentations</span></span>

<span data-ttu-id="b9a58-125">Cada fonte de mídia fornece um descritor de apresentação que descreve a configuração padrão para a origem.</span><span class="sxs-lookup"><span data-stu-id="b9a58-125">Every media source provides a presentation descriptor that describes the default configuration for the source.</span></span> <span data-ttu-id="b9a58-126">Na configuração padrão, pelo menos um fluxo é selecionado e cada fluxo selecionado tem um tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="b9a58-126">In the default configuration, at least one stream is selected, and every selected stream has a media type.</span></span> <span data-ttu-id="b9a58-127">Para obter o descritor de apresentação, chame [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="b9a58-127">To get the presentation descriptor, call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span> <span data-ttu-id="b9a58-128">O método retorna um ponteiro [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="b9a58-128">The method returns an [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) pointer.</span></span>

<span data-ttu-id="b9a58-129">Você pode modificar o descritor de apresentação da origem para selecionar um conjunto diferente de fluxos.</span><span class="sxs-lookup"><span data-stu-id="b9a58-129">You can modify the source's presentation descriptor to select a different set of streams.</span></span> <span data-ttu-id="b9a58-130">Não modifique o descritor de apresentação a menos que a origem da mídia seja interrompida.</span><span class="sxs-lookup"><span data-stu-id="b9a58-130">Do not modify the presentation descriptor unless the media source is stopped.</span></span> <span data-ttu-id="b9a58-131">As alterações são aplicadas quando você chama [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) para iniciar a origem.</span><span class="sxs-lookup"><span data-stu-id="b9a58-131">The changes are applied when you call [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) to start the source.</span></span>

<span data-ttu-id="b9a58-132">Para obter o número de fluxos, chame [**IMFPresentationDescriptor:: GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount).</span><span class="sxs-lookup"><span data-stu-id="b9a58-132">To get the number of streams, call [**IMFPresentationDescriptor::GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount).</span></span> <span data-ttu-id="b9a58-133">Para obter o descritor de fluxo para um fluxo, chame [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) e passe o índice do fluxo.</span><span class="sxs-lookup"><span data-stu-id="b9a58-133">To get the stream descriptor for a stream, call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) and pass in the index of the stream.</span></span> <span data-ttu-id="b9a58-134">Os fluxos são indexados de zero.</span><span class="sxs-lookup"><span data-stu-id="b9a58-134">Streams are indexed from zero.</span></span> <span data-ttu-id="b9a58-135">O método **GetStreamDescriptorByIndex** retorna um ponteiro [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="b9a58-135">The **GetStreamDescriptorByIndex** method returns an [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) pointer.</span></span> <span data-ttu-id="b9a58-136">Ele também retorna um sinalizador booliano que indica se o fluxo está selecionado.</span><span class="sxs-lookup"><span data-stu-id="b9a58-136">It also returns a Boolean flag indicating whether the stream is selected.</span></span> <span data-ttu-id="b9a58-137">Se o fluxo for selecionado, a origem da mídia produzirá dados para esse fluxo.</span><span class="sxs-lookup"><span data-stu-id="b9a58-137">If the stream is selected, the media source produces data for that stream.</span></span> <span data-ttu-id="b9a58-138">Caso contrário, a origem não produzirá nenhum dado para esse fluxo.</span><span class="sxs-lookup"><span data-stu-id="b9a58-138">Otherwise, the source does not produce any data for that stream.</span></span> <span data-ttu-id="b9a58-139">Para selecionar um fluxo, chame [**IMFPresentationDescriptor:: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) com o índice do fluxo.</span><span class="sxs-lookup"><span data-stu-id="b9a58-139">To select a stream, call [**IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) with the index of the stream.</span></span> <span data-ttu-id="b9a58-140">Para anular a seleção de um fluxo, chame [**IMFPresentationDescriptor::D eselectstream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).</span><span class="sxs-lookup"><span data-stu-id="b9a58-140">To deselect a stream, call [**IMFPresentationDescriptor::DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream).</span></span>

<span data-ttu-id="b9a58-141">O código a seguir mostra como obter o descritor de apresentação de uma origem de mídia e enumerar os fluxos.</span><span class="sxs-lookup"><span data-stu-id="b9a58-141">The following code shows how to get the presentation descriptor from a media source and enumerate the streams.</span></span>


```C++
HRESULT hr = S_OK;
DWORD cStreams = 0;
BOOL  fSelected = FALSE;

IMFPresentationDescriptor *pPresentation = NULL;
IMFStreamDescriptor *pStreamDesc = NULL;

hr = pSource->CreatePresentationDescriptor(&pPresentation);

if (SUCCEEDED(hr))
{
    hr = pPresentation->GetStreamDescriptorCount(&cStreams);
}

if (SUCCEEDED(hr))
{
    for (DWORD iStream = 0; iStream < cStreams; iStream++)
    {
        hr = pPresentation->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);

        if (FAILED(hr))
        {
            break;
        }

        /*  Use the stream descriptor. (Not shown.) */

        SAFE_RELEASE(pStreamDesc);
    }
}
SAFE_RELEASE(pPresentation);
SAFE_RELEASE(pStreamDesc);
```



## <a name="media-type-handlers"></a><span data-ttu-id="b9a58-142">Manipuladores de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="b9a58-142">Media Type Handlers</span></span>

<span data-ttu-id="b9a58-143">Para alterar o tipo de mídia do fluxo ou obter o tipo de mídia atual do fluxo, use o manipulador de tipo de mídia do descritor de fluxo.</span><span class="sxs-lookup"><span data-stu-id="b9a58-143">To change the stream's media type or to get the stream's current media type, use the stream descriptor's media type handler.</span></span> <span data-ttu-id="b9a58-144">Chame [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) para obter o manipulador de tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="b9a58-144">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) to get the media type handler.</span></span> <span data-ttu-id="b9a58-145">Esse método retorna um ponteiro [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) .</span><span class="sxs-lookup"><span data-stu-id="b9a58-145">This method returns an [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) pointer.</span></span>

<span data-ttu-id="b9a58-146">Se você simplesmente deseja saber que tipo de dados está no fluxo, como áudio ou vídeo, chame [**IMFMediaTypeHandler:: Getmajortype**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype).</span><span class="sxs-lookup"><span data-stu-id="b9a58-146">If you simply want to know what kind of data is in the stream, such as audio or video, call [**IMFMediaTypeHandler::GetMajorType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmajortype).</span></span> <span data-ttu-id="b9a58-147">Esse método retorna o GUID para o tipo de mídia principal.</span><span class="sxs-lookup"><span data-stu-id="b9a58-147">This method returns the GUID for the major media type.</span></span> <span data-ttu-id="b9a58-148">Por exemplo, um aplicativo de reprodução normalmente conecta um fluxo de áudio ao processador de áudio e um fluxo de vídeo ao processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b9a58-148">For example, a playback application typically connects an audio stream to the audio renderer and a video stream to the video renderer.</span></span> <span data-ttu-id="b9a58-149">Se você usar a sessão de mídia ou o carregador de topologia para criar uma topologia, o GUID de tipo principal poderá ser a única informação de formato de que você precisa.</span><span class="sxs-lookup"><span data-stu-id="b9a58-149">If you use the Media Session or the topology loader to build a topology, the major type GUID might be the only format information that you need.</span></span>

<span data-ttu-id="b9a58-150">Se seu aplicativo precisar de informações mais detalhadas sobre o formato atual, chame [**IMFMediaTypeHandler:: GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype).</span><span class="sxs-lookup"><span data-stu-id="b9a58-150">If your application needs more detailed information about the current format, call [**IMFMediaTypeHandler::GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype).</span></span> <span data-ttu-id="b9a58-151">Esse método retorna um ponteiro para a interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) do tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="b9a58-151">This method returns a pointer to the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface of the media type.</span></span> <span data-ttu-id="b9a58-152">Use esta interface para obter os detalhes do formato.</span><span class="sxs-lookup"><span data-stu-id="b9a58-152">Use this interface to get the details of the format.</span></span>

<span data-ttu-id="b9a58-153">O manipulador de tipo de mídia também contém uma lista de tipos de mídia com suporte para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="b9a58-153">The media type handler also contains a list of supported media types for the stream.</span></span> <span data-ttu-id="b9a58-154">Para obter o tamanho da lista, chame [**IMFMediaTypeHandler:: GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount).</span><span class="sxs-lookup"><span data-stu-id="b9a58-154">To get the size of the list, call [**IMFMediaTypeHandler::GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount).</span></span> <span data-ttu-id="b9a58-155">Para obter um tipo de mídia da lista, chame [**IMFMediaTypeHandler:: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) com o índice do tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="b9a58-155">To get a media type from the list, call [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) with the index of the media type.</span></span> <span data-ttu-id="b9a58-156">Os tipos de mídia são retornados na ordem aproximada de preferência.</span><span class="sxs-lookup"><span data-stu-id="b9a58-156">Media types are returned in the approximate order of preference.</span></span> <span data-ttu-id="b9a58-157">Por exemplo, para formatos de áudio, taxas de exemplo mais altas são preferenciais em relação às taxas de amostra mais baixas.</span><span class="sxs-lookup"><span data-stu-id="b9a58-157">For example, for audio formats, higher sample rates are preferred over lower sample rates.</span></span> <span data-ttu-id="b9a58-158">No entanto, não há nenhuma regra definitiva que governa a ordenação, portanto, você deve tratá-la simplesmente como uma diretriz.</span><span class="sxs-lookup"><span data-stu-id="b9a58-158">However, there is no definitive rule that governs the ordering, so you should treat it simply as a guideline.</span></span>

<span data-ttu-id="b9a58-159">A lista de tipos com suporte pode não conter todos os tipos de mídia possíveis aos quais o fluxo dá suporte.</span><span class="sxs-lookup"><span data-stu-id="b9a58-159">The list of supported types might not contain every possible media type that the stream supports.</span></span> <span data-ttu-id="b9a58-160">Para testar se um tipo de mídia específico tem suporte, chame [**IMFMediaTypeHandler:: IsMediaTypeSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported).</span><span class="sxs-lookup"><span data-stu-id="b9a58-160">To test whether a particular media type is supported, call [**IMFMediaTypeHandler::IsMediaTypeSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported).</span></span> <span data-ttu-id="b9a58-161">Para definir o tipo de mídia, chame [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype).</span><span class="sxs-lookup"><span data-stu-id="b9a58-161">To set the media type, call [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype).</span></span> <span data-ttu-id="b9a58-162">Se o método tiver sucesso, o fluxo conterá dados que estejam de acordo com o formato especificado.</span><span class="sxs-lookup"><span data-stu-id="b9a58-162">If the method succeeds, the stream will contain data that conforms to the specified format.</span></span> <span data-ttu-id="b9a58-163">O método **SetCurrentMediaType** não altera a lista de tipos preferenciais.</span><span class="sxs-lookup"><span data-stu-id="b9a58-163">The **SetCurrentMediaType** method does not change the list of preferred types.</span></span>

<span data-ttu-id="b9a58-164">O código a seguir mostra como obter o manipulador de tipo de mídia, enumerar os tipos de mídia preferenciais e definir o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="b9a58-164">The following code shows how to get the media type handler, enumerate the preferred media types, and set the media type.</span></span> <span data-ttu-id="b9a58-165">Este exemplo pressupõe que o aplicativo tem algum algoritmo, não mostrado aqui, para selecionar o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="b9a58-165">This example assumes that the application has some algorithm, not shown here, for selecting the media type.</span></span> <span data-ttu-id="b9a58-166">As especificações dependerão muito do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b9a58-166">The specifics will depend greatly on your application.</span></span>


```C++
HRESULT hr = S_OK;
DWORD cTypes = 0;
BOOL  bTypeOK = FALSE;

IMFMediaTypeHandler *pHandler = NULL;
IMFMediaType *pMediaType = NULL;

hr = pStreamDesc->GetMediaTypeHandler(&pHandler);

if (SUCCEEDED(hr))
{
    hr = pHandler->GetMediaTypeCount(&cTypes);
}

if (SUCCEEDED(hr))
{
    for (DWORD iType = 0; iType < cTypes; iType++)
    {   
        hr = pHandler->GetMediaTypeByIndex(iType, &pMediaType);

        if (FAILED(hr))
        {
            break;
        }

        /* Examine the media type. (Not shown.)  */

        /* If this media type is acceptable, set the media type. */

        if (bTypeOK)
        {
            hr = pHandler->SetCurrentMediaType(pMediaType);
            break;
        }

        SAFE_RELEASE(pMediaType);
    }
}    

SAFE_RELEASE(pMediaType);
SAFE_RELEASE(pHandler);
```



## <a name="related-topics"></a><span data-ttu-id="b9a58-167">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b9a58-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9a58-168">Fontes de mídia</span><span class="sxs-lookup"><span data-stu-id="b9a58-168">Media Sources</span></span>](media-sources.md)
</dt> <dt>

[<span data-ttu-id="b9a58-169">APIs da plataforma Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b9a58-169">Media Foundation Platform APIs</span></span>](media-foundation-platform-apis.md)
</dt> </dl>

 

 



