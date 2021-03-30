---
title: Sobre o IMediaObject
description: Sobre o IMediaObject
ms.assetid: c483f74a-efd8-4a9f-a719-686099755e63
keywords:
- Plug-ins do Windows Media Player, interfaces
- plug-ins, interfaces
- plug-ins de processamento de sinal digital, interfaces
- Plug-ins do DSP, interfaces
- interfaces, plug-ins do DSP
- Plug-ins do Windows Media Player, interface IMediaObject
- plug-ins, interface IMediaObject
- plug-ins de processamento de sinal digital, interface IMediaObject
- Plug-ins do DSP, interface IMediaObject
- Interface IMediaObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbbecd749242b67bc5c8f36b3c7a2c0a5fbe461
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635084"
---
# <a name="about-imediaobject"></a><span data-ttu-id="c3c9d-113">Sobre o IMediaObject</span><span class="sxs-lookup"><span data-stu-id="c3c9d-113">About IMediaObject</span></span>

<span data-ttu-id="c3c9d-114">A interface **IMediaObject** é a interface necessária para o DMOs.</span><span class="sxs-lookup"><span data-stu-id="c3c9d-114">The **IMediaObject** interface is the required interface for DMOs.</span></span> <span data-ttu-id="c3c9d-115">**IMediaObject** contém os métodos que um plug-in de DSP do Windows Media Player usa para obter dados do Windows Media Player, para processar os dados e para retornar os dados processados para o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="c3c9d-115">**IMediaObject** contains the methods that a Windows Media Player DSP plug-in uses to get data from Windows Media Player, to process the data, and to return the processed data to Windows Media Player.</span></span> <span data-ttu-id="c3c9d-116">Para obter a documentação completa da interface **IMediaObject** , consulte a seção DirectShow do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="c3c9d-116">For complete documentation of the **IMediaObject** interface, see the DirectShow section of the Windows SDK.</span></span>

<span data-ttu-id="c3c9d-117">Os métodos de **IMediaObject** podem ser categorizados da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c3c9d-117">The methods of **IMediaObject** can be categorized as follows:</span></span>

## <a name="methods-that-handle-format-negotiation"></a><span data-ttu-id="c3c9d-118">Métodos que manipulam a negociação de formato</span><span class="sxs-lookup"><span data-stu-id="c3c9d-118">Methods that Handle Format Negotiation</span></span>

<span data-ttu-id="c3c9d-119">Esses são os métodos que o Windows Media Player chama para obter informações sobre os formatos de dados com suporte no plug-in.</span><span class="sxs-lookup"><span data-stu-id="c3c9d-119">These are the methods that Windows Media Player calls to get information about the data formats supported by the plug-in.</span></span> <span data-ttu-id="c3c9d-120">Esses métodos incluem:</span><span class="sxs-lookup"><span data-stu-id="c3c9d-120">These methods include:</span></span>

-   <span data-ttu-id="c3c9d-121">**GetInputMaxLatency**</span><span class="sxs-lookup"><span data-stu-id="c3c9d-121">**GetInputMaxLatency**</span></span>
-   <span data-ttu-id="c3c9d-122">**GetInputSizeInfo**</span><span class="sxs-lookup"><span data-stu-id="c3c9d-122">**GetInputSizeInfo**</span></span>
-   <span data-ttu-id="c3c9d-123">**GetInputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="c3c9d-123">**GetInputStreamInfo**</span></span>
-   <span data-ttu-id="c3c9d-124">**GetInputType**</span><span class="sxs-lookup"><span data-stu-id="c3c9d-124">**GetInputType**</span></span>
-   <span data-ttu-id="c3c9d-125">**GetOutputSizeInfo**</span><span class="sxs-lookup"><span data-stu-id="c3c9d-125">**GetOutputSizeInfo**</span></span>
-   <span data-ttu-id="c3c9d-126">**GetOutputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="c3c9d-126">**GetOutputStreamInfo**</span></span>
-   <span data-ttu-id="c3c9d-127">**GetOutputType**</span><span class="sxs-lookup"><span data-stu-id="c3c9d-127">**GetOutputType**</span></span>
-   <span data-ttu-id="c3c9d-128">**GetStreamCount**</span><span class="sxs-lookup"><span data-stu-id="c3c9d-128">**GetStreamCount**</span></span>
-   <span data-ttu-id="c3c9d-129">**SetInputMaxLatency**</span><span class="sxs-lookup"><span data-stu-id="c3c9d-129">**SetInputMaxLatency**</span></span>
-   <span data-ttu-id="c3c9d-130">**SetInputType**</span><span class="sxs-lookup"><span data-stu-id="c3c9d-130">**SetInputType**</span></span>
-   <span data-ttu-id="c3c9d-131">**Setoutputtypetype**</span><span class="sxs-lookup"><span data-stu-id="c3c9d-131">**SetOutputType**</span></span>

<span data-ttu-id="c3c9d-132">Vários desses métodos, como **GetInputType** e **SetInputType**, usam a estrutura do **\_ \_ tipo de mídia DMO** para descrever o formato dos dados usados por um fluxo.</span><span class="sxs-lookup"><span data-stu-id="c3c9d-132">Several of these methods, such as **GetInputType** and **SetInputType**, use the **DMO\_MEDIA\_TYPE** structure to describe the format of the data used by a stream.</span></span> <span data-ttu-id="c3c9d-133">Quando o Windows Media Player chama esses métodos, ele fornece um ponteiro para uma estrutura de **\_ \_ tipo de mídia DMO** .</span><span class="sxs-lookup"><span data-stu-id="c3c9d-133">When Windows Media Player calls these methods, it provides a pointer to a **DMO\_MEDIA\_TYPE** structure.</span></span> <span data-ttu-id="c3c9d-134">Se um método como **SetInputType** especificar as informações do tipo de mídia, o plug-in deverá copiar a estrutura do **\_ \_ tipo de mídia DMO** para uma variável de membro e inspecionar seus membros de dados para determinar o tipo de dados que o Windows Media Player fornecerá no buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="c3c9d-134">If a method such as **SetInputType** specifies the media type information, the plug-in should copy the **DMO\_MEDIA\_TYPE** structure to a member variable and inspect its data members to determine the type of data that Windows Media Player will provide in the input buffer.</span></span> <span data-ttu-id="c3c9d-135">Se um método como **GetInputType** recuperar as informações do tipo de mídia, o plug-in deverá copiar o endereço da variável de membro que contém a estrutura do **\_ \_ tipo de mídia DMO** para o ponteiro fornecido pelo Windows Media Player na lista de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c3c9d-135">If a method such as **GetInputType** retrieves the media type information, the plug-in should copy the address of the member variable containing the **DMO\_MEDIA\_TYPE** structure to the pointer provided by Windows Media Player in the parameter list.</span></span>

<span data-ttu-id="c3c9d-136">O Windows Media Player usa principalmente dois membros da estrutura de **\_ \_ tipo de mídia DMO** :</span><span class="sxs-lookup"><span data-stu-id="c3c9d-136">Windows Media Player mainly uses two members of the **DMO\_MEDIA\_TYPE** structure:</span></span>

-   <span data-ttu-id="c3c9d-137">**majortype**: um GUID (identificador global exclusivo) que especifica a categoria geral da mídia, como áudio ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="c3c9d-137">**majortype**: A globally unique identifier (GUID) that specifies the overall category of the media, such as audio or video.</span></span>
-   <span data-ttu-id="c3c9d-138">**subtipo**: um GUID que especifica uma descrição mais detalhada da mídia, como áudio PCM.</span><span class="sxs-lookup"><span data-stu-id="c3c9d-138">**subtype**: A GUID that specifies a more detailed description of the media, such as PCM audio.</span></span>

<span data-ttu-id="c3c9d-139">Essas GUIDs podem ser encontradas no cabeçalho chamado UUIDs. h, que está incluído com o SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="c3c9d-139">These GUIDs can be found in the header named uuids.h, which is included with the Windows SDK.</span></span>

<span data-ttu-id="c3c9d-140">Métodos como **GetInputSizeInfo** fornecem informações ao Windows Media Player sobre a quantidade de memória necessária para alocar os buffers de processamento.</span><span class="sxs-lookup"><span data-stu-id="c3c9d-140">Methods such as **GetInputSizeInfo** provide information to Windows Media Player about how much memory is required to allocate the processing buffers.</span></span> <span data-ttu-id="c3c9d-141">Métodos como **GetStreamCount** e **GetOutputStreamInfo** fornecem informações para o Windows Media Player sobre o número e o caractere dos fluxos com suporte pelo plug-in do DSP.</span><span class="sxs-lookup"><span data-stu-id="c3c9d-141">Methods such as **GetStreamCount** and **GetOutputStreamInfo** provide information to Windows Media Player about the number and character of the streams supported by the DSP plug-in.</span></span>

<span data-ttu-id="c3c9d-142">**GetInputMaxLatency** e **SetInputMaxLatency** são implementados pelo DMOs em casos especiais.</span><span class="sxs-lookup"><span data-stu-id="c3c9d-142">**GetInputMaxLatency** and **SetInputMaxLatency** are implemented by DMOs in special cases.</span></span> <span data-ttu-id="c3c9d-143">Plug-ins de DSP do Windows Media Player devem retornar E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="c3c9d-143">Windows Media Player DSP plug-ins should return E\_NOTIMPL.</span></span>

## <a name="methods-that-specify-or-retrieve-state-information"></a><span data-ttu-id="c3c9d-144">Métodos que especificam ou recuperam informações de estado</span><span class="sxs-lookup"><span data-stu-id="c3c9d-144">Methods that Specify or Retrieve State Information</span></span>

<span data-ttu-id="c3c9d-145">Esses são os métodos que o Windows Media Player chama para obter ou definir valores relacionados ao estado atual do plug-in.</span><span class="sxs-lookup"><span data-stu-id="c3c9d-145">These are the methods that Windows Media Player calls to get or set values related to the current state of the plug-in.</span></span> <span data-ttu-id="c3c9d-146">Esses métodos incluem:</span><span class="sxs-lookup"><span data-stu-id="c3c9d-146">These methods include:</span></span>

-   <span data-ttu-id="c3c9d-147">**GetInputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="c3c9d-147">**GetInputCurrentType**</span></span>
-   <span data-ttu-id="c3c9d-148">**GetInputStatus**</span><span class="sxs-lookup"><span data-stu-id="c3c9d-148">**GetInputStatus**</span></span>
-   <span data-ttu-id="c3c9d-149">**GetOutputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="c3c9d-149">**GetOutputCurrentType**</span></span>

<span data-ttu-id="c3c9d-150">**GetInputCurrentType** e **GetOutputCurrentType** usam a estrutura do **\_ \_ tipo de mídia DMO** para retornar informações ao Windows Media Player sobre os tipos de mídia definidos anteriormente para os fluxos de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="c3c9d-150">**GetInputCurrentType** and **GetOutputCurrentType** use the **DMO\_MEDIA\_TYPE** structure to return information to Windows Media Player about the media types previously set for the input and output streams.</span></span> <span data-ttu-id="c3c9d-151">**GetInputStatus** retorna um sinalizador que informa ao Windows Media Player se o plug-in do DSP pode aceitar dados de entrada.</span><span class="sxs-lookup"><span data-stu-id="c3c9d-151">**GetInputStatus** returns a flag that tells Windows Media Player whether the DSP plug-in can accept input data.</span></span>

## <a name="methods-that-handle-buffering-and-processing-data"></a><span data-ttu-id="c3c9d-152">Métodos que lidam com buffer e processando dados</span><span class="sxs-lookup"><span data-stu-id="c3c9d-152">Methods that Handle Buffering and Processing Data</span></span>

<span data-ttu-id="c3c9d-153">Esses são os métodos que o Windows Media Player chama para iniciar os vários processos que o plug-in executa para fazer o processamento de sinal digital.</span><span class="sxs-lookup"><span data-stu-id="c3c9d-153">These are the methods that Windows Media Player calls to initiate the various processes that the plug-in performs to do the digital signal processing.</span></span> <span data-ttu-id="c3c9d-154">Esses métodos incluem:</span><span class="sxs-lookup"><span data-stu-id="c3c9d-154">These methods include:</span></span>

-   <span data-ttu-id="c3c9d-155">**AllocateStreamingResources**</span><span class="sxs-lookup"><span data-stu-id="c3c9d-155">**AllocateStreamingResources**</span></span>
-   <span data-ttu-id="c3c9d-156">**Descontinuidade**</span><span class="sxs-lookup"><span data-stu-id="c3c9d-156">**Discontinuity**</span></span>
-   <span data-ttu-id="c3c9d-157">**Liberar**</span><span class="sxs-lookup"><span data-stu-id="c3c9d-157">**Flush**</span></span>
-   <span data-ttu-id="c3c9d-158">**FreeStreamingResources**</span><span class="sxs-lookup"><span data-stu-id="c3c9d-158">**FreeStreamingResources**</span></span>
-   <span data-ttu-id="c3c9d-159">**Bloquear**</span><span class="sxs-lookup"><span data-stu-id="c3c9d-159">**Lock**</span></span>
-   <span data-ttu-id="c3c9d-160">**ProcessInput**</span><span class="sxs-lookup"><span data-stu-id="c3c9d-160">**ProcessInput**</span></span>
-   <span data-ttu-id="c3c9d-161">**ProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="c3c9d-161">**ProcessOutput**</span></span>

<span data-ttu-id="c3c9d-162">O Windows Media Player chama **AllocateStreamingResources** e **FreeStreamingResources** para fornecer o plug-in do DSP com uma oportunidade de configurar ou liberar os buffers adicionais que o plug-in pode exigir para processamento interno.</span><span class="sxs-lookup"><span data-stu-id="c3c9d-162">Windows Media Player calls **AllocateStreamingResources** and **FreeStreamingResources** to provide the DSP plug-in with an opportunity to set up or release any additional buffers the plug-in may require for internal processing.</span></span>

<span data-ttu-id="c3c9d-163">Os plug-ins do DSP do Windows Media Player não precisam usar o método de **descontinuidade** do DMO.</span><span class="sxs-lookup"><span data-stu-id="c3c9d-163">Windows Media Player DSP plug-ins do not need to use the DMO **Discontinuity** method.</span></span>

<span data-ttu-id="c3c9d-164">O Windows Media Player chama **flush** para direcionar o plug-in do DSP para liberar todos os dados armazenados em buffer internamente.</span><span class="sxs-lookup"><span data-stu-id="c3c9d-164">Windows Media Player calls **Flush** to direct the DSP plug-in to flush all internally buffered data.</span></span> <span data-ttu-id="c3c9d-165">O plug-in deve liberar todas as referências às interfaces **IMediaBuffer** , limpar quaisquer valores que especifiquem o carimbo de data/hora ou o tamanho da amostra para o buffer de mídia e reinicializar todos os Estados internos que dependem do conteúdo do exemplo de mídia.</span><span class="sxs-lookup"><span data-stu-id="c3c9d-165">The plug-in should release any references to **IMediaBuffer** interfaces, clear any values that specify the time stamp or sample length for the media buffer, and reinitialize any internal states that depend upon the contents of the media sample.</span></span>

<span data-ttu-id="c3c9d-166">O Windows Media Player chama ProcessInput para passar um ponteiro para uma interface **IMediaBuffer** para o plug-in do DSP.</span><span class="sxs-lookup"><span data-stu-id="c3c9d-166">Windows Media Player calls ProcessInput to pass a pointer to an **IMediaBuffer** interface to the DSP plug-in.</span></span> <span data-ttu-id="c3c9d-167">Essa interface fornece acesso ao buffer de entrada alocado pelo Windows Media Player para fornecer dados ao plug-in.</span><span class="sxs-lookup"><span data-stu-id="c3c9d-167">This interface provides access to the input buffer allocated by Windows Media Player to supply data to the plug-in.</span></span> <span data-ttu-id="c3c9d-168">Subseqüentemente, o Windows Media Player chama **ProcessOutput** para passar um ponteiro para uma interface **IMediaBuffer** que fornece acesso ao buffer de saída alocado pelo Windows Media Player para receber os dados processados do plug-in do DSP.</span><span class="sxs-lookup"><span data-stu-id="c3c9d-168">Windows Media Player subsequently calls **ProcessOutput** to pass a pointer to an **IMediaBuffer** interface that provides access to the output buffer allocated by Windows Media Player to receive the processed data from the DSP plug-in.</span></span>

<span data-ttu-id="c3c9d-169">A interface **IMediaObject** inclui um método chamado **Lock**.</span><span class="sxs-lookup"><span data-stu-id="c3c9d-169">The **IMediaObject** interface includes a method named **Lock**.</span></span> <span data-ttu-id="c3c9d-170">Esse método foi projetado para adquirir ou liberar um bloqueio no DMO para manter o DMO serializado ao executar várias operações.</span><span class="sxs-lookup"><span data-stu-id="c3c9d-170">This method is designed to acquire or release a lock on the DMO to keep the DMO serialized when performing multiple operations.</span></span> <span data-ttu-id="c3c9d-171">A versão de **IMediaObject:: Lock** no código do assistente substitui a implementação da ATL do **bloqueio**.</span><span class="sxs-lookup"><span data-stu-id="c3c9d-171">The version of **IMediaObject::Lock** in the wizard code overrides the ATL implementation of **Lock**.</span></span> <span data-ttu-id="c3c9d-172">Como o Windows Media Player serializa chamadas feitas à interface DMO de um plug-in DSP, a implementação do **bloqueio** simplesmente retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c3c9d-172">Because Windows Media Player serializes calls made to the DMO interface of a DSP plug-in, the implementation of **Lock** simply returns S\_OK.</span></span> <span data-ttu-id="c3c9d-173">Para obter detalhes sobre como criar um DMO multithread, consulte a seção DirectShow do SDK do Windows.</span><span class="sxs-lookup"><span data-stu-id="c3c9d-173">For details about how to create a multithreaded DMO, refer to the DirectShow section of the Windows SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3c9d-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c3c9d-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3c9d-175">**Interfaces necessárias**</span><span class="sxs-lookup"><span data-stu-id="c3c9d-175">**Required Interfaces**</span></span>](required-interfaces.md)
</dt> </dl>

 

 




