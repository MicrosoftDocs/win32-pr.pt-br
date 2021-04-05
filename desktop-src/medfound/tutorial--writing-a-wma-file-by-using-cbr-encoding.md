---
description: Este tutorial demonstra como gravar um novo arquivo de áudio (. WMA) extraindo o conteúdo de mídia de um arquivo de áudio descompactado (. wav) e, em seguida, compactando-o no formato ASF.
ms.assetid: f310c6ed-52e7-4828-9d4c-2f7ced9080c5
title: 'Tutorial: gravando um arquivo WMA usando objetos WMContainer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d156b75ced6cde2953ec90362ed13b0cc53bb83c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827798"
---
# <a name="tutorial-writing-a-wma-file-by-using-wmcontainer-objects"></a><span data-ttu-id="cc751-103">Tutorial: gravando um arquivo WMA usando objetos WMContainer</span><span class="sxs-lookup"><span data-stu-id="cc751-103">Tutorial: Writing a WMA File by Using WMContainer Objects</span></span>

<span data-ttu-id="cc751-104">Este tutorial demonstra como gravar um novo arquivo de áudio (. WMA) extraindo o conteúdo de mídia de um arquivo de áudio descompactado (. wav) e, em seguida, compactando-o no formato ASF.</span><span class="sxs-lookup"><span data-stu-id="cc751-104">This tutorial demonstrates writing a new audio file (.wma) by extracting media content from an uncompressed audio file (.wav) and then compressing it in ASF format.</span></span> <span data-ttu-id="cc751-105">O modo de codificação usado para a conversão é [constante de codificação de taxa de bits](constant-bit-rate-encoding.md) (CBR).</span><span class="sxs-lookup"><span data-stu-id="cc751-105">The encoding mode used for the conversion is [Constant Bit Rate Encoding](constant-bit-rate-encoding.md) (CBR).</span></span> <span data-ttu-id="cc751-106">Nesse modo, antes da sessão de codificação, o aplicativo especifica uma taxa de bits de destino que o codificador deve atingir.</span><span class="sxs-lookup"><span data-stu-id="cc751-106">In this mode, before the encoding session, the application specifies a target bit rate that the encoder must achieve.</span></span>

<span data-ttu-id="cc751-107">Neste tutorial, você criará um aplicativo de console que usa os nomes de dados de entrada e saída como argumentos.</span><span class="sxs-lookup"><span data-stu-id="cc751-107">In this tutorial, you will create a console application that takes the input and output filenames as arguments.</span></span> <span data-ttu-id="cc751-108">O aplicativo obtém os exemplos de mídia descompactados de um aplicativo de análise de arquivo Wave, que é fornecido com este tutorial.</span><span class="sxs-lookup"><span data-stu-id="cc751-108">The application gets the uncompressed media samples from a wave file parsing application, which is provided with this tutorial.</span></span> <span data-ttu-id="cc751-109">Esses exemplos são enviados para o codificador para conversão no formato Windows Media Audio 9.</span><span class="sxs-lookup"><span data-stu-id="cc751-109">These samples are sent to the encoder for conversion to Windows Media Audio 9 format.</span></span> <span data-ttu-id="cc751-110">O codificador está configurado para codificação de CBR e usa a primeira taxa de bits disponível durante a negociação do tipo de mídia como a taxa de bits de destino.</span><span class="sxs-lookup"><span data-stu-id="cc751-110">The encoder is configured for CBR encoding and uses the first bit rate available during media type negotiation as the target bit rate.</span></span> <span data-ttu-id="cc751-111">Os exemplos codificados são enviados para o multiplexador para pacotes no formato de dados ASF.</span><span class="sxs-lookup"><span data-stu-id="cc751-111">The encoded samples are sent to the multiplexer for packetization in ASF data format.</span></span> <span data-ttu-id="cc751-112">Esses pacotes serão gravados em um fluxo de bytes que representa o objeto de dados ASF.</span><span class="sxs-lookup"><span data-stu-id="cc751-112">These packets will be written to a byte stream that represents the ASF Data Object.</span></span> <span data-ttu-id="cc751-113">Depois que a seção de dados estiver pronta, você criará um arquivo de áudio ASF e gravará o novo objeto de cabeçalho ASF que consolida todas as informações de cabeçalho e, em seguida, acrescentará o fluxo de bytes do objeto de dados ASF.</span><span class="sxs-lookup"><span data-stu-id="cc751-113">After the data section is ready, you will create an ASF audio file and write the new ASF Header Object that consolidates all the header information and then append the ASF Data Object byte stream.</span></span>

<span data-ttu-id="cc751-114">Este tutorial contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="cc751-114">This tutorial contains the following sections:</span></span>

-   [<span data-ttu-id="cc751-115">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="cc751-115">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="cc751-116">Terminologia</span><span class="sxs-lookup"><span data-stu-id="cc751-116">Terminology</span></span>](#terminology)
-   [<span data-ttu-id="cc751-117">1. configurar o projeto</span><span class="sxs-lookup"><span data-stu-id="cc751-117">1. Set up the Project</span></span>](#1-set-up-the-project)
-   [<span data-ttu-id="cc751-118">2. declarar funções auxiliares</span><span class="sxs-lookup"><span data-stu-id="cc751-118">2. Declare Helper Functions</span></span>](#2-declare-helper-functions)
-   [<span data-ttu-id="cc751-119">3. abrir um arquivo de áudio</span><span class="sxs-lookup"><span data-stu-id="cc751-119">3. Open an Audio File</span></span>](#3-open-an-audio-file)
-   [<span data-ttu-id="cc751-120">4. configurar o codificador</span><span class="sxs-lookup"><span data-stu-id="cc751-120">4. Configure the Encoder</span></span>](#4-configure-the-encoder)
-   [<span data-ttu-id="cc751-121">5. Crie o objeto ContentInfo do ASF.</span><span class="sxs-lookup"><span data-stu-id="cc751-121">5. Create the ASF ContentInfo object.</span></span>](#5-create-the-asf-contentinfo-object)
-   [<span data-ttu-id="cc751-122">6. criar o multiplexador de ASF</span><span class="sxs-lookup"><span data-stu-id="cc751-122">6. Create the ASF Multiplexer</span></span>](#6-create-the-asf-multiplexer)
-   [<span data-ttu-id="cc751-123">7. gerar novos pacotes de dados ASF</span><span class="sxs-lookup"><span data-stu-id="cc751-123">7. Generate New ASF Data Packets</span></span>](#7-generate-new-asf-data-packets)
-   [<span data-ttu-id="cc751-124">8. gravar o arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="cc751-124">8. Write the ASF File</span></span>](#8-write-the-asf-file)
-   [<span data-ttu-id="cc751-125">9. definir a função de Entry-Point</span><span class="sxs-lookup"><span data-stu-id="cc751-125">9. Define the Entry-Point Function</span></span>](#9-define-the-entry-point-function)
-   [<span data-ttu-id="cc751-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cc751-126">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="cc751-127">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="cc751-127">Prerequisites</span></span>

<span data-ttu-id="cc751-128">Este tutorial pressupõe o seguinte:</span><span class="sxs-lookup"><span data-stu-id="cc751-128">This tutorial assumes the following:</span></span>

-   <span data-ttu-id="cc751-129">Você está familiarizado com a estrutura de um arquivo ASF e os componentes fornecidos pelo Media Foundation para trabalhar com objetos ASF.</span><span class="sxs-lookup"><span data-stu-id="cc751-129">You are familiar with the structure of an ASF file and the components provided by Media Foundation to work with ASF Objects.</span></span> <span data-ttu-id="cc751-130">Esses componentes incluem ContentInfo, Splitter, multiplexador e objetos de perfil.</span><span class="sxs-lookup"><span data-stu-id="cc751-130">These components include ContentInfo, splitter, multiplexer, and profile objects.</span></span> <span data-ttu-id="cc751-131">Para obter mais informações, consulte [componentes ASF do WMContainer](wmcontainer-asf-components.md).</span><span class="sxs-lookup"><span data-stu-id="cc751-131">For more information, see [WMContainer ASF Components](wmcontainer-asf-components.md).</span></span>
-   <span data-ttu-id="cc751-132">Você está familiarizado com os codificadores de mídia do Windows e os vários tipos de codificação, particularmente CBR.</span><span class="sxs-lookup"><span data-stu-id="cc751-132">You are familiar with Windows Media encoders, and the various encoding types, particularly CBR.</span></span> <span data-ttu-id="cc751-133">Para obter mais informações, consulte [codificadores de mídia do Windows](windows-media-encoders.md) .</span><span class="sxs-lookup"><span data-stu-id="cc751-133">For more information, see [Windows Media Encoders](windows-media-encoders.md) .</span></span>
-   <span data-ttu-id="cc751-134">Você está familiarizado com [buffers de mídia](media-buffers.md) e fluxos de bytes: especificamente, operações de arquivo usando um fluxo de bytes e gravando o conteúdo de um buffer de mídia em um fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="cc751-134">You are familiar with [Media Buffers](media-buffers.md) and byte streams: Specifically, file operations using a byte stream, and writing the contents of a media buffer to a byte stream.</span></span>

## <a name="terminology"></a><span data-ttu-id="cc751-135">Terminologia</span><span class="sxs-lookup"><span data-stu-id="cc751-135">Terminology</span></span>

<span data-ttu-id="cc751-136">Este tutorial usa os seguintes termos:</span><span class="sxs-lookup"><span data-stu-id="cc751-136">This tutorial uses the following terms:</span></span>

-   <span data-ttu-id="cc751-137">Tipo de mídia de origem: objeto de tipo de mídia, expõe a interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , que descreve o conteúdo do arquivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="cc751-137">Source media type: Media type object, exposes [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface, which describes the contents of the input file.</span></span>
-   <span data-ttu-id="cc751-138">Perfil de áudio: objeto de perfil, expõe a interface [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) , que contém somente fluxos de áudio do arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="cc751-138">Audio profile: Profile object, exposes [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface, which contains only audio streams of the output file.</span></span>
-   <span data-ttu-id="cc751-139">Exemplo de fluxo: a amostra de mídia, expõe a interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , representa os dados de mídia do arquivo de entrada obtidos do codificador em um estado compactado.</span><span class="sxs-lookup"><span data-stu-id="cc751-139">Stream sample: Media sample, exposes [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, represents the input file's media data obtained from the encoder in a compressed state.</span></span>
-   <span data-ttu-id="cc751-140">Objeto ContentInfo: o [objeto ASF ContentInfo](asf-contentinfo-object.md), expõe a interface [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , que representa o objeto de cabeçalho ASF do arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="cc751-140">ContentInfo object: [ASF ContentInfo Object](asf-contentinfo-object.md), exposes [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface, which represents the ASF Header Object of the output file.</span></span>
-   <span data-ttu-id="cc751-141">Fluxo de bytes de dados: o objeto de fluxo de bytes, expõe a interface [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , que representa a parte inteira do objeto de dados ASF do arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="cc751-141">Data byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which represents the entire ASF Data Object portion of the output file.</span></span>
-   <span data-ttu-id="cc751-142">Pacote de dados: exemplo de mídia, expõe a interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , gerada pelo [Multiplexador de ASF](asf-multiplexer.md); representa um pacote de dados ASF que será gravado no fluxo de bytes de dados.</span><span class="sxs-lookup"><span data-stu-id="cc751-142">Data packet: Media sample, exposes [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, generated by the [ASF Multiplexer](asf-multiplexer.md); represents an ASF data packet that will be written to the data byte stream.</span></span>
-   <span data-ttu-id="cc751-143">Fluxo de bytes de saída: objeto de fluxo de bytes, expõe a interface [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , que contém o conteúdo do arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="cc751-143">Output byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which contains the contents of the output file.</span></span>

## <a name="1-set-up-the-project"></a><span data-ttu-id="cc751-144">1. configurar o projeto</span><span class="sxs-lookup"><span data-stu-id="cc751-144">1. Set up the Project</span></span>

1.  <span data-ttu-id="cc751-145">Inclua os seguintes cabeçalhos no arquivo de origem:</span><span class="sxs-lookup"><span data-stu-id="cc751-145">Include the following headers in your source file:</span></span>

    ```C++
    #include <new>
    #include <stdio.h>       // Standard I/O
    #include <windows.h>     // Windows headers
    #include <mfapi.h>       // Media Foundation platform
    #include <wmcontainer.h> // ASF interfaces
    #include <mferror.h>     // Media Foundation error codes
    ```

    

2.  <span data-ttu-id="cc751-146">Link para os seguintes arquivos de biblioteca:</span><span class="sxs-lookup"><span data-stu-id="cc751-146">Link to the following library files:</span></span>

    -   <span data-ttu-id="cc751-147">mfplat. lib</span><span class="sxs-lookup"><span data-stu-id="cc751-147">mfplat.lib</span></span>
    -   <span data-ttu-id="cc751-148">MF. lib</span><span class="sxs-lookup"><span data-stu-id="cc751-148">mf.lib</span></span>
    -   <span data-ttu-id="cc751-149">mfuuid. lib</span><span class="sxs-lookup"><span data-stu-id="cc751-149">mfuuid.lib</span></span>

3.  <span data-ttu-id="cc751-150">Declare a função [SafeRelease](saferelease.md) .</span><span class="sxs-lookup"><span data-stu-id="cc751-150">Declare the [SafeRelease](saferelease.md) function.</span></span>
4.  <span data-ttu-id="cc751-151">Inclua a classe CWmaEncoder em seu projeto.</span><span class="sxs-lookup"><span data-stu-id="cc751-151">Include the CWmaEncoder class in your project.</span></span> <span data-ttu-id="cc751-152">Para obter o código-fonte completo dessa classe, consulte [código de exemplo do codificador](encoder-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="cc751-152">For the complete source code of this class, see [Encoder Example Code](encoder-example-code.md).</span></span>

## <a name="2-declare-helper-functions"></a><span data-ttu-id="cc751-153">2. declarar funções auxiliares</span><span class="sxs-lookup"><span data-stu-id="cc751-153">2. Declare Helper Functions</span></span>

<span data-ttu-id="cc751-154">Este tutorial usa as seguintes funções auxiliares para ler e gravar a partir de um fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="cc751-154">This tutorial uses the following helper functions to read and write from a byte stream.</span></span>

-   <span data-ttu-id="cc751-155">`AppendToByteStream`: Anexa o conteúdo de um fluxo de bytes a outro fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="cc751-155">`AppendToByteStream`: Appends the contents of one byte stream to another byte stream.</span></span>
-   <span data-ttu-id="cc751-156">WriteBufferToByteStream: grava dados de um buffer de mídia em um fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="cc751-156">WriteBufferToByteStream: Writes data from a media buffer to a byte stream.</span></span>

<span data-ttu-id="cc751-157">Para obter mais informações, consulte [**IMFByteStream:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span><span class="sxs-lookup"><span data-stu-id="cc751-157">For more information, see [**IMFByteStream::Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span></span> <span data-ttu-id="cc751-158">O código a seguir mostra essas funções auxiliares:</span><span class="sxs-lookup"><span data-stu-id="cc751-158">The following code shows these helper functions:</span></span>


```C++
//-------------------------------------------------------------------
// AppendToByteStream
//
// Reads the contents of pSrc and writes them to pDest.
//-------------------------------------------------------------------

HRESULT AppendToByteStream(IMFByteStream *pSrc, IMFByteStream *pDest)
{
    HRESULT hr = S_OK;

    const DWORD READ_SIZE = 1024;

    BYTE buffer[READ_SIZE];

    while (1)
    {
        ULONG cbRead;

        hr = pSrc->Read(buffer, READ_SIZE, &cbRead);

        if (FAILED(hr)) { break; }

        if (cbRead == 0)
        {
            break;
        }

        hr = pDest->Write(buffer, cbRead, &cbRead);

        if (FAILED(hr)) { break; }
    }

    return hr;
}
```




```C++
//-------------------------------------------------------------------
// WriteBufferToByteStream
//
// Writes data from a media buffer to a byte stream.
//-------------------------------------------------------------------

HRESULT WriteBufferToByteStream(
    IMFByteStream *pStream,   // Pointer to the byte stream.
    IMFMediaBuffer *pBuffer,  // Pointer to the media buffer.
    DWORD *pcbWritten         // Receives the number of bytes written.
    )
{
    HRESULT hr = S_OK;
    DWORD cbData = 0;
    DWORD cbWritten = 0;
    BYTE *pMem = NULL;

    hr = pBuffer->Lock(&pMem, NULL, &cbData);

    if (SUCCEEDED(hr))
    {
        hr = pStream->Write(pMem, cbData, &cbWritten);
    }

    if (SUCCEEDED(hr))
    {
        if (pcbWritten)
        {
            *pcbWritten = cbWritten;
        }
    }

    if (pMem)
    {
        pBuffer->Unlock();
    }
    return hr;
}
```



## <a name="3-open-an-audio-file"></a><span data-ttu-id="cc751-159">3. abrir um arquivo de áudio</span><span class="sxs-lookup"><span data-stu-id="cc751-159">3. Open an Audio File</span></span>

<span data-ttu-id="cc751-160">Este tutorial pressupõe que seu aplicativo irá gerar áudio descompactado para codificação.</span><span class="sxs-lookup"><span data-stu-id="cc751-160">This tutorial assumes that your application will generate uncompressed audio for encoding.</span></span> <span data-ttu-id="cc751-161">Para essa finalidade, duas funções são declaradas neste tutorial:</span><span class="sxs-lookup"><span data-stu-id="cc751-161">For that purpose, two functions are declared in this tutorial:</span></span>


```C++
HRESULT OpenAudioFile(PCWSTR pszURL, IMFMediaType **ppAudioFormat);
HRESULT GetNextAudioSample(BOOL *pbEOS, IMFSample **ppSample);
```



<span data-ttu-id="cc751-162">A implementação dessas funções é deixada para o leitor.</span><span class="sxs-lookup"><span data-stu-id="cc751-162">The implementation of these functions is left to the reader.</span></span>

-   <span data-ttu-id="cc751-163">A `OpenAudioFile` função deve abrir o arquivo de mídia especificado por *pszURL* e retornar um ponteiro para um tipo de mídia que descreve um fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="cc751-163">The `OpenAudioFile` function should open the media file specified by *pszURL* and return a pointer to a media type that describes an audio stream.</span></span>
-   <span data-ttu-id="cc751-164">A `GetNextAudioSample` função deve ler áudio PCM não compactado do arquivo que foi aberto pelo `OpenAudioFile` .</span><span class="sxs-lookup"><span data-stu-id="cc751-164">The `GetNextAudioSample` function should read uncompressed PCM audio from the file that was opened by `OpenAudioFile`.</span></span> <span data-ttu-id="cc751-165">Quando o final do arquivo for atingido, *pbEOS* receberá o valor **true**.</span><span class="sxs-lookup"><span data-stu-id="cc751-165">When the end of the file is reached, *pbEOS* receives the value **TRUE**.</span></span> <span data-ttu-id="cc751-166">Caso contrário, o *ppSample* receberá um exemplo de mídia que contém o buffer de áudio.</span><span class="sxs-lookup"><span data-stu-id="cc751-166">Otherwise, *ppSample* receives a media sample that contains the audio buffer.</span></span>

## <a name="4-configure-the-encoder"></a><span data-ttu-id="cc751-167">4. configurar o codificador</span><span class="sxs-lookup"><span data-stu-id="cc751-167">4. Configure the Encoder</span></span>

<span data-ttu-id="cc751-168">Em seguida, crie o codificador, configure-o para produzir exemplos de fluxo codificados em CBR e negocie os tipos de mídia de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="cc751-168">Next, create the encoder, configure it to produce CBR-encoded stream samples, and negotiate the input and the output media types.</span></span>

<span data-ttu-id="cc751-169">Em Media Foundation, os codificadores (expõem a interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) ) são implementados como [transformações de Media Foundation](media-foundation-transforms.md) (MFT).</span><span class="sxs-lookup"><span data-stu-id="cc751-169">In Media Foundation, encoders (expose the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface) are implemented as [Media Foundation Transforms](media-foundation-transforms.md) (MFT).</span></span>

<span data-ttu-id="cc751-170">Neste tutorial, o codificador é implementado na `CWmaEncoder` classe que fornece um wrapper para o MFT.</span><span class="sxs-lookup"><span data-stu-id="cc751-170">In this tutorial, the encoder is implemented in the `CWmaEncoder` class that provides a wrapper for the MFT.</span></span> <span data-ttu-id="cc751-171">Para obter o código-fonte completo dessa classe, consulte [código de exemplo do codificador](encoder-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="cc751-171">For the complete source code of this class, see [Encoder Example Code](encoder-example-code.md).</span></span>

> [!Note]  
> <span data-ttu-id="cc751-172">Opcionalmente, você pode especificar o tipo de codificação como CBR.</span><span class="sxs-lookup"><span data-stu-id="cc751-172">You can optionally specify the encoding type as CBR.</span></span> <span data-ttu-id="cc751-173">Por padrão, o codificador está configurado para usar a codificação CBR.</span><span class="sxs-lookup"><span data-stu-id="cc751-173">By default, the encoder is configured to use CBR encoding.</span></span> <span data-ttu-id="cc751-174">Para obter mais informações, consulte [codificação de taxa de bits constante](constant-bit-rate-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="cc751-174">For more information, see [Constant Bit Rate Encoding](constant-bit-rate-encoding.md).</span></span> <span data-ttu-id="cc751-175">Você pode definir propriedades adicionais dependendo do tipo de codificação, para obter informações sobre as propriedades que são específicas para um modo de codificação, consulte [codificação de taxa de bits variável baseada em qualidade](quality-based-variable-bit-rate--vbr--encoding.md), [codificação de taxa de bits variável irrestrita](unconstrained-variable-bit-rate--vbr--encoding.md)e [codificação de taxa de bits variável com restrição de pico](peak-constrained-variable-bit-rate--vbr--encoding.md).</span><span class="sxs-lookup"><span data-stu-id="cc751-175">You can set additional properties depending on the type of encoding, for information about the properties that are specific to an encoding mode, see [Quality-Based Variable Bit Rate Encoding](quality-based-variable-bit-rate--vbr--encoding.md), [Unconstrained Variable Bit Rate Encoding](unconstrained-variable-bit-rate--vbr--encoding.md), and [Peak-Constrained Variable Bit Rate Encoding](peak-constrained-variable-bit-rate--vbr--encoding.md).</span></span>

 


```C++
    CWmaEncoder* pEncoder = NULL; //Pointer to the Encoder object.

    hr = OpenAudioFile(sInputFileName, &pInputType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Initialize the WMA encoder wrapper.

    pEncoder = new (std::nothrow) CWmaEncoder();
    if (pEncoder == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pEncoder->Initialize();
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetEncodingType(EncodeMode_CBR);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetInputType(pInputType);
    if (FAILED(hr))
    {
        goto done;
    }
```



## <a name="5-create-the-asf-contentinfo-object"></a><span data-ttu-id="cc751-176">5. Crie o objeto ContentInfo do ASF.</span><span class="sxs-lookup"><span data-stu-id="cc751-176">5. Create the ASF ContentInfo object.</span></span>

<span data-ttu-id="cc751-177">O [objeto ASF ContentInfo](asf-contentinfo-object.md) contém informações sobre os vários objetos de cabeçalho do arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="cc751-177">The [ASF ContentInfo Object](asf-contentinfo-object.md) contains information about the various header objects of the output file.</span></span>

<span data-ttu-id="cc751-178">Primeiro, crie um perfil de ASF para o fluxo de áudio:</span><span class="sxs-lookup"><span data-stu-id="cc751-178">First, create an ASF profile for the audio stream:</span></span>

1.  <span data-ttu-id="cc751-179">Chame [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) para criar um objeto de perfil ASF vazio.</span><span class="sxs-lookup"><span data-stu-id="cc751-179">Call [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) to create an empty ASF profile object.</span></span> <span data-ttu-id="cc751-180">O perfil ASF expõe a interface [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) .</span><span class="sxs-lookup"><span data-stu-id="cc751-180">The ASF profile exposes the [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface.</span></span> <span data-ttu-id="cc751-181">Para obter mais informações, consulte [criando e configurando fluxos ASF](creating-and-configuring-asf-streams.md).</span><span class="sxs-lookup"><span data-stu-id="cc751-181">For more information, see [Creating and Configuring ASF Streams](creating-and-configuring-asf-streams.md).</span></span>
2.  <span data-ttu-id="cc751-182">Obtenha o formato de áudio codificado do `CWmaEncoder` objeto.</span><span class="sxs-lookup"><span data-stu-id="cc751-182">Get the encoded audio format from the `CWmaEncoder` object.</span></span>
3.  <span data-ttu-id="cc751-183">Chame [**IMFASFProfile:: CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) para criar um novo fluxo para o perfil ASF.</span><span class="sxs-lookup"><span data-stu-id="cc751-183">Call [**IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) to create a new stream for the ASF profile.</span></span> <span data-ttu-id="cc751-184">Passe um ponteiro para a interface [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , que representa o formato de fluxo.</span><span class="sxs-lookup"><span data-stu-id="cc751-184">Pass in a pointer to the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface, which represents the stream format.</span></span>
4.  <span data-ttu-id="cc751-185">Chame [**IMFASFStreamConfig:: SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) para atribuir um identificador de fluxo.</span><span class="sxs-lookup"><span data-stu-id="cc751-185">Call [**IMFASFStreamConfig::SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) to assign a stream identifier.</span></span>
5.  <span data-ttu-id="cc751-186">Defina os parâmetros de "Bucket de vazamentos" definindo o atributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) no objeto de fluxo.</span><span class="sxs-lookup"><span data-stu-id="cc751-186">Set the "leaky bucket" parameters by setting the [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) attribute on the stream object.</span></span>
6.  <span data-ttu-id="cc751-187">Chame [**IMFASFProfile:: SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) para adicionar o novo fluxo ao perfil.</span><span class="sxs-lookup"><span data-stu-id="cc751-187">Call [**IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) to add the new stream to the profile.</span></span>

<span data-ttu-id="cc751-188">Agora, crie o objeto ContentInfo do ASF da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="cc751-188">Now create the ASF ContentInfo object as follows:</span></span>

1.  <span data-ttu-id="cc751-189">Chame [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) para criar um objeto ContentInfo vazio.</span><span class="sxs-lookup"><span data-stu-id="cc751-189">Call [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) to create an empty ContentInfo object.</span></span>
2.  <span data-ttu-id="cc751-190">Chame [**IMFASFContentInfo:: setprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) para definir o perfil de ASF.</span><span class="sxs-lookup"><span data-stu-id="cc751-190">Call [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) to set the ASF profile.</span></span>

<span data-ttu-id="cc751-191">O código a seguir mostra estas etapas:</span><span class="sxs-lookup"><span data-stu-id="cc751-191">The following code shows these steps:</span></span>


```C++
HRESULT CreateASFContentInfo(
    CWmaEncoder* pEncoder,
    IMFASFContentInfo** ppContentInfo
    )
{
    HRESULT hr = S_OK;
    
    IMFASFProfile* pProfile = NULL;
    IMFMediaType* pMediaType = NULL;
    IMFASFStreamConfig* pStream = NULL;
    IMFASFContentInfo* pContentInfo = NULL;

    // Create the ASF profile object.

    hr = MFCreateASFProfile(&pProfile); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a stream description for the encoded audio.

    hr = pEncoder->GetOutputType(&pMediaType); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->CreateStream(pMediaType, &pStream); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pStream->SetStreamNumber(DEFAULT_STREAM_NUMBER); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Set "leaky bucket" values.

    LeakyBucket bucket;

    hr = pEncoder->GetLeakyBucket1(&bucket);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pStream->SetBlob(
        MF_ASFSTREAMCONFIG_LEAKYBUCKET1, 
        (UINT8*)&bucket, 
        sizeof(bucket)
        );

    if (FAILED(hr))
    {
        goto done;
    }

    //Add the stream to the profile

    hr = pProfile->SetStream(pStream);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the ASF ContentInfo object.

    hr = MFCreateASFContentInfo(&pContentInfo); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pContentInfo->SetProfile(pProfile); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.

    *ppContentInfo = pContentInfo;
    (*ppContentInfo)->AddRef();

done:
    SafeRelease(&pProfile);
    SafeRelease(&pStream);
    SafeRelease(&pMediaType);
    SafeRelease(&pContentInfo);
    return hr;
}
```



## <a name="6-create-the-asf-multiplexer"></a><span data-ttu-id="cc751-192">6. criar o multiplexador de ASF</span><span class="sxs-lookup"><span data-stu-id="cc751-192">6. Create the ASF Multiplexer</span></span>

<span data-ttu-id="cc751-193">O [multiplexador ASF](asf-multiplexer.md) gera pacotes de dados ASF.</span><span class="sxs-lookup"><span data-stu-id="cc751-193">The [ASF Multiplexer](asf-multiplexer.md) generates ASF data packets.</span></span>

1.  <span data-ttu-id="cc751-194">Chame [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer) para criar o multiplexador de ASF.</span><span class="sxs-lookup"><span data-stu-id="cc751-194">Call [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer) to create the ASF multiplexer.</span></span>
2.  <span data-ttu-id="cc751-195">Chame [**IMFASFMultiplexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) para inicializar o multiplexador.</span><span class="sxs-lookup"><span data-stu-id="cc751-195">Call [**IMFASFMultiplexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) to initialize the multiplexer.</span></span> <span data-ttu-id="cc751-196">Passe um ponteiro para o objeto de informações de conteúdo do ASF, que foi criado na seção anterior.</span><span class="sxs-lookup"><span data-stu-id="cc751-196">Pass in a pointer to the ASF Content Info object, which was created in the previous section.</span></span>
3.  <span data-ttu-id="cc751-197">Chame [**IMFASFMultiplexer:: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) para definir o sinalizador **de \_ taxa de \_ \_ bits de AutoAjuste do Multiplexador MFASF** .</span><span class="sxs-lookup"><span data-stu-id="cc751-197">Call [**IMFASFMultiplexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) to set the **MFASF\_MULTIPLEXER\_AUTOADJUST\_BITRATE** flag.</span></span> <span data-ttu-id="cc751-198">Quando essa configuração é usada, o multiplexador ajusta automaticamente a taxa de bits do conteúdo ASF para corresponder às características dos fluxos que estão sendo multiplexados.</span><span class="sxs-lookup"><span data-stu-id="cc751-198">When this setting is used, the multiplexer automatically adjusts the bit rate of the ASF content to match the characteristics of the streams being multiplexed.</span></span>


```C++
HRESULT CreateASFMux( 
    IMFASFContentInfo* pContentInfo,
    IMFASFMultiplexer** ppMultiplexer
    )
{
    HRESULT hr = S_OK;
    
    IMFMediaType* pMediaType = NULL;
    IMFASFMultiplexer *pMultiplexer = NULL;

    // Create and initialize the ASF Multiplexer object.

    hr = MFCreateASFMultiplexer(&pMultiplexer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pMultiplexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    // Enable automatic bit-rate adjustment.

    hr = pMultiplexer->SetFlags(MFASF_MULTIPLEXER_AUTOADJUST_BITRATE);
    if (FAILED(hr))
    {
        goto done;
    }

    *ppMultiplexer = pMultiplexer;
    (*ppMultiplexer)->AddRef();

done:
    SafeRelease(&pMultiplexer);
    return hr;
}
```



## <a name="7-generate-new-asf-data-packets"></a><span data-ttu-id="cc751-199">7. gerar novos pacotes de dados ASF</span><span class="sxs-lookup"><span data-stu-id="cc751-199">7. Generate New ASF Data Packets</span></span>

<span data-ttu-id="cc751-200">Em seguida, gere pacotes de dados ASF para o novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="cc751-200">Next, generate ASF data packets for the new file.</span></span> <span data-ttu-id="cc751-201">Esses pacotes de dados constituem o objeto de dados ASF final para o novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="cc751-201">These data packets will constitute the final ASF Data Object for the new file.</span></span> <span data-ttu-id="cc751-202">Para gerar novos pacotes de dados ASF:</span><span class="sxs-lookup"><span data-stu-id="cc751-202">To generate new ASF data packets:</span></span>

1.  <span data-ttu-id="cc751-203">Chame [**MFCreateTempFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatetempfile) para criar um fluxo de bytes temporário para manter os pacotes de dados ASF.</span><span class="sxs-lookup"><span data-stu-id="cc751-203">Call [**MFCreateTempFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatetempfile) to create a temporary byte stream to hold the ASF data packets.</span></span>
2.  <span data-ttu-id="cc751-204">Chame a função definida pelo aplicativo `GetNextAudioSample` para obter dados de áudio não compactados para o codificador.</span><span class="sxs-lookup"><span data-stu-id="cc751-204">Call the application-defined `GetNextAudioSample` function to get uncompressed audio data for the encoder.</span></span>
3.  <span data-ttu-id="cc751-205">Passe o áudio descompactado para o codificador para compactação.</span><span class="sxs-lookup"><span data-stu-id="cc751-205">Pass the uncompressed audio to the encoder for compression.</span></span> <span data-ttu-id="cc751-206">Para obter mais informações, consulte [processando dados no codificador](processing-data-in-the-encoder.md)</span><span class="sxs-lookup"><span data-stu-id="cc751-206">For more information, see [Processing Data in the Encoder](processing-data-in-the-encoder.md)</span></span>
4.  <span data-ttu-id="cc751-207">Chame [**IMFASFMultiplexer::P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) para enviar os exemplos de áudio compactados para o multiplexador de ASF para pacotes.</span><span class="sxs-lookup"><span data-stu-id="cc751-207">Call [**IMFASFMultiplexer::ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) to send the compressed audio samples to the ASF multiplexer for packetization.</span></span>
5.  <span data-ttu-id="cc751-208">Obtenha os pacotes ASF do Multiplexador e grave-os no fluxo de bytes temporário.</span><span class="sxs-lookup"><span data-stu-id="cc751-208">Get the ASF packets from the multiplexer and write them to the temporary byte stream.</span></span> <span data-ttu-id="cc751-209">Para obter mais informações, consulte [gerando novos pacotes de dados ASF](generating-new-asf-data-packets.md).</span><span class="sxs-lookup"><span data-stu-id="cc751-209">For more information, see [Generating New ASF Data Packets](generating-new-asf-data-packets.md).</span></span>
6.  <span data-ttu-id="cc751-210">Quando você chegar ao final do fluxo de origem, dissipe o codificador e extraia as amostras compactadas restantes do codificador.</span><span class="sxs-lookup"><span data-stu-id="cc751-210">When you reach the end of the source stream, drain the encoder and pull the remaining compressed samples from the encoder.</span></span> <span data-ttu-id="cc751-211">Para obter mais informações sobre como descarregar uma MFT, consulte [modelo básico de processamento de MFT](basic-mft-processing-model.md).</span><span class="sxs-lookup"><span data-stu-id="cc751-211">For more information about draining an MFT, see [Basic MFT Processing Model](basic-mft-processing-model.md).</span></span>
7.  <span data-ttu-id="cc751-212">Depois que todas as amostras forem enviadas ao Multiplexador, chame [**IMFASFMultiplexer:: flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) e receba os pacotes ASF restantes do Multiplexador.</span><span class="sxs-lookup"><span data-stu-id="cc751-212">After all samples are sent to the multiplexer, call [**IMFASFMultiplexer::Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) and pull the remaining ASF packets from the multiplexer.</span></span>
8.  <span data-ttu-id="cc751-213">Chame [**IMFASFMultiplexer:: End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end).</span><span class="sxs-lookup"><span data-stu-id="cc751-213">Call [**IMFASFMultiplexer::End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end).</span></span>

<span data-ttu-id="cc751-214">O código a seguir gera pacotes de dados ASF.</span><span class="sxs-lookup"><span data-stu-id="cc751-214">The following code generates ASF data packets.</span></span> <span data-ttu-id="cc751-215">A função retorna um ponteiro para um fluxo de bytes que contém o objeto de dados ASF.</span><span class="sxs-lookup"><span data-stu-id="cc751-215">The function returns a pointer to a byte stream that contains the ASF Data Object.</span></span>


```C++
HRESULT EncodeData(
    CWmaEncoder* pEncoder, 
    IMFASFContentInfo* pContentInfo,
    IMFASFMultiplexer* pMux, 
    IMFByteStream** ppDataStream) 
{
    HRESULT hr = S_OK;

    IMFByteStream* pStream = NULL;
    IMFSample* pInputSample = NULL;
    IMFSample* pWmaSample = NULL;

    BOOL bEOF = FALSE;

   // Create a temporary file to hold the data stream.
   hr = MFCreateTempFile(
        MF_ACCESSMODE_READWRITE, 
        MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE,
        &pStream
        );

   if (FAILED(hr))
   {
       goto done;
   }

    BOOL bNeedInput = TRUE;

    while (TRUE)
    {
        if (bNeedInput)
        {
            hr = GetNextAudioSample(&bEOF, &pInputSample);
            if (FAILED(hr))
            {
                goto done;
            }

            if (bEOF)
            {
                // Reached the end of the input file.
                break;
            }

            // Encode the uncompressed audio sample.
            hr = pEncoder->ProcessInput(pInputSample);
            if (FAILED(hr))
            {
                goto done;
            }

            bNeedInput = FALSE;
        }

        if (bNeedInput == FALSE)
        {
            // Get data from the encoder.

            hr = pEncoder->ProcessOutput(&pWmaSample);
            if (FAILED(hr))
            {
                goto done;
            }

            // pWmaSample can be NULL if the encoder needs more input.

            if (pWmaSample)
            {
                hr = pMux->ProcessSample(DEFAULT_STREAM_NUMBER, pWmaSample, 0);
                if (FAILED(hr))
                {
                    goto done;
                }

                //Collect the data packets and write them to a stream
                hr = GenerateASFDataPackets(pMux, pStream);
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            else
            {
                bNeedInput = TRUE;
            }
        }
        
        SafeRelease(&pInputSample);
        SafeRelease(&pWmaSample);
    }

    // Drain the MFT and pull any remaining samples from the encoder.

    hr = pEncoder->Drain();
    if (FAILED(hr))
    {
        goto done;
    }

    while (TRUE)
    {
        hr = pEncoder->ProcessOutput(&pWmaSample);
        if (FAILED(hr))
        {
            goto done;
        }

        if (pWmaSample == NULL)
        {
            break;
        }

        hr = pMux->ProcessSample(DEFAULT_STREAM_NUMBER, pWmaSample, 0);
        if (FAILED(hr))
        {
            goto done;
        }

        //Collect the data packets and write them to a stream
        hr = GenerateASFDataPackets(pMux, pStream);
        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pWmaSample);
    }

    // Flush the mux and get any pending ASF data packets.
    hr = pMux->Flush();
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GenerateASFDataPackets(pMux, pStream);
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Update the ContentInfo object
    hr = pMux->End(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    //Return stream to the caller that contains the ASF encoded data.
    *ppDataStream = pStream;
    (*ppDataStream)->AddRef();

done:
    SafeRelease(&pStream);
    SafeRelease(&pInputSample);
    SafeRelease(&pWmaSample);
    return hr;
}
```



<span data-ttu-id="cc751-216">O código para a `GenerateASFDataPackets` função é mostrado no tópico [gerando novos pacotes de dados ASF](generating-new-asf-data-packets.md).</span><span class="sxs-lookup"><span data-stu-id="cc751-216">Code for the `GenerateASFDataPackets` function is shown in the topic [Generating New ASF Data Packets](generating-new-asf-data-packets.md).</span></span>

## <a name="8-write-the-asf-file"></a><span data-ttu-id="cc751-217">8. gravar o arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="cc751-217">8. Write the ASF File</span></span>

<span data-ttu-id="cc751-218">Em seguida, grave o cabeçalho ASF em um buffer de mídia chamando [**IMFASFContentInfo:: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span><span class="sxs-lookup"><span data-stu-id="cc751-218">Next, write the ASF header to a media buffer by calling [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span></span> <span data-ttu-id="cc751-219">Esse método converte os dados armazenados no objeto ContentInfo em dados binários no formato de objeto de cabeçalho ASF.</span><span class="sxs-lookup"><span data-stu-id="cc751-219">This method converts data stored in the ContentInfo object into binary data in ASF Header Object format.</span></span> <span data-ttu-id="cc751-220">Para obter mais informações, consulte [gerando um novo objeto de cabeçalho ASF](generating-a-new-asf-header-object.md).</span><span class="sxs-lookup"><span data-stu-id="cc751-220">For more information, see [Generating a New ASF Header Object](generating-a-new-asf-header-object.md).</span></span>

<span data-ttu-id="cc751-221">Depois que o novo objeto de cabeçalho ASF tiver sido gerado, crie um fluxo de bytes para o arquivo de saída.</span><span class="sxs-lookup"><span data-stu-id="cc751-221">After the new ASF Header Object has been generated, create a byte stream for the output file.</span></span> <span data-ttu-id="cc751-222">Primeiro, grave o objeto de cabeçalho no fluxo de bytes de saída.</span><span class="sxs-lookup"><span data-stu-id="cc751-222">First write the Header Object to the output byte stream.</span></span> <span data-ttu-id="cc751-223">Siga o objeto de cabeçalho com o objeto de dados contido no fluxo de bytes de dados.</span><span class="sxs-lookup"><span data-stu-id="cc751-223">Follow the Header Object with the Data Object contained in the data byte stream.</span></span>


```C++
HRESULT WriteASFFile( 
     IMFASFContentInfo *pContentInfo, 
     IMFByteStream *pDataStream,
     PCWSTR pszFile
     )
{
    HRESULT hr = S_OK;
    
    IMFMediaBuffer* pHeaderBuffer = NULL;
    IMFByteStream* pWmaStream = NULL;

    DWORD cbHeaderSize = 0;
    DWORD cbWritten = 0;

    //Create output file
    hr = MFCreateFile(MF_ACCESSMODE_WRITE, MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE, pszFile, &pWmaStream);

    if (FAILED(hr))
    {
        goto done;
    }


    // Get the size of the ASF Header Object.
    hr = pContentInfo->GenerateHeader (NULL, &cbHeaderSize);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a media buffer.
    hr = MFCreateMemoryBuffer(cbHeaderSize, &pHeaderBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    // Populate the media buffer with the ASF Header Object.
    hr = pContentInfo->GenerateHeader(pHeaderBuffer, &cbHeaderSize);
    if (FAILED(hr))
    {
        goto done;
    }

    // Write the ASF header to the output file.
    hr = WriteBufferToByteStream(pWmaStream, pHeaderBuffer, &cbWritten);
    if (FAILED(hr))
    {
        goto done;
    }

    // Append the data stream to the file.

    hr = pDataStream->SetCurrentPosition(0);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = AppendToByteStream(pDataStream, pWmaStream);

done:
    SafeRelease(&pHeaderBuffer);
    SafeRelease(&pWmaStream);
    return hr;
}
```



## <a name="9-define-the-entry-point-function"></a><span data-ttu-id="cc751-224">9. definir a função de Entry-Point</span><span class="sxs-lookup"><span data-stu-id="cc751-224">9. Define the Entry-Point Function</span></span>

<span data-ttu-id="cc751-225">Agora você pode colocar as etapas anteriores juntas em um aplicativo completo.</span><span class="sxs-lookup"><span data-stu-id="cc751-225">Now you can put the previous steps together into a complete application.</span></span> <span data-ttu-id="cc751-226">Antes de usar qualquer um dos objetos Media Foundation, inicialize a plataforma Media Foundation chamando [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span><span class="sxs-lookup"><span data-stu-id="cc751-226">Before using any of the Media Foundation objects, initialize the Media Foundation platform by calling [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span></span> <span data-ttu-id="cc751-227">Quando terminar, chame [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span><span class="sxs-lookup"><span data-stu-id="cc751-227">When you are done, call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span> <span data-ttu-id="cc751-228">Para obter mais informações, consulte [inicializando Media Foundation](initializing-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="cc751-228">For more information, see [Initializing Media Foundation](initializing-media-foundation.md).</span></span>

<span data-ttu-id="cc751-229">O código a seguir mostra o aplicativo de console completo.</span><span class="sxs-lookup"><span data-stu-id="cc751-229">The following code shows the complete console application.</span></span> <span data-ttu-id="cc751-230">O argumento de linha de comando especifica o nome do arquivo a ser convertido e o nome do novo arquivo de áudio.</span><span class="sxs-lookup"><span data-stu-id="cc751-230">The command-line argument specifies the name of the file to convert and the name of the new audio file.</span></span>


```C++
int wmain(int argc, WCHAR* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 3)
    {
        wprintf_s(L"Usage: %s input.wmv, %s output.wma");
        return 0;
    }

    const WCHAR* sInputFileName = argv[1];    // Source file name
    const WCHAR* sOutputFileName = argv[2];  // Output file name
    
    IMFMediaType* pInputType = NULL;
    IMFASFContentInfo* pContentInfo = NULL;
    IMFASFMultiplexer* pMux = NULL;
    IMFByteStream* pDataStream = NULL;

    CWmaEncoder* pEncoder = NULL; //Pointer to the Encoder object.

    HRESULT hr = CoInitializeEx(
        NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);

    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFStartup(MF_VERSION);
    if (FAILED(hr))
    {
        goto done;
    }

    CWmaEncoder* pEncoder = NULL; //Pointer to the Encoder object.

    hr = OpenAudioFile(sInputFileName, &pInputType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Initialize the WMA encoder wrapper.

    pEncoder = new (std::nothrow) CWmaEncoder();
    if (pEncoder == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pEncoder->Initialize();
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetEncodingType(EncodeMode_CBR);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetInputType(pInputType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the WMContainer objects.
    hr = CreateASFContentInfo(pEncoder, &pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CreateASFMux(pContentInfo, &pMux);
    if (FAILED(hr))
    {
        goto done;
    }

    // Convert uncompressed data to ASF format.
    hr = EncodeData(pEncoder, pContentInfo, pMux, &pDataStream);
    if (FAILED(hr))
    {
        goto done;
    }

    // Write the ASF objects to the output file.
    hr = WriteASFFile(pContentInfo, pDataStream, sOutputFileName);

done:
    SafeRelease(&pInputType);
    SafeRelease(&pContentInfo);
    SafeRelease(&pMux);
    SafeRelease(&pDataStream);
    delete pEncoder;

    MFShutdown();
    CoUninitialize();

    if (FAILED(hr))
    {
        wprintf_s(L"Error: 0x%X\n", hr);
    }

    return 0;
} 
```



## <a name="related-topics"></a><span data-ttu-id="cc751-231">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cc751-231">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc751-232">Componentes ASF WMContainer</span><span class="sxs-lookup"><span data-stu-id="cc751-232">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="cc751-233">Suporte a ASF no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cc751-233">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



