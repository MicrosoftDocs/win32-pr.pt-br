---
description: A codificação refere-se ao processo de conversão de mídia digital de um formato para outro. Por exemplo, converter áudio MP3 no formato de áudio do Windows Media, conforme definido pela especificação ASF (Advanced Systems Format).
ms.assetid: 4fe202d8-c8f5-4e9a-ad40-1aea8f767362
title: 'Tutorial: 1-transmitir codificação de mídia do Windows'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d670b107f315966a048a2f847183431f9a57bd4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103663809"
---
# <a name="tutorial-1-pass-windows-media-encoding"></a><span data-ttu-id="22284-104">Tutorial: 1-transmitir codificação de mídia do Windows</span><span class="sxs-lookup"><span data-stu-id="22284-104">Tutorial: 1-Pass Windows Media Encoding</span></span>

<span data-ttu-id="22284-105">A codificação refere-se ao processo de conversão de mídia digital de um formato para outro.</span><span class="sxs-lookup"><span data-stu-id="22284-105">Encoding refers to the process of converting digital media from one format into another.</span></span> <span data-ttu-id="22284-106">Por exemplo, converter áudio MP3 no formato de áudio do Windows Media, conforme definido pela especificação ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="22284-106">For example, converting MP3 audio into Windows Media Audio format as defined by the Advanced Systems Format (ASF) specification.</span></span>

<span data-ttu-id="22284-107">**Observação**  A especificação de ASF define um tipo de contêiner para o arquivo de saída (. WMA ou. wmv) que pode conter dados de mídia em qualquer formato, compactado ou descompactado.</span><span class="sxs-lookup"><span data-stu-id="22284-107">**Note**  The ASF specification defines a container type for the output file (.wma or .wmv) that can contain media data in any format, compressed or uncompressed.</span></span> <span data-ttu-id="22284-108">Por exemplo, um contêiner ASF, como um arquivo. WMA, pode conter dados de mídia no formato MP3.</span><span class="sxs-lookup"><span data-stu-id="22284-108">For example, an ASF container such as a .wma file can contain media data in MP3 format.</span></span> <span data-ttu-id="22284-109">O processo de codificação converte o formato real dos dados contidos no arquivo.</span><span class="sxs-lookup"><span data-stu-id="22284-109">The encoding process converts the actual format of the data contained within the file.</span></span>

<span data-ttu-id="22284-110">Este tutorial demonstra a fonte de entrada codificar conteúdo claro (não protegido por DRM) no conteúdo do Windows Media e gravar os dados em um novo arquivo ASF (. WM \* ) usando componentes ASF da camada de pipeline.</span><span class="sxs-lookup"><span data-stu-id="22284-110">This tutorial demonstrates encoding clear content (non DRM-protected) input source into Windows Media content and writing the data in a new ASF file (.wm\*) by using Pipeline Layer ASF Components.</span></span> <span data-ttu-id="22284-111">Esses componentes serão usados para criar uma topologia de codificação parcial, que será controlada por uma instância da sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="22284-111">These components will be used to build a partial encoding topology, which will be controlled by an instance of the Media Session.</span></span>

<span data-ttu-id="22284-112">Neste tutorial, você criará um aplicativo de console que usa os nomes de dados de entrada e saída e o modo de codificação como argumentos.</span><span class="sxs-lookup"><span data-stu-id="22284-112">In this tutorial, you will create a console application that takes the input and output filenames, and the encoding mode as arguments.</span></span> <span data-ttu-id="22284-113">O arquivo de entrada pode estar em um formato de mídia compactado ou não compactado.</span><span class="sxs-lookup"><span data-stu-id="22284-113">The input file can be in a compressed or an uncompressed media format.</span></span> <span data-ttu-id="22284-114">Os modos de codificação válidos são "CBR" (taxa de bits constante) ou "VBR" (taxa de bits variável).</span><span class="sxs-lookup"><span data-stu-id="22284-114">The valid encoding modes are "CBR" (constant bit rate) or "VBR" (variable bit rate).</span></span> <span data-ttu-id="22284-115">O aplicativo cria uma origem de mídia para representar a origem especificada pelo nome de arquivo de entrada e o coletor de arquivos ASF para arquivar o conteúdo codificado do arquivo de origem em um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="22284-115">The application creates a media source to represent the source specified by the input filename, and the ASF file sink to archive the encoded contents of source file into an ASF file.</span></span> <span data-ttu-id="22284-116">Para manter o cenário simples de implementar, o arquivo de saída terá apenas um fluxo de áudio e um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="22284-116">To keep the scenario simple to implement, the output file will have only one audio stream and one video stream.</span></span> <span data-ttu-id="22284-117">O aplicativo insere o codec Windows Media Audio 9,1 Professional para a conversão de formato de fluxo de áudio e o codec do Windows Media Video 9 para o fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="22284-117">The application inserts the Windows Media Audio 9.1 Professional codec for the audio stream format conversion and Windows Media Video 9 codec for the video stream.</span></span>

<span data-ttu-id="22284-118">Para a codificação de taxa de bits constante, antes do início da sessão de codificação, o codificador deve saber a taxa de bits de destino que ela deve atingir.</span><span class="sxs-lookup"><span data-stu-id="22284-118">For constant bit rate encoding, before the encoding session begins, the encoder must know the target bit rate that it must achieve.</span></span> <span data-ttu-id="22284-119">Neste tutorial, para o modo "CBR", o aplicativo usa a taxa de bits disponível com o primeiro tipo de mídia de saída que é recuperado do codificador durante a negociação do tipo de mídia como a taxa de bits de destino.</span><span class="sxs-lookup"><span data-stu-id="22284-119">In this tutorial, for "CBR" mode, the application uses the bit rate available with the first output media type that is retrieved from the encoder during media type negotiation as the target bit rate.</span></span> <span data-ttu-id="22284-120">Para a codificação de taxa de bits variável, este tutorial demonstra a codificação com a taxa de bits variável, definindo um nível de qualidade.</span><span class="sxs-lookup"><span data-stu-id="22284-120">For variable bit rate encoding, this tutorial demonstrates encoding with variable bit rate by setting a quality level.</span></span> <span data-ttu-id="22284-121">Os fluxos de áudio são codificados no nível de qualidade de 98 e fluxos de vídeo no nível de qualidade de 95.</span><span class="sxs-lookup"><span data-stu-id="22284-121">The audio streams are encoded at the quality level of 98 and video streams at the quality level of 95.</span></span>

<span data-ttu-id="22284-122">O procedimento a seguir resume as etapas para codificar o conteúdo do Windows Media em um contêiner ASF usando um modo de codificação de 1 passagem.</span><span class="sxs-lookup"><span data-stu-id="22284-122">The following procedure summarizes the steps for encoding Windows Media content in an ASF container by using a 1-pass encoding mode.</span></span>

1.  <span data-ttu-id="22284-123">Crie uma origem de mídia para o especificado usando o resolvedor de origem.</span><span class="sxs-lookup"><span data-stu-id="22284-123">Create a media source for the specified by using the source resolver.</span></span>
2.  <span data-ttu-id="22284-124">Enumere os fluxos na origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="22284-124">Enumerate the streams in the media source.</span></span>
3.  <span data-ttu-id="22284-125">Crie o coletor de mídia ASF e adicione coletores de fluxo dependendo dos fluxos na origem de mídia que precisam ser codificados.</span><span class="sxs-lookup"><span data-stu-id="22284-125">Create the ASF media sink and add stream sinks depending on the streams in the media source that need to be encoded.</span></span>
4.  <span data-ttu-id="22284-126">Configure o coletor de mídia com as propriedades de codificação necessárias.</span><span class="sxs-lookup"><span data-stu-id="22284-126">Configure the media sink with the required encoding properties.</span></span>
5.  <span data-ttu-id="22284-127">Crie os codificadores de mídia do Windows para os fluxos no arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="22284-127">Create the Windows Media encoders for the streams in the output file.</span></span>
6.  <span data-ttu-id="22284-128">Configure os codificadores com as propriedades definidas no coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="22284-128">Configure the encoders with the properties that are set on the media sink.</span></span>
7.  <span data-ttu-id="22284-129">Crie uma topologia de codificação parcial.</span><span class="sxs-lookup"><span data-stu-id="22284-129">Build a partial encoding topology.</span></span>
8.  <span data-ttu-id="22284-130">Crie uma instância da sessão de mídia e defina a topologia na sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="22284-130">Instantiate the Media Session and set the topology on the Media Session.</span></span>
9.  <span data-ttu-id="22284-131">Inicie a sessão de codificação controlando a sessão de mídia e obtendo todos os eventos relevantes da sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="22284-131">Start the encoding session by controlling the Media Session and getting all the relevant events from the Media Session.</span></span>
10. <span data-ttu-id="22284-132">Para a codificação de VBR, obtenha os valores de propriedade de codificação do codificador e defina-os no coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="22284-132">For VBR encoding, get the encoding property values from the encoder and set them on the media sink.</span></span>
11. <span data-ttu-id="22284-133">Feche e desligue a sessão de codificação.</span><span class="sxs-lookup"><span data-stu-id="22284-133">Close and shutdown the encoding session.</span></span>

<span data-ttu-id="22284-134">Este tutorial contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="22284-134">This tutorial contains the following sections:</span></span>

-   [<span data-ttu-id="22284-135">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="22284-135">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="22284-136">Configurar o projeto</span><span class="sxs-lookup"><span data-stu-id="22284-136">Set up the Project</span></span>](#set-up-the-project)
-   [<span data-ttu-id="22284-137">Criar a origem da mídia</span><span class="sxs-lookup"><span data-stu-id="22284-137">Create the Media Source</span></span>](#create-the-media-source)
-   [<span data-ttu-id="22284-138">Criar o coletor de arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="22284-138">Create the ASF File Sink</span></span>](#create-the-asf-file-sink)
    -   [<span data-ttu-id="22284-139">Criar o objeto de perfil ASF</span><span class="sxs-lookup"><span data-stu-id="22284-139">Create the ASF Profile Object</span></span>](#create-the-asf-profile-object)
    -   [<span data-ttu-id="22284-140">Criar um tipo de mídia de áudio compactado</span><span class="sxs-lookup"><span data-stu-id="22284-140">Create a Compressed Audio Media Type</span></span>](#create-a-compressed-audio-media-type)
    -   [<span data-ttu-id="22284-141">Criar um tipo de mídia de vídeo compactado</span><span class="sxs-lookup"><span data-stu-id="22284-141">Create a Compressed Video Media Type</span></span>](#create-a-compressed-video-media-type)
    -   [<span data-ttu-id="22284-142">Criar o objeto ContentInfo do ASF</span><span class="sxs-lookup"><span data-stu-id="22284-142">Create the ASF ContentInfo Object</span></span>](#create-the-asf-contentinfo-object)
    -   [<span data-ttu-id="22284-143">Criar o coletor de arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="22284-143">Create the ASF File Sink</span></span>](#create-the-asf-file-sink)
-   [<span data-ttu-id="22284-144">Criar a topologia de codificação parcial</span><span class="sxs-lookup"><span data-stu-id="22284-144">Build the Partial Encoding Topology</span></span>](#build-the-partial-encoding-topology)
    -   [<span data-ttu-id="22284-145">Criar o nó de topologia de origem para a origem de mídia</span><span class="sxs-lookup"><span data-stu-id="22284-145">Create the Source Topology Node for the Media Source</span></span>](#create-the-source-topology-node-for-the-media-source)
    -   [<span data-ttu-id="22284-146">Instanciar os codificadores necessários e criar os nós de transformação</span><span class="sxs-lookup"><span data-stu-id="22284-146">Instantiate the Required Encoders and Create the Transform Nodes</span></span>](#instantiate-the-required-encoders-and-create-the-transform-nodes)
    -   [<span data-ttu-id="22284-147">Criar os nós de topologia de saída para o coletor de arquivos</span><span class="sxs-lookup"><span data-stu-id="22284-147">Create the Output Topology Nodes for the File Sink</span></span>](#create-the-output-topology-nodes-for-the-file-sink)
    -   [<span data-ttu-id="22284-148">Conectar os nós de origem, transformação e coletor</span><span class="sxs-lookup"><span data-stu-id="22284-148">Connect the Source, Transform, and Sink Nodes</span></span>](#connect-the-source-transform-and-sink-nodes)
-   [<span data-ttu-id="22284-149">Manipulando a sessão de codificação</span><span class="sxs-lookup"><span data-stu-id="22284-149">Handling the Encoding Session</span></span>](#handling-the-encoding-session)
-   [<span data-ttu-id="22284-150">Atualizar propriedades de codificação no coletor de arquivos</span><span class="sxs-lookup"><span data-stu-id="22284-150">Update Encoding Properties in the File Sink</span></span>](#update-encoding-properties-in-the-file-sink)
-   [<span data-ttu-id="22284-151">Implementar principal</span><span class="sxs-lookup"><span data-stu-id="22284-151">Implement Main</span></span>](#implement-main)
-   [<span data-ttu-id="22284-152">Testar o arquivo de saída</span><span class="sxs-lookup"><span data-stu-id="22284-152">Test the Output File</span></span>](#test-the-output-file)
-   [<span data-ttu-id="22284-153">Códigos de erro comuns e dicas de depuração</span><span class="sxs-lookup"><span data-stu-id="22284-153">Common Error Codes and Debugging Tips</span></span>](#common-error-codes-and-debugging-tips)
-   [<span data-ttu-id="22284-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="22284-154">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="22284-155">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="22284-155">Prerequisites</span></span>

<span data-ttu-id="22284-156">Este tutorial pressupõe o seguinte:</span><span class="sxs-lookup"><span data-stu-id="22284-156">This tutorial assumes the following:</span></span>

-   <span data-ttu-id="22284-157">Você está familiarizado com a [estrutura do arquivo ASF](asf-file-structure.md), os [componentes ASF da camada de Pipeline](pipeline-layer-asf-components.md) fornecidos pelo Media Foundation para trabalhar com objetos ASF.</span><span class="sxs-lookup"><span data-stu-id="22284-157">You are familiar with the [ASF File Structure](asf-file-structure.md), the [Pipeline Layer ASF Components](pipeline-layer-asf-components.md) provided by Media Foundation to work with ASF Objects.</span></span> <span data-ttu-id="22284-158">Esses componentes incluem os seguintes objetos:</span><span class="sxs-lookup"><span data-stu-id="22284-158">These components include the following objects:</span></span>
    -   [<span data-ttu-id="22284-159">Fontes de mídia</span><span class="sxs-lookup"><span data-stu-id="22284-159">Media Sources</span></span>](media-sources.md)

        <span data-ttu-id="22284-160">**Observação**  Se você estiver executando transclassificação (convertendo um arquivo de taxa de bits maior em um arquivo de taxa de bits inferior sem alterar os formatos), você usará a [fonte de mídia do ASF](asf-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="22284-160">**Note**  If you are performing transrating (converting a higher bit-rate file to a lower bit-rate file without changing formats), you will use the [ASF Media Source](asf-media-source.md).</span></span>

    -   [<span data-ttu-id="22284-161">Codificadores de mídia do Windows</span><span class="sxs-lookup"><span data-stu-id="22284-161">Windows Media Encoders</span></span>](windows-media-encoders.md)
    -   [<span data-ttu-id="22284-162">Coletores de mídia ASF</span><span class="sxs-lookup"><span data-stu-id="22284-162">ASF Media Sinks</span></span>](asf-media-sinks.md)
    -   [<span data-ttu-id="22284-163">Objeto ASF ContentInfo</span><span class="sxs-lookup"><span data-stu-id="22284-163">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
    -   [<span data-ttu-id="22284-164">Perfil ASF</span><span class="sxs-lookup"><span data-stu-id="22284-164">ASF Profile</span></span>](asf-profile.md)

-   <span data-ttu-id="22284-165">Você está familiarizado com os codificadores de mídia do Windows e os vários tipos de codificação, especialmente a [codificação de taxa de bits constante](constant-bit-rate-encoding.md) e a [codificação de taxa de bits variável baseada em qualidade](quality-based-variable-bit-rate--vbr--encoding.md).</span><span class="sxs-lookup"><span data-stu-id="22284-165">You are familiar with Windows Media encoders, and the various encoding types, particularly [Constant Bit Rate Encoding](constant-bit-rate-encoding.md) and [Quality-Based Variable Bit Rate Encoding](quality-based-variable-bit-rate--vbr--encoding.md).</span></span>
-   <span data-ttu-id="22284-166">Você está familiarizado com as operações de MFT do codificador.</span><span class="sxs-lookup"><span data-stu-id="22284-166">You are familiar with encoder MFT operations.</span></span> <span data-ttu-id="22284-167">Especificamente, a criação de uma instância do codificador e a configuração de tipos de entrada e saída no codificador.</span><span class="sxs-lookup"><span data-stu-id="22284-167">Specifically, creating an instance of the encoder and setting input and output types on the encoder.</span></span>
-   <span data-ttu-id="22284-168">Você está familiarizado com objetos de topologia e como criar uma topologia de codificação.</span><span class="sxs-lookup"><span data-stu-id="22284-168">You are familiar with topology objects and how to build an encoding topology.</span></span> <span data-ttu-id="22284-169">Para obter mais informações sobre topologias e nós de topologia, consulte [criando topologias](creating-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="22284-169">For more information about topologies and topology nodes, see [Creating Topologies](creating-topologies.md).</span></span>
-   <span data-ttu-id="22284-170">Você está familiarizado com o modelo de evento da [sessão de mídia](media-session.md)e as operações de controle de fluxo.</span><span class="sxs-lookup"><span data-stu-id="22284-170">You are familiar with [Media Session](media-session.md)'s event model and the flow control operations.</span></span> <span data-ttu-id="22284-171">Para obter informações, consulte [eventos de sessão de mídia](media-session-events.md).</span><span class="sxs-lookup"><span data-stu-id="22284-171">For information, see [Media Session Events](media-session-events.md).</span></span>

## <a name="set-up-the-project"></a><span data-ttu-id="22284-172">Configurar o projeto</span><span class="sxs-lookup"><span data-stu-id="22284-172">Set up the Project</span></span>

1.  <span data-ttu-id="22284-173">Inclua os seguintes cabeçalhos no arquivo de origem:</span><span class="sxs-lookup"><span data-stu-id="22284-173">Include the following headers in your source file:</span></span>

    ```C++
    #include <new>
    #include <mfidl.h>            // Media Foundation interfaces
    #include <mfapi.h>            // Media Foundation platform APIs
    #include <mferror.h>        // Media Foundation error codes
    #include <wmcontainer.h>    // ASF-specific components
    #include <wmcodecdsp.h>        // Windows Media DSP interfaces
    #include <Dmo.h>            // DMO objects
    #include <uuids.h>            // Definition for FORMAT_VideoInfo
    #include <propvarutil.h>
    
    ```

    

2.  <span data-ttu-id="22284-174">Link para os seguintes arquivos de biblioteca:</span><span class="sxs-lookup"><span data-stu-id="22284-174">Link to the following library files:</span></span>

    ```C++
    // The required link libraries 
    #pragma comment(lib, "mfplat")
    #pragma comment(lib, "mf")
    #pragma comment(lib, "mfuuid")
    #pragma comment(lib, "msdmo")
    #pragma comment(lib, "strmiids")
    #pragma comment(lib, "propsys")
    
    ```

    

3.  <span data-ttu-id="22284-175">Declare a função [SafeRelease](saferelease.md) .</span><span class="sxs-lookup"><span data-stu-id="22284-175">Declare the [SafeRelease](saferelease.md) function.</span></span>

    ```C++
    template <class T> void SafeRelease(T **ppT)
    {
        if (*ppT)
        {
            (*ppT)->Release();
            *ppT = NULL;
        }
    }
    ```

    

4.  <span data-ttu-id="22284-176">Declare a enumeração do modo de codificação \_ para definir os tipos de codificação CBR e VBR.</span><span class="sxs-lookup"><span data-stu-id="22284-176">Declare the ENCODING\_MODE enumeration to define CBR and VBR encoding types.</span></span>

    ```C++
    // Encoding mode
    typedef enum ENCODING_MODE {
      NONE  = 0x00000000,
      CBR   = 0x00000001,
      VBR   = 0x00000002,
    } ;
    
    ```

    

5.  <span data-ttu-id="22284-177">Defina uma constante para a janela de buffer para um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="22284-177">Define a constant for buffer window for a video stream.</span></span>

    ```C++
    // Video buffer window
    const INT32 VIDEO_WINDOW_MSEC = 3000;
    
    ```

    

## <a name="create-the-media-source"></a><span data-ttu-id="22284-178">Criar a origem da mídia</span><span class="sxs-lookup"><span data-stu-id="22284-178">Create the Media Source</span></span>

<span data-ttu-id="22284-179">Crie uma origem de mídia para a fonte de entrada.</span><span class="sxs-lookup"><span data-stu-id="22284-179">Create a media source for the input source.</span></span> <span data-ttu-id="22284-180">O Media Foundation fornece fontes de mídia internas para vários formatos de mídia: MP3, MP4/3GP, AVI/WAVE.</span><span class="sxs-lookup"><span data-stu-id="22284-180">Media Foundation provides built-in media sources for various media formats: MP3, MP4/3GP, AVI/WAVE.</span></span> <span data-ttu-id="22284-181">Para obter informações sobre os formatos com suporte pelo Media Foundation, consulte [formatos de mídia com suporte no Media Foundation](supported-media-formats-in-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="22284-181">For information about the formats supported by Media Foundation, see [Supported Media Formats in Media Foundation](supported-media-formats-in-media-foundation.md).</span></span>

<span data-ttu-id="22284-182">Para criar a origem de mídia, use o [resolvedor de origem](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="22284-182">To create the media source, use the [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="22284-183">Esse objeto analisa a URL que foi especificada para o arquivo de origem e cria a origem de mídia apropriada.</span><span class="sxs-lookup"><span data-stu-id="22284-183">This object analyzes the URL that was specified for the source file and creates the appropriate media source.</span></span>

<span data-ttu-id="22284-184">Faça as seguintes chamadas:</span><span class="sxs-lookup"><span data-stu-id="22284-184">Make the following calls:</span></span>

-   [<span data-ttu-id="22284-185">**MFCreateSourceResolver**</span><span class="sxs-lookup"><span data-stu-id="22284-185">**MFCreateSourceResolver**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver)
-   [<span data-ttu-id="22284-186">**IMFSourceResolver::CreateObjectFromURL**</span><span class="sxs-lookup"><span data-stu-id="22284-186">**IMFSourceResolver::CreateObjectFromURL**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)

    <span data-ttu-id="22284-187">Para obter mais informações sobre essas chamadas, consulte [usando o resolvedor de origem](using-the-source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="22284-187">For more information about these calls, see [Using the Source Resolver](using-the-source-resolver.md).</span></span>

    <span data-ttu-id="22284-188">Se o arquivo de entrada estiver no formato ASF e você quiser convertê-lo em um arquivo de taxa de bits diferente sem alterar os formatos, o resolvedor de origem criará uma instância da [fonte de mídia ASF](asf-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="22284-188">If your input file is in ASF format and you want to convert it to a different bit-rate file without changing formats, the source solver creates an instance of the [ASF Media Source](asf-media-source.md).</span></span>

<span data-ttu-id="22284-189">O exemplo de código a seguir mostra uma função createmedianame que cria uma origem de mídia para o arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="22284-189">The following code example shows a function CreateMediaSource that creates a media source for the specified file.</span></span>


```C++
//  Create a media source from a URL.
HRESULT CreateMediaSource(PCWSTR sURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source.

    // Note: For simplicity this sample uses the synchronous method to create 
    // the media source. However, creating a media source can take a noticeable
    // amount of time, especially for a network source. For a more responsive 
    // UI, use the asynchronous BeginCreateObjectFromURL method.

    hr = pSourceResolver->CreateObjectFromURL(
        sURL,                       // URL of the source.
        MF_RESOLUTION_MEDIASOURCE,  // Create a source object.
        NULL,                       // Optional property store.
        &ObjectType,        // Receives the created object type. 
        &pSource            // Receives a pointer to the media source.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



## <a name="create-the-asf-file-sink"></a><span data-ttu-id="22284-190">Criar o coletor de arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="22284-190">Create the ASF File Sink</span></span>

<span data-ttu-id="22284-191">Crie uma instância do coletor de arquivo ASF que arquivará dados de mídia codificados em um arquivo ASF no final da sessão de codificação.</span><span class="sxs-lookup"><span data-stu-id="22284-191">Create an instance of the ASF file sink that will archive encoded media data to an ASF file at the end of the encoding session.</span></span>

<span data-ttu-id="22284-192">Neste tutorial, você criará um objeto de ativação para o coletor de arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="22284-192">In this tutorial, you will create an activation object for the ASF file sink.</span></span> <span data-ttu-id="22284-193">O coletor de arquivos precisa das seguintes informações para criar os coletores de fluxo necessários.</span><span class="sxs-lookup"><span data-stu-id="22284-193">The file sink needs the following information in order to create the required stream sinks.</span></span>

-   <span data-ttu-id="22284-194">Os fluxos a serem codificados e gravados no arquivo final.</span><span class="sxs-lookup"><span data-stu-id="22284-194">The streams to be encoded and written in the final file.</span></span>
-   <span data-ttu-id="22284-195">As propriedades de codificação que são usadas para codificar o conteúdo de mídia, como, tipo de codificação, número de passagens de codificação e as propriedades relacionadas.</span><span class="sxs-lookup"><span data-stu-id="22284-195">The encoding properties that are used to encode the media content, such as, type of encoding, number of encoding passes, and the related properties.</span></span>
-   <span data-ttu-id="22284-196">As propriedades de arquivo global que indicam ao coletor de mídia se ele deve ajustar os parâmetros de Bucket de vazamento (taxa de bits e tamanho do buffer) automaticamente.</span><span class="sxs-lookup"><span data-stu-id="22284-196">The global file properties that indicate to the media sink whether it should adjust the leaky bucket parameters (bit rate and buffer size) automatically.</span></span>

<span data-ttu-id="22284-197">As informações de fluxo são configuradas no objeto de perfil ASF e a codificação e as propriedades globais são definidas em um repositório de propriedades gerenciado pelo objeto ASF ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="22284-197">The stream information is configured in the ASF Profile object and the encoding and global properties are set in a property store managed by the ASF ContentInfo Object.</span></span>

<span data-ttu-id="22284-198">Para obter uma visão geral do coletor de arquivos ASF, consulte [coletores de mídia ASF](asf-media-sinks.md).</span><span class="sxs-lookup"><span data-stu-id="22284-198">For an overview of the ASF file sink, see [ASF Media Sinks](asf-media-sinks.md).</span></span>

### <a name="create-the-asf-profile-object"></a><span data-ttu-id="22284-199">Criar o objeto de perfil ASF</span><span class="sxs-lookup"><span data-stu-id="22284-199">Create the ASF Profile Object</span></span>

<span data-ttu-id="22284-200">Para que o coletor de arquivos ASF grave dados de mídia codificados em um arquivo ASF, o coletor precisa saber o número de fluxos e o tipo de fluxos para os quais criar coletores de fluxo.</span><span class="sxs-lookup"><span data-stu-id="22284-200">For the ASF file sink to write encoded media data into an ASF file, the sink needs to know the number of streams and the type of streams for which to create stream sinks.</span></span> <span data-ttu-id="22284-201">Neste tutorial, você extrairá essas informações da origem de mídia e criará os fluxos de saída correspondentes.</span><span class="sxs-lookup"><span data-stu-id="22284-201">In this tutorial you will extract that information from the media source and create corresponding output streams.</span></span> <span data-ttu-id="22284-202">Restrinja os fluxos de saída para um fluxo de áudio e um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="22284-202">Restrict your output streams to one audio stream and one video stream.</span></span> <span data-ttu-id="22284-203">Para cada fluxo selecionado na origem, crie um fluxo de destino e adicione-o ao perfil.</span><span class="sxs-lookup"><span data-stu-id="22284-203">For each selected stream in the source, create a target stream and add it to the profile.</span></span>

<span data-ttu-id="22284-204">Para implementar essa etapa, você precisa dos seguintes objetos.</span><span class="sxs-lookup"><span data-stu-id="22284-204">To implement this step, you need the following objects.</span></span>

-   [<span data-ttu-id="22284-205">Perfil ASF</span><span class="sxs-lookup"><span data-stu-id="22284-205">ASF Profile</span></span>](asf-profile.md)
-   <span data-ttu-id="22284-206">Descritor de apresentação para a origem de mídia</span><span class="sxs-lookup"><span data-stu-id="22284-206">Presentation Descriptor for the media source</span></span>
-   <span data-ttu-id="22284-207">Os descritores de fluxo para os fluxos selecionados na origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="22284-207">Stream descriptors for the selected streams in the media source.</span></span>
-   <span data-ttu-id="22284-208">Tipos de mídia para os fluxos selecionados.</span><span class="sxs-lookup"><span data-stu-id="22284-208">Media Types for the selected streams.</span></span>

<span data-ttu-id="22284-209">As etapas a seguir descrevem o processo de criação do perfil ASF e dos fluxos de destino.</span><span class="sxs-lookup"><span data-stu-id="22284-209">The following steps describe the process of creating the ASF profile and the target streams.</span></span>

<span data-ttu-id="22284-210">**Para criar o perfil ASF**</span><span class="sxs-lookup"><span data-stu-id="22284-210">**To create the ASF profile**</span></span>

1.  <span data-ttu-id="22284-211">Chame [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) para criar um objeto de perfil vazio.</span><span class="sxs-lookup"><span data-stu-id="22284-211">Call [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) to create an empty profile object.</span></span>
2.  <span data-ttu-id="22284-212">Chame [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) para criar o descritor de apresentação para a origem de mídia criada na etapa descrita na seção "criar fonte de mídia" deste tutorial.</span><span class="sxs-lookup"><span data-stu-id="22284-212">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) to create the presentation descriptor for the media source created in the step described in the "Create the Media Source" section of this tutorial.</span></span>
3.  <span data-ttu-id="22284-213">Chame [**IMFPresentationDescriptor:: GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) para obter o número de fluxos na origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="22284-213">Call [**IMFPresentationDescriptor::GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) to get the number of streams in the media source.</span></span>
4.  <span data-ttu-id="22284-214">Chame [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) para cada fluxo na origem da mídia, obtenha o descritor de fluxo do fluxo.</span><span class="sxs-lookup"><span data-stu-id="22284-214">Call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) for each stream in the media source, get the stream's stream descriptor.</span></span>
5.  <span data-ttu-id="22284-215">Chame [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) seguido por [**IMFMediaTypeHandler:: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) e obtenha o primeiro tipo de mídia para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="22284-215">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) followed by [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) and get the first media type for the stream.</span></span>

    <span data-ttu-id="22284-216">**Observação**   Para evitar chamadas complexas, suponha que apenas um tipo de mídia exista por fluxo e selecione o primeiro tipo de mídia do fluxo.</span><span class="sxs-lookup"><span data-stu-id="22284-216">**Note**   To avoid complex calls, assume that only one media type exists per stream and select the first media type of the stream.</span></span> <span data-ttu-id="22284-217">Para fluxos complexos, você precisa enumerar cada tipo de mídia do manipulador de tipo de mídia e escolher o tipo de mídia que deseja codificar.</span><span class="sxs-lookup"><span data-stu-id="22284-217">For complex streams, you need to enumerate each media type from the media type handler and choose the media type that you would like to encode.</span></span>

6.  <span data-ttu-id="22284-218">Chame I [**IMFMediaType:: Getmajortype**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) para obter o tipo principal do fluxo para determinar se o fluxo contém áudio ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="22284-218">Call I [**IMFMediaType::GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) to get the major type of the stream to determine whether the stream is contains audio or video.</span></span>
7.  <span data-ttu-id="22284-219">Dependendo do tipo principal do fluxo, crie tipos de mídia de destino.</span><span class="sxs-lookup"><span data-stu-id="22284-219">Depending on the major type of the stream, create target media types.</span></span> <span data-ttu-id="22284-220">Esses tipos de mídia irão conter informações de formato que o codificador usará durante a sessão de codificação.</span><span class="sxs-lookup"><span data-stu-id="22284-220">These media types will hold format information that the encoder will use during the encoding session.</span></span> <span data-ttu-id="22284-221">As seções a seguir deste tutorial descrevem o processo de criação dos tipos de mídia de destino.</span><span class="sxs-lookup"><span data-stu-id="22284-221">The following sections of this tutorial describe the process of creating the target media types.</span></span>
    -   <span data-ttu-id="22284-222">Criar um tipo de mídia de áudio compactado</span><span class="sxs-lookup"><span data-stu-id="22284-222">Create a Compressed Audio Media Type</span></span>
    -   <span data-ttu-id="22284-223">Criar um tipo de mídia de vídeo compactado</span><span class="sxs-lookup"><span data-stu-id="22284-223">Create a Compressed Video Media Type</span></span>
8.  <span data-ttu-id="22284-224">Crie um fluxo com base no tipo de mídia de destino, configure o fluxo de acordo com os requisitos do aplicativo e adicione o fluxo ao perfil.</span><span class="sxs-lookup"><span data-stu-id="22284-224">Create a stream based on the target media type, configure the stream according to the application's requirements, and add the stream to the profile.</span></span> <span data-ttu-id="22284-225">Para obter mais informações, consulte [adicionando informações de fluxo ao coletor de arquivo ASF](adding-stream-information-to-the-asf-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="22284-225">For more information, see [Adding Stream Information to the ASF File Sink](adding-stream-information-to-the-asf-file-sink.md).</span></span>

    1.  <span data-ttu-id="22284-226">Chame [**IMFASFProfile:: CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) e passe o tipo de mídia de destino para criar o fluxo de saída.</span><span class="sxs-lookup"><span data-stu-id="22284-226">Call [**IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) and pass the target media type to create the output stream.</span></span> <span data-ttu-id="22284-227">O método recupera a interface IMFASFStreamConfig do objeto Stream.</span><span class="sxs-lookup"><span data-stu-id="22284-227">The method retrieves the IMFASFStreamConfig interface of the stream object.</span></span>
    2.  <span data-ttu-id="22284-228">Configure o fluxo.</span><span class="sxs-lookup"><span data-stu-id="22284-228">Configure the stream.</span></span>
        -   <span data-ttu-id="22284-229">Chame [**IMFASFStreamConfig:: SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) para atribuir um número ao fluxo.</span><span class="sxs-lookup"><span data-stu-id="22284-229">Call [**IMFASFStreamConfig::SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) to assign a number to the stream.</span></span> <span data-ttu-id="22284-230">Essa configuração é obrigatória.</span><span class="sxs-lookup"><span data-stu-id="22284-230">This setting is mandatory.</span></span>
        -   <span data-ttu-id="22284-231">Opcionalmente, configure os parâmetros de Bucket vazado, a extensão de carga, a exclusão mútua em cada fluxo chamando métodos [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) e atributos de configuração de fluxo relevantes.</span><span class="sxs-lookup"><span data-stu-id="22284-231">Optionally configure the leaky bucket parameters, payload extension, mutual exclusion on each stream by calling [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) methods and relevant stream configuration attributes.</span></span>
    3.  <span data-ttu-id="22284-232">Adicione as propriedades de codificação de nível de fluxo usando o objeto ContentInfo do ASF.</span><span class="sxs-lookup"><span data-stu-id="22284-232">Add the stream level encoding properties by using the ASF ContentInfo object.</span></span> <span data-ttu-id="22284-233">Para obter mais informações sobre esta etapa, consulte a seção "criar o objeto ASF ContentInfo" neste tutorial.</span><span class="sxs-lookup"><span data-stu-id="22284-233">For more information about this step, see the "Create the ASF ContentInfo Object" section in this tutorial.</span></span>
    4.  <span data-ttu-id="22284-234">Chame [**IMFASFProfile:: SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) para adicionar o fluxo ao perfil.</span><span class="sxs-lookup"><span data-stu-id="22284-234">Call [**IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) to add the stream to the profile.</span></span>

    <span data-ttu-id="22284-235">O exemplo de código a seguir cria um fluxo de áudio de saída.</span><span class="sxs-lookup"><span data-stu-id="22284-235">The following code example creates an output audio stream.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  CreateAudioStream
    //  Create an audio stream and add it to the profile.
    //
    //  pProfile: A pointer to the ASF profile.
    //  wStreamNumber: Stream number to assign for the new stream.
    //-------------------------------------------------------------------

    HRESULT CreateAudioStream(IMFASFProfile* pProfile, WORD wStreamNumber)
    {
        if (!pProfile)
        {
            return E_INVALIDARG;
        }
        if (wStreamNumber < 1 || wStreamNumber > 127 )
        {
            return MF_E_INVALIDSTREAMNUMBER;
        }

        IMFMediaType* pAudioType = NULL;
        IMFASFStreamConfig* pAudioStream = NULL;
        
        //Create an output type from the encoder
        HRESULT hr = GetOutputTypeFromWMAEncoder(&pAudioType);
        if (FAILED(hr))
        {
            goto done;
        }
        
        //Create a new stream with the audio type
        hr = pProfile->CreateStream(pAudioType, &pAudioStream);
        if (FAILED(hr))
        {
            goto done;
        }

        //Set stream number
        hr = pAudioStream->SetStreamNumber(wStreamNumber);
        if (FAILED(hr))
        {
            goto done;
        }
        
        //Add the stream to the profile
        hr = pProfile->SetStream(pAudioStream);
        if (FAILED(hr))
        {
            goto done;
        }

        wprintf_s(L"Audio Stream created. Stream Number: %d.\n", wStreamNumber);

    done:
        SafeRelease(&pAudioStream);
        SafeRelease(&pAudioType);
        return hr;
    }
    ```

    

    <span data-ttu-id="22284-236">O exemplo de código a seguir cria um fluxo de vídeo de saída.</span><span class="sxs-lookup"><span data-stu-id="22284-236">The following code example creates an output video stream.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  CreateVideoStream
    //  Create an video stream and add it to the profile.
    //
    //  pProfile: A pointer to the ASF profile.
    //  wStreamNumber: Stream number to assign for the new stream.
    //    pType: A pointer to the source's video media type.
    //-------------------------------------------------------------------

    HRESULT CreateVideoStream(IMFASFProfile* pProfile, WORD wStreamNumber, IMFMediaType* pType)
    {
        if (!pProfile)
        {
            return E_INVALIDARG;
        }
        if (wStreamNumber < 1 || wStreamNumber > 127 )
        {
            return MF_E_INVALIDSTREAMNUMBER;
        }

        HRESULT hr = S_OK;

        
        IMFMediaType* pVideoType = NULL;
        IMFASFStreamConfig* pVideoStream = NULL;

        UINT32 dwBitRate = 0;
            
        //Create a new video type from the source type
        hr = CreateCompressedVideoType(pType, &pVideoType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Create a new stream with the video type
        hr = pProfile->CreateStream(pVideoType, &pVideoStream);
        if (FAILED(hr))
        {
            goto done;
        }
        

        //Set a valid stream number
        hr = pVideoStream->SetStreamNumber(wStreamNumber);
        if (FAILED(hr))
        {
            goto done;
        }

        //Add the stream to the profile
        hr = pProfile->SetStream(pVideoStream);
        if (FAILED(hr))
        {
            goto done;
        }

        wprintf_s(L"Video Stream created. Stream Number: %d .\n", wStreamNumber);

    done:

        SafeRelease(&pVideoStream);
        SafeRelease(&pVideoType);

        return hr;
    }
    ```

    

<span data-ttu-id="22284-237">O exemplo de código a seguir cria fluxos de saída dependendo dos fluxos na origem.</span><span class="sxs-lookup"><span data-stu-id="22284-237">The following code example creates output streams depending on the streams in the source.</span></span>


```C++
    //For each stream in the source, add target stream information in the profile
    for (DWORD iStream = 0; iStream < dwSrcStream; iStream++)
    {
        hr = pPD->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);
        if (FAILED(hr))
        {
            goto done;
        }

        if (!fSelected)
        {
            continue;
        }

        //Get the media type handler
        hr = pStreamDesc->GetMediaTypeHandler(&pHandler);
        if (FAILED(hr))
        {
            goto done;
        }

        //Get the first media type 
        hr = pHandler->GetMediaTypeByIndex(0, &pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Get the major type
        hr = pMediaType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        // If this is a video stream, create the target video stream
        if (guidMajor == MFMediaType_Video)
        {
            //The stream level encoding properties will be set in this call
            hr = CreateVideoStream(pProfile, wStreamID, pMediaType);

            if (FAILED(hr))
            {
                goto done;
            }
        }
        
        // If this is an audio stream, create the target audio stream
        if (guidMajor == MFMediaType_Audio)
        {
            //The stream level encoding properties will be set in this call
            hr = CreateAudioStream(pProfile, wStreamID);

            if (FAILED(hr))
            {
                goto done;
            }
        }

        //Get stream's encoding property
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamID, &pContentInfoProps);
        if (FAILED(hr))
        {
            goto done;
        }

        //Set the stream-level encoding properties
        hr = SetEncodingProperties(guidMajor, pContentInfoProps);       
        if (FAILED(hr))
        {
            goto done;
        }


        SafeRelease(&pMediaType);
        SafeRelease(&pStreamDesc);
        SafeRelease(&pContentInfoProps);
        wStreamID++;
    }
```



### <a name="create-a-compressed-audio-media-type"></a><span data-ttu-id="22284-238">Criar um tipo de mídia de áudio compactado</span><span class="sxs-lookup"><span data-stu-id="22284-238">Create a Compressed Audio Media Type</span></span>

<span data-ttu-id="22284-239">Se você quiser incluir um fluxo de áudio no arquivo de saída, crie um tipo de áudio especificando as características do tipo codificado definindo os atributos necessários.</span><span class="sxs-lookup"><span data-stu-id="22284-239">If you want to include an audio stream in the output file, create an audio type by specifying the characteristics of the encoded type by setting the required attributes.</span></span> <span data-ttu-id="22284-240">Para garantir que o tipo de áudio seja compatível com o codificador de áudio do Windows Media, crie uma instância do MFT do codificador, defina as propriedades de codificação e obtenha um tipo de mídia chamando [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span><span class="sxs-lookup"><span data-stu-id="22284-240">To make sure that the audio type is compatible with the Windows Media audio encoder, instantiate the encoder MFT, set the encoding properties, and get a media type by calling [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span></span> <span data-ttu-id="22284-241">Obtenha o tipo de saída necessário fazendo um loop por todos os tipos disponíveis, obtendo os atributos de cada tipo de mídia e selecionando o tipo mais próximo de seus requisitos.</span><span class="sxs-lookup"><span data-stu-id="22284-241">Get the required output type by looping through all the available types, getting the attributes of each media type, and selecting the type that is closest to your requirements.</span></span> <span data-ttu-id="22284-242">Neste tutorial, obtenha o primeiro tipo disponível da lista de tipos de mídia de saída com suporte pelo codificador.</span><span class="sxs-lookup"><span data-stu-id="22284-242">In this tutorial, get the first available type from the list of output media types supported by the encoder.</span></span>

<span data-ttu-id="22284-243">**Observação**  Para o Windows 7, Media Foundation fornece uma nova função, [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) que recupera uma lista dos tipos de áudio compatíveis.</span><span class="sxs-lookup"><span data-stu-id="22284-243">**Note**  For Windows 7, Media Foundation provides a new function, [**MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) that retrieves a list of the compatible audio types.</span></span> <span data-ttu-id="22284-244">Essa função só obtém tipos de mídia para codificação de CBR.</span><span class="sxs-lookup"><span data-stu-id="22284-244">This function only gets media types for CBR encoding.</span></span>

<span data-ttu-id="22284-245">Um tipo de áudio completo deve ter os seguintes atributos definidos:</span><span class="sxs-lookup"><span data-stu-id="22284-245">A complete audio type must have the following attributes set:</span></span>

-   [<span data-ttu-id="22284-246">**\_ \_ tipo principal MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="22284-246">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)
-   [<span data-ttu-id="22284-247">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="22284-247">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)
-   [<span data-ttu-id="22284-248">**\_canais de \_ número de áudio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22284-248">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)
-   [<span data-ttu-id="22284-249">**\_amostras de áudio MF MT \_ \_ \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="22284-249">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)
-   [<span data-ttu-id="22284-250">**\_alinhamento de \_ bloco de áudio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="22284-250">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)
-   [<span data-ttu-id="22284-251">**áudio do MF \_ MT \_ média de \_ \_ bytes \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="22284-251">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [<span data-ttu-id="22284-252">**\_bits de áudio MF MT \_ \_ \_ por \_ amostra**</span><span class="sxs-lookup"><span data-stu-id="22284-252">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)

<span data-ttu-id="22284-253">O exemplo de código a seguir cria um tipo de áudio compactado obtendo um tipo compatível do codificador de áudio do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="22284-253">The following code example creates a compressed audio type by getting a compatible type from the Windows Media Audio encoder.</span></span> <span data-ttu-id="22284-254">A implementação de setencodingproperties é mostrada na seção "criar o objeto ASF ContentInfo" deste tutorial.</span><span class="sxs-lookup"><span data-stu-id="22284-254">The implementation for SetEncodingProperties is shown in the "Create the ASF ContentInfo Object" section of this tutorial.</span></span>


```C++
//-------------------------------------------------------------------
//  GetOutputTypeFromWMAEncoder
//  Gets a compatible output type from the Windows Media audio encoder.
//
//  ppAudioType: Receives a pointer to the media type.
//-------------------------------------------------------------------

HRESULT GetOutputTypeFromWMAEncoder(IMFMediaType** ppAudioType)
{
    if (!ppAudioType)
    {
        return E_POINTER;
    }

    IMFTransform* pMFT = NULL;
    IMFMediaType* pType = NULL;
    IPropertyStore* pProps = NULL;

    //We need to find a suitable output media type
    //We need to create the encoder to get the available output types
    //and discard the instance.

    CLSID *pMFTCLSIDs = NULL;   // Pointer to an array of CLISDs. 
    UINT32 cCLSID = 0;            // Size of the array.

    MFT_REGISTER_TYPE_INFO tinfo;
    
    tinfo.guidMajorType = MFMediaType_Audio;
    tinfo.guidSubtype = MFAudioFormat_WMAudioV9;

    // Look for an encoder.
    HRESULT hr = MFTEnum(
        MFT_CATEGORY_AUDIO_ENCODER,
        0,                  // Reserved
        NULL,                // Input type to match. None.
        &tinfo,             // WMV encoded type.
        NULL,               // Attributes to match. (None.)
        &pMFTCLSIDs,        // Receives a pointer to an array of CLSIDs.
        &cCLSID             // Receives the size of the array.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // MFTEnum can return zero matches.
    if (cCLSID == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
        goto done;
    }
    else
    {
        // Create the MFT decoder
        hr = CoCreateInstance(pMFTCLSIDs[0], NULL,
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pMFT));

        if (FAILED(hr))
        {
            goto done;
        }

    }

    // Get the encoder's property store

    hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
    if (FAILED(hr))
    {
        goto done;
    }
    
    //Set encoding properties
    hr = SetEncodingProperties(MFMediaType_Audio, pProps);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get the first output type
    //You can loop through the available output types to choose 
    //the one that meets your target requirements
    hr = pMFT->GetOutputAvailableType(0, 0, &pType);
    if (FAILED(hr))
    {
        goto done;
    }

    //Return to the caller
    *ppAudioType = pType;
    (*ppAudioType)->AddRef();
    
done:
    SafeRelease(&pProps);
    SafeRelease(&pType);
    SafeRelease(&pMFT);
    CoTaskMemFree(pMFTCLSIDs);
    return hr;
}
```



### <a name="create-a-compressed-video-media-type"></a><span data-ttu-id="22284-255">Criar um tipo de mídia de vídeo compactado</span><span class="sxs-lookup"><span data-stu-id="22284-255">Create a Compressed Video Media Type</span></span>

<span data-ttu-id="22284-256">Se você quiser incluir um fluxo de vídeo no arquivo de saída, crie um tipo de vídeo codificado completo.</span><span class="sxs-lookup"><span data-stu-id="22284-256">If you want to include a video stream in the output file, create a complete-encoded video type.</span></span> <span data-ttu-id="22284-257">O tipo de mídia completo deve incluir a taxa de bits e os dados privados do codec desejados.</span><span class="sxs-lookup"><span data-stu-id="22284-257">The complete media type must include the desired bit rate and codec private data.</span></span>

<span data-ttu-id="22284-258">Há duas maneiras de criar um tipo de mídia de vídeo completo.</span><span class="sxs-lookup"><span data-stu-id="22284-258">There are two ways you can create a complete video media type.</span></span>

-   <span data-ttu-id="22284-259">Crie um tipo de mídia vazio e copie os atributos do tipo de mídia do tipo de vídeo de origem e substitua o atributo de [**\_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md) pela constante de GUID MFVideoFormat \_ WMV3.</span><span class="sxs-lookup"><span data-stu-id="22284-259">Create an empty media type and copy the media type attributes from the source video type and overwrite the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute with the GUID constant MFVideoFormat\_WMV3.</span></span>

    <span data-ttu-id="22284-260">Um tipo de vídeo completo deve ter os seguintes atributos definidos:</span><span class="sxs-lookup"><span data-stu-id="22284-260">A complete video type must have the following attributes set:</span></span>

    -   <span data-ttu-id="22284-261">\_ \_ tipo principal MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="22284-261">MF\_MT\_MAJOR\_TYPE</span></span>
    -   <span data-ttu-id="22284-262">subtipo MF \_ MT \_</span><span class="sxs-lookup"><span data-stu-id="22284-262">MF\_MT\_SUBTYPE</span></span>
    -   <span data-ttu-id="22284-263">\_taxa de \_ quadros MF MT \_</span><span class="sxs-lookup"><span data-stu-id="22284-263">MF\_MT\_FRAME\_RATE</span></span>
    -   <span data-ttu-id="22284-264">\_tamanho do \_ quadro MF MT \_</span><span class="sxs-lookup"><span data-stu-id="22284-264">MF\_MT\_FRAME\_SIZE</span></span>
    -   <span data-ttu-id="22284-265">\_modo de \_ entrelaçamento do MF MT \_</span><span class="sxs-lookup"><span data-stu-id="22284-265">MF\_MT\_INTERLACE\_MODE</span></span>
    -   <span data-ttu-id="22284-266">taxa de proporção de pixel do MF \_ MT \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="22284-266">MF\_MT\_PIXEL\_ASPECT\_RATIO</span></span>
    -   <span data-ttu-id="22284-267">\_taxa de \_ \_ bits média de MF MT</span><span class="sxs-lookup"><span data-stu-id="22284-267">MF\_MT\_AVG\_BITRATE</span></span>
    -   <span data-ttu-id="22284-268">dados de usuário do MF \_ MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="22284-268">MF\_MT\_USER\_DATA</span></span>

    <span data-ttu-id="22284-269">O exemplo de código a seguir cria um tipo de vídeo compactado do tipo de vídeo da origem.</span><span class="sxs-lookup"><span data-stu-id="22284-269">The following code example creates a compressed video type from the source's video type.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  CreateCompressedVideoType
    //  Creates an output type from source's video media type.
    //
    //    pType: A pointer to the source's video media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT CreateCompressedVideoType(
            IMFMediaType* pType, 
            IMFMediaType** ppVideoType)
    {
        if (!pType)
        {
            return E_INVALIDARG;
        }
        if (!ppVideoType)
        {
            return E_POINTER;
        }
        
        HRESULT hr = S_OK;
        MFRatio fps = { 0 };
        MFRatio par = { 0 };
        UINT32 width = 0, height = 0;
        UINT32 interlace = MFVideoInterlace_Unknown;
        UINT32 fSamplesIndependent = 0;
        UINT32 cBitrate = 0;

        IMFMediaType* pMediaType = NULL;

        GUID guidMajor = GUID_NULL;

        hr = pType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMajor != MFMediaType_Video )
        {
            hr = MF_E_INVALID_FORMAT;
            goto done;
        }

        hr = MFCreateMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pType->CopyAllItems(pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Fill the missing attributes
        //1. Frame rate
        hr = MFGetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, (UINT32*)&fps.Numerator, (UINT32*)&fps.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            fps.Numerator = 30000;
            fps.Denominator = 1001;

            hr = MFSetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, fps.Numerator, fps.Denominator);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        ////2. Frame size
        hr = MFGetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, &width, &height);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            width = 1280;
            height = 720;
                
            hr = MFSetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, width, height);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        ////3. Interlace mode
        
        if (FAILED(pMediaType->GetUINT32(MF_MT_INTERLACE_MODE, &interlace)))
        {
            hr = pMediaType->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        ////4. Pixel aspect Ratio
        hr = MFGetAttributeRatio(pMediaType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32*)&par.Numerator, (UINT32*)&par.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            par.Numerator = par.Denominator = 1;
            hr = MFSetAttributeRatio(pMediaType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32)par.Numerator, (UINT32)par.Denominator);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        //6. bit rate
        if (FAILED(pMediaType->GetUINT32(MF_MT_AVG_BITRATE, &cBitrate)))
        {
            hr = pMediaType->SetUINT32(MF_MT_AVG_BITRATE, 1000000);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        hr = pMediaType->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_WMV3);
        if (FAILED(hr))
        {
            goto done;
        }

        // Return the pointer to the caller.
        *ppVideoType = pMediaType;
        (*ppVideoType)->AddRef();


    done:
        SafeRelease(&pMediaType);
        return hr;
    }
    
    ```

    

-   <span data-ttu-id="22284-270">Obtenha um tipo de mídia compatível do codificador de vídeo do Windows Media definindo as propriedades de codificação e, em seguida, chamando [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span><span class="sxs-lookup"><span data-stu-id="22284-270">Get a compatible media type from the Windows Media video encoder by setting the encoding properties and then calling [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).</span></span> <span data-ttu-id="22284-271">Esse método retorna o tipo parcial.</span><span class="sxs-lookup"><span data-stu-id="22284-271">This method returns the partial type.</span></span> <span data-ttu-id="22284-272">Certifique-se de converter o tipo parcial para um tipo completo adicionando as seguintes informações:</span><span class="sxs-lookup"><span data-stu-id="22284-272">Make sure you convert the partial type to a complete type by adding the following information:</span></span>

    -   <span data-ttu-id="22284-273">Defina a taxa de bits do vídeo no atributo de taxa de bits [**\_ \_ média \_ MF MT**](mf-mt-avg-bitrate-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="22284-273">Set the video bit rate in the [**MF\_MT\_AVG\_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute.</span></span>
    -   <span data-ttu-id="22284-274">Adicione dados privados de codec definindo o atributo de [**\_ dados de \_ usuário \_ MF MT**](mf-mt-user-data-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="22284-274">Add codec private data by setting the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute.</span></span> <span data-ttu-id="22284-275">Para obter instruções detalhadas, consulte "dados de codec privado" em [Configurando um codificador WMV](configuring-a-wmv-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="22284-275">For detailed instructions, see "Private Codec Data" in [Configuring a WMV Encoder](configuring-a-wmv-encoder.md).</span></span>

    <span data-ttu-id="22284-276">Como [**IWMCodecPrivateData:: GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) verifica a taxa de bits antes de retornar os dados privados do codec, certifique-se de definir a taxa de bits antes de obter os dados privados do codec.</span><span class="sxs-lookup"><span data-stu-id="22284-276">Because [**IWMCodecPrivateData::GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) checks the bit rate before returning the codec private data, make sure that you set the bit rate before getting the codec private data.</span></span>

    <span data-ttu-id="22284-277">O exemplo de código a seguir cria um tipo de vídeo compactado obtendo um tipo compatível do codificador de vídeo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="22284-277">The following code example creates a compressed video type by getting a compatible type from the Windows Media Video encoder.</span></span> <span data-ttu-id="22284-278">Ele também cria um tipo de vídeo descompactado e o define como a entrada do codificador.</span><span class="sxs-lookup"><span data-stu-id="22284-278">It also creates an uncompressed video type and sets it as the encoder's input.</span></span> <span data-ttu-id="22284-279">Isso é implementado na função auxiliar CreateUncompressedVideoType.</span><span class="sxs-lookup"><span data-stu-id="22284-279">This is implemented in the helper function CreateUncompressedVideoType.</span></span> <span data-ttu-id="22284-280">GetOutputTypeFromWMVEncoder converte o tipo parcial retornado em um tipo completo adicionando dados privados do codec.</span><span class="sxs-lookup"><span data-stu-id="22284-280">GetOutputTypeFromWMVEncoder converts the returned partial type into a complete type by adding codec private data.</span></span> <span data-ttu-id="22284-281">A implementação de setencodingproperties é mostrada na seção "criar o objeto ASF ContentInfo" deste tutorial.</span><span class="sxs-lookup"><span data-stu-id="22284-281">The implementation for SetEncodingProperties is shown in the "Create the ASF ContentInfo Object" section of this tutorial.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  GetOutputTypeFromWMVEncoder
    //  Gets a compatible output type from the Windows Media video encoder.
    //
    //  pType: A pointer to the source video stream's media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT GetOutputTypeFromWMVEncoder(IMFMediaType* pType, IMFMediaType** ppVideoType)
    {
        if (!ppVideoType)
        {
            return E_POINTER;
        }

        IMFTransform* pMFT = NULL;
        IPropertyStore* pProps = NULL;
        IMFMediaType* pInputType = NULL;
        IMFMediaType* pOutputType = NULL;
        
        UINT32 cBitrate = 0;

        //We need to find a suitable output media type
        //We need to create the encoder to get the available output types
        //and discard the instance.

        CLSID *pMFTCLSIDs = NULL;   // Pointer to an array of CLISDs. 
        UINT32 cCLSID = 0;          // Size of the array.

        MFT_REGISTER_TYPE_INFO tinfo;
        
        tinfo.guidMajorType = MFMediaType_Video;
        tinfo.guidSubtype = MFVideoFormat_WMV3;

        // Look for an encoder.
        HRESULT hr = MFTEnum(
            MFT_CATEGORY_VIDEO_ENCODER,
            0,                  // Reserved
            NULL,               // Input type to match. None.
            &tinfo,             // WMV encoded type.
            NULL,               // Attributes to match. (None.)
            &pMFTCLSIDs,        // Receives a pointer to an array of CLSIDs.
            &cCLSID             // Receives the size of the array.
            );
        if (FAILED(hr))
        {
            goto done;
        }

        // MFTEnum can return zero matches.
        if (cCLSID == 0)
        {
            hr = MF_E_TOPO_CODEC_NOT_FOUND;
            goto done;
        }
        else
        {
            //Create the MFT decoder
            hr = CoCreateInstance(pMFTCLSIDs[0], NULL,
                CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pMFT));
            if (FAILED(hr))
            {
                goto done;
            }

        }
        
        //Get the video encoder property store
        hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
        if (FAILED(hr))
        {
            goto done;
        }

        //Set encoding properties
        hr = SetEncodingProperties(MFMediaType_Video, pProps);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = CreateUncompressedVideoType(pType, &pInputType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMFT->SetInputType(0, pInputType, 0);

        //Get the first output type
        //You can loop through the available output types to choose 
        //the one that meets your target requirements
        hr =  pMFT->GetOutputAvailableType(0, 0, &pOutputType);
        if (FAILED(hr))
        {
            goto done;
        }
        
        hr = pType->GetUINT32(MF_MT_AVG_BITRATE, &cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        //Now set the bit rate
        hr = pOutputType->SetUINT32(MF_MT_AVG_BITRATE, cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = AddPrivateData(pMFT, pOutputType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Return to the caller
        *ppVideoType = pOutputType;
        (*ppVideoType)->AddRef();
        
    done:
        SafeRelease(&pProps);
        SafeRelease(&pOutputType);
        SafeRelease(&pInputType);
        SafeRelease(&pMFT);
        CoTaskMemFree(pMFTCLSIDs);
        return hr;
    }
    ```

    

    <span data-ttu-id="22284-282">O exemplo de código a seguir cria um tipo de vídeo descompactado.</span><span class="sxs-lookup"><span data-stu-id="22284-282">The following code example creates an uncompressed video type.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  CreateUncompressedVideoType
    //  Creates an uncompressed video type.
    //
    //    pType: A pointer to the source's video media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT CreateUncompressedVideoType(IMFMediaType* pType, IMFMediaType** ppMediaType)
    {
        if (!pType)
        {
            return E_INVALIDARG;
        }
        if (!ppMediaType)
        {
            return E_POINTER;
        }
        
        MFRatio fps = { 0 };
        MFRatio par = { 0 };
        UINT32 width = 0, height = 0;
        UINT32 interlace = MFVideoInterlace_Unknown;
        UINT32 cBitrate = 0;

        IMFMediaType* pMediaType = NULL;

        GUID guidMajor = GUID_NULL;

        HRESULT hr = pType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMajor != MFMediaType_Video )
        {
            hr = MF_E_INVALID_FORMAT;
            goto done;
        }

        hr = MFGetAttributeRatio(pType, MF_MT_FRAME_RATE, (UINT32*)&fps.Numerator, (UINT32*)&fps.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            fps.Numerator = 30000;
            fps.Denominator = 1001;

        }
        hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            width = 1280;
            height = 720;

        }

        interlace = MFGetAttributeUINT32(pType, MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);

        hr = MFGetAttributeRatio(pType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32*)&par.Numerator, (UINT32*)&par.Denominator);
        if (FAILED(hr))
        {
            par.Numerator = par.Denominator = 1;
        }

        cBitrate = MFGetAttributeUINT32(pType, MF_MT_AVG_BITRATE, 1000000);

        hr = MFCreateMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetGUID(MF_MT_MAJOR_TYPE, guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_RGB32);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = MFSetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, fps.Numerator, fps.Denominator);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = MFSetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, width, height);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetUINT32(MF_MT_INTERLACE_MODE, 2);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaType->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaType->SetUINT32(MF_MT_AVG_BITRATE, cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        // Return the pointer to the caller.
        *ppMediaType = pMediaType;
        (*ppMediaType)->AddRef();


    done:
        SafeRelease(&pMediaType);
        return hr;
    }
    ```

    

    <span data-ttu-id="22284-283">O exemplo de código a seguir adiciona dados privados de codec ao tipo de mídia de vídeo especificado.</span><span class="sxs-lookup"><span data-stu-id="22284-283">The following code example adds codec private data to the specified video media type.</span></span>

    ```C++
    //
    // AddPrivateData
    // Appends the private codec data to a media type.
    //
    // pMFT: The video encoder
    // pTypeOut: A video type from the encoder's type list.
    //
    // The function modifies pTypeOut by adding the codec data.
    //

    HRESULT AddPrivateData(IMFTransform *pMFT, IMFMediaType *pTypeOut)
    {
        HRESULT hr = S_OK;
        ULONG cbData = 0;
        BYTE *pData = NULL;

        IWMCodecPrivateData *pPrivData = NULL;

        DMO_MEDIA_TYPE mtOut = { 0 };

        // Convert the type to a DMO type.
        hr = MFInitAMMediaTypeFromMFMediaType(
            pTypeOut, 
            FORMAT_VideoInfo, 
            (AM_MEDIA_TYPE*)&mtOut
            );
        
        if (SUCCEEDED(hr))
        {
            hr = pMFT->QueryInterface(IID_PPV_ARGS(&pPrivData));
        }

        if (SUCCEEDED(hr))
        {
            hr = pPrivData->SetPartialOutputType(&mtOut);
        }

        //
        // Get the private codec data
        //

        // First get the buffer size.
        if (SUCCEEDED(hr))
        {
            hr = pPrivData->GetPrivateData(NULL, &cbData);
        }

        if (SUCCEEDED(hr))
        {
            pData = new BYTE[cbData];

            if (pData == NULL)
            {
                hr = E_OUTOFMEMORY;
            }
        }

        // Now get the data.
        if (SUCCEEDED(hr))
        {
            hr = pPrivData->GetPrivateData(pData, &cbData);
        }

        // Add the data to the media type.
        if (SUCCEEDED(hr))
        {
            hr = pTypeOut->SetBlob(MF_MT_USER_DATA, pData, cbData);
        }

        delete [] pData;
        MoFreeMediaType(&mtOut);
        SafeRelease(&pPrivData);
        return hr;
    }
    ```

    

### <a name="create-the-asf-contentinfo-object"></a><span data-ttu-id="22284-284">Criar o objeto ContentInfo do ASF</span><span class="sxs-lookup"><span data-stu-id="22284-284">Create the ASF ContentInfo Object</span></span>

<span data-ttu-id="22284-285">O objeto ASF ContentInfo é um componente de nível WMContainer que é projetado principalmente para armazenar informações de objeto de cabeçalho ASF.</span><span class="sxs-lookup"><span data-stu-id="22284-285">The ASF ContentInfo object is a WMContainer level component that is primarily designed to store ASF Header Object information.</span></span> <span data-ttu-id="22284-286">O coletor de arquivo ASF implementa o objeto ContentInfo para armazenar informações (em um repositório de propriedades) que serão usadas para gravar o objeto de cabeçalho ASF do arquivo codificado.</span><span class="sxs-lookup"><span data-stu-id="22284-286">The ASF file sink, implements the ContentInfo object in order to store information (in a property store) that will be used to write the ASF Header Object of the encoded file.</span></span> <span data-ttu-id="22284-287">Para fazer isso, você deve criar e configurar o seguinte conjunto de informações no objeto ContentInfo antes de iniciar a sessão de codificação.</span><span class="sxs-lookup"><span data-stu-id="22284-287">To do so, you must create and configure the following set of information on the ContentInfo object before starting the encoding session.</span></span>

1.  <span data-ttu-id="22284-288">Chame [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) para criar um objeto ContentInfo vazio.</span><span class="sxs-lookup"><span data-stu-id="22284-288">Call [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) to create an empty ContentInfo object.</span></span>

    <span data-ttu-id="22284-289">O exemplo de código a seguir cria um objeto ContentInfo vazio.</span><span class="sxs-lookup"><span data-stu-id="22284-289">The following code example creates an empty ContentInfo object.</span></span>

    ```C++
        // Create an empty ContentInfo object
        hr = MFCreateASFContentInfo(&pContentInfo);
        if (FAILED(hr))
        {
            goto done;
        }
    
    ```

    

2.  <span data-ttu-id="22284-290">Chame [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) para obter o armazenamento de propriedades no nível de fluxo do coletor de arquivo.</span><span class="sxs-lookup"><span data-stu-id="22284-290">Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) to get the file sink's stream-level property store.</span></span> <span data-ttu-id="22284-291">Nesta chamada, você precisa passar o número de fluxo que você atribuiu para o fluxo ao criar o perfil ASF.</span><span class="sxs-lookup"><span data-stu-id="22284-291">In this call, you need to pass the stream number that you assigned for the stream while creating the ASF profile.</span></span>
3.  <span data-ttu-id="22284-292">Defina as [Propriedades de codificação](configuring-the-encoder.md) no nível de fluxo no repositório de propriedades de fluxo do coletor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="22284-292">Set the stream-level [Encoding Properties](configuring-the-encoder.md) in the file sink's stream property store.</span></span> <span data-ttu-id="22284-293">Para obter mais informações, consulte "Propriedades de codificação de fluxo" em [Propriedades de configuração no coletor de arquivos](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="22284-293">For more information, see "Stream Encoding Properties" in [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>

    <span data-ttu-id="22284-294">O exemplo de código a seguir define as propriedades de nível de fluxo no repositório de propriedades do coletor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="22284-294">The following code example sets the stream level properties in the file sink's property store.</span></span>

    ```C++
            //Get stream's encoding property
            hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamID, &pContentInfoProps);
            if (FAILED(hr))
            {
                goto done;
            }

            //Set the stream-level encoding properties
            hr = SetEncodingProperties(guidMajor, pContentInfoProps);       
            if (FAILED(hr))
            {
                goto done;
            }

    
    ```

    

    <span data-ttu-id="22284-295">O exemplo de código a seguir mostra a implementação de setencodingproperties.</span><span class="sxs-lookup"><span data-stu-id="22284-295">The following code example shows the implementation for SetEncodingProperties.</span></span> <span data-ttu-id="22284-296">Essa função define as propriedades de codificação de nível de fluxo para CBR e VBR.</span><span class="sxs-lookup"><span data-stu-id="22284-296">This function sets stream level encoding properties for CBR and VBR.</span></span>

    ```C++
    //-------------------------------------------------------------------
    //  SetEncodingProperties
    //  Create a media source from a URL.
    //
    //  guidMT:  Major type of the stream, audio or video
    //  pProps:  A pointer to the property store in which 
    //           to set the required encoding properties.
    //-------------------------------------------------------------------

    HRESULT SetEncodingProperties (const GUID guidMT, IPropertyStore* pProps)
    {
        if (!pProps)
        {
            return E_INVALIDARG;
        }

        if (EncodingMode == NONE)
        {
            return MF_E_NOT_INITIALIZED;
        }
       
        HRESULT hr = S_OK;

        PROPVARIANT var;

        switch (EncodingMode)
        {
            case CBR:
                // Set VBR to false.
                hr = InitPropVariantFromBoolean(FALSE, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Set the video buffer window.
                if (guidMT == MFMediaType_Video)
                {
                    hr = InitPropVariantFromInt32(VIDEO_WINDOW_MSEC, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_VIDEOWINDOW, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                break;

            case VBR:
                //Set VBR to true.
                hr = InitPropVariantFromBoolean(TRUE, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Number of encoding passes is 1.

                hr = InitPropVariantFromInt32(1, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_PASSESUSED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Set the quality level.

                if (guidMT == MFMediaType_Audio)
                {
                    hr = InitPropVariantFromUInt32(98, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_DESIRED_VBRQUALITY, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                else if (guidMT == MFMediaType_Video)
                {
                    hr = InitPropVariantFromUInt32(95, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_VBRQUALITY, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                break;

            default:
                hr = E_UNEXPECTED;
                break;
        }    

    done:
        PropVariantClear(&var);
        return hr;
    }
    ```

    

4.  <span data-ttu-id="22284-297">Chame [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) para obter o repositório de propriedades globais do coletor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="22284-297">Call [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) to get the file sink's global property store.</span></span> <span data-ttu-id="22284-298">Nesta chamada, você precisa passar 0 no primeiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="22284-298">In this call, you need to pass 0 in the first parameter.</span></span> <span data-ttu-id="22284-299">Para obter mais informações, consulte "Propriedades do coletor de arquivo global" em [definindo propriedades no coletor de arquivos](setting-properties-in-the-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="22284-299">For more information, see "Global File Sink Properties" in [Setting Properties in the File Sink](setting-properties-in-the-file-sink.md).</span></span>
5.  <span data-ttu-id="22284-300">Defina a [**\_ taxa de \_ \_ bits de ajuste de MFPKEY ASFMEDIASINK**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) para Variant \_ true para garantir que os valores de Bucket de vazamento no Multiplexador de ASF sejam ajustados corretamente.</span><span class="sxs-lookup"><span data-stu-id="22284-300">Set the [**MFPKEY\_ASFMEDIASINK\_AUTOADJUST\_BITRATE**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) to VARIANT\_TRUE to ensure the leaky bucket values in the ASF multiplexer are adjusted properly.</span></span> <span data-ttu-id="22284-301">Para obter informações sobre essa propriedade, consulte "inicialização do Multiplexador e configurações de Bucket de vazamentos" em [criando o objeto multiplexador](creating-the-multiplexer-object.md).</span><span class="sxs-lookup"><span data-stu-id="22284-301">For information about this property, see "Multiplexer Initialization and Leaky Bucket Settings" in [Creating the Multiplexer Object](creating-the-multiplexer-object.md).</span></span>

    <span data-ttu-id="22284-302">O exemplo de código a seguir define as propriedades de nível de fluxo no repositório de propriedades do coletor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="22284-302">The following code example sets the stream level properties in the file sink's property store.</span></span>

    ```C++
        //Now we need to set global properties that will be set on the media sink
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(0, &pContentInfoProps);
        if (FAILED(hr))
        {
            goto done;
        }

        //Auto adjust Bitrate
        var.vt = VT_BOOL;
        var.boolVal = VARIANT_TRUE;

        hr = pContentInfoProps->SetValue(MFPKEY_ASFMEDIASINK_AUTOADJUST_BITRATE, var);
        
        //Initialize with the profile
        hr = pContentInfo->SetProfile(pProfile);
        if (FAILED(hr))
        {
            goto done;
        }
    ```

    

    > [!Note]  
    > <span data-ttu-id="22284-303">Há outras propriedades que você pode definir no nível global do coletor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="22284-303">There are other properties that you can set at the global level for the file sink.</span></span> <span data-ttu-id="22284-304">Para obter mais informações, consulte "Configurando o objeto ContentInfo com as configurações do codificador" em [definindo propriedades no objeto ContentInfo](setting-properties-in-the-contentinfo-object.md).</span><span class="sxs-lookup"><span data-stu-id="22284-304">For more information, see "Configuring the ContentInfo Object with Encoder Settings" in [Setting Properties in the ContentInfo Object](setting-properties-in-the-contentinfo-object.md).</span></span>

     

<span data-ttu-id="22284-305">Você usará o ContentInfo do ASF configurado para criar um objeto de ativação para o coletor de arquivos ASF (descrito na próxima seção).</span><span class="sxs-lookup"><span data-stu-id="22284-305">You will use the configured ASF ContentInfo to create an activation object for the ASF file sink (described in the next section).</span></span>

<span data-ttu-id="22284-306">Se você estiver criando um [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)(coletor de arquivos fora de processo), ou seja, usando um objeto de ativação, poderá usar o objeto ContentInfo configurado para instanciar o coletor de mídia ASF (descrito na próxima seção).</span><span class="sxs-lookup"><span data-stu-id="22284-306">If you are creating an out-of-process file sink ([**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)), that is by using an activation object, you can use the configured ContentInfo object to instantiate the ASF media sink (described in the next section).</span></span> <span data-ttu-id="22284-307">Se você estiver criando um coletor de arquivos em processo ([**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)), em vez de criar o objeto ContentInfo vazio, conforme descrito na etapa 1, obtenha uma referência à interface [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) chamando **IMFMediaSink:: QueryInterface** no coletor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="22284-307">If you are creating an in-process file sink ([**MFCreateASFMediaSink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)), instead of creating the empty ContentInfo object as described in step 1, get a reference to the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface by calling **IMFMediaSink::QueryInterface** on the file sink.</span></span> <span data-ttu-id="22284-308">Em seguida, você deve configurar o objeto ContentInfo conforme descrito nesta seção.</span><span class="sxs-lookup"><span data-stu-id="22284-308">You must then configure the ContentInfo object as described in this section.</span></span>

### <a name="create-the-asf-file-sink"></a><span data-ttu-id="22284-309">Criar o coletor de arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="22284-309">Create the ASF File Sink</span></span>

<span data-ttu-id="22284-310">Nesta etapa do tutorial, você usará o ASF ContentInfo configurado, que você criou na etapa anterior, para criar um objeto de ativação para o coletor de arquivo ASF chamando a função [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) .</span><span class="sxs-lookup"><span data-stu-id="22284-310">In this step of the tutorial, you will use the configured ASF ContentInfo, which you created in the previous step, to create an activation object for the ASF file sink by calling the [**MFCreateASFMediaSinkActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) function.</span></span> <span data-ttu-id="22284-311">Para obter mais informações, consulte [criando o coletor de arquivo ASF](creating-the-asf-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="22284-311">For more information, see [Creating the ASF File Sink](creating-the-asf-file-sink.md).</span></span>

<span data-ttu-id="22284-312">O exemplo de código a seguir cria o objeto de ativação para o coletor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="22284-312">The following code example creates the activation object for the file sink.</span></span>


```C++
    //Create the activation object for the  file sink
    hr = MFCreateASFMediaSinkActivate(sURL, pContentInfo, &pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

```



## <a name="build-the-partial-encoding-topology"></a><span data-ttu-id="22284-313">Criar a topologia de codificação parcial</span><span class="sxs-lookup"><span data-stu-id="22284-313">Build the Partial Encoding Topology</span></span>

<span data-ttu-id="22284-314">Em seguida, você criará uma topologia de codificação parcial criando nós de topologia para a origem de mídia, os codificadores de mídia do Windows necessários e o coletor de arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="22284-314">Next, you will build a partial encoding topology by creating topology nodes for the media source, the required Windows Media encoders, and the ASF file sink.</span></span> <span data-ttu-id="22284-315">Depois de adicionar os nós de topologia, você conectará os nós de origem, transformação e coletor.</span><span class="sxs-lookup"><span data-stu-id="22284-315">After adding the topology nodes, you will connect the source, transform, and the sink nodes.</span></span> <span data-ttu-id="22284-316">Antes de adicionar nós de topologia, você deve criar um objeto de topologia vazio chamando [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).</span><span class="sxs-lookup"><span data-stu-id="22284-316">Before adding topology nodes, you must create an empty topology object by calling [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).</span></span>

### <a name="create-the-source-topology-node-for-the-media-source"></a><span data-ttu-id="22284-317">Criar o nó de topologia de origem para a origem de mídia</span><span class="sxs-lookup"><span data-stu-id="22284-317">Create the Source Topology Node for the Media Source</span></span>

<span data-ttu-id="22284-318">Nesta etapa, você criará o nó de topologia de origem para a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="22284-318">In this step, you will create the source topology node for the media source.</span></span>

<span data-ttu-id="22284-319">Para criar esse nó, você precisará das seguintes referências:</span><span class="sxs-lookup"><span data-stu-id="22284-319">To create this node you need the following references:</span></span>

-   <span data-ttu-id="22284-320">Um ponteiro para a origem de mídia que você criou na etapa descrita na seção "criar a fonte de mídia" deste tutorial.</span><span class="sxs-lookup"><span data-stu-id="22284-320">A pointer to the media source that you created in the step described in the "Create the Media Source" section of this tutorial.</span></span>
-   <span data-ttu-id="22284-321">Um ponteiro para o descritor de apresentação para a origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="22284-321">A pointer to the presentation descriptor for the media source.</span></span> <span data-ttu-id="22284-322">Você pode obter uma referência à interface IMFPresentationDescriptor da origem da mídia chamando [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span><span class="sxs-lookup"><span data-stu-id="22284-322">You can get a reference to IMFPresentationDescriptor interface of the media source by calling [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).</span></span>
-   <span data-ttu-id="22284-323">Um ponteiro para o descritor de fluxo para cada fluxo na origem de mídia para o qual você criou um fluxo de destino na etapa descrita na seção "criar o objeto de perfil ASF" deste tutorial.</span><span class="sxs-lookup"><span data-stu-id="22284-323">A pointer to the stream descriptor for each stream in the media source for which you have created a target stream in the step described in the "Create the ASF Profile Object" section of this tutorial.</span></span>

<span data-ttu-id="22284-324">Para obter mais informações sobre como criar nós de origem e código de exemplo, consulte [criando nós de origem](creating-source-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="22284-324">For more information about creating source nodes and code example, see [Creating Source Nodes](creating-source-nodes.md).</span></span>

<span data-ttu-id="22284-325">O exemplo de código a seguir cria uma topologia parcial adicionando o nó de origem e os nós de transformação necessários.</span><span class="sxs-lookup"><span data-stu-id="22284-325">The following code example creates a partial topology by adding the source node and the required transform nodes.</span></span> <span data-ttu-id="22284-326">Esse código chama as funções auxiliares AddSourceNode e AddTransformOutputNodes.</span><span class="sxs-lookup"><span data-stu-id="22284-326">This code calls the helper functions AddSourceNode, and AddTransformOutputNodes.</span></span> <span data-ttu-id="22284-327">Essas funções são incluídas posteriormente neste tutorial.</span><span class="sxs-lookup"><span data-stu-id="22284-327">These functions are included later in this tutorial.</span></span>


```C++
//-------------------------------------------------------------------
//  BuildPartialTopology
//  Create a partial encoding topology by adding the source and the sink.
//
//  pSource:  A pointer to the media source to enumerate the source streams.
//  pSinkActivate: A pointer to the activation object for ASF file sink.
//  ppTopology:  Receives a pointer to the topology.
//-------------------------------------------------------------------

HRESULT BuildPartialTopology(
       IMFMediaSource *pSource, 
       IMFActivate* pSinkActivate,
       IMFTopology** ppTopology)
{
    if (!pSource || !pSinkActivate)
    {
        return E_INVALIDARG;
    }
    if (!ppTopology)
    {
        return E_POINTER;
    }

    HRESULT hr = S_OK;

    IMFPresentationDescriptor* pPD = NULL;
    IMFStreamDescriptor *pStreamDesc = NULL;
    IMFMediaTypeHandler* pMediaTypeHandler = NULL;
    IMFMediaType* pSrcType = NULL;

    IMFTopology* pTopology = NULL;
    IMFTopologyNode* pSrcNode = NULL;
    IMFTopologyNode* pEncoderNode = NULL;
    IMFTopologyNode* pOutputNode = NULL;


    DWORD cElems = 0;
    DWORD dwSrcStream = 0;
    DWORD StreamID = 0;
    GUID guidMajor = GUID_NULL;
    BOOL fSelected = FALSE;


    //Create the topology that represents the encoding pipeline
    hr = MFCreateTopology (&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

        
    hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pPD->GetStreamDescriptorCount(&dwSrcStream);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD iStream = 0; iStream < dwSrcStream; iStream++)
    {
        hr = pPD->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);
        if (FAILED(hr))
        {
            goto done;
        }

        if (!fSelected)
        {
            continue;
        }

        hr = AddSourceNode(pTopology, pSource, pPD, pStreamDesc, &pSrcNode);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStreamDesc->GetMediaTypeHandler (&pMediaTypeHandler);
        if (FAILED(hr))
        {
            goto done;
        }
        
        hr = pStreamDesc->GetStreamIdentifier(&StreamID);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaTypeHandler->GetMediaTypeByIndex(0, &pSrcType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pSrcType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = AddTransformOutputNodes(pTopology, pSinkActivate, pSrcType, &pEncoderNode);
        if (FAILED(hr))
        {
            goto done;
        }

        //now we have the transform node, connect it to the source node
        hr = pSrcNode->ConnectOutput(0, pEncoderNode, 0);
        if (FAILED(hr))
        {
            goto done;
        }
                

        SafeRelease(&pStreamDesc);
        SafeRelease(&pMediaTypeHandler);
        SafeRelease(&pSrcType);
        SafeRelease(&pEncoderNode);
        SafeRelease(&pOutputNode);
        guidMajor = GUID_NULL;
    }

    *ppTopology = pTopology;
   (*ppTopology)->AddRef();


    wprintf_s(L"Partial Topology Built.\n");

done:
    SafeRelease(&pStreamDesc);
    SafeRelease(&pMediaTypeHandler);
    SafeRelease(&pSrcType);
    SafeRelease(&pEncoderNode);
    SafeRelease(&pOutputNode);
    SafeRelease(&pTopology);

    return hr;
}
```



<span data-ttu-id="22284-328">O exemplo de código a seguir cria e adiciona o nó de topologia de origem à topologia de codificação.</span><span class="sxs-lookup"><span data-stu-id="22284-328">The following code example creates and adds the source topology node to the encoding topology.</span></span> <span data-ttu-id="22284-329">Ele usa ponteiros para um objeto de topologia anteriormente, a origem de mídia para enumerar os fluxos de origem, o descritor de apresentação da origem de mídia e o descritor de fluxo da origem de mídia.</span><span class="sxs-lookup"><span data-stu-id="22284-329">It takes pointers to a previously topology object, the media source to enumerate the source streams, the media source's presentation descriptor, and the media source's stream descriptor.</span></span> <span data-ttu-id="22284-330">O chamador recebe um ponteiro para o nó de topologia de origem.</span><span class="sxs-lookup"><span data-stu-id="22284-330">The caller receives a pointer to the source topology node.</span></span>


```C++
// Add a source node to a topology.
HRESULT AddSourceNode(
    IMFTopology *pTopology,           // Topology.
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    IMFStreamDescriptor *pSD,         // Stream descriptor.
    IMFTopologyNode **ppNode)         // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_SOURCESTREAM_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the attributes.
    hr = pNode->SetUnknown(MF_TOPONODE_SOURCE, pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_PRESENTATION_DESCRIPTOR, pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_STREAM_DESCRIPTOR, pSD);
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



### <a name="instantiate-the-required-encoders-and-create-the-transform-nodes"></a><span data-ttu-id="22284-331">Instanciar os codificadores necessários e criar os nós de transformação</span><span class="sxs-lookup"><span data-stu-id="22284-331">Instantiate the Required Encoders and Create the Transform Nodes</span></span>

<span data-ttu-id="22284-332">O pipeline de Media Foundation não insere automaticamente os codificadores do Windows Media necessários para os fluxos que ele deve codificar.</span><span class="sxs-lookup"><span data-stu-id="22284-332">The Media Foundation pipeline does not automatically insert the required Windows Media encoders for the streams that it must encode.</span></span> <span data-ttu-id="22284-333">O aplicativo deve adicionar os codificadores manualmente.</span><span class="sxs-lookup"><span data-stu-id="22284-333">The application must add the encoders manually.</span></span> <span data-ttu-id="22284-334">Para fazer isso, enumere os fluxos no perfil ASF que você criou na etapa descrita na seção "criar o objeto de perfil ASF" deste tutorial.</span><span class="sxs-lookup"><span data-stu-id="22284-334">To do so, enumerate the streams in the ASF profile that you created in the step described in the "Create the ASF Profile Object" section of this tutorial.</span></span> <span data-ttu-id="22284-335">Para cada fluxo na origem e o fluxo correspondente no perfil, crie uma instância dos codificadores necessários.</span><span class="sxs-lookup"><span data-stu-id="22284-335">For each stream in the source and the corresponding stream in the profile, instantiate the required encoders.</span></span> <span data-ttu-id="22284-336">Para esta etapa, você precisa de um ponteiro para o objeto de ativação do coletor de arquivos que você criou na etapa descrita na seção "criar o coletor de arquivo ASF" deste tutorial.</span><span class="sxs-lookup"><span data-stu-id="22284-336">For this step, you need a pointer to the activation object for the file sink that you created in the step described in the "Create the ASF File Sink" section of this tutorial.</span></span>

<span data-ttu-id="22284-337">Para obter uma visão geral sobre a criação de codificadores por meio de objetos de ativação, consulte [usando objetos de ativação de um codificador](using-an-encoder-s-activation-objects.md).</span><span class="sxs-lookup"><span data-stu-id="22284-337">For an overview on creating encoders through activation objects, see [Using an Encoder's Activation Objects](using-an-encoder-s-activation-objects.md).</span></span>

<span data-ttu-id="22284-338">O procedimento a seguir descreve as etapas necessárias para criar uma instância dos codificadores necessários.</span><span class="sxs-lookup"><span data-stu-id="22284-338">The following procedure describes the steps required to instantiate the required encoders.</span></span>

1.  <span data-ttu-id="22284-339">Obtenha uma referência ao objeto ContentInfo do coletor chamando [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) no coletor de arquivos ativar e, em seguida, consultando o [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) no coletor de arquivos chamando **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="22284-339">Get a reference to the sink's ContentInfo object by calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) on the file sink activate and then querying for [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) from the file sink by calling **QueryInterface**.</span></span>
2.  <span data-ttu-id="22284-340">Obtenha o perfil de ASF associado ao objeto ContentInfo chamando [**IMFASFContentInfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span><span class="sxs-lookup"><span data-stu-id="22284-340">Get the ASF profile associated with the ContentInfo object by calling [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span></span>
3.  <span data-ttu-id="22284-341">Enumere os fluxos no perfil.</span><span class="sxs-lookup"><span data-stu-id="22284-341">Enumerate the streams in the profile.</span></span> <span data-ttu-id="22284-342">Para isso, você precisará da contagem de fluxos e de uma referência para a interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) de cada fluxo.</span><span class="sxs-lookup"><span data-stu-id="22284-342">For this you will need the stream count and a reference to each stream's [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span>

    <span data-ttu-id="22284-343">Chame os seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="22284-343">Call the following methods:</span></span>

    -   [<span data-ttu-id="22284-344">**IMFASFProfile::GetStreamCount**</span><span class="sxs-lookup"><span data-stu-id="22284-344">**IMFASFProfile::GetStreamCount**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)
    -   [<span data-ttu-id="22284-345">**IMFASFProfile:: GetStream**</span><span class="sxs-lookup"><span data-stu-id="22284-345">**IMFASFProfile::GetStream**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream)

4.  <span data-ttu-id="22284-346">Para cada fluxo, obtenha o tipo principal e as propriedades de codificação do fluxo do objeto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="22284-346">For each stream get the major type and the stream's encoding properties from the ContentInfo object.</span></span>

    <span data-ttu-id="22284-347">Chame os seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="22284-347">Call the following methods:</span></span>

    -   [<span data-ttu-id="22284-348">**IMFASFStreamConfig:: GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="22284-348">**IMFASFStreamConfig::GetMediaType**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype)
    -   [<span data-ttu-id="22284-349">**IMFMediaType:: getmajortype**</span><span class="sxs-lookup"><span data-stu-id="22284-349">**IMFMediaType::GetMajorType**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype)
    -   [<span data-ttu-id="22284-350">**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="22284-350">**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore)

        <span data-ttu-id="22284-351">Para essa chamada, você precisa do número de fluxo recuperado pela chamada [**IMFASFProfile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) .</span><span class="sxs-lookup"><span data-stu-id="22284-351">For this call you need the stream number retrieved by the [**IMFASFProfile::GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) call.</span></span>

5.  <span data-ttu-id="22284-352">Dependendo do tipo de fluxo, áudio ou vídeo, instancie o objeto de ativação para o codificador chamando [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) ou [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate).</span><span class="sxs-lookup"><span data-stu-id="22284-352">Depending on the type of the stream, audio or video, instantiate the activation object for the encoder by calling [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) or [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate).</span></span>

    <span data-ttu-id="22284-353">Para chamar essas funções, você precisará das seguintes referências:</span><span class="sxs-lookup"><span data-stu-id="22284-353">To call these functions, you need the following references:</span></span>

    -   <span data-ttu-id="22284-354">Um ponteiro para o tipo de mídia do fluxo recuperado por [**IMFASFStreamConfig:: GetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype) na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="22284-354">A pointer to the stream's media type retrieved by [**IMFASFStreamConfig::GetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype) in the previous step.</span></span>
    -   <span data-ttu-id="22284-355">Um ponteiro para o armazenamento de propriedade de codificação do fluxo recuperado por [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore).</span><span class="sxs-lookup"><span data-stu-id="22284-355">A pointer to the stream's encoding property store retrieved by [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore).</span></span> <span data-ttu-id="22284-356">Ao passar um ponteiro para o repositório de propriedades, as propriedades do fluxo definidas no coletor de arquivos são copiadas no MFT do codificador.</span><span class="sxs-lookup"><span data-stu-id="22284-356">By passing a pointer to the property store, the stream properties set in the file sink are copied on the encoder MFT.</span></span>

6.  <span data-ttu-id="22284-357">Atualize o parâmetro de Bucket de vazamento para o fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="22284-357">Update the leaky bucket parameter for the audio stream.</span></span>

    <span data-ttu-id="22284-358">[**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) define o tipo de saída no MFT do codificador subjacente para o codec de áudio do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="22284-358">[**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) sets the output type on the underlying encoder MFT for the Windows Media audio codec.</span></span> <span data-ttu-id="22284-359">Depois que o tipo de mídia de saída é definido, o codificador Obtém a taxa média de bits do tipo de mídia de saída, calcula a taxa de bits da janela de buffer Rage e define os valores de Bucket de vazamento que serão usados durante a sessão de codificação.</span><span class="sxs-lookup"><span data-stu-id="22284-359">After the output media type is set, the encoder gets the average bit rate from the output media type, calculates the buffer window rage bit rate, and sets the leaky bucket values that will be used during the encoding session.</span></span> <span data-ttu-id="22284-360">Você pode atualizar esses valores no coletor de arquivos consultando o codificador ou definindo valores personalizados.</span><span class="sxs-lookup"><span data-stu-id="22284-360">You can update these values in the file sink by either querying the encoder or setting custom values.</span></span> <span data-ttu-id="22284-361">Para atualizar os valores, você precisará do seguinte conjunto de informações:</span><span class="sxs-lookup"><span data-stu-id="22284-361">To update values you need the following set of information:</span></span>

    -   <span data-ttu-id="22284-362">Taxa média de bits: Obtenha a taxa média de bits do conjunto de atributos de [**\_ \_ \_ \_ bytes \_ por \_ segundo de áudio MF MT**](mf-mt-audio-avg-bytes-per-second-attribute.md) definido no tipo de mídia de saída selecionado durante a negociação do tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="22284-362">Average bit rate: Get the average bit rate from the [**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute set on the output media type that is selected during media type negotiation.</span></span>
    -   <span data-ttu-id="22284-363">Janela buffer: você pode recuperá-la chamando [**IWMCodecLeakyBucket:: GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md).</span><span class="sxs-lookup"><span data-stu-id="22284-363">Buffer window: you can retrieve it by calling [**IWMCodecLeakyBucket::GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md).</span></span>
    -   <span data-ttu-id="22284-364">Tamanho do buffer inicial: Defina como 0.</span><span class="sxs-lookup"><span data-stu-id="22284-364">Initial buffer size: Set to 0.</span></span>

    <span data-ttu-id="22284-365">Crie uma matriz de DWORDs e defina o valor na propriedade [**MFPKEY \_ ASFSTREAMSINK \_ corrigida de \_ LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) do coletor de fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="22284-365">Create an array of DWORDs and set the value in the [**MFPKEY\_ASFSTREAMSINK\_CORRECTED\_LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) property of the audio stream sink.</span></span> <span data-ttu-id="22284-366">Se você não fornecer os valores atualizados, a sessão de mídia os definirá adequadamente.</span><span class="sxs-lookup"><span data-stu-id="22284-366">If you do not provide the updated values, the Media Session sets them appropriately.</span></span>

    <span data-ttu-id="22284-367">Para obter mais informações, consulte [o modelo de buffer de buckets de vazamento](the-leaky-bucket-buffer-model.md).</span><span class="sxs-lookup"><span data-stu-id="22284-367">For more information, see [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md).</span></span>

<span data-ttu-id="22284-368">Os objetos de ativação criados na etapa 5 devem ser adicionados à topologia como nós de topologia de transformação.</span><span class="sxs-lookup"><span data-stu-id="22284-368">The activation objects created in step 5 must be added to the topology as transform topology nodes.</span></span> <span data-ttu-id="22284-369">Para obter mais informações e código de exemplo, consulte "criando um nó de transformação de um objeto de ativação" em [criando nós de transformação](creating-transform-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="22284-369">For more information and code example, see "Creating a Transform Node from an Activation Object" in [Creating Transform Nodes](creating-transform-nodes.md).</span></span>

<span data-ttu-id="22284-370">O exemplo de código a seguir cria e adiciona o codificador necessário ativa.</span><span class="sxs-lookup"><span data-stu-id="22284-370">The following code example creates and adds the required encoder activates.</span></span> <span data-ttu-id="22284-371">Ele usa ponteiros para um objeto de topologia criado anteriormente, o objeto de ativação do coletor de arquivos e o tipo de mídia do fluxo de origem.</span><span class="sxs-lookup"><span data-stu-id="22284-371">It takes pointers to a previously created topology object, the file sink's activation object and the source stream's media type.</span></span> <span data-ttu-id="22284-372">Ele também chama AddOutputNode (consulte o próximo exemplo de código) que cria e adiciona o nó do coletor à topologia de codificação.</span><span class="sxs-lookup"><span data-stu-id="22284-372">It also calls AddOutputNode (see next code example) that creates and adds the sink node to the encoding topology.</span></span> <span data-ttu-id="22284-373">O chamador recebe um ponteiro para o nó de topologia de origem.</span><span class="sxs-lookup"><span data-stu-id="22284-373">It The caller receives a pointer to the source topology node.</span></span>


```C++
//-------------------------------------------------------------------
//  AddTransformOutputNodes
//  Creates and adds the sink node to the encoding topology.
//  Creates and adds the required encoder activates.

//  pTopology:  A pointer to the topology.
//  pSinkActivate:  A pointer to the file sink's activation object.
//  pSourceType: A pointer to the source stream's media type.
//  ppNode:  Receives a pointer to the topology node.
//-------------------------------------------------------------------

HRESULT AddTransformOutputNodes(
    IMFTopology* pTopology,
    IMFActivate* pSinkActivate,
    IMFMediaType* pSourceType,
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    if (!pTopology || !pSinkActivate || !pSourceType)
    {
        return E_INVALIDARG;
    }

    IMFTopologyNode* pEncNode = NULL;
    IMFTopologyNode* pOutputNode = NULL;
    IMFASFContentInfo* pContentInfo = NULL;
    IMFASFProfile* pProfile = NULL;
    IMFASFStreamConfig* pStream = NULL;
    IMFMediaType* pMediaType = NULL;
    IPropertyStore* pProps = NULL;
    IMFActivate *pEncoderActivate = NULL;
    IMFMediaSink *pSink = NULL; 

    GUID guidMT = GUID_NULL;
    GUID guidMajor = GUID_NULL;

    DWORD cStreams = 0;
    WORD wStreamNumber = 0;

    HRESULT hr = S_OK;
        
    hr = pSourceType->GetMajorType(&guidMajor);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the node.
    hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pEncNode);
    if (FAILED(hr))
    {
        goto done;
    }
    
    //Activate the sink
    hr = pSinkActivate->ActivateObject(__uuidof(IMFMediaSink), (void**)&pSink);
    if (FAILED(hr))
    {
        goto done;
    }
    //find the media type in the sink
    //Get content info from the sink
    hr = pSink->QueryInterface(__uuidof(IMFASFContentInfo), (void**)&pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }
    

    hr = pContentInfo->GetProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->GetStreamCount(&cStreams);
    if (FAILED(hr))
    {
        goto done;
    }

    for(DWORD index = 0; index < cStreams ; index++)
    {
        hr = pProfile->GetStream(index, &wStreamNumber, &pStream);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pStream->GetMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->GetMajorType(&guidMT);
        if (FAILED(hr))
        {
            goto done;
        }
        if (guidMT!=guidMajor)
        {
            SafeRelease(&pStream);
            SafeRelease(&pMediaType);
            guidMT = GUID_NULL;

            continue;
        }
        //We need to activate the encoder
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamNumber, &pProps);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMT == MFMediaType_Audio)
        {
             hr = MFCreateWMAEncoderActivate(pMediaType, pProps, &pEncoderActivate);
            if (FAILED(hr))
            {
                goto done;
            }
            wprintf_s(L"Audio Encoder created. Stream Number: %d .\n", wStreamNumber);

            break;
        }
        if (guidMT == MFMediaType_Video)
        {
            hr = MFCreateWMVEncoderActivate(pMediaType, pProps, &pEncoderActivate);
            if (FAILED(hr))
            {
                goto done;
            }
            wprintf_s(L"Video Encoder created. Stream Number: %d .\n", wStreamNumber);

            break;
        }
    }

    // Set the object pointer.
    hr = pEncNode->SetObject(pEncoderActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the node to the topology.
    hr = pTopology->AddNode(pEncNode);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the output node to this node.
    hr = AddOutputNode(pTopology, pSinkActivate, wStreamNumber, &pOutputNode);
    if (FAILED(hr))
    {
        goto done;
    }

    //now we have the output node, connect it to the transform node
    hr = pEncNode->ConnectOutput(0, pOutputNode, 0);
    if (FAILED(hr))
    {
        goto done;
    }

   // Return the pointer to the caller.
    *ppNode = pEncNode;
    (*ppNode)->AddRef();


done:
    SafeRelease(&pEncNode);
    SafeRelease(&pOutputNode);
    SafeRelease(&pEncoderActivate);
    SafeRelease(&pMediaType);
    SafeRelease(&pProps);
    SafeRelease(&pStream);
    SafeRelease(&pProfile);
    SafeRelease(&pContentInfo);
    SafeRelease(&pSink);
    return hr;
}
```



### <a name="create-the-output-topology-nodes-for-the-file-sink"></a><span data-ttu-id="22284-374">Criar os nós de topologia de saída para o coletor de arquivos</span><span class="sxs-lookup"><span data-stu-id="22284-374">Create the Output Topology Nodes for the File Sink</span></span>

<span data-ttu-id="22284-375">Nesta etapa, você criará o nó de topologia de saída para o coletor de arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="22284-375">In this step, you will create the output topology node for the ASF file sink.</span></span>

<span data-ttu-id="22284-376">Para criar esse nó, você precisará das seguintes referências:</span><span class="sxs-lookup"><span data-stu-id="22284-376">To create this node you need the following references:</span></span>

-   <span data-ttu-id="22284-377">Um ponteiro para o objeto de ativação que você criou na etapa descrita na seção "criar o coletor de arquivo ASF" deste tutorial.</span><span class="sxs-lookup"><span data-stu-id="22284-377">A pointer to the activation object that you created in the step described in the "Create the ASF File Sink" section of this tutorial.</span></span>
-   <span data-ttu-id="22284-378">Os números de fluxo para identificar os coletores de fluxo adicionados ao coletor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="22284-378">The stream numbers to identify the stream sinks added to the file sink.</span></span> <span data-ttu-id="22284-379">Os números de fluxo correspondem à identificação do fluxo que foi definido durante a criação do fluxo.</span><span class="sxs-lookup"><span data-stu-id="22284-379">The stream numbers match the stream's identification that was set during stream creation.</span></span>

<span data-ttu-id="22284-380">Para obter mais informações sobre como criar nós de saída e um exemplo de código, consulte "criando um nó de saída de um objeto de ativação" em [criando nós de saída](creating-output-nodes.md).</span><span class="sxs-lookup"><span data-stu-id="22284-380">For more information about creating output nodes and code example, see "Creating an Output Node from an Activation Object" in [Creating Output Nodes](creating-output-nodes.md).</span></span>

<span data-ttu-id="22284-381">Se você não estiver usando o objeto de ativação para o coletor de arquivos, deverá enumerar os coletores de fluxo no coletor de arquivos ASF e definir cada coletor de fluxo como o nó de saída na topologia.</span><span class="sxs-lookup"><span data-stu-id="22284-381">If you are not using activation object for the file sink, you must enumerate the stream sinks in the ASF file sink and set each stream sink as the output node in the topology.</span></span> <span data-ttu-id="22284-382">Para obter informações sobre a enumeração do coletor de fluxo, consulte "enumerando coletores de fluxo" em [adicionando informações de fluxo ao coletor de arquivo ASF](adding-stream-information-to-the-asf-file-sink.md).</span><span class="sxs-lookup"><span data-stu-id="22284-382">For information about stream sink enumeration, see "Enumerating Stream Sinks" in [Adding Stream Information to the ASF File Sink](adding-stream-information-to-the-asf-file-sink.md).</span></span>

<span data-ttu-id="22284-383">O exemplo de código a seguir cria e adiciona o nó do coletor à topologia de codificação.</span><span class="sxs-lookup"><span data-stu-id="22284-383">The following code example creates and adds the sink node to the encoding topology.</span></span> <span data-ttu-id="22284-384">Ele usa ponteiros para um objeto de topologia criado anteriormente, o objeto de ativação do coletor de arquivos e o número de identificação do fluxo.</span><span class="sxs-lookup"><span data-stu-id="22284-384">It takes pointers to a previously created topology object, the file sink's activation object and the stream's identification number.</span></span> <span data-ttu-id="22284-385">O chamador recebe um ponteiro para o nó de topologia de origem.</span><span class="sxs-lookup"><span data-stu-id="22284-385">It The caller receives a pointer to the source topology node.</span></span>


```C++
// Add an output node to a topology.
HRESULT AddOutputNode(
    IMFTopology *pTopology,     // Topology.
    IMFActivate *pActivate,     // Media sink activation object.
    DWORD dwId,                 // Identifier of the stream sink.
    IMFTopologyNode **ppNode)   // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_OUTPUT_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the object pointer.
    hr = pNode->SetObject(pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the stream sink ID attribute.
    hr = pNode->SetUINT32(MF_TOPONODE_STREAMID, dwId);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUINT32(MF_TOPONODE_NOSHUTDOWN_ON_REMOVE, FALSE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



<span data-ttu-id="22284-386">O exemplo de código a seguir enumera os coletores de fluxo para um determinado coletor de mídia.</span><span class="sxs-lookup"><span data-stu-id="22284-386">The following code example enumerates the stream sinks for a given media sink.</span></span>


```C++
//-------------------------------------------------------------------
//  EnumerateStreamSinks
//  Enumerates the stream sinks within the specified media sink.
//
//  pSink:  A pointer to the media sink.
//-------------------------------------------------------------------
HRESULT EnumerateStreamSinks (IMFMediaSink* pSink)
{
    if (!pSink)
    {
        return E_INVALIDARG;
    }
    
    IMFStreamSink* pStreamSink = NULL;
    DWORD cStreamSinks = 0;

    HRESULT hr = pSink->GetStreamSinkCount(&cStreamSinks);
    if (FAILED(hr))
    {
        goto done;
    }

    for(DWORD index = 0; index < cStreamSinks; index++)
    {
        hr = pSink->GetStreamSinkByIndex (index, &pStreamSink);
        if (FAILED(hr))
        {
            goto done;
        }

        //Use the stream sink
        //Not shown.
    }
done:
    SafeRelease(&pStreamSink);

    return hr;
}
```



### <a name="connect-the-source-transform-and-sink-nodes"></a><span data-ttu-id="22284-387">Conectar os nós de origem, transformação e coletor</span><span class="sxs-lookup"><span data-stu-id="22284-387">Connect the Source, Transform, and Sink Nodes</span></span>

<span data-ttu-id="22284-388">Nesta etapa, você conectará o nó de origem ao nó de transformação que faz referência à codificação ativada que você criou na etapa descrita na seção "instanciar os codificadores necessários e criar os nós de transformação" deste tutorial.</span><span class="sxs-lookup"><span data-stu-id="22284-388">In this step, you will connect the source node to the transform node referencing the encoding activates that you created in the step described in the "Instantiate the Required Encoders and Create the Transform Nodes" section of this tutorial.</span></span> <span data-ttu-id="22284-389">O nó de transformação será conectado ao nó de saída que contém o objeto de ativação para o coletor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="22284-389">The transform node will be connected to the output node containing the activation object for the file sink.</span></span>

## <a name="handling-the-encoding-session"></a><span data-ttu-id="22284-390">Manipulando a sessão de codificação</span><span class="sxs-lookup"><span data-stu-id="22284-390">Handling the Encoding Session</span></span>

<span data-ttu-id="22284-391">Na etapa, você executará as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="22284-391">In the step, you will perform the following steps:</span></span>

1.  <span data-ttu-id="22284-392">Chame [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) para criar uma sessão de codificação.</span><span class="sxs-lookup"><span data-stu-id="22284-392">Call [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create an encoding session.</span></span>
2.  <span data-ttu-id="22284-393">Chame [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) para definir a topologia de codificação na sessão.</span><span class="sxs-lookup"><span data-stu-id="22284-393">Call [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) to set the encoding topology on the session.</span></span> <span data-ttu-id="22284-394">Se a chamada for concluída, a sessão de mídia avaliará os nós de topologia e inserirá objetos de transformação adicionais, como um decodificador que converte a origem compactada especificada em amostras não compactadas para alimentar como entrada para o codificador.</span><span class="sxs-lookup"><span data-stu-id="22284-394">If the call completes, the Media Session evaluates the topology nodes and inserts additional transform objects such as a decoder that converts the specified compressed source to uncompressed samples to feed as input to the encoder.</span></span>
3.  <span data-ttu-id="22284-395">Chame [**IMFMediaSession:: GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) para solicitar os eventos gerados pela sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="22284-395">Call [**IMFMediaSession::GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) to request for the events raised by the Media Session.</span></span>

    <span data-ttu-id="22284-396">No loop de eventos, você iniciará e fechará a sessão de codificação dependendo dos eventos gerados pela sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="22284-396">In the event loop you will start and close the encoding session depending on the events raised by the Media Session.</span></span> <span data-ttu-id="22284-397">A chamada [**IMFMediaSession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) resulta na sessão de mídia que gera o evento [MESessionTopologyStatus](mesessiontopologystatus.md) com o \_ sinalizador MF TOPOSTATUS \_ Ready definido.</span><span class="sxs-lookup"><span data-stu-id="22284-397">The [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) call results in Media Session raising the [MESessionTopologyStatus](mesessiontopologystatus.md) event with the MF\_TOPOSTATUS\_READY flag set.</span></span> <span data-ttu-id="22284-398">Todos os eventos são gerados de forma assíncrona e um aplicativo pode recuperar esses eventos de forma síncrona ou assíncrona.</span><span class="sxs-lookup"><span data-stu-id="22284-398">All events are generated asynchronously and an application can retrieve these events synchronously or asynchronously.</span></span> <span data-ttu-id="22284-399">Como o aplicativo neste tutorial é um aplicativo de console e o bloqueio de threads de interface do usuário não é uma preocupação, obteremos os eventos da sessão de mídia de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="22284-399">Because the application in this tutorial is a console application and blocking user interface threads is not a concern, we will get the events from Media Session synchronously.</span></span>

    <span data-ttu-id="22284-400">Para obter os eventos de forma assíncrona, seu aplicativo deve implementar a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="22284-400">To get the events asynchronously, your application must implement the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> <span data-ttu-id="22284-401">Para obter mais informações e um exemplo de implementação dessa interface, consulte "manipulando eventos de sessão" em [How to Play Media files with Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="22284-401">For more information and an example implementation of this interface, see "Handling Session Events" in [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span>

<span data-ttu-id="22284-402">No loop de eventos para obter eventos de sessão de mídia, aguarde o evento [MESessionTopologyStatus](mesessiontopologystatus.md) que é gerado quando a topologia [**IMFMediaSession::**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) Seté concluída e a topologia é resolvida.</span><span class="sxs-lookup"><span data-stu-id="22284-402">In the event loop for getting Media Session events, wait for the [MESessionTopologyStatus](mesessiontopologystatus.md) event that is raised when the [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) completes and the topology is resolved.</span></span> <span data-ttu-id="22284-403">Após obter o evento MESessionTopologyStatus, inicie a sessão de codificação chamando [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span><span class="sxs-lookup"><span data-stu-id="22284-403">Upon getting the MESessionTopologyStatus event, start the encoding session by calling [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span> <span data-ttu-id="22284-404">A sessão de mídia gera o evento [MEEndOfPresentation](meendofpresentation.md) quando todas as operações de codificação são concluídas.</span><span class="sxs-lookup"><span data-stu-id="22284-404">The Media Session generates the [MEEndOfPresentation](meendofpresentation.md) event when all of the encoding operations are complete.</span></span> <span data-ttu-id="22284-405">Esse evento deve ser tratado para codificação de VBR e é discutido na próxima seção "atualizar propriedades de codificação no coletor de arquivos para codificação de VBR" deste tutorial.</span><span class="sxs-lookup"><span data-stu-id="22284-405">This event must be handled for VBR encoding and is discussed in the next section "Update Encoding Properties on the File Sink for VBR Encoding" of this tutorial.</span></span>

<span data-ttu-id="22284-406">A sessão de mídia gera o objeto de cabeçalho ASF e finaliza o arquivo quando a sessão de codificação é concluída e, em seguida, gera o evento [MESessionClosed](mesessionclosed.md) .</span><span class="sxs-lookup"><span data-stu-id="22284-406">The Media Session generates the ASF Header Object and finalizes the file when the encoding session completes and then raises the [MESessionClosed](mesessionclosed.md) event.</span></span> <span data-ttu-id="22284-407">Esse evento deve ser tratado com a execução de operações de desligamento apropriadas na sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="22284-407">This event must be handled by performing proper shutdown operations on the Media Session.</span></span> <span data-ttu-id="22284-408">Para iniciar as operações de desligamento, chame [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span><span class="sxs-lookup"><span data-stu-id="22284-408">To begin the shutdown operations, call [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span> <span data-ttu-id="22284-409">Depois que a sessão de codificação for fechada, você não poderá definir outra topologia para codificação na mesma instância de sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="22284-409">After the encoding session is closed, you cannot set another topology for encoding on the same Media Session instance.</span></span> <span data-ttu-id="22284-410">Para codificar outro arquivo, a sessão de mídia atual deve ser fechada e liberada e a nova topologia deve ser definida em uma sessão de mídia recém-criada.</span><span class="sxs-lookup"><span data-stu-id="22284-410">To encode another file, the current Media Session must be closed and released and the new topology must be set on a newly created Media Session.</span></span> <span data-ttu-id="22284-411">O exemplo de código a seguir cria a sessão de mídia, define a topologia de codificação e manipula os eventos de sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="22284-411">The following code example creates the Media Session, sets the encoding topology and handles the Media Session events.</span></span>

<span data-ttu-id="22284-412">O exemplo de código a seguir cria a sessão de mídia, define a topologia de codificação e controla a sessão de codificação manipulando eventos da sessão de mídia.</span><span class="sxs-lookup"><span data-stu-id="22284-412">The following code example creates the Media Session, sets the encoding topology, and controls the encoding session by handling events from the Media Session.</span></span>


```C++
//-------------------------------------------------------------------
//  Encode
//  Controls the encoding session and handles events from the media session.
//
//  pTopology:  A pointer to the encoding topology.
//-------------------------------------------------------------------

HRESULT Encode(IMFTopology *pTopology)
{
    if (!pTopology)
    {
        return E_INVALIDARG;
    }
    
    IMFMediaSession *pSession = NULL;
    IMFMediaEvent* pEvent = NULL;
    IMFTopology* pFullTopology = NULL;
    IUnknown* pTopoUnk = NULL;


    MediaEventType meType = MEUnknown;  // Event type

    HRESULT hr = S_OK;
    HRESULT hrStatus = S_OK;            // Event status
                
    MF_TOPOSTATUS TopoStatus = MF_TOPOSTATUS_INVALID; // Used with MESessionTopologyStatus event.    
        

    hr = MFCreateMediaSession(NULL, &pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSession->SetTopology(MFSESSION_SETTOPOLOGY_IMMEDIATE, pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get media session events synchronously
    while (1)
    {
        hr = pSession->GetEvent(0, &pEvent);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEvent->GetType(&meType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEvent->GetStatus(&hrStatus);
        if (FAILED(hr))
        {
            goto done;
        }
        if (FAILED(hrStatus))
        {
            hr = hrStatus;
            goto done;
        }

       switch(meType)
        {
            case MESessionTopologyStatus:
                {
                    // Get the status code.
                    MF_TOPOSTATUS status = (MF_TOPOSTATUS)MFGetAttributeUINT32(
                                             pEvent, MF_EVENT_TOPOLOGY_STATUS, MF_TOPOSTATUS_INVALID);

                    if (status == MF_TOPOSTATUS_READY)
                    {
                        PROPVARIANT var;
                        PropVariantInit(&var);
                        wprintf_s(L"Topology resolved and set on the media session.\n");

                        hr = pSession->Start(NULL, &var);
                        if (FAILED(hr))
                        {
                            goto done;
                        }

                    }
                    if (status == MF_TOPOSTATUS_STARTED_SOURCE)
                    {
                        wprintf_s(L"Encoding started.\n");
                        break;
                    }
                    if (status == MF_TOPOSTATUS_ENDED)
                    {
                        wprintf_s(L"Encoding complete.\n");
                        hr = pSession->Close();
                        if (FAILED(hr))
                        {
                            goto done;
                        }

                        break;
                    }
                }
                break;


            case MESessionEnded:
                wprintf_s(L"Encoding complete.\n");
                hr = pSession->Close();
                if (FAILED(hr))
                {
                    goto done;
                }
                break;

            case MEEndOfPresentation:
                {
                    if (EncodingMode == VBR)
                    {
                        hr = pSession->GetFullTopology(MFSESSION_GETFULLTOPOLOGY_CURRENT, 0, &pFullTopology);
                        if (FAILED(hr))
                        {
                            goto done;
                        }
                        hr = PostEncodingUpdate(pFullTopology);
                        if (FAILED(hr))
                        {
                            goto done;
                        }
                        wprintf_s(L"Updated sinks for VBR. \n");
                    }
                }
                break;

            case MESessionClosed:
                wprintf_s(L"Encoding session closed.\n");

                hr = pSession->Shutdown();
                goto done;
        }
        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pEvent);

    }
done:
    SafeRelease(&pEvent);
    SafeRelease(&pSession);
    SafeRelease(&pFullTopology);
    SafeRelease(&pTopoUnk);
    return hr;
}
```



## <a name="update-encoding-properties-in-the-file-sink"></a><span data-ttu-id="22284-413">Atualizar propriedades de codificação no coletor de arquivos</span><span class="sxs-lookup"><span data-stu-id="22284-413">Update Encoding Properties in the File Sink</span></span>

<span data-ttu-id="22284-414">Determinadas propriedades de codificação, como a taxa de bits de codificação e os valores de buckets de vazamento precisos, não são conhecidas até que a codificação seja concluída, especialmente para a codificação de VBR.</span><span class="sxs-lookup"><span data-stu-id="22284-414">Certain encoding properties such as the encoding bit rate and the accurate leaky bucket values are not known until the encoding is complete, especially for VBR encoding.</span></span> <span data-ttu-id="22284-415">Para obter os valores corretos, o aplicativo deve aguardar o evento [MEEndOfPresentation](meendofpresentation.md) que indica que a sessão de codificação foi concluída.</span><span class="sxs-lookup"><span data-stu-id="22284-415">To get the correct values the application must wait for the [MEEndOfPresentation](meendofpresentation.md) event that indicates that the encoding session is complete.</span></span> <span data-ttu-id="22284-416">Os valores de Bucket de vazamento devem ser atualizados no coletor para que o objeto de cabeçalho ASF possa refletir os valores precisos.</span><span class="sxs-lookup"><span data-stu-id="22284-416">The leaky bucket values must be updated in the sink so that the ASF Header Object can reflect the accurate values.</span></span>

<span data-ttu-id="22284-417">O procedimento a seguir descreve as etapas necessárias para percorrer os nós na topologia de codificação para obter o nó de coletor de arquivo e definir as propriedades de Bucket de vazamento necessárias.</span><span class="sxs-lookup"><span data-stu-id="22284-417">The following procedure describes the steps required to traverse the nodes in the encoding topology to get the file sink node and set the required leaky bucket properties.</span></span>

<span data-ttu-id="22284-418">**Para atualizar os valores da propriedade post Encoding no coletor de arquivo ASF**</span><span class="sxs-lookup"><span data-stu-id="22284-418">**To update the post encoding property values on the ASF file sink**</span></span>

1.  <span data-ttu-id="22284-419">Chame [**IMFTopology:: GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) para obter a coleção de nós de saída da topologia de codificação.</span><span class="sxs-lookup"><span data-stu-id="22284-419">Call [**IMFTopology::GetOutputNodeCollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) to get the output node collection from the encoding topology.</span></span>
2.  <span data-ttu-id="22284-420">Para cada nó, obtenha um ponteiro para o coletor de fluxo no nó chamando [**IMFTopologyNode:: GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject).</span><span class="sxs-lookup"><span data-stu-id="22284-420">For each node, get a pointer to the stream sink in the node by calling [**IMFTopologyNode::GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject).</span></span> <span data-ttu-id="22284-421">Consulta para a interface [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) no ponteiro [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) retornado por **IMFTopologyNode:: GetObject**.</span><span class="sxs-lookup"><span data-stu-id="22284-421">Query for the [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) interface on the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer returned by **IMFTopologyNode::GetObject**.</span></span>
3.  <span data-ttu-id="22284-422">Para cada coletor de fluxo, obtenha o nó downstream (codificador) chamando [**IMFTopologyNode:: getinput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinput).</span><span class="sxs-lookup"><span data-stu-id="22284-422">For each stream sink get the downstream node (encoder) by calling [**IMFTopologyNode::GetInput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinput).</span></span>
4.  <span data-ttu-id="22284-423">Consulte o nó para obter o ponteiro [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) do nó do codificador.</span><span class="sxs-lookup"><span data-stu-id="22284-423">Query the node to get the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) pointer from the encoder node.</span></span>
5.  <span data-ttu-id="22284-424">Consulte o codificador para o ponteiro [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para obter o armazenamento de propriedade de codificação do codificador.</span><span class="sxs-lookup"><span data-stu-id="22284-424">Query the encoder for the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to get the encoding property store from the encoder.</span></span>
6.  <span data-ttu-id="22284-425">Consulte o coletor de fluxo para o ponteiro [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para obter o repositório de propriedades do coletor de fluxo.</span><span class="sxs-lookup"><span data-stu-id="22284-425">Query the stream sink for the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to get the stream sink's property store.</span></span>
7.  <span data-ttu-id="22284-426">Chame [**IPropertyStore:: GetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para obter os valores de propriedade necessários do repositório de propriedades do codificador e copie-os para o repositório de propriedades do coletor de fluxo chamando **IPropertyStore:: SetValue**.</span><span class="sxs-lookup"><span data-stu-id="22284-426">Call [**IPropertyStore::GetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore) to get the required property values from the encoder's property store and copy them to the stream sink's property store by calling **IPropertyStore::SetValue**.</span></span>

<span data-ttu-id="22284-427">A tabela a seguir mostra os valores de propriedade de codificação post que devem ser definidos no coletor de fluxo para o fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="22284-427">The following table shows the post encoding property values that must be set on the stream sink for the video stream.</span></span>



| <span data-ttu-id="22284-428">Tipo de codificação</span><span class="sxs-lookup"><span data-stu-id="22284-428">Encoding type</span></span>                                                                                  | <span data-ttu-id="22284-429">Nome da propriedade (GetValue)</span><span class="sxs-lookup"><span data-stu-id="22284-429">Property name (GetValue)</span></span>                                                                        | <span data-ttu-id="22284-430">Nome da propriedade (DefinirValor)</span><span class="sxs-lookup"><span data-stu-id="22284-430">Property name (SetValue)</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22284-431">Codificação de taxa de bits constante</span><span class="sxs-lookup"><span data-stu-id="22284-431">Constant Bit Rate Encoding</span></span>](constant-bit-rate-encoding.md)                                   | <span data-ttu-id="22284-432">MFPKEY \_ BAVG</span><span class="sxs-lookup"><span data-stu-id="22284-432">MFPKEY\_BAVG</span></span><br/> <span data-ttu-id="22284-433">MFPKEY \_ RAVG</span><span class="sxs-lookup"><span data-stu-id="22284-433">MFPKEY\_RAVG</span></span><br/>                                                 | <span data-ttu-id="22284-434">MFPKEY \_ stat \_ BAVG</span><span class="sxs-lookup"><span data-stu-id="22284-434">MFPKEY\_STAT\_BAVG</span></span><br/> <span data-ttu-id="22284-435">MFPKEY \_ stat \_ RAVG</span><span class="sxs-lookup"><span data-stu-id="22284-435">MFPKEY\_STAT\_RAVG</span></span><br/>                                                             |
| [<span data-ttu-id="22284-436">Codificação de taxa de bits variável baseada em qualidade</span><span class="sxs-lookup"><span data-stu-id="22284-436">Quality-Based Variable Bit Rate Encoding</span></span>](quality-based-variable-bit-rate--vbr--encoding.md) | <span data-ttu-id="22284-437">MFPKEY \_ BAVG</span><span class="sxs-lookup"><span data-stu-id="22284-437">MFPKEY\_BAVG</span></span><br/> <span data-ttu-id="22284-438">MFPKEY \_ RAVG</span><span class="sxs-lookup"><span data-stu-id="22284-438">MFPKEY\_RAVG</span></span><br/> <span data-ttu-id="22284-439">MFPKEY \_ BMAX</span><span class="sxs-lookup"><span data-stu-id="22284-439">MFPKEY\_BMAX</span></span><br/> <span data-ttu-id="22284-440">MFPKEY \_ RMAX</span><span class="sxs-lookup"><span data-stu-id="22284-440">MFPKEY\_RMAX</span></span><br/> | <span data-ttu-id="22284-441">MFPKEY \_ stat \_ BAVG</span><span class="sxs-lookup"><span data-stu-id="22284-441">MFPKEY\_STAT\_BAVG</span></span><br/> <span data-ttu-id="22284-442">MFPKEY \_ stat \_ RAVG</span><span class="sxs-lookup"><span data-stu-id="22284-442">MFPKEY\_STAT\_RAVG</span></span><br/> <span data-ttu-id="22284-443">MFPKEY \_ stat \_ BMAX</span><span class="sxs-lookup"><span data-stu-id="22284-443">MFPKEY\_STAT\_BMAX</span></span><br/> <span data-ttu-id="22284-444">MFPKEY \_ stat \_ RMAX</span><span class="sxs-lookup"><span data-stu-id="22284-444">MFPKEY\_STAT\_RMAX</span></span><br/> |



 

<span data-ttu-id="22284-445">O exemplo de código a seguir define os valores de propriedade de pós-codificação.</span><span class="sxs-lookup"><span data-stu-id="22284-445">The following code example sets the post-encoding property values.</span></span>


```C++
//-------------------------------------------------------------------
//  PostEncodingUpdate
//  Updates the file sink with encoding properties set on the encoder
//  during the encoding session.
    //1. Get the output nodes
    //2. For each node, get the downstream node
    //3. For the downstream node, get the MFT
    //4. Get the property store
    //5. Get the required values
    //6. Set them on the stream sink
//
//  pTopology: A pointer to the full topology retrieved from the media session.
//-------------------------------------------------------------------

HRESULT PostEncodingUpdate(IMFTopology *pTopology)
{
    if (!pTopology)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_OK;

    IMFCollection* pOutputColl = NULL;
    IUnknown* pNodeUnk = NULL;
    IMFMediaType* pType = NULL;
    IMFTopologyNode* pNode = NULL;
    IUnknown* pSinkUnk = NULL;
    IMFStreamSink* pStreamSink = NULL;
    IMFTopologyNode* pEncoderNode = NULL;
    IUnknown* pEncoderUnk = NULL;
    IMFTransform* pEncoder = NULL;
    IPropertyStore* pStreamSinkProps = NULL;
    IPropertyStore* pEncoderProps = NULL;

    GUID guidMajorType = GUID_NULL;

    PROPVARIANT var;
    PropVariantInit( &var );

    DWORD cElements = 0;

    hr = pTopology->GetOutputNodeCollection( &pOutputColl);
    if (FAILED(hr))
    {
        goto done;
    }


    hr = pOutputColl->GetElementCount(&cElements);
    if (FAILED(hr))
    {
        goto done;
    }


    for(DWORD index = 0; index < cElements; index++)
    {
        hr = pOutputColl->GetElement(index, &pNodeUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNodeUnk->QueryInterface(IID_IMFTopologyNode, (void**)&pNode);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetInputPrefType(0, &pType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pType->GetMajorType( &guidMajorType );
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetObject(&pSinkUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pSinkUnk->QueryInterface(IID_IMFStreamSink, (void**)&pStreamSink);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetInput( 0, &pEncoderNode, NULL );
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoderNode->GetObject(&pEncoderUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoderUnk->QueryInterface(IID_IMFTransform, (void**)&pEncoder);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStreamSink->QueryInterface(IID_IPropertyStore, (void**)&pStreamSinkProps);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoder->QueryInterface(IID_IPropertyStore, (void**)&pEncoderProps);
        if (FAILED(hr))
        {
            goto done;
        }

        if( guidMajorType == MFMediaType_Video )
        {            
            hr = pEncoderProps->GetValue( MFPKEY_BAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_RAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RAVG, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_BMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_RMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }
        }
        else if( guidMajorType == MFMediaType_Audio )
        {      
            hr = pEncoderProps->GetValue( MFPKEY_STAT_BAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }
            
            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_RAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }
            
            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_BMAX, &var);
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_RMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RMAX, var );         
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_WMAENC_AVGBYTESPERSEC, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_WMAENC_AVGBYTESPERSEC, var );         
            if (FAILED(hr))
            {
                goto done;
            }
        } 
        PropVariantClear( &var ); 
   }
done:
    SafeRelease (&pOutputColl);
    SafeRelease (&pNodeUnk);
    SafeRelease (&pType);
    SafeRelease (&pNode);
    SafeRelease (&pSinkUnk);
    SafeRelease (&pStreamSink);
    SafeRelease (&pEncoderNode);
    SafeRelease (&pEncoderUnk);
    SafeRelease (&pEncoder);
    SafeRelease (&pStreamSinkProps);
    SafeRelease (&pEncoderProps);

    return hr;
   
}
```



## <a name="implement-main"></a><span data-ttu-id="22284-446">Implementar principal</span><span class="sxs-lookup"><span data-stu-id="22284-446">Implement Main</span></span>

<span data-ttu-id="22284-447">O exemplo de código a seguir mostra a função main do seu aplicativo de console.</span><span class="sxs-lookup"><span data-stu-id="22284-447">The following code example shows the main function of your console application.</span></span>


```C++
int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 4)
    {
        wprintf_s(L"Usage: %s inputaudio.mp3, %s output.wm*, %Encoding Type: CBR, VBR\n");
        return 0;
    }


    HRESULT             hr = S_OK;

    IMFMediaSource* pSource = NULL;
    IMFTopology* pTopology = NULL;
    IMFActivate* pFileSinkActivate = NULL;

    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);
    if (FAILED(hr))
    {
        goto done;
    }

    //Set the requested encoding mode
    if (wcscmp(argv[3], L"CBR")==0)
    {
        EncodingMode = CBR;
    }
    else if (wcscmp(argv[3], L"VBR")==0)
    {
        EncodingMode = VBR;
    }
    else
    {
        EncodingMode = CBR;
    }

    // Start up Media Foundation platform.
    hr = MFStartup(MF_VERSION);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the media source
    hr = CreateMediaSource(argv[1], &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the file sink activate
    hr = CreateMediaSink(argv[2], pSource, &pFileSinkActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    //Build the encoding topology.
    hr = BuildPartialTopology(pSource, pFileSinkActivate, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Instantiate the media session and start encoding
    hr = Encode(pTopology);
    if (FAILED(hr))
    {
        goto done;
    }


done:
    // Clean up.
    SafeRelease(&pSource);
    SafeRelease(&pTopology);
    SafeRelease(&pFileSinkActivate);

    MFShutdown();
    CoUninitialize();

    if (FAILED(hr))
    {
        wprintf_s(L"Could not create the output file due to 0x%X\n", hr);
    }
    return 0;
}
```



## <a name="test-the-output-file"></a><span data-ttu-id="22284-448">Testar o arquivo de saída</span><span class="sxs-lookup"><span data-stu-id="22284-448">Test the Output File</span></span>

<span data-ttu-id="22284-449">A lista a seguir descreve uma lista de verificação para testar o arquivo codificado.</span><span class="sxs-lookup"><span data-stu-id="22284-449">The following list describes a check list for testing the encoded file.</span></span> <span data-ttu-id="22284-450">Esses valores podem ser verificados na caixa de diálogo Propriedades do arquivo que você pode exibir clicando com o botão direito do mouse no arquivo codificado e selecionando **Propriedades** no menu de contexto.</span><span class="sxs-lookup"><span data-stu-id="22284-450">These values can be checked in the file properties dialog box that you can display by right-clicking the encoded file and selecting **Properties** from the context menu.</span></span>

-   <span data-ttu-id="22284-451">O caminho do arquivo codificado é preciso.</span><span class="sxs-lookup"><span data-stu-id="22284-451">The path of the encoded file is accurate.</span></span>
-   <span data-ttu-id="22284-452">O tamanho do arquivo é maior que zero KB e a duração da reprodução corresponde à duração do arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="22284-452">The size of the file is more than zero KB and the play duration matches the source file's duration.</span></span>
-   <span data-ttu-id="22284-453">Para o fluxo de vídeo, verifique a largura e a altura do quadro, taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="22284-453">For the video stream, check the frame width and height, frame rate.</span></span> <span data-ttu-id="22284-454">Esses valores devem corresponder aos valores que você especificou no perfil ASF criado na etapa descrita na seção "criar o objeto de perfil ASF".</span><span class="sxs-lookup"><span data-stu-id="22284-454">These values should match the values that you specified in the ASF profile that you created in the step described in the section "Create the ASF Profile Object".</span></span>
-   <span data-ttu-id="22284-455">Para o fluxo de áudio, a taxa de bits deve ser próxima ao valor especificado no tipo de mídia de destino.</span><span class="sxs-lookup"><span data-stu-id="22284-455">For the audio stream, the bit rate must be close to the value you specified on the target media type.</span></span>
-   <span data-ttu-id="22284-456">Abra o arquivo no Windows Media Player e verifique a qualidade da codificação.</span><span class="sxs-lookup"><span data-stu-id="22284-456">Open the file in Windows Media Player and check the quality of the encoding.</span></span>
-   <span data-ttu-id="22284-457">Abra o arquivo ASF no ASFViewer para ver a estrutura de um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="22284-457">Open the ASF file in ASFViewer to see the structure of an ASF file.</span></span> <span data-ttu-id="22284-458">Essa ferramenta pode ser baixada deste [site da Microsoft](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span><span class="sxs-lookup"><span data-stu-id="22284-458">This tool can be downloaded from this [Microsoft website](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span></span>

## <a name="common-error-codes-and-debugging-tips"></a><span data-ttu-id="22284-459">Códigos de erro comuns e dicas de depuração</span><span class="sxs-lookup"><span data-stu-id="22284-459">Common Error Codes and Debugging Tips</span></span>

<span data-ttu-id="22284-460">A lista a seguir descreve os códigos de erro comuns que você pode receber e as dicas de depuração.</span><span class="sxs-lookup"><span data-stu-id="22284-460">The following list describes the common error codes that your might receive and the debugging tips.</span></span>

-   <span data-ttu-id="22284-461">A chamada para [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) interrompe o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="22284-461">The call to [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) stalls the application.</span></span>

    <span data-ttu-id="22284-462">Verifique se você inicializou a plataforma Media Foundation chamando [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span><span class="sxs-lookup"><span data-stu-id="22284-462">Make sure that you have initialized the Media Foundation platform by calling [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span></span> <span data-ttu-id="22284-463">Essa função configura a plataforma assíncrona que é usada por todos os métodos que iniciam operações assíncronas, como [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), internamente.</span><span class="sxs-lookup"><span data-stu-id="22284-463">This function sets up the asynchronous platform that is used by all methods that start asynchronous operations, such as [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), internally.</span></span>

-   <span data-ttu-id="22284-464">[**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) retorna HRESULT 0x80070002 "o sistema não pode localizar o arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="22284-464">[**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) returns HRESULT 0x80070002 "The system cannot find the file specified.</span></span>

    <span data-ttu-id="22284-465">Verifique se o nome do arquivo de entrada especificado pelo usuário no primeiro argumento existe.</span><span class="sxs-lookup"><span data-stu-id="22284-465">Make sure that the input file name specified by the user in the first argument exists.</span></span>

-   <span data-ttu-id="22284-466">HRESULT 0x80070020 "o processo não pode acessar o arquivo porque ele está sendo usado por outro processo.</span><span class="sxs-lookup"><span data-stu-id="22284-466">HRESULT 0x80070020 "The process cannot access the file because it is being used by another process.</span></span> <span data-ttu-id="22284-467">"</span><span class="sxs-lookup"><span data-stu-id="22284-467">"</span></span>

    <span data-ttu-id="22284-468">Certifique-se de que a entrada e os arquivos de saída não estejam atualmente em uso por outro recurso no sistema.</span><span class="sxs-lookup"><span data-stu-id="22284-468">Make sure that the input and the output files are not currently in use by another resource in the system.</span></span>

-   <span data-ttu-id="22284-469">Chamadas para métodos [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) retornam MF \_ E \_ INVALIDMEDIATYPE.</span><span class="sxs-lookup"><span data-stu-id="22284-469">Calls to [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) methods return MF\_E\_INVALIDMEDIATYPE.</span></span>

    <span data-ttu-id="22284-470">Certifique-se de que as seguintes condições sejam verdadeiras:</span><span class="sxs-lookup"><span data-stu-id="22284-470">Make sure that the following conditions are true:</span></span>

    -   <span data-ttu-id="22284-471">O tipo de entrada ou o tipo de saída especificado é compatível com os tipos de mídia aos quais o codificador dá suporte.</span><span class="sxs-lookup"><span data-stu-id="22284-471">The input type or the output type that you specified is compatible with media types that the encoder supports.</span></span>
    -   <span data-ttu-id="22284-472">Os tipos de mídia que você especificou estão completos.</span><span class="sxs-lookup"><span data-stu-id="22284-472">The media types that you specified are complete.</span></span> <span data-ttu-id="22284-473">Para que os tipos de mídia sejam concluídos, consulte os atributos necessários nas seções "criar um tipo de mídia de áudio compactado" e "criar um tipo de mídia de vídeo compactado" deste tutorial.</span><span class="sxs-lookup"><span data-stu-id="22284-473">For media types to be complete, see the required attributes in the "Create a Compressed Audio Media Type" and "Create a Compressed Video Media Type" sections of this tutorial.</span></span>
    -   <span data-ttu-id="22284-474">Verifique se você definiu a taxa de bits de destino no tipo de mídia parcial ao qual está adicionando os dados privados do codec.</span><span class="sxs-lookup"><span data-stu-id="22284-474">Make sure that you have set the target bit rate on the partial media type to which you are adding the codec private data.</span></span>

-   <span data-ttu-id="22284-475">A sessão de mídia retorna MF \_ E \_ não há suporte para \_ \_ o tipo de D3D no status do evento.</span><span class="sxs-lookup"><span data-stu-id="22284-475">The Media Session returns MF\_E\_UNSUPPORTED\_D3D\_TYPE in the event status.</span></span>

    <span data-ttu-id="22284-476">Esse erro é retornado quando o tipo de mídia da origem indica um modo de entrelaçamento misto sem suporte pelo codificador de vídeo do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="22284-476">This error is returned when the source's media type indicates a mixed interlace mode that is not supported by Windows Media Video encoder.</span></span> <span data-ttu-id="22284-477">Se o tipo de mídia de vídeo compactado estiver definido para usar o modo progressivo, o pipeline deverá usar uma transformação de desentrelaçamento.</span><span class="sxs-lookup"><span data-stu-id="22284-477">If your compressed video media type is set to use progressive mode, the pipeline must use a de-interlacing transform.</span></span> <span data-ttu-id="22284-478">Como o pipeline não consegue encontrar uma correspondência (indicada por esse código de erro), você deve inserir um desentrelaçador (processador de vídeo transcodificar) entre os nós do decodificador e do codificador manualmente.</span><span class="sxs-lookup"><span data-stu-id="22284-478">Because the pipeline is unable to find a match (indicated by this error code), you must insert a de-interlacer (transcode video processor) between the decoder and encoder nodes manually.</span></span>

-   <span data-ttu-id="22284-479">A sessão de mídia retorna E \_ INVALIDARG no status do evento.</span><span class="sxs-lookup"><span data-stu-id="22284-479">The Media Session returns E\_INVALIDARG in the event status.</span></span>

    <span data-ttu-id="22284-480">Esse erro é retornado quando os atributos de tipo de mídia da origem não são compatíveis com os atributos do tipo de mídia de saída definido no codificador de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="22284-480">This error is returned when the source's media type attributes are not compatible with the attributes of the output media type set on the Windows Media encoder.</span></span>

-   <span data-ttu-id="22284-481">[**IWMCodecPrivateData:: GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) retorna HRESULT 0x80040203 "ocorreu um erro de sintaxe ao tentar avaliar uma cadeia de caracteres de consulta"</span><span class="sxs-lookup"><span data-stu-id="22284-481">[**IWMCodecPrivateData::GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) returns HRESULT 0x80040203 "A syntax error occurred trying to evaluate a query string"</span></span>

    <span data-ttu-id="22284-482">Verifique se o tipo de entrada está definido no MFT do codificador.</span><span class="sxs-lookup"><span data-stu-id="22284-482">Make sure that the input type is set on the encoder MFT.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22284-483">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="22284-483">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22284-484">Componentes ASF da camada de pipeline</span><span class="sxs-lookup"><span data-stu-id="22284-484">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)
</dt> </dl>

 

 
