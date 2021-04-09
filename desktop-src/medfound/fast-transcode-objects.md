---
description: Este tópico descreveu como usar a API de transcodificação para codificar um arquivo de mídia.
ms.assetid: 52b27359-b319-41a0-88e8-d23567420e92
title: Usando a API de transcodificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb97dd61ef75e71a82b522b65b682f861022bcf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089740"
---
# <a name="using-the-transcode-api"></a><span data-ttu-id="f1c3e-103">Usando a API de transcodificação</span><span class="sxs-lookup"><span data-stu-id="f1c3e-103">Using the Transcode API</span></span>

<span data-ttu-id="f1c3e-104">Este tópico descreveu como usar a API de transcodificação para codificar um arquivo de mídia.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-104">This topic described how to use the transcode API to encode a media file.</span></span>

-   [<span data-ttu-id="f1c3e-105">Visão geral</span><span class="sxs-lookup"><span data-stu-id="f1c3e-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="f1c3e-106">Criando uma origem de mídia</span><span class="sxs-lookup"><span data-stu-id="f1c3e-106">Creating a Media Source</span></span>](#creating-a-media-source)
-   [<span data-ttu-id="f1c3e-107">Criando um perfil transcodificar</span><span class="sxs-lookup"><span data-stu-id="f1c3e-107">Creating a Transcode Profile</span></span>](#creating-a-transcode-profile)
    -   [<span data-ttu-id="f1c3e-108">Atributos de áudio</span><span class="sxs-lookup"><span data-stu-id="f1c3e-108">Audio Attributes</span></span>](#audio-attributes)
    -   [<span data-ttu-id="f1c3e-109">Atributos de vídeo</span><span class="sxs-lookup"><span data-stu-id="f1c3e-109">Video Attributes</span></span>](#video-attributes)
    -   [<span data-ttu-id="f1c3e-110">Atributos de contêiner</span><span class="sxs-lookup"><span data-stu-id="f1c3e-110">Container Attributes</span></span>](#container-attributes)
-   [<span data-ttu-id="f1c3e-111">Criando uma topologia de transcodificação</span><span class="sxs-lookup"><span data-stu-id="f1c3e-111">Creating a Transcode Topology</span></span>](#creating-a-transcode-topology)
-   [<span data-ttu-id="f1c3e-112">Executando a sessão de codificação</span><span class="sxs-lookup"><span data-stu-id="f1c3e-112">Running the Encoding Session</span></span>](#running-the-encoding-session)
-   [<span data-ttu-id="f1c3e-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f1c3e-113">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="f1c3e-114">Visão geral</span><span class="sxs-lookup"><span data-stu-id="f1c3e-114">Overview</span></span>

<span data-ttu-id="f1c3e-115">Antes de usar a API de transcodificação, o aplicativo deve ter as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="f1c3e-115">Before using the transcode API, the application must have the following pieces of information:</span></span>

-   <span data-ttu-id="f1c3e-116">O caminho ou a URL para um arquivo de mídia existente que será codificado novamente.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-116">The path or URL to an existing media file that will be re-encoded.</span></span>
-   <span data-ttu-id="f1c3e-117">O nome do arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-117">The name of the output file.</span></span>
-   <span data-ttu-id="f1c3e-118">O tipo de contêiner para o arquivo de saída, como MP4 ou ASF (Advanced Streaming Format).</span><span class="sxs-lookup"><span data-stu-id="f1c3e-118">The container type for the output file, such as MP4 or Advanced Streaming Format (ASF).</span></span>
-   <span data-ttu-id="f1c3e-119">O formato de codificação.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-119">The encoding format.</span></span> <span data-ttu-id="f1c3e-120">Essas informações incluem os tipos de mídia que descrevem os fluxos de áudio e vídeo codificados.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-120">This information includes the media types that describe the encoded audio and video streams.</span></span>

<span data-ttu-id="f1c3e-121">Para usar a API de transcodificação, um aplicativo executa as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-121">To use the transcode API, an application performs the following steps.</span></span>

1.  <span data-ttu-id="f1c3e-122">Crie uma origem de mídia para ler o arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-122">Create a media source to read the source file.</span></span>
2.  <span data-ttu-id="f1c3e-123">Criar um perfil transcodificar.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-123">Create a transcode profile.</span></span> <span data-ttu-id="f1c3e-124">Adicione atributos que descrevem o fluxo de áudio, o fluxo de vídeo e o contêiner de arquivos.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-124">Add attributes that describe the audio stream, video stream, and file container.</span></span>
3.  <span data-ttu-id="f1c3e-125">Use o perfil transcodificar para criar uma topologia de codificação.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-125">Use the transcode profile to create an encoding topology.</span></span> <span data-ttu-id="f1c3e-126">(Para obter mais informações sobre topologias, consulte [about topologias](about-topologies.md).)</span><span class="sxs-lookup"><span data-stu-id="f1c3e-126">(For more information about topologies, see [About Topologies](about-topologies.md).)</span></span>
4.  <span data-ttu-id="f1c3e-127">Defina a topologia na [sessão de mídia](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="f1c3e-127">Set the topology on the [Media Session](media-session.md).</span></span>
5.  <span data-ttu-id="f1c3e-128">Inicie a sessão de mídia e aguarde o evento [MESessionEnded](mesessionended.md) .</span><span class="sxs-lookup"><span data-stu-id="f1c3e-128">Start the Media Session and wait for the [MESessionEnded](mesessionended.md) event.</span></span>

<span data-ttu-id="f1c3e-129">O restante deste tópico descreve essas etapas mais detalhadamente.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-129">The remainder of this topic describes these steps in more detail.</span></span>

## <a name="creating-a-media-source"></a><span data-ttu-id="f1c3e-130">Criando uma origem de mídia</span><span class="sxs-lookup"><span data-stu-id="f1c3e-130">Creating a Media Source</span></span>

<span data-ttu-id="f1c3e-131">Uma origem de mídia é um objeto que lê e analisa o arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-131">A media source is an object that reads and parses the source file.</span></span> <span data-ttu-id="f1c3e-132">Para criar uma fonte de mídia, use o [resolvedor de origem](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="f1c3e-132">To create a media source, use the [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="f1c3e-133">Você pode encontrar um código de exemplo no tópico [usando o resolvedor de origem](using-the-source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="f1c3e-133">You can find example code in the topic [Using the Source Resolver](using-the-source-resolver.md).</span></span>

## <a name="creating-a-transcode-profile"></a><span data-ttu-id="f1c3e-134">Criando um perfil transcodificar</span><span class="sxs-lookup"><span data-stu-id="f1c3e-134">Creating a Transcode Profile</span></span>

<span data-ttu-id="f1c3e-135">Um *perfil transcodificar* descreve o formato e as configurações que são usadas para codificar o arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-135">A *transcode profile* describes the format and settings that are used to encode the output file.</span></span> <span data-ttu-id="f1c3e-136">O perfil transcodificar contém três conjuntos de atributos:</span><span class="sxs-lookup"><span data-stu-id="f1c3e-136">The transcode profile contains three sets of attributes:</span></span>

-   <span data-ttu-id="f1c3e-137">Atributos de áudio: Descreva as configurações de formato de áudio de destino e codificador de áudio.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-137">Audio attributes: Describe the target audio format and audio encoder settings.</span></span>
-   <span data-ttu-id="f1c3e-138">Atributos de vídeo: Descreva as configurações de formato de vídeo de destino e codificador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-138">Video attributes: Describe the target video format and video encoder settings.</span></span>
-   <span data-ttu-id="f1c3e-139">Atributos de contêiner: defina o tipo de contêiner de arquivo, bem como algumas configurações de codificação globais.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-139">Container attributes: Define the type of file container, as well as some global encoding settings.</span></span>

<span data-ttu-id="f1c3e-140">Para criar um perfil de transcodificação, chame a função [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) .</span><span class="sxs-lookup"><span data-stu-id="f1c3e-140">To create a transcode profile, call the [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) function.</span></span> <span data-ttu-id="f1c3e-141">Essa função retorna um ponteiro para a interface [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) .</span><span class="sxs-lookup"><span data-stu-id="f1c3e-141">This function returns a pointer to the [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) interface.</span></span> <span data-ttu-id="f1c3e-142">O objeto de perfil inicial está vazio; Ele não contém nenhum atributo.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-142">The initial profile object is empty; it contains no attributes.</span></span> <span data-ttu-id="f1c3e-143">A próxima etapa é adicionar os atributos que definem o perfil.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-143">The next step is to add the attributes that define the profile.</span></span>

### <a name="audio-attributes"></a><span data-ttu-id="f1c3e-144">Atributos de áudio</span><span class="sxs-lookup"><span data-stu-id="f1c3e-144">Audio Attributes</span></span>

<span data-ttu-id="f1c3e-145">Para adicionar atributos para o fluxo de áudio, chame [**IMFTranscodeProfile:: Setaudioattributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes).</span><span class="sxs-lookup"><span data-stu-id="f1c3e-145">To add attributes for the audio stream, call [**IMFTranscodeProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes).</span></span> <span data-ttu-id="f1c3e-146">Esses atributos especificam como o fluxo de áudio é codificado.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-146">These attributes specify how the audio stream is encoded.</span></span> <span data-ttu-id="f1c3e-147">Se o arquivo de saída não contiver um fluxo de áudio, omita esses atributos.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-147">If the output file will not contain an audio stream, omit these attributes.</span></span>

<span data-ttu-id="f1c3e-148">Os atributos de áudio se enquadram em duas categorias:</span><span class="sxs-lookup"><span data-stu-id="f1c3e-148">Audio attributes fall into two categories:</span></span>

-   <span data-ttu-id="f1c3e-149">Atributos que especificam o formato do fluxo codificado</span><span class="sxs-lookup"><span data-stu-id="f1c3e-149">Attributes that specify the format of the encoded stream</span></span>
-   <span data-ttu-id="f1c3e-150">Atributos que especificam outros parâmetros de codificação.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-150">Attributes that specify other encoding parameters.</span></span>

<span data-ttu-id="f1c3e-151">Os atributos de formato são simplesmente atributos de tipo de mídia, conforme descrito na seção [tipos de mídia de áudio](audio-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="f1c3e-151">Format attributes are simply media-type attributes, as described in the section [Audio Media Types](audio-media-types.md).</span></span> <span data-ttu-id="f1c3e-152">O conjunto exato de atributos de formato depende do codificador.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-152">The exact set of format attributes depends on the encoder.</span></span> <span data-ttu-id="f1c3e-153">(Consulte [formatos de mídia com suporte no Media Foundation](supported-media-formats-in-media-foundation.md).) Aqui está uma lista de atributos típicos de formato de áudio:</span><span class="sxs-lookup"><span data-stu-id="f1c3e-153">(See [Supported Media Formats in Media Foundation](supported-media-formats-in-media-foundation.md).) Here is a list of typical audio format attributes:</span></span>



| <span data-ttu-id="f1c3e-154">Atributo de formato</span><span class="sxs-lookup"><span data-stu-id="f1c3e-154">Format Attribute</span></span>                                                                         | <span data-ttu-id="f1c3e-155">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1c3e-155">Description</span></span>                                                      |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="f1c3e-156">subtipo MF \_ MT \_</span><span class="sxs-lookup"><span data-stu-id="f1c3e-156">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="f1c3e-157">O subtipo.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-157">The subtype.</span></span> <span data-ttu-id="f1c3e-158">Consulte [GUIDs de subtipo de áudio](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="f1c3e-158">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span> |
| [<span data-ttu-id="f1c3e-159">\_canais de \_ número de áudio MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="f1c3e-159">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="f1c3e-160">O número de canais de áudio.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-160">The number of audio channels.</span></span>                                    |
| [<span data-ttu-id="f1c3e-161">\_amostras de áudio MF MT \_ \_ \_ por \_ segundo</span><span class="sxs-lookup"><span data-stu-id="f1c3e-161">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="f1c3e-162">O número de amostras de áudio por segundo.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-162">The number of audio samples per second.</span></span>                          |
| [<span data-ttu-id="f1c3e-163">\_alinhamento de \_ bloco de áudio MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="f1c3e-163">MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="f1c3e-164">O alinhamento do bloco.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-164">The block alignment.</span></span>                                             |
| [<span data-ttu-id="f1c3e-165">áudio do MF \_ MT \_ média de \_ \_ bytes \_ por \_ segundo</span><span class="sxs-lookup"><span data-stu-id="f1c3e-165">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="f1c3e-166">O número médio de bytes por segundo (a taxa de bits codificada).</span><span class="sxs-lookup"><span data-stu-id="f1c3e-166">The average number of bytes per second (the encoded bit rate).</span></span>   |



 

<span data-ttu-id="f1c3e-167">Os parâmetros de codificação a seguir são definidos.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-167">The following encoding parameters are defined.</span></span>



| <span data-ttu-id="f1c3e-168">Parâmetro de codificação</span><span class="sxs-lookup"><span data-stu-id="f1c3e-168">Encoding Parameter</span></span>                                                             | <span data-ttu-id="f1c3e-169">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1c3e-169">Description</span></span>                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="f1c3e-170">\_ \_ \_ codificador de inserção do MF transcodificar não cercamento \_</span><span class="sxs-lookup"><span data-stu-id="f1c3e-170">MF\_TRANSCODE\_DONOT\_INSERT\_ENCODER</span></span>](mf-transcode-donot-insert-encoder.md) | <span data-ttu-id="f1c3e-171">Impede que a API de transcodificação Insira um codificador para o fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-171">Prevents the transcode API from inserting an encoder for the audio stream.</span></span> |
| [<span data-ttu-id="f1c3e-172">\_ENCODINGPROFILE de transcodificação MF \_</span><span class="sxs-lookup"><span data-stu-id="f1c3e-172">MF\_TRANSCODE\_ENCODINGPROFILE</span></span>](mf-transcode-encodingprofile.md)             | <span data-ttu-id="f1c3e-173">Especifica o modelo de conformidade do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-173">Specifies the device conformance template.</span></span> <span data-ttu-id="f1c3e-174">(Aplica-se somente a arquivos ASF.)</span><span class="sxs-lookup"><span data-stu-id="f1c3e-174">(Applies only to ASF files.)</span></span>    |
| [<span data-ttu-id="f1c3e-175">\_QUALITYVSSPEED de transcodificação MF \_</span><span class="sxs-lookup"><span data-stu-id="f1c3e-175">MF\_TRANSCODE\_QUALITYVSSPEED</span></span>](mf-transcode-qualityvsspeed.md)               | <span data-ttu-id="f1c3e-176">Especifica a compensação entre a qualidade de codificação e a velocidade.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-176">Specifies the trade-off between encoding quality and speed.</span></span>                |



 

<span data-ttu-id="f1c3e-177">Você deve definir os atributos de formato.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-177">You must set the format attributes.</span></span> <span data-ttu-id="f1c3e-178">Os parâmetros de codificação são opcionais.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-178">The encoding parameters are optional.</span></span>

<span data-ttu-id="f1c3e-179">Uma maneira de encontrar um formato compatível com o codificador é chamar a função [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) .</span><span class="sxs-lookup"><span data-stu-id="f1c3e-179">One way to find a format that is compatible with the encoder is to call the [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) function.</span></span> <span data-ttu-id="f1c3e-180">O codificador desejado é especificado por subtipo.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-180">The desired encoder is specified by subtype.</span></span> <span data-ttu-id="f1c3e-181">A função retorna uma coleção de tipos de mídia para esse codificador.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-181">The function returns a collection of media types for that encoder.</span></span> <span data-ttu-id="f1c3e-182">Você pode selecionar um tipo na lista e copiar os atributos para o perfil.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-182">You can select a type from the list and copy the attributes to the profile.</span></span> <span data-ttu-id="f1c3e-183">Para obter um exemplo de código que usa essa abordagem, consulte [tutorial: codificando um arquivo WMA](tutorial--converting-an-mp3-file-to-a-wma-file.md).</span><span class="sxs-lookup"><span data-stu-id="f1c3e-183">For example code that uses this approach, see [Tutorial: Encoding a WMA File](tutorial--converting-an-mp3-file-to-a-wma-file.md).</span></span>

### <a name="video-attributes"></a><span data-ttu-id="f1c3e-184">Atributos de vídeo</span><span class="sxs-lookup"><span data-stu-id="f1c3e-184">Video Attributes</span></span>

<span data-ttu-id="f1c3e-185">Para adicionar atributos para o fluxo de vídeo, chame [**IMFTranscodeProfile:: Setvideoattributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes).</span><span class="sxs-lookup"><span data-stu-id="f1c3e-185">To add attributes for the video stream, call [**IMFTranscodeProfile::SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes).</span></span> <span data-ttu-id="f1c3e-186">Esses atributos especificam como o fluxo de vídeo é codificado.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-186">These attributes specify how the video stream is encoded.</span></span> <span data-ttu-id="f1c3e-187">Se o arquivo de saída não contiver um fluxo de vídeo, omita esses atributos.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-187">If the output file will not contain a video stream, omit these attributes.</span></span>

<span data-ttu-id="f1c3e-188">Assim como acontece com os atributos de áudio, os atributos de vídeo se enquadram em duas categorias:</span><span class="sxs-lookup"><span data-stu-id="f1c3e-188">As with audio attributes, the video attributes fall into two categories:</span></span>

-   <span data-ttu-id="f1c3e-189">Atributos que especificam o formato do fluxo codificado</span><span class="sxs-lookup"><span data-stu-id="f1c3e-189">Attributes that specify the format of the encoded stream</span></span>
-   <span data-ttu-id="f1c3e-190">Atributos que especificam outros parâmetros de codificação.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-190">Attributes that specify other encoding parameters.</span></span>

<span data-ttu-id="f1c3e-191">Os atributos de formato são atributos de tipo de mídia, conforme descrito na seção [tipos de mídia de vídeo](video-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="f1c3e-191">Format attributes are media-type attributes, as described in the section [Video Media Types](video-media-types.md).</span></span> <span data-ttu-id="f1c3e-192">Aqui está uma lista de atributos típicos de formato de vídeo:</span><span class="sxs-lookup"><span data-stu-id="f1c3e-192">Here is a list of typical video format attributes:</span></span>



| <span data-ttu-id="f1c3e-193">Atributo de formato</span><span class="sxs-lookup"><span data-stu-id="f1c3e-193">Format Attribute</span></span>                                                       | <span data-ttu-id="f1c3e-194">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1c3e-194">Description</span></span>                                                      |
|------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="f1c3e-195">subtipo MF \_ MT \_</span><span class="sxs-lookup"><span data-stu-id="f1c3e-195">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                         | <span data-ttu-id="f1c3e-196">O subtipo.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-196">The subtype.</span></span> <span data-ttu-id="f1c3e-197">Consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="f1c3e-197">See [Video Subtype GUIDs](video-subtype-guids.md).</span></span> |
| [<span data-ttu-id="f1c3e-198">\_taxa de \_ quadros MF MT \_</span><span class="sxs-lookup"><span data-stu-id="f1c3e-198">MF\_MT\_FRAME\_RATE</span></span>](mf-mt-frame-rate-attribute.md)                  | <span data-ttu-id="f1c3e-199">A taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-199">The frame rate.</span></span>                                                  |
| [<span data-ttu-id="f1c3e-200">\_tamanho do \_ quadro MF MT \_</span><span class="sxs-lookup"><span data-stu-id="f1c3e-200">MF\_MT\_FRAME\_SIZE</span></span>](mf-mt-frame-size-attribute.md)                  | <span data-ttu-id="f1c3e-201">O tamanho do quadro.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-201">The frame size.</span></span>                                                  |
| [<span data-ttu-id="f1c3e-202">**\_taxa de \_ \_ bits média de MF MT**</span><span class="sxs-lookup"><span data-stu-id="f1c3e-202">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)            | <span data-ttu-id="f1c3e-203">A taxa média de bits.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-203">The average bit rate.</span></span>                                            |
| [<span data-ttu-id="f1c3e-204">taxa de proporção de pixel do MF \_ MT \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="f1c3e-204">MF\_MT\_PIXEL\_ASPECT\_RATIO</span></span>](mf-mt-pixel-aspect-ratio-attribute.md) | <span data-ttu-id="f1c3e-205">A taxa de proporção de pixel.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-205">The pixel aspect ratio.</span></span>                                          |



 

<span data-ttu-id="f1c3e-206">Os parâmetros de codificação a seguir são definidos.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-206">The following encoding parameters are defined.</span></span>



| <span data-ttu-id="f1c3e-207">Parâmetro de codificação</span><span class="sxs-lookup"><span data-stu-id="f1c3e-207">Encoding Parameter</span></span>                                                             | <span data-ttu-id="f1c3e-208">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1c3e-208">Description</span></span>                                                                |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="f1c3e-209">\_ \_ \_ codificador de inserção do MF transcodificar não cercamento \_</span><span class="sxs-lookup"><span data-stu-id="f1c3e-209">MF\_TRANSCODE\_DONOT\_INSERT\_ENCODER</span></span>](mf-transcode-donot-insert-encoder.md) | <span data-ttu-id="f1c3e-210">Impede que a API de transcodificação Insira um codificador para o fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-210">Prevents the transcode API from inserting an encoder for the video stream.</span></span> |
| [<span data-ttu-id="f1c3e-211">\_ENCODINGPROFILE de transcodificação MF \_</span><span class="sxs-lookup"><span data-stu-id="f1c3e-211">MF\_TRANSCODE\_ENCODINGPROFILE</span></span>](mf-transcode-encodingprofile.md)             | <span data-ttu-id="f1c3e-212">Especifica o modelo de conformidade do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-212">Specifies the device conformance template.</span></span> <span data-ttu-id="f1c3e-213">(Aplica-se somente a arquivos ASF.)</span><span class="sxs-lookup"><span data-stu-id="f1c3e-213">(Applies only to ASF files.)</span></span>    |
| [<span data-ttu-id="f1c3e-214">\_QUALITYVSSPEED de transcodificação MF \_</span><span class="sxs-lookup"><span data-stu-id="f1c3e-214">MF\_TRANSCODE\_QUALITYVSSPEED</span></span>](mf-transcode-qualityvsspeed.md)               | <span data-ttu-id="f1c3e-215">Especifica a compensação entre a qualidade de codificação e a velocidade.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-215">Specifies the trade-off between encoding quality and speed.</span></span>                |



 

<span data-ttu-id="f1c3e-216">Você deve definir os atributos de formato.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-216">You must set the format attributes.</span></span> <span data-ttu-id="f1c3e-217">Os parâmetros de codificação são opcionais.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-217">The encoding parameters are optional.</span></span>

### <a name="container-attributes"></a><span data-ttu-id="f1c3e-218">Atributos de contêiner</span><span class="sxs-lookup"><span data-stu-id="f1c3e-218">Container Attributes</span></span>

<span data-ttu-id="f1c3e-219">Os atributos de contêiner definem as características de nível de arquivo do arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-219">Container attributes define file-level characteristics of the output file.</span></span> <span data-ttu-id="f1c3e-220">Para definir atributos de contêiner, chame [**IMFTranscodeProfile:: Setcontêinerattributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).</span><span class="sxs-lookup"><span data-stu-id="f1c3e-220">To set container attributes, call [**IMFTranscodeProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes).</span></span> <span data-ttu-id="f1c3e-221">Os atributos a seguir são definidos.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-221">The following attributes are defined.</span></span>



| <span data-ttu-id="f1c3e-222">Atributo</span><span class="sxs-lookup"><span data-stu-id="f1c3e-222">Attribute</span></span>                                                                          | <span data-ttu-id="f1c3e-223">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1c3e-223">Description</span></span>                                                                                                                                            |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f1c3e-224">\_perfil de ajuste de transcodificação MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="f1c3e-224">MF\_TRANSCODE\_ADJUST\_PROFILE</span></span>](mf-transcode-adjust-profile.md)                  | <span data-ttu-id="f1c3e-225">Define as configurações de fluxo a serem usadas para a topologia de transcodificação.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-225">Defines the stream settings to use for the transcode topology.</span></span> <span data-ttu-id="f1c3e-226">Você pode definir os sinalizadores para usar as configurações de fonte de entrada ou usar atributos de fluxo personalizados.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-226">You can set the flags to use the input source settings or use custom stream attributes.</span></span> |
| [<span data-ttu-id="f1c3e-227">\_contêinertype de transcodificação MF \_</span><span class="sxs-lookup"><span data-stu-id="f1c3e-227">MF\_TRANSCODE\_CONTAINERTYPE</span></span>](mf-transcode-containertype.md)                     | <span data-ttu-id="f1c3e-228">Especifica o formato de arquivo do arquivo de saída, como MP4 ou ASF.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-228">Specifies the file format of the output file, such as MP4 or ASF.</span></span> <span data-ttu-id="f1c3e-229">Com base nesse valor, o coletor de mídia apropriado é adicionado à topologia.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-229">Based on this value, the appropriate media sink is added to the topology.</span></span>            |
| [<span data-ttu-id="f1c3e-230">\_transferência de \_ \_ metadados ignorar a transcodificação MF \_</span><span class="sxs-lookup"><span data-stu-id="f1c3e-230">MF\_TRANSCODE\_SKIP\_METADATA\_TRANSFER</span></span>](mf-transcode-skip-metadata-transfer.md) | <span data-ttu-id="f1c3e-231">Especifica se os metadados da origem são copiados para o arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-231">Specifies whether metadata from the source is copied to the output file.</span></span>                                                                               |
| [<span data-ttu-id="f1c3e-232">\_topologymode de transcodificação MF \_</span><span class="sxs-lookup"><span data-stu-id="f1c3e-232">MF\_TRANSCODE\_TOPOLOGYMODE</span></span>](mf-transcode-topologymode.md)                       | <span data-ttu-id="f1c3e-233">Especifica se os codecs baseados em hardware podem ser usados durante a transcodificação.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-233">Specifies whether hardware-based codecs may be used during transcoding.</span></span>                                                                                |
| [<span data-ttu-id="f1c3e-234">\_Atributo de \_ desbloqueio de FIELDOFUSE MFT \_</span><span class="sxs-lookup"><span data-stu-id="f1c3e-234">MFT\_FIELDOFUSE\_UNLOCK\_Attribute</span></span>](mft-fieldofuse-unlock-attribute.md)          | <span data-ttu-id="f1c3e-235">Desbloqueia um codec que tem restrições de campo de uso.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-235">Unlocks a codec that has field-of-use restrictions.</span></span> <span data-ttu-id="f1c3e-236">Para obter mais informações, consulte [campo de restrições de uso](field-of-use-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="f1c3e-236">For more information, see [Field of Use Restrictions](field-of-use-restrictions.md).</span></span>              |



 

<span data-ttu-id="f1c3e-237">O [atributo \_ \_ ContainerType de transcodificação MF](mf-transcode-containertype.md) é necessário.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-237">The [MF\_TRANSCODE\_CONTAINERTYPE](mf-transcode-containertype.md) attribute is required.</span></span> <span data-ttu-id="f1c3e-238">Os outros atributos de contêiner são opcionais.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-238">The other container attributes are optional.</span></span>

## <a name="creating-a-transcode-topology"></a><span data-ttu-id="f1c3e-239">Criando uma topologia de transcodificação</span><span class="sxs-lookup"><span data-stu-id="f1c3e-239">Creating a Transcode Topology</span></span>

<span data-ttu-id="f1c3e-240">A topologia de transcodificação é uma topologia parcial que contém a origem da mídia, os codecs apropriados e o coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-240">The transcode topology is a partial topology that contains the media source, the appropriate codecs, and the media sink.</span></span> <span data-ttu-id="f1c3e-241">Para criar a topologia de transcodificação, chame para a função [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) .</span><span class="sxs-lookup"><span data-stu-id="f1c3e-241">To create the transcode topology, call to the [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) function.</span></span> <span data-ttu-id="f1c3e-242">Essa função usa os seguintes parâmetros como entrada:</span><span class="sxs-lookup"><span data-stu-id="f1c3e-242">This function takes the following parameters as input:</span></span>

-   <span data-ttu-id="f1c3e-243">Um ponteiro para a interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) da fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-243">A pointer to the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) interface of the media source.</span></span>
-   <span data-ttu-id="f1c3e-244">O nome do arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-244">The name of the output file.</span></span>
-   <span data-ttu-id="f1c3e-245">Um ponteiro para a interface [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) do perfil transcodificar.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-245">A pointer to the [**IMFTranscodeProfile**](/windows/desktop/api/mfidl/nn-mfidl-imftranscodeprofile) interface of the transcode profile.</span></span>

<span data-ttu-id="f1c3e-246">A função retorna um ponteiro para a interface [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) .</span><span class="sxs-lookup"><span data-stu-id="f1c3e-246">The function returns a pointer to the [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface.</span></span>

## <a name="running-the-encoding-session"></a><span data-ttu-id="f1c3e-247">Executando a sessão de codificação</span><span class="sxs-lookup"><span data-stu-id="f1c3e-247">Running the Encoding Session</span></span>

<span data-ttu-id="f1c3e-248">Depois de criar a topologia, você estará pronto para codificar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-248">After you create the topology, you are ready to encode the file.</span></span> <span data-ttu-id="f1c3e-249">Você pode descartar o perfil neste momento.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-249">You can discard the profile at this point.</span></span>

1.  <span data-ttu-id="f1c3e-250">Chame [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) para criar a sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-250">Call [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create the Media Session.</span></span>
2.  <span data-ttu-id="f1c3e-251">Chame [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) para definir a topologia na sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-251">Call [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) to set the topology on the Media Session.</span></span>
3.  <span data-ttu-id="f1c3e-252">Chame [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) para iniciar a sessão de codificação.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-252">Call [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) to start the encoding session.</span></span>
4.  <span data-ttu-id="f1c3e-253">Aguarde o evento [MESessionEnded](mesessionended.md) .</span><span class="sxs-lookup"><span data-stu-id="f1c3e-253">Wait for the [MESessionEnded](mesessionended.md) event.</span></span>
5.  <span data-ttu-id="f1c3e-254">Chame [**IMFMediaSession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) para fechar a sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-254">Call [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) to close the Media Session.</span></span>
6.  <span data-ttu-id="f1c3e-255">Aguarde o evento [MESessionClosed](mesessionclosed.md) .</span><span class="sxs-lookup"><span data-stu-id="f1c3e-255">Wait for the [MESessionClosed](mesessionclosed.md) event.</span></span>
7.  <span data-ttu-id="f1c3e-256">Chame [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span><span class="sxs-lookup"><span data-stu-id="f1c3e-256">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span></span>
8.  <span data-ttu-id="f1c3e-257">Chame [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span><span class="sxs-lookup"><span data-stu-id="f1c3e-257">Call [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span>

<span data-ttu-id="f1c3e-258">A maior parte do tempo gasto na codificação ocorre entre as etapas 3 e 4.</span><span class="sxs-lookup"><span data-stu-id="f1c3e-258">Most of the time spent encoding occurs between steps 3 and 4.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1c3e-259">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f1c3e-259">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1c3e-260">API de transcodificação</span><span class="sxs-lookup"><span data-stu-id="f1c3e-260">Transcode API</span></span>](transcode-api.md)
</dt> <dt>

[<span data-ttu-id="f1c3e-261">Sobre a sessão de mídia</span><span class="sxs-lookup"><span data-stu-id="f1c3e-261">About the Media Session</span></span>](about-the-media-session.md)
</dt> </dl>

 

 



