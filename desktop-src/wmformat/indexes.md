---
title: Índices
description: Índices
ms.assetid: 54c694f6-3c10-4d7c-bcd1-f2b17d652e8e
keywords:
- SDK do Windows Media Format, índices
- ASF (Advanced Systems Format), índices
- ASF (formato de sistemas avançados), índices
- SDK do Windows Media Format, índices temporais
- ASF (Advanced Systems Format), índices temporais
- ASF (formato de sistemas avançados), índices temporais
- SDK do Windows Media Format, índices baseados em quadros
- ASF (Advanced Systems Format), índices baseados em quadros
- ASF (formato de sistemas avançados), índices baseados em quadros
- SDK do Windows Media Format, códigos de tempo SMPTE
- Formato de sistema avançado (ASF), códigos de tempo SMPTE
- ASF (formato de sistemas avançados), códigos de tempo SMPTE
- índices, sobre
- índices temporais
- índices baseados em quadros
- Códigos de tempo SMPTE, índices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2e5a194f9c495720cbc40ccdb192509723eee0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822908"
---
# <a name="indexes"></a><span data-ttu-id="fbce6-119">Índices</span><span class="sxs-lookup"><span data-stu-id="fbce6-119">Indexes</span></span>

<span data-ttu-id="fbce6-120">Um requisito comum para aplicativos que lêem arquivos de mídia digital é a capacidade de buscar um ponto específico no conteúdo.</span><span class="sxs-lookup"><span data-stu-id="fbce6-120">A common requirement for applications that read digital media files is the ability to seek to a specific point in the content.</span></span> <span data-ttu-id="fbce6-121">A busca pode ser difícil porque não há nenhuma garantia de que os vários fluxos em um arquivo tenham amostras com horas de início simultâneas.</span><span class="sxs-lookup"><span data-stu-id="fbce6-121">Seeking can be difficult because there is no guarantee that the various streams in a file have samples with concurrent start times.</span></span> <span data-ttu-id="fbce6-122">Esse problema é resolvido com o uso de *índices*.</span><span class="sxs-lookup"><span data-stu-id="fbce6-122">This problem is addressed with the use of *indexes*.</span></span> <span data-ttu-id="fbce6-123">Um índice é um objeto em um arquivo ASF que equivale a exemplos de vídeo com seus tempos de apresentação.</span><span class="sxs-lookup"><span data-stu-id="fbce6-123">An index is an object in an ASF file that equates video samples with their presentation times.</span></span> <span data-ttu-id="fbce6-124">Nenhum índice é necessário para fluxos de áudio porque os dados de áudio estão mais bem conectados com o tempo de apresentação do que os dados de vídeo.</span><span class="sxs-lookup"><span data-stu-id="fbce6-124">No index is required for audio streams because audio data is more closely connected with presentation time than video data is.</span></span>

<span data-ttu-id="fbce6-125">O objeto indexador do Windows Media Format SDK pode criar três tipos diferentes de índices: índices temporais, índices baseados em quadros e índices de código de tempo SMPTE.</span><span class="sxs-lookup"><span data-stu-id="fbce6-125">The indexer object of the Windows Media Format SDK can create three different types of indexes: temporal indexes, frame-based indexes, and SMPTE time code indexes.</span></span>

<span data-ttu-id="fbce6-126">Os índices temporais são o tipo mais comum.</span><span class="sxs-lookup"><span data-stu-id="fbce6-126">Temporal indexes are the most common type.</span></span> <span data-ttu-id="fbce6-127">Eles simplesmente correspondem a exemplos de vídeo com os tempos de apresentação correspondentes.</span><span class="sxs-lookup"><span data-stu-id="fbce6-127">They simply equate video samples with the corresponding presentation times.</span></span>

<span data-ttu-id="fbce6-128">Um índice baseado em quadros é igual a exemplos de vídeo com números de quadros de vídeo e tempos de apresentação.</span><span class="sxs-lookup"><span data-stu-id="fbce6-128">A frame-based index equates video samples with video frame numbers and presentation times.</span></span> <span data-ttu-id="fbce6-129">Os números de quadro são particularmente úteis em aplicativos que editam vídeo.</span><span class="sxs-lookup"><span data-stu-id="fbce6-129">Frame numbers are particularly useful in applications that edit video.</span></span>

<span data-ttu-id="fbce6-130">Um índice de código de tempo de SMTP é o tipo mais raro de índice.</span><span class="sxs-lookup"><span data-stu-id="fbce6-130">A SMTPE time code index is the rarest type of index.</span></span> <span data-ttu-id="fbce6-131">Ele usa o código de tempo SMPTE como a base do índice e pode ser usado somente em fluxos que têm carimbos de data/hora SMPTE incluídos com seus exemplos.</span><span class="sxs-lookup"><span data-stu-id="fbce6-131">It uses SMPTE time code as the basis of the index and can be used only on streams that have SMPTE time stamps included with their samples.</span></span> <span data-ttu-id="fbce6-132">Para obter mais informações sobre o código de tempo SMPTE, consulte [suporte ao código de tempo SMPTE](smpte-time-code-support.md).</span><span class="sxs-lookup"><span data-stu-id="fbce6-132">For more information about SMPTE time code, see [SMPTE Time Code Support](smpte-time-code-support.md).</span></span>

<span data-ttu-id="fbce6-133">Um arquivo ASF pode conter um índice de cada tipo para cada fluxo de vídeo que ele contém.</span><span class="sxs-lookup"><span data-stu-id="fbce6-133">An ASF file can contain an index of each type for each video stream it contains.</span></span> <span data-ttu-id="fbce6-134">Como padrão, um índice temporal é incluído para cada fluxo de vídeo em arquivos criados pelo objeto gravador.</span><span class="sxs-lookup"><span data-stu-id="fbce6-134">As a default, a temporal index is included for each video stream in files created by the writer object.</span></span> <span data-ttu-id="fbce6-135">Você pode alterar as configurações de indexação automática para seus arquivos de acordo com suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="fbce6-135">You can change the automatic indexing settings for your files to suit your needs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fbce6-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fbce6-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbce6-137">**Recursos de arquivo ASF**</span><span class="sxs-lookup"><span data-stu-id="fbce6-137">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="fbce6-138">**Trabalhando com índices**</span><span class="sxs-lookup"><span data-stu-id="fbce6-138">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> <dt>

[<span data-ttu-id="fbce6-139">**Lendo arquivos com o leitor assíncrono**</span><span class="sxs-lookup"><span data-stu-id="fbce6-139">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="fbce6-140">**Lendo arquivos com o leitor síncrono**</span><span class="sxs-lookup"><span data-stu-id="fbce6-140">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




