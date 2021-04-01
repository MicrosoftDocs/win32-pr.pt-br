---
title: Trabalhando com coletores de gravador
description: Trabalhando com coletores de gravador
ms.assetid: 1ad28684-47d2-4ddb-bf18-22310f0392a0
keywords:
- ASF (Advanced Systems Format), coletores de gravador
- ASF (formato de sistemas avançados), coletores de gravador
- ASF (Advanced Systems Format), coletores
- ASF (formato de sistemas avançados), coletores
- coletores, coletores de gravador
- coletores de gravador, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d5b690d9e1ab25d15f7c1e8612bf20e32f87c81
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640113"
---
# <a name="working-with-writer-sinks"></a><span data-ttu-id="1013b-109">Trabalhando com coletores de gravador</span><span class="sxs-lookup"><span data-stu-id="1013b-109">Working with Writer Sinks</span></span>

<span data-ttu-id="1013b-110">O objeto gravador do SDK do Windows Media Format processa dados de mídia de entrada em um fluxo de bits.</span><span class="sxs-lookup"><span data-stu-id="1013b-110">The writer object of the Windows Media Format SDK processes input media data into a bit stream.</span></span> <span data-ttu-id="1013b-111">No entanto, o objeto Writer não entrega o fluxo de bits para seu destino final (seja para um arquivo ou um local de rede).</span><span class="sxs-lookup"><span data-stu-id="1013b-111">However, the writer object does not deliver the bit stream to its final destination (either to a file or a network location).</span></span> <span data-ttu-id="1013b-112">Para gravar o conteúdo do ASF em um formato utilizável, você deve usar coletores de gravador.</span><span class="sxs-lookup"><span data-stu-id="1013b-112">To write the ASF content to a usable format, you must use writer sinks.</span></span>

<span data-ttu-id="1013b-113">O objeto Writer dá suporte a três tipos de coletores: coletores de arquivos, coletores de rede e coletores de push.</span><span class="sxs-lookup"><span data-stu-id="1013b-113">The writer object supports three types of sinks: file sinks, network sinks, and push sinks.</span></span> <span data-ttu-id="1013b-114">Um coletor de arquivos grava o conteúdo ASF em um arquivo ASF no disco.</span><span class="sxs-lookup"><span data-stu-id="1013b-114">A file sink writes ASF content to an ASF file on disk.</span></span> <span data-ttu-id="1013b-115">Um coletor de rede transmite o conteúdo do ASF de um endereço de rede.</span><span class="sxs-lookup"><span data-stu-id="1013b-115">A network sink broadcasts ASF content from a network address.</span></span> <span data-ttu-id="1013b-116">Um coletor de push entrega dados a um servidor que executa os serviços de mídia do Windows para que o servidor possa disponibilizar o conteúdo para seu público-alvo.</span><span class="sxs-lookup"><span data-stu-id="1013b-116">A push sink delivers data to a server running Windows Media Services so that the server can make the content available to its intended audience.</span></span> <span data-ttu-id="1013b-117">Você também pode criar seus próprios coletores para fornecer dados de ASF de qualquer maneira que seja necessária para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1013b-117">You can also create your own sinks to deliver ASF data in whatever way is required by your application.</span></span> <span data-ttu-id="1013b-118">Para obter informações sobre coletores de rede e coletores de push, consulte [enviando dados de ASF por meio de uma rede](sending-asf-data-over-a-network.md).</span><span class="sxs-lookup"><span data-stu-id="1013b-118">For information about network sinks and push sinks, see [Sending ASF Data Over a Network](sending-asf-data-over-a-network.md).</span></span> <span data-ttu-id="1013b-119">O restante desta seção aborda os coletores de gravador.</span><span class="sxs-lookup"><span data-stu-id="1013b-119">The remainder of this section discusses writer sinks.</span></span>

<span data-ttu-id="1013b-120">Você pode configurar um ou mais coletores para cada instância do gravador que você usa.</span><span class="sxs-lookup"><span data-stu-id="1013b-120">You can configure one or more sinks for each instance of the writer you use.</span></span> <span data-ttu-id="1013b-121">Cada coletor manipula apenas um único destino.</span><span class="sxs-lookup"><span data-stu-id="1013b-121">Each sink handles only a single destination.</span></span> <span data-ttu-id="1013b-122">Por exemplo, se você quiser escrever três arquivos ao mesmo tempo, deverá criar e configurar um coletor de arquivo separado para cada um.</span><span class="sxs-lookup"><span data-stu-id="1013b-122">For example, if you want to write three files at once, you must create and configure a separate file sink for each.</span></span>

<span data-ttu-id="1013b-123">As seções a seguir descrevem o uso de coletores de gravador.</span><span class="sxs-lookup"><span data-stu-id="1013b-123">The following sections describe the use of writer sinks.</span></span>



| <span data-ttu-id="1013b-124">Seção</span><span class="sxs-lookup"><span data-stu-id="1013b-124">Section</span></span>                                                                      | <span data-ttu-id="1013b-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="1013b-125">Description</span></span>                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="1013b-126">Adicionando coletores ao gravador</span><span class="sxs-lookup"><span data-stu-id="1013b-126">Adding Sinks to the Writer</span></span>](adding-sinks-to-the-writer.md)                 | <span data-ttu-id="1013b-127">Descreve como adicionar coletores ao gravador.</span><span class="sxs-lookup"><span data-stu-id="1013b-127">Describes how to add sinks to the writer.</span></span>                                        |
| [<span data-ttu-id="1013b-128">Enumerando coletores</span><span class="sxs-lookup"><span data-stu-id="1013b-128">Enumerating Sinks</span></span>](enumerating-sinks.md)                                   | <span data-ttu-id="1013b-129">Descreve como enumerar os coletores que foram adicionados ao gravador.</span><span class="sxs-lookup"><span data-stu-id="1013b-129">Describes how to enumerate the sinks that have been added to the writer.</span></span>         |
| [<span data-ttu-id="1013b-130">Obtendo mensagens de erro de um coletor</span><span class="sxs-lookup"><span data-stu-id="1013b-130">Getting Error Messages from a Sink</span></span>](getting-error-messages-from-a-sink.md) | <span data-ttu-id="1013b-131">Descreve como configurar coletores para fornecer mensagens de status ao seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1013b-131">Describes how to configure sinks to deliver status messages to your application.</span></span> |
| [<span data-ttu-id="1013b-132">Uso de coletores de arquivos</span><span class="sxs-lookup"><span data-stu-id="1013b-132">Using File Sinks</span></span>](using-file-sinks.md)                                     | <span data-ttu-id="1013b-133">Descreve como usar um coletor de arquivos do Writer para criar um arquivo ASF no disco.</span><span class="sxs-lookup"><span data-stu-id="1013b-133">Describes how to use a writer file sink to create an ASF file on disk.</span></span>           |
| [<span data-ttu-id="1013b-134">Usando coletores personalizados</span><span class="sxs-lookup"><span data-stu-id="1013b-134">Using Custom Sinks</span></span>](using-custom-sinks.md)                                 | <span data-ttu-id="1013b-135">Descreve como criar e usar seus próprios coletores personalizados para fornecer dados ASF.</span><span class="sxs-lookup"><span data-stu-id="1013b-135">Describes how to create and use your own custom sinks to deliver ASF data.</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="1013b-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1013b-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1013b-137">**Interface IWMWriterAdvanced**</span><span class="sxs-lookup"><span data-stu-id="1013b-137">**IWMWriterAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[<span data-ttu-id="1013b-138">**Interface IWMWriterSink**</span><span class="sxs-lookup"><span data-stu-id="1013b-138">**IWMWriterSink Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)
</dt> <dt>

[<span data-ttu-id="1013b-139">**Gravando arquivos ASF**</span><span class="sxs-lookup"><span data-stu-id="1013b-139">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




