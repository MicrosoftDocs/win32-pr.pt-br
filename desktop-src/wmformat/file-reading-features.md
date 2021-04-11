---
title: Recursos de leitura de arquivo
description: Recursos de leitura de arquivo
ms.assetid: ba6dd328-2250-4867-94e0-f66c70ac1bac
keywords:
- SDK do Windows Media Format, recursos de leitura de arquivos
- SDK do Windows Media Format, leitura de arquivo assíncrono
- SDK do Windows Media Format, leitura de arquivos síncrona
- ASF (Advanced Systems Format), recursos de leitura de arquivos
- ASF (formato de sistemas avançados), recursos de leitura de arquivos
- ASF (Advanced Systems Format), leitura de arquivos assíncronos
- ASF (formato de sistemas avançados), leitura de arquivo assíncrono
- ASF (Advanced Systems Format), leitura síncrona de arquivos
- ASF (formato de sistemas avançados), leitura síncrona de arquivos
- leitura de arquivo assíncrono
- leitura de arquivo síncrona
- leitores síncronos, recursos de leitura de arquivos
- leitura de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a83d3ce112d0d9e47626b4f7850f760da5c6583e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292769"
---
# <a name="file-reading-features"></a><span data-ttu-id="7cd13-116">Recursos de leitura de arquivo</span><span class="sxs-lookup"><span data-stu-id="7cd13-116">File Reading Features</span></span>

<span data-ttu-id="7cd13-117">A leitura de arquivos ASF é um dos principais recursos do SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="7cd13-117">Reading ASF files is one of the primary features of the Windows Media Format SDK.</span></span> <span data-ttu-id="7cd13-118">Há suporte para dois tipos de leitura: assíncrono e síncrono.</span><span class="sxs-lookup"><span data-stu-id="7cd13-118">Two types of reading are supported: asynchronous and synchronous.</span></span> <span data-ttu-id="7cd13-119">A leitura de arquivos assíncronos é tratada pelo objeto leitor.</span><span class="sxs-lookup"><span data-stu-id="7cd13-119">Asynchronous file reading is handled by the reader object.</span></span> <span data-ttu-id="7cd13-120">O objeto leitor síncrono é usado para ler arquivos de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="7cd13-120">The synchronous reader object is used to read files synchronously.</span></span> <span data-ttu-id="7cd13-121">Para obter mais informações sobre os diferentes objetos de leitura, consulte [objeto leitor](reader-object.md) e [objeto leitor síncrono](synchronous-reader-object.md).</span><span class="sxs-lookup"><span data-stu-id="7cd13-121">For more information about the different reading objects, see [Reader Object](reader-object.md) and [Synchronous Reader Object](synchronous-reader-object.md).</span></span>

<span data-ttu-id="7cd13-122">No cenário de leitura de arquivo assíncrono mais básico, você deve implementar um método de retorno de chamada que o objeto leitor chamará quando as amostras estiverem prontas.</span><span class="sxs-lookup"><span data-stu-id="7cd13-122">In the most basic asynchronous file reading scenario, you must implement a callback method that the reader object will call when samples are ready.</span></span> <span data-ttu-id="7cd13-123">Depois de começar a ler um arquivo, seu aplicativo aguardará que os exemplos sejam entregues ao seu método de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="7cd13-123">After you begin reading a file, your application waits for the samples to be delivered to your callback method.</span></span> <span data-ttu-id="7cd13-124">A leitura assíncrona é útil para aplicativos de Player e oferece suporte a recursos não disponíveis com leitura síncrona.</span><span class="sxs-lookup"><span data-stu-id="7cd13-124">Asynchronous reading is useful for player applications, and supports features not available with synchronous reading.</span></span> <span data-ttu-id="7cd13-125">Se seu aplicativo precisar ler arquivos de um local de rede ou interagir com um servidor que executa o Windows Media Services, você deverá usar o objeto leitor.</span><span class="sxs-lookup"><span data-stu-id="7cd13-125">If your application needs to read files from a network location, or interact with a server running Windows Media Services, you must use the reader object.</span></span> <span data-ttu-id="7cd13-126">A desvantagem do objeto leitor é que um thread separado é usado para cada saída entregue.</span><span class="sxs-lookup"><span data-stu-id="7cd13-126">The disadvantage of the reader object is that a separate thread is used for each output delivered.</span></span> <span data-ttu-id="7cd13-127">Além disso, o objeto leitor não é tão flexível quanto o leitor síncrono em como ele pode fornecer exemplos.</span><span class="sxs-lookup"><span data-stu-id="7cd13-127">Additionally, the reader object is not as flexible as the synchronous reader in how it can deliver samples.</span></span>

<span data-ttu-id="7cd13-128">Com o leitor síncrono, você não precisa usar nenhum método de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="7cd13-128">With the synchronous reader you do not need to use any callback methods.</span></span> <span data-ttu-id="7cd13-129">Em vez disso, você seleciona uma parte do arquivo para ler e recuperar os exemplos, um por vez, com chamadas de método.</span><span class="sxs-lookup"><span data-stu-id="7cd13-129">Instead, you select a portion of the file to read and retrieve the samples one at a time with method calls.</span></span> <span data-ttu-id="7cd13-130">O leitor síncrono é adequado às necessidades dos aplicativos de edição de conteúdo, onde o acesso rápido a amostras específicas é essencial.</span><span class="sxs-lookup"><span data-stu-id="7cd13-130">The synchronous reader is well suited to the needs of content-editing applications, where quick access to specific samples is essential.</span></span> <span data-ttu-id="7cd13-131">Como nenhum método de retorno de chamada é usado pelo leitor síncrono, você pode criar aplicativos para ler arquivos ASF com um mínimo de sobrecarga de codificação.</span><span class="sxs-lookup"><span data-stu-id="7cd13-131">Because no callback methods are used by the synchronous reader, you can create applications to read ASF files with a minimum of coding overhead.</span></span> <span data-ttu-id="7cd13-132">No entanto, o leitor síncrono não pode abrir um arquivo de um local de rede ou interagir com um servidor que executa o Windows Media Services ou ler arquivos protegidos com [*DRM*](wmformat-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="7cd13-132">However, the synchronous reader cannot open a file from a network location, or interact with a server running Windows Media Services, or read files protected with [*DRM*](wmformat-glossary.md).</span></span>

<span data-ttu-id="7cd13-133">Os tópicos a seguir abordam os recursos do leitor e do leitor síncrono.</span><span class="sxs-lookup"><span data-stu-id="7cd13-133">The following topics discuss the features of the reader and the synchronous reader.</span></span>



| <span data-ttu-id="7cd13-134">Tópico</span><span class="sxs-lookup"><span data-stu-id="7cd13-134">Topic</span></span>                                                              | <span data-ttu-id="7cd13-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="7cd13-135">Description</span></span>                                                                                                        |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7cd13-136">Suporte de amostra alocado pelo usuário</span><span class="sxs-lookup"><span data-stu-id="7cd13-136">User Allocated Sample Support</span></span>](user-allocated-sample-support.md) | <span data-ttu-id="7cd13-137">Discute a alocação de buffer no leitor e no leitor síncrono e como a alocação do usuário pode melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="7cd13-137">Discusses buffer allocation in the reader and synchronous reader, and how user allocation can improve performance.</span></span> |
| [<span data-ttu-id="7cd13-138">Enumeração de formato de saída</span><span class="sxs-lookup"><span data-stu-id="7cd13-138">Output Format Enumeration</span></span>](output-format-enumeration.md)         | <span data-ttu-id="7cd13-139">Discute a enumeração de formato de saída.</span><span class="sxs-lookup"><span data-stu-id="7cd13-139">Discusses output format enumeration.</span></span>                                                                               |



 

<span data-ttu-id="7cd13-140">Além disso, os tópicos a seguir da seção recursos de escrita também se aplicam à leitura de arquivos:</span><span class="sxs-lookup"><span data-stu-id="7cd13-140">In addition, the following topics from the writing features section also apply to file reading:</span></span>

-   [<span data-ttu-id="7cd13-141">Redimensionamento de vídeo</span><span class="sxs-lookup"><span data-stu-id="7cd13-141">Video Resizing</span></span>](video-resizing.md)
-   [<span data-ttu-id="7cd13-142">Conversão de espaço de cor</span><span class="sxs-lookup"><span data-stu-id="7cd13-142">Color Space Conversion</span></span>](color-space-conversion.md)
-   [<span data-ttu-id="7cd13-143">Reamostragem de áudio</span><span class="sxs-lookup"><span data-stu-id="7cd13-143">Audio Resampling</span></span>](audio-resampling.md)

## <a name="related-topics"></a><span data-ttu-id="7cd13-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7cd13-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cd13-145">**Recursos**</span><span class="sxs-lookup"><span data-stu-id="7cd13-145">**Features**</span></span>](features.md)
</dt> <dt>

[<span data-ttu-id="7cd13-146">**Lendo arquivos ASF**</span><span class="sxs-lookup"><span data-stu-id="7cd13-146">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




