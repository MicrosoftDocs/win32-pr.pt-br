---
title: Objeto do gravador
description: Objeto do gravador
ms.assetid: 8058b7fe-7d02-4572-ad43-6867d4ceb7e9
keywords:
- SDK do Windows Media Format, objetos do Writer
- Formato de sistema avançado (ASF), objetos de gravador
- ASF (formato de sistemas avançados), objetos de gravador
- objetos, objetos de gravador
- objetos do gravador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42d4783a8330ac1f0f16bc2ca2de4e843cbacc06
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103640304"
---
# <a name="writer-object"></a><span data-ttu-id="e5a10-108">Objeto do gravador</span><span class="sxs-lookup"><span data-stu-id="e5a10-108">Writer Object</span></span>

<span data-ttu-id="e5a10-109">O objeto Writer é usado para gravar arquivos de mídia digital usando a estrutura de arquivos ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="e5a10-109">The writer object is used to write digital media files using the advanced systems format (ASF) file structure.</span></span> <span data-ttu-id="e5a10-110">O processo de gravação de um arquivo de mídia digital envolve muitas etapas internas ao gravador, que coordenam a compactação, o pacote e a multiplexação.</span><span class="sxs-lookup"><span data-stu-id="e5a10-110">The process of writing a digital media file involves many steps internal to the writer, which coordinates compression, packetization, and multiplexing.</span></span>

<span data-ttu-id="e5a10-111">O objeto gravador inclui interfaces para saída para arquivos ou uma rede, dá suporte a uma interface de retorno de chamada e pode criar um ou mais objetos de propriedades de mídia de entrada.</span><span class="sxs-lookup"><span data-stu-id="e5a10-111">The writer object includes interfaces for output to files or a network, supports one callback interface, and can create one or more input media properties objects.</span></span>

<span data-ttu-id="e5a10-112">O objeto Writer é criado pela função [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter), que define um ponteiro para uma interface **IWMWriter** .</span><span class="sxs-lookup"><span data-stu-id="e5a10-112">The writer object is created by the function [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter), which sets a pointer to an **IWMWriter** interface.</span></span> <span data-ttu-id="e5a10-113">As outras interfaces do objeto gravador podem ser obtidas chamando o método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="e5a10-113">The other interfaces of the writer object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="e5a10-114">As interfaces a seguir são suportadas pelo objeto gravador.</span><span class="sxs-lookup"><span data-stu-id="e5a10-114">The following interfaces are supported by the writer object.</span></span>



| <span data-ttu-id="e5a10-115">Interface</span><span class="sxs-lookup"><span data-stu-id="e5a10-115">Interface</span></span>                                          | <span data-ttu-id="e5a10-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5a10-116">Description</span></span>                                                                                                                                                                                               |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5a10-117">**IWMDRMWriter**</span><span class="sxs-lookup"><span data-stu-id="e5a10-117">**IWMDRMWriter**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)               | <span data-ttu-id="e5a10-118">Fornece métodos para gerar chaves [*DRM*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="e5a10-118">Provides methods to generate [*DRM*](wmformat-glossary.md) keys.</span></span>                                                                                                |
| [<span data-ttu-id="e5a10-119">**IWMDRMWriter2**</span><span class="sxs-lookup"><span data-stu-id="e5a10-119">**IWMDRMWriter2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter2)             | <span data-ttu-id="e5a10-120">Configura o objeto gravador para gravar um arquivo que contém um fluxo previamente criptografado que está em conformidade com o protocolo Windows Media DRM 10 para dispositivos de rede.</span><span class="sxs-lookup"><span data-stu-id="e5a10-120">Configures the writer object to write a file containing a pre-encrypted stream that conforms to the Windows Media DRM 10 for Network Devices protocol.</span></span>                                                    |
| [<span data-ttu-id="e5a10-121">**IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="e5a10-121">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)             | <span data-ttu-id="e5a10-122">Gerencia a especificação e a recuperação de informações de cabeçalho, como metadados, [*marcadores*](wmformat-glossary.md)e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="e5a10-122">Manages the specification and retrieval of header information, such as metadata, [*markers*](wmformat-glossary.md), and so on.</span></span>                                                           |
| [<span data-ttu-id="e5a10-123">**IWMHeaderInfo2**</span><span class="sxs-lookup"><span data-stu-id="e5a10-123">**IWMHeaderInfo2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)           | <span data-ttu-id="e5a10-124">Gerencia a enumeração por meio das informações de codec disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e5a10-124">Manages enumerating through the available codec information.</span></span> <span data-ttu-id="e5a10-125">Herda todos os métodos de **IWMHeaderInfo**.</span><span class="sxs-lookup"><span data-stu-id="e5a10-125">Inherits all of the methods of **IWMHeaderInfo**.</span></span>                                                                                            |
| [<span data-ttu-id="e5a10-126">**IWMHeaderInfo3**</span><span class="sxs-lookup"><span data-stu-id="e5a10-126">**IWMHeaderInfo3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)           | <span data-ttu-id="e5a10-127">Gerencia a enumeração por meio das informações de codec disponíveis.</span><span class="sxs-lookup"><span data-stu-id="e5a10-127">Manages enumerating through the available codec information.</span></span> <span data-ttu-id="e5a10-128">Herda todos os métodos de **IWMHeaderInfo** e **IWMHeaderInfo2**.</span><span class="sxs-lookup"><span data-stu-id="e5a10-128">Inherits all of the methods of **IWMHeaderInfo** and **IWMHeaderInfo2**.</span></span>                                                                     |
| [<span data-ttu-id="e5a10-129">**IWMWatermarkInfo**</span><span class="sxs-lookup"><span data-stu-id="e5a10-129">**IWMWatermarkInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo)       | <span data-ttu-id="e5a10-130">Fornece acesso a informações sobre os sistemas de marca d' água presentes no sistema.</span><span class="sxs-lookup"><span data-stu-id="e5a10-130">Provides access to information about watermarking systems present on the system.</span></span>                                                                                                                          |
| [<span data-ttu-id="e5a10-131">**IWMWriter**</span><span class="sxs-lookup"><span data-stu-id="e5a10-131">**IWMWriter**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)                     | <span data-ttu-id="e5a10-132">Inicia e interrompe a gravação de arquivos ASF; Ele inclui métodos para alocar buffers, configurar e recuperar propriedades de entrada, definir perfis e nomes de arquivos de saída e desbloquear o gravador.</span><span class="sxs-lookup"><span data-stu-id="e5a10-132">Starts and stops the writing of ASF files; it includes methods for allocating buffers, setting and retrieving input properties, setting profiles and output file names, and unlocking the writer.</span></span>         |
| [<span data-ttu-id="e5a10-133">**IWMWriterAdvanced**</span><span class="sxs-lookup"><span data-stu-id="e5a10-133">**IWMWriterAdvanced**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)     | <span data-ttu-id="e5a10-134">Adiciona, obtém e remove objetos de coletor especificados; Recupera estatísticas, número de coletores e a hora do relógio para o qual o gravador está trabalhando; e executa outras funções avançadas.</span><span class="sxs-lookup"><span data-stu-id="e5a10-134">Adds, gets, and removes specified sink objects; retrieves statistics, number of sinks, and the clock time the writer is working to; and performs other advanced functions.</span></span>                                |
| [<span data-ttu-id="e5a10-135">**IWMWriterAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="e5a10-135">**IWMWriterAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)   | <span data-ttu-id="e5a10-136">Fornece algumas funcionalidades avançadas, especialmente para lidar com vídeo desentrelaçado.</span><span class="sxs-lookup"><span data-stu-id="e5a10-136">Provides some advanced functionality, particularly for handling deinterlaced video.</span></span> <span data-ttu-id="e5a10-137">Herda todos os métodos de **IWMWriterAdvanced**.</span><span class="sxs-lookup"><span data-stu-id="e5a10-137">Inherits all of the methods of **IWMWriterAdvanced**.</span></span>                                                                 |
| [<span data-ttu-id="e5a10-138">**IWMWriterAdvanced3**</span><span class="sxs-lookup"><span data-stu-id="e5a10-138">**IWMWriterAdvanced3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)   | <span data-ttu-id="e5a10-139">Fornece funcionalidade de gravador adicional, incluindo a capacidade de obter estatísticas de gravador detalhadas.</span><span class="sxs-lookup"><span data-stu-id="e5a10-139">Provides additional writer functionality, including the ability to get detailed writer statistics.</span></span> <span data-ttu-id="e5a10-140">Herda todos os métodos de **IWMWriterAdvanced** e **IWMWriterAdvanced2**.</span><span class="sxs-lookup"><span data-stu-id="e5a10-140">Inherits all of the methods of **IWMWriterAdvanced** and **IWMWriterAdvanced2**.</span></span>                       |
| [<span data-ttu-id="e5a10-141">**IWMWriterPostView**</span><span class="sxs-lookup"><span data-stu-id="e5a10-141">**IWMWriterPostView**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview)     | <span data-ttu-id="e5a10-142">Gerencia algumas funcionalidades de gravação avançadas relacionadas a exemplos de visualização.</span><span class="sxs-lookup"><span data-stu-id="e5a10-142">Manages some advanced writing functionality related to postviewing samples.</span></span> <span data-ttu-id="e5a10-143">A visualização está exibindo a saída, geralmente de um codificador, para verificar se o processo de codificação/decodificação está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="e5a10-143">Postviewing is viewing the output, usually from an encoder, to check that the encoding/decoding process is working correctly.</span></span> |
| [<span data-ttu-id="e5a10-144">**IWMWriterPreprocess**</span><span class="sxs-lookup"><span data-stu-id="e5a10-144">**IWMWriterPreprocess**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpreprocess) | <span data-ttu-id="e5a10-145">Gerencia passagens de pré-processamento feitas pelo gravador.</span><span class="sxs-lookup"><span data-stu-id="e5a10-145">Manages preprocessing passes made by the writer.</span></span> <span data-ttu-id="e5a10-146">Os passos de pré-processamento são usados para melhorar a qualidade da saída codificada.</span><span class="sxs-lookup"><span data-stu-id="e5a10-146">Preprocessing passes are used to improve the quality of encoded output.</span></span>                                                                                  |



 

<span data-ttu-id="e5a10-147">A interface de retorno de chamada a seguir deve ser implementada pelo aplicativo para acompanhar o progresso da visualização.</span><span class="sxs-lookup"><span data-stu-id="e5a10-147">The following callback interface must be implemented by the application to track the progress of postviewing.</span></span>



| <span data-ttu-id="e5a10-148">Interface</span><span class="sxs-lookup"><span data-stu-id="e5a10-148">Interface</span></span>                                                      | <span data-ttu-id="e5a10-149">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5a10-149">Description</span></span>                                                                                              |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5a10-150">**IWMWriterPostViewCallback**</span><span class="sxs-lookup"><span data-stu-id="e5a10-150">**IWMWriterPostViewCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback) | <span data-ttu-id="e5a10-151">Gerencia como exemplos não compactados são recebidos do objeto gravador para visualizar o que o codec está fazendo.</span><span class="sxs-lookup"><span data-stu-id="e5a10-151">Manages how uncompressed samples are received from the writer object to preview what the codec is doing.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e5a10-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e5a10-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5a10-153">**Objetos**</span><span class="sxs-lookup"><span data-stu-id="e5a10-153">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="e5a10-154">**Gravando arquivos ASF**</span><span class="sxs-lookup"><span data-stu-id="e5a10-154">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




