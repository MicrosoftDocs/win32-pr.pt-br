---
title: Gravando arquivos ASF
description: Gravando arquivos ASF
ms.assetid: d722b676-bf65-4f91-8118-bb12d3bbb6cb
keywords:
- Windows Media Format SDK, gravando arquivos ASF
- SDK do Windows Media Format, criando arquivos ASF
- SDK do Windows Media Format, formato de sistemas avançados (ASF)
- ASF (Advanced Systems Format), gravando arquivos
- ASF (formato de sistemas avançados), gravando arquivos
- ASF (Advanced Systems Format), criando arquivos
- ASF (formato de sistemas avançados), criando arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c13c1af0d3699c89d26f007e00675ea563639c4e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103823564"
---
# <a name="writing-asf-files"></a><span data-ttu-id="5cd81-110">Gravando arquivos ASF</span><span class="sxs-lookup"><span data-stu-id="5cd81-110">Writing ASF Files</span></span>

<span data-ttu-id="5cd81-111">Você pode usar o objeto gravador do SDK do Windows Media Format para criar arquivos ASF a partir de dados de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="5cd81-111">You can use the writer object of the Windows Media Format SDK to create ASF files from digital media data.</span></span> <span data-ttu-id="5cd81-112">Para criar uma instância do objeto Writer, chame a função [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) .</span><span class="sxs-lookup"><span data-stu-id="5cd81-112">To create an instance of the writer object, call the [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) function.</span></span> <span data-ttu-id="5cd81-113">O objeto Writer coordena a funcionalidade de vários componentes, incluindo codecs, que são externos ao Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="5cd81-113">The writer object coordinates the functionality of a number of components, including codecs, which are external to the Windows Media Format SDK.</span></span>

<span data-ttu-id="5cd81-114">A funcionalidade básica do objeto gravador pode ser dividida nas etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="5cd81-114">The basic functionality of the writer object can be broken down into the following steps.</span></span> <span data-ttu-id="5cd81-115">Nestas etapas, "o aplicativo" refere-se ao programa que você escreve usando o SDK do Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="5cd81-115">In these steps, "the application" refers to the program you write using the Windows Media Format SDK.</span></span>

1.  <span data-ttu-id="5cd81-116">O aplicativo fornece ao gravador um perfil a ser usado na criação do arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="5cd81-116">The application supplies the writer with a profile to use in creating the ASF file.</span></span> <span data-ttu-id="5cd81-117">Quando o gravador carrega os dados de perfil, ele atribui um número de entrada a cada conexão do perfil.</span><span class="sxs-lookup"><span data-stu-id="5cd81-117">When the writer loads the profile data, it assigns an input number to each connection of the profile.</span></span>
2.  <span data-ttu-id="5cd81-118">O aplicativo fornece ao gravador um nome de arquivo de saída para o arquivo a ser gravado.</span><span class="sxs-lookup"><span data-stu-id="5cd81-118">The application supplies the writer with an output file name for the file to be written.</span></span> <span data-ttu-id="5cd81-119">O gravador cria um objeto de coletor de arquivo do gravador para gerenciar a criação e a entrada do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5cd81-119">The writer creates a writer file sink object to manage the file creation and input.</span></span> <span data-ttu-id="5cd81-120">Para obter mais informações, consulte [objeto de coletor de arquivo do gravador](writer-file-sink-object.md).</span><span class="sxs-lookup"><span data-stu-id="5cd81-120">For more information, see [Writer File Sink Object](writer-file-sink-object.md).</span></span>
3.  <span data-ttu-id="5cd81-121">O gravador cria um cabeçalho para o novo arquivo com base nas informações do perfil.</span><span class="sxs-lookup"><span data-stu-id="5cd81-121">The writer creates a header for the new file based on information in the profile.</span></span>
4.  <span data-ttu-id="5cd81-122">O aplicativo passa amostras descompactadas para o gravador.</span><span class="sxs-lookup"><span data-stu-id="5cd81-122">The application passes uncompressed samples to the writer.</span></span> <span data-ttu-id="5cd81-123">Os exemplos são passados um de cada vez em buffers encapsulados em objetos de buffer.</span><span class="sxs-lookup"><span data-stu-id="5cd81-123">Samples are passed one at a time in buffers wrapped in buffer objects.</span></span> <span data-ttu-id="5cd81-124">O aplicativo deve passar amostras para cada fluxo simultaneamente para que o gravador receba todos os exemplos em ordem de tempo de apresentação.</span><span class="sxs-lookup"><span data-stu-id="5cd81-124">The application should pass samples for each stream concurrently so that the writer receives all samples in presentation-time order.</span></span>
5.  <span data-ttu-id="5cd81-125">O gravador passa os exemplos para o codec apropriado para compactação.</span><span class="sxs-lookup"><span data-stu-id="5cd81-125">The writer passes the samples to the appropriate codec for compression.</span></span> <span data-ttu-id="5cd81-126">Quando o gravador recebe os exemplos compactados, ele os intercala com exemplos de outros fluxos, de modo que os exemplos vão para o arquivo na ordem de tempo da apresentação, independentemente do fluxo.</span><span class="sxs-lookup"><span data-stu-id="5cd81-126">When the writer receives the compressed samples, it interleaves them with samples from the other streams so that samples go into the file in presentation time order irrespective of stream.</span></span> <span data-ttu-id="5cd81-127">Os dados de exemplo são então feitos em pacotes e gravados na seção de dados do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5cd81-127">The sample data is then made into packets and written to the data section of the file.</span></span>
6.  <span data-ttu-id="5cd81-128">Quando todas as amostras são processadas, o gravador pode adicionar um índice ao arquivo para melhorar o desempenho de busca.</span><span class="sxs-lookup"><span data-stu-id="5cd81-128">When all samples are processed, the writer can add an index to the file to enhance seeking performance.</span></span>

<span data-ttu-id="5cd81-129">Essas etapas são ilustradas no aplicativo de exemplo WMStats, entre outras.</span><span class="sxs-lookup"><span data-stu-id="5cd81-129">These steps are illustrated in the WMStats sample application, among others.</span></span> <span data-ttu-id="5cd81-130">Para obter mais informações, consulte [aplicativos de exemplo](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="5cd81-130">For more information, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="5cd81-131">O gravador também dá suporte à funcionalidade mais avançada, permitindo que você faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="5cd81-131">The writer also supports more advanced functionality, enabling you to do the following:</span></span>

-   <span data-ttu-id="5cd81-132">Edite metadados no cabeçalho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5cd81-132">Edit metadata in the header of the file.</span></span>
-   <span data-ttu-id="5cd81-133">Escreva amostras precompactadas.</span><span class="sxs-lookup"><span data-stu-id="5cd81-133">Write precompressed samples.</span></span>
-   <span data-ttu-id="5cd81-134">Gravar em coletores de rede para streaming de dados dinâmicos.</span><span class="sxs-lookup"><span data-stu-id="5cd81-134">Write to network sinks for streaming live data.</span></span>
-   <span data-ttu-id="5cd81-135">Gravar em coletores de arquivo para opções avançadas de controle de arquivo.</span><span class="sxs-lookup"><span data-stu-id="5cd81-135">Write to file sinks for advanced file control options.</span></span>
-   <span data-ttu-id="5cd81-136">Gravar em coletores de push para distribuição para servidores que fornecerão conteúdo aos usuários finais.</span><span class="sxs-lookup"><span data-stu-id="5cd81-136">Write to push sinks for distribution to servers that will deliver content to end users.</span></span>
-   <span data-ttu-id="5cd81-137">Forneça exemplos de exibição prévia para verificação da saída.</span><span class="sxs-lookup"><span data-stu-id="5cd81-137">Deliver postview samples for verification of output.</span></span>
-   <span data-ttu-id="5cd81-138">Entregar as estatísticas de desempenho do gravador.</span><span class="sxs-lookup"><span data-stu-id="5cd81-138">Deliver writer-performance statistics.</span></span>

<span data-ttu-id="5cd81-139">As seções a seguir descrevem o uso do objeto do gravador em detalhes.</span><span class="sxs-lookup"><span data-stu-id="5cd81-139">The following sections describe the use of the writer object in detail.</span></span>



| <span data-ttu-id="5cd81-140">Seção</span><span class="sxs-lookup"><span data-stu-id="5cd81-140">Section</span></span>                                                                    | <span data-ttu-id="5cd81-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="5cd81-141">Description</span></span>                                                                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5cd81-142">Usar perfis com o gravador</span><span class="sxs-lookup"><span data-stu-id="5cd81-142">To Use Profiles with the Writer</span></span>](to-use-profiles-with-the-writer.md)     | <span data-ttu-id="5cd81-143">Descreve como especificar um perfil a ser usado com o gravador.</span><span class="sxs-lookup"><span data-stu-id="5cd81-143">Describes how to specify a profile to use with the writer.</span></span>                                             |
| [<span data-ttu-id="5cd81-144">Trabalhando com entradas</span><span class="sxs-lookup"><span data-stu-id="5cd81-144">Working with Inputs</span></span>](working-with-inputs.md)                             | <span data-ttu-id="5cd81-145">Descreve como identificar e definir as configurações de entrada no gravador.</span><span class="sxs-lookup"><span data-stu-id="5cd81-145">Describes how to identify and configure the input settings in the writer.</span></span>                              |
| [<span data-ttu-id="5cd81-146">Para editar metadados com o gravador</span><span class="sxs-lookup"><span data-stu-id="5cd81-146">To Edit Metadata with the Writer</span></span>](to-edit-metadata-with-the-writer.md)   | <span data-ttu-id="5cd81-147">Descreve como usar o gravador para editar metadados para um novo arquivo.</span><span class="sxs-lookup"><span data-stu-id="5cd81-147">Describes how to use the writer to edit metadata for a new file.</span></span>                                       |
| [<span data-ttu-id="5cd81-148">Para escrever exemplos</span><span class="sxs-lookup"><span data-stu-id="5cd81-148">To Write Samples</span></span>](to-write-samples.md)                                   | <span data-ttu-id="5cd81-149">Descreve como passar amostras para o gravador.</span><span class="sxs-lookup"><span data-stu-id="5cd81-149">Describes how to pass samples to the writer.</span></span>                                                           |
| [<span data-ttu-id="5cd81-150">Definindo extensões de unidade de dados</span><span class="sxs-lookup"><span data-stu-id="5cd81-150">Setting Data Unit Extensions</span></span>](setting-data-unit-extensions.md)           | <span data-ttu-id="5cd81-151">Descreve como adicionar dados estendidos a exemplos.</span><span class="sxs-lookup"><span data-stu-id="5cd81-151">Describes how to add extended data to samples.</span></span>                                                         |
| [<span data-ttu-id="5cd81-152">Gravando amostras compactadas</span><span class="sxs-lookup"><span data-stu-id="5cd81-152">Writing Compressed Samples</span></span>](writing-compressed-samples.md)               | <span data-ttu-id="5cd81-153">Descreve como passar amostras compactadas previamente para o gravador.</span><span class="sxs-lookup"><span data-stu-id="5cd81-153">Describes how to pass pre-compressed samples to the writer.</span></span>                                            |
| [<span data-ttu-id="5cd81-154">Gravando fluxos de imagem</span><span class="sxs-lookup"><span data-stu-id="5cd81-154">Writing Image Streams</span></span>](writing-image-streams.md)                         | <span data-ttu-id="5cd81-155">Descreve como configurar uma entrada para um fluxo de imagem.</span><span class="sxs-lookup"><span data-stu-id="5cd81-155">Describes how to configure an input for an image stream.</span></span>                                               |
| [<span data-ttu-id="5cd81-156">Escrevendo amostras de imagens de vídeo</span><span class="sxs-lookup"><span data-stu-id="5cd81-156">Writing Video Image Samples</span></span>](writing-video-image-samples.md)             | <span data-ttu-id="5cd81-157">Descreve como configurar exemplos de imagem de vídeo.</span><span class="sxs-lookup"><span data-stu-id="5cd81-157">Describes how to configure Video Image samples.</span></span>                                                        |
| [<span data-ttu-id="5cd81-158">Gravando fluxos de taxa de bits variáveis</span><span class="sxs-lookup"><span data-stu-id="5cd81-158">Writing Variable Bit Rate Streams</span></span>](writing-variable-bit-rate-streams.md) | <span data-ttu-id="5cd81-159">Descreve como gravar fluxos de taxa de bits variável (VBR).</span><span class="sxs-lookup"><span data-stu-id="5cd81-159">Describes how to write variable bit rate (VBR) streams.</span></span>                                                |
| [<span data-ttu-id="5cd81-160">Usando a codificação Two-Pass</span><span class="sxs-lookup"><span data-stu-id="5cd81-160">Using Two-Pass Encoding</span></span>](using-two-pass-encoding.md)                     | <span data-ttu-id="5cd81-161">Descreve como fazer com que o codec execute uma passagem preliminar antes de gravar o arquivo.</span><span class="sxs-lookup"><span data-stu-id="5cd81-161">Describes how to have the codec perform a preliminary pass before writing the file.</span></span>                    |
| [<span data-ttu-id="5cd81-162">Para forçar a inserção de Key-Frame</span><span class="sxs-lookup"><span data-stu-id="5cd81-162">To Force Key-Frame Insertion</span></span>](to-force-key-frame-insertion.md)           | <span data-ttu-id="5cd81-163">Descreve como forçar manualmente o codec para codificar um exemplo como um quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="5cd81-163">Describes how to manually force the codec to encode a sample as a key frame.</span></span>                           |
| [<span data-ttu-id="5cd81-164">Para gerenciar a latência do gravador</span><span class="sxs-lookup"><span data-stu-id="5cd81-164">To Manage Writer Latency</span></span>](to-manage-writer-latency.md)                   | <span data-ttu-id="5cd81-165">Descreve como minimizar o tempo que o gravador leva para processar amostras em um arquivo ou coletor de saída.</span><span class="sxs-lookup"><span data-stu-id="5cd81-165">Describes how to minimize the time it takes the writer to process samples into an output file or sink.</span></span> |
| [<span data-ttu-id="5cd81-166">Trabalhando com coletores de gravador</span><span class="sxs-lookup"><span data-stu-id="5cd81-166">Working with Writer Sinks</span></span>](working-with-writer-sinks.md)                 | <span data-ttu-id="5cd81-167">Descreve como usar coletores de gravador para entregar seu conteúdo a arquivos ou locais de rede.</span><span class="sxs-lookup"><span data-stu-id="5cd81-167">Describes how to use writer sinks to deliver your content to files or network locations.</span></span>               |
| [<span data-ttu-id="5cd81-168">Para obter estatísticas do gravador</span><span class="sxs-lookup"><span data-stu-id="5cd81-168">To Get Writer Statistics</span></span>](to-get-writer-statistics.md)                   | <span data-ttu-id="5cd81-169">Descreve como obter estatísticas para o gravador.</span><span class="sxs-lookup"><span data-stu-id="5cd81-169">Describes how to get statistics for the writer.</span></span>                                                        |
| [<span data-ttu-id="5cd81-170">Para usar a exibição do gravador</span><span class="sxs-lookup"><span data-stu-id="5cd81-170">To Use Writer Postview</span></span>](to-use-writer-postview.md)                       | <span data-ttu-id="5cd81-171">Descreve como obter amostras não compactadas à medida que você escreve um arquivo para verificação.</span><span class="sxs-lookup"><span data-stu-id="5cd81-171">Describes how to get uncompressed samples as you write a file for verification.</span></span>                        |



 

## <a name="related-topics"></a><span data-ttu-id="5cd81-172">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5cd81-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cd81-173">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="5cd81-173">**Programming Guide**</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="5cd81-174">**Objeto de coletor de arquivo do gravador**</span><span class="sxs-lookup"><span data-stu-id="5cd81-174">**Writer File Sink Object**</span></span>](writer-file-sink-object.md)
</dt> <dt>

[<span data-ttu-id="5cd81-175">**Objeto de coletor de rede do gravador**</span><span class="sxs-lookup"><span data-stu-id="5cd81-175">**Writer Network Sink Object**</span></span>](writer-network-sink-object.md)
</dt> <dt>

[<span data-ttu-id="5cd81-176">**Objeto do gravador**</span><span class="sxs-lookup"><span data-stu-id="5cd81-176">**Writer Object**</span></span>](writer-object.md)
</dt> </dl>

 

 




