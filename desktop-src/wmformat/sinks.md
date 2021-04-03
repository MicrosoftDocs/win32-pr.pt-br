---
title: Coletores
description: Coletores
ms.assetid: 6781a326-a30a-4d4d-96db-332d0f681a31
keywords:
- SDK do Windows Media Format, coletores
- SDK do Windows Media Format, coletores de arquivos
- ASF (Advanced Systems Format), coletores
- ASF (formato de sistemas avançados), coletores
- ASF (Advanced Systems Format), coletores de arquivos
- ASF (formato de sistemas avançados), coletores de arquivo
- SDK do Windows Media Format, coletores de rede
- SDK do Windows Media Format, coletores push
- ASF (Advanced Systems Format), coletores de rede
- ASF (formato de sistemas avançados), coletores de rede
- ASF (Advanced Systems Format), coletores push
- ASF (formato de sistemas avançados), coletores push
- coletores, sobre
- coletores de arquivos, sobre
- coletores de rede
- coletores push
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a62548f159172f58d4f52b0289c5adbfef02f55
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007136"
---
# <a name="sinks"></a><span data-ttu-id="24ed0-119">Coletores</span><span class="sxs-lookup"><span data-stu-id="24ed0-119">Sinks</span></span>

<span data-ttu-id="24ed0-120">O objeto do gravador do Windows Media Format SDK fornece conteúdo processado para coletores.</span><span class="sxs-lookup"><span data-stu-id="24ed0-120">The writer object of the Windows Media Format SDK delivers processed content to sinks.</span></span> <span data-ttu-id="24ed0-121">Cada coletor é um objeto que entrega dados.</span><span class="sxs-lookup"><span data-stu-id="24ed0-121">Each sink is an object that delivers data.</span></span> <span data-ttu-id="24ed0-122">O ponto de entrega depende do tipo de coletor.</span><span class="sxs-lookup"><span data-stu-id="24ed0-122">The point of delivery depends upon the type of sink.</span></span> <span data-ttu-id="24ed0-123">Há três tipos de coletores: coletores de arquivos, coletores de rede e coletores de push.</span><span class="sxs-lookup"><span data-stu-id="24ed0-123">There are three types of sinks: file sinks, network sinks, and push sinks.</span></span>

## <a name="file-sinks"></a><span data-ttu-id="24ed0-124">Coletores de arquivos</span><span class="sxs-lookup"><span data-stu-id="24ed0-124">File Sinks</span></span>

<span data-ttu-id="24ed0-125">Coletores de arquivos gravam conteúdo ASF em um arquivo em uma unidade local ou de rede.</span><span class="sxs-lookup"><span data-stu-id="24ed0-125">File sinks write ASF content to a file on a local or network drive.</span></span> <span data-ttu-id="24ed0-126">Quando você usa o objeto Writer para gravar um arquivo sem adicionar explicitamente um coletor de arquivos, o gravador criará um para você usando o nome passado para [**IWMWriter:: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename).</span><span class="sxs-lookup"><span data-stu-id="24ed0-126">When you use the writer object to write a file without explicitly adding a file sink, the writer will create one for you using the name you pass to [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename).</span></span> <span data-ttu-id="24ed0-127">Você pode atribuir vários coletores de arquivo a um objeto gravador para gravar o conteúdo em vários arquivos ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="24ed0-127">You can assign multiple file sinks to a writer object to write the content in several files at once.</span></span>

<span data-ttu-id="24ed0-128">Usando um coletor de arquivos, você pode controlar vários aspectos do arquivo.</span><span class="sxs-lookup"><span data-stu-id="24ed0-128">By using a file sink, you can control many aspects of the file.</span></span> <span data-ttu-id="24ed0-129">Os recursos a seguir estão disponíveis por meio de um coletor de arquivos.</span><span class="sxs-lookup"><span data-stu-id="24ed0-129">The following features are available through a file sink.</span></span>

-   <span data-ttu-id="24ed0-130">Monitoramento de estatísticas de arquivo.</span><span class="sxs-lookup"><span data-stu-id="24ed0-130">File statistics monitoring.</span></span> <span data-ttu-id="24ed0-131">Você pode monitorar o tamanho do arquivo e a duração à medida que ele está sendo criado.</span><span class="sxs-lookup"><span data-stu-id="24ed0-131">You can monitor the file size and duration as it is being created.</span></span>
-   <span data-ttu-id="24ed0-132">Criação de arquivo de conteúdo parcial.</span><span class="sxs-lookup"><span data-stu-id="24ed0-132">Partial content file creation.</span></span> <span data-ttu-id="24ed0-133">Os coletores de arquivos podem ser configurados para começar a gravar conteúdo em um horário específico e para terminar a gravação em um horário específico.</span><span class="sxs-lookup"><span data-stu-id="24ed0-133">File sinks can be configured to begin writing content at a specific time and to end writing at a specific time.</span></span> <span data-ttu-id="24ed0-134">Isso permite que você crie vários arquivos que contenham seções diferentes do mesmo conteúdo na mesma passagem de escrita.</span><span class="sxs-lookup"><span data-stu-id="24ed0-134">This enables you to create multiple files containing different sections of the same content in the same writing pass.</span></span>

## <a name="network-sinks"></a><span data-ttu-id="24ed0-135">Coletores de rede</span><span class="sxs-lookup"><span data-stu-id="24ed0-135">Network Sinks</span></span>

<span data-ttu-id="24ed0-136">Coletores de rede difundem o conteúdo para um endereço de rede.</span><span class="sxs-lookup"><span data-stu-id="24ed0-136">Network sinks broadcast content to a network address.</span></span> <span data-ttu-id="24ed0-137">A leitura de clientes pode se conectar ao endereço para receber a transmissão.</span><span class="sxs-lookup"><span data-stu-id="24ed0-137">Reading clients can connect to the address to receive the broadcast.</span></span>

## <a name="push-sinks"></a><span data-ttu-id="24ed0-138">Coletores push</span><span class="sxs-lookup"><span data-stu-id="24ed0-138">Push Sinks</span></span>

<span data-ttu-id="24ed0-139">Coletores Push entregam conteúdo do gravador para um servidor que executa os serviços de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="24ed0-139">Push sinks deliver content from the writer to a server running Windows Media Services.</span></span> <span data-ttu-id="24ed0-140">Os coletores de push normalmente são usados em cenários em que um computador codifica conteúdo ao vivo e o entrega a um ou mais servidores para distribuição ampla.</span><span class="sxs-lookup"><span data-stu-id="24ed0-140">Push sinks are typically used in scenarios where one computer encodes live content and delivers it to one or more servers for wide distribution.</span></span> <span data-ttu-id="24ed0-141">O uso de um coletor de push permite dedicar computadores a tarefas específicas, economizando largura de banda e capacidade de processamento em cada servidor.</span><span class="sxs-lookup"><span data-stu-id="24ed0-141">Using a push sink enables you to dedicate computers to specific tasks, saving bandwidth and processing power on each server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24ed0-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="24ed0-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24ed0-143">**Recursos de gravação de arquivo**</span><span class="sxs-lookup"><span data-stu-id="24ed0-143">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="24ed0-144">**Trabalhando com coletores de gravador**</span><span class="sxs-lookup"><span data-stu-id="24ed0-144">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




