---
title: Exclusão mútua
description: Exclusão mútua
ms.assetid: 3a3f6763-a241-4bbd-a6e8-62041b05622d
keywords:
- SDK do Windows Media Format, exclusão mútua
- ASF (Advanced Systems Format), exclusão mútua
- ASF (formato de sistemas avançados), exclusão mútua
- SDK do Windows Media Format, exclusão mútua do MBR
- ASF (Advanced Systems Format), exclusão mútua de MBR
- ASF (formato de sistemas avançados), exclusão mútua de MBR
- SDK do Windows Media Format, taxa de bits múltipla (MBR)
- ASF (Advanced Systems Format), taxa de bits múltipla (MBR)
- ASF (formato de sistemas avançados), taxa de bits múltipla (MBR)
- exclusão mútua, sobre
- taxa de bits múltipla (MBR), exclusão mútua
- MBR (taxa de bits múltipla), exclusão mútua
- exclusão mútua, taxa de bits
- exclusão mútua, linguagem
- exclusão mútua, apresentação
- exclusão mútua, desconhecida
- exclusão mútua, recursos
- exclusão mútua, recursos avançados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd00bf5bcb544d2541a6bc5465171fe9bacc1b9c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103823004"
---
# <a name="mutual-exclusion"></a><span data-ttu-id="b6203-121">Exclusão mútua</span><span class="sxs-lookup"><span data-stu-id="b6203-121">Mutual Exclusion</span></span>

<span data-ttu-id="b6203-122">Cada arquivo ASF contém um ou mais fluxos, cada um contendo dados de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="b6203-122">Every ASF file contains one or more streams, each containing digital media data.</span></span> <span data-ttu-id="b6203-123">Em circunstâncias normais, cada fluxo é associado a uma única saída.</span><span class="sxs-lookup"><span data-stu-id="b6203-123">Under normal circumstances, each stream is associated with a single output.</span></span> <span data-ttu-id="b6203-124">Na reprodução, o objeto leitor fornece amostras para cada saída.</span><span class="sxs-lookup"><span data-stu-id="b6203-124">On playback, the reader object delivers samples for each output.</span></span> <span data-ttu-id="b6203-125">Portanto, como padrão, cada fluxo em um arquivo ASF é entregue pelo leitor na reprodução.</span><span class="sxs-lookup"><span data-stu-id="b6203-125">So, as a default, every stream in an ASF file is delivered by the reader on playback.</span></span>

<span data-ttu-id="b6203-126">Há situações em que você não deseja que todos os fluxos sejam entregues ao cliente.</span><span class="sxs-lookup"><span data-stu-id="b6203-126">There are situations where you do not want every stream delivered to the client.</span></span> <span data-ttu-id="b6203-127">Por exemplo, se você criar um arquivo de vídeo com cinco fluxos de áudio, um para cada um dos cinco idiomas, você deseja que apenas um deles seja entregue por vez.</span><span class="sxs-lookup"><span data-stu-id="b6203-127">For example, if you create a video file with five audio streams, one for each of five languages, you want only one of them to be delivered at a time.</span></span> <span data-ttu-id="b6203-128">A exclusão mútua é um recurso do SDK do Windows Media Format que permite especificar um número de fluxos mutuamente exclusivos que todos correspondem à mesma saída.</span><span class="sxs-lookup"><span data-stu-id="b6203-128">Mutual exclusion is a feature of the Windows Media Format SDK that enables you to specify a number of mutually exclusive streams that all equate to the same output.</span></span>

<span data-ttu-id="b6203-129">A exclusão mútua é definida no perfil usado para criar um arquivo.</span><span class="sxs-lookup"><span data-stu-id="b6203-129">Mutual exclusion is defined in the profile used to create a file.</span></span> <span data-ttu-id="b6203-130">Você configura a exclusão mútua em um perfil usando objetos de exclusão mútua.</span><span class="sxs-lookup"><span data-stu-id="b6203-130">You configure mutual exclusion in a profile by using mutual exclusion objects.</span></span> <span data-ttu-id="b6203-131">Você adiciona fluxos um de cada vez ao objeto de exclusão mútua, define o tipo e inclui o objeto no perfil.</span><span class="sxs-lookup"><span data-stu-id="b6203-131">You add streams one at a time to the mutual exclusion object, set the type, and include the object in the profile.</span></span>

<span data-ttu-id="b6203-132">O Windows Media Format SDK reconhece quatro tipos de exclusão mútua:</span><span class="sxs-lookup"><span data-stu-id="b6203-132">The Windows Media Format SDK recognizes four types of mutual exclusion:</span></span>

-   <span data-ttu-id="b6203-133">Taxa de bits</span><span class="sxs-lookup"><span data-stu-id="b6203-133">Bit rate</span></span>
-   <span data-ttu-id="b6203-134">Idioma</span><span class="sxs-lookup"><span data-stu-id="b6203-134">Language</span></span>
-   <span data-ttu-id="b6203-135">Apresentação</span><span class="sxs-lookup"><span data-stu-id="b6203-135">Presentation</span></span>
-   <span data-ttu-id="b6203-136">Unknown</span><span class="sxs-lookup"><span data-stu-id="b6203-136">Unknown</span></span>

## <a name="mutual-exclusion-by-bit-rate"></a><span data-ttu-id="b6203-137">Exclusão mútua por taxa de bits</span><span class="sxs-lookup"><span data-stu-id="b6203-137">Mutual Exclusion by Bit Rate</span></span>

<span data-ttu-id="b6203-138">A exclusão mútua da taxa de bits é um tipo especial de exclusão mútua e é mais comumente conhecida como exclusão mútua de taxa de bits múltipla (MBR).</span><span class="sxs-lookup"><span data-stu-id="b6203-138">Bit rate mutual exclusion is a special type of mutual exclusion and is more commonly referred to as multiple bit rate (MBR) mutual exclusion.</span></span> <span data-ttu-id="b6203-139">Uma exclusão mútua de MBR contém um número de fluxos que se originam da mesma entrada, mas são codificados em taxas de bits diferentes.</span><span class="sxs-lookup"><span data-stu-id="b6203-139">An MBR mutual exclusion contains a number of streams that all originate from the same input, but are encoded at different bit rates.</span></span> <span data-ttu-id="b6203-140">Ao reproduzir um arquivo com MBR, o leitor determina o melhor fluxo a ser usado com base na largura de banda disponível.</span><span class="sxs-lookup"><span data-stu-id="b6203-140">When playing a file with MBR, the reader determines the best stream to use based on the available bandwidth.</span></span>

<span data-ttu-id="b6203-141">O SDK do Windows Media Format dá suporte a MBR para fluxos de áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="b6203-141">The Windows Media Format SDK supports MBR for audio and video streams.</span></span> <span data-ttu-id="b6203-142">O SDK também dá suporte a um tipo especial de vídeo MBR chamado vários MBR de tamanho de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b6203-142">The SDK also supports a special type of MBR video called multiple video size MBR.</span></span> <span data-ttu-id="b6203-143">Isso é semelhante ao vídeo MBR normal, exceto pelo fato de que os fluxos individuais podem ter diferentes tamanhos de quadro.</span><span class="sxs-lookup"><span data-stu-id="b6203-143">This is like normal MBR video except that the individual streams can have different frame sizes.</span></span> <span data-ttu-id="b6203-144">Por exemplo, você pode ter alguns fluxos no tamanho de vídeo padrão 320 x 240 e outros com taxas de bits mais altas e tamanho de vídeo 640 x 480.</span><span class="sxs-lookup"><span data-stu-id="b6203-144">For example, you might have some streams at the default 320 x 240 video size and some others with higher bit rates and 640 x 480 video size.</span></span>

## <a name="mutual-exclusion-by-language"></a><span data-ttu-id="b6203-145">Exclusão mútua por idioma</span><span class="sxs-lookup"><span data-stu-id="b6203-145">Mutual Exclusion by Language</span></span>

<span data-ttu-id="b6203-146">A exclusão mútua baseada em linguagem é projetada para uso com conteúdo (geralmente áudio) registrado em várias linguagens.</span><span class="sxs-lookup"><span data-stu-id="b6203-146">Language-based mutual exclusion is designed for use with content (usually audio) recorded in several languages.</span></span> <span data-ttu-id="b6203-147">Uma exclusão mútua baseada em linguagem inclui vários fluxos originados de entradas exclusivas.</span><span class="sxs-lookup"><span data-stu-id="b6203-147">A language-based mutual exclusion includes several streams that originate from unique inputs.</span></span> <span data-ttu-id="b6203-148">Cada entrada tem o mesmo conteúdo, mas em um idioma diferente.</span><span class="sxs-lookup"><span data-stu-id="b6203-148">Each input is the same content, but in a different language.</span></span>

<span data-ttu-id="b6203-149">Para que a exclusão mútua por idioma funcione, o aplicativo de leitura deve incluir a lógica para selecionar o idioma apropriado.</span><span class="sxs-lookup"><span data-stu-id="b6203-149">For mutual exclusion by language to work, the reading application must include logic to select the appropriate language.</span></span> <span data-ttu-id="b6203-150">Se você escrever um aplicativo para reproduzir arquivos ASF e desejar dar suporte a arquivos com a exclusão mútua baseada em idioma, deverá selecionar o fluxo apropriado antes de começar a reprodução.</span><span class="sxs-lookup"><span data-stu-id="b6203-150">If you write an application to play ASF files, and you want to support files with language-based mutual exclusion, you should select the appropriate stream before beginning playback.</span></span>

## <a name="mutual-exclusion-by-presentation"></a><span data-ttu-id="b6203-151">Exclusão mútua por apresentação</span><span class="sxs-lookup"><span data-stu-id="b6203-151">Mutual Exclusion by Presentation</span></span>

<span data-ttu-id="b6203-152">A exclusão mútua baseada em apresentação é fornecida para dar suporte a fluxos de vídeo que contêm o mesmo conteúdo codificado com taxas de proporção diferentes.</span><span class="sxs-lookup"><span data-stu-id="b6203-152">Presentation-based mutual exclusion is provided to support video streams that contain the same content encoded with different aspect ratios.</span></span> <span data-ttu-id="b6203-153">Normalmente, isso é usado ao fornecer vídeo em uma versão Letterbox (taxa de proporção 16:9), bem como formatado para telas de televisão (taxa de proporção 4:3).</span><span class="sxs-lookup"><span data-stu-id="b6203-153">Typically, this is used when providing video in a letterbox version (aspect ratio 16:9) as well as formatted for television screens (aspect ratio 4:3).</span></span>

<span data-ttu-id="b6203-154">A seleção de uma apresentação para reprodução é geralmente determinada pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="b6203-154">The selection of a presentation for playback is most often determined by the user.</span></span> <span data-ttu-id="b6203-155">Se você escrever um aplicativo para reproduzir arquivos ASF e desejar dar suporte a arquivos com a exclusão mútua baseada em apresentação, deverá apresentar ao usuário a opção de selecionar um tipo de apresentação para exibição.</span><span class="sxs-lookup"><span data-stu-id="b6203-155">If you write an application to play ASF files and want to support files with presentation based mutual exclusion, you should present the user with the option of selecting a presentation type for viewing.</span></span>

## <a name="unknown-mutual-exclusion"></a><span data-ttu-id="b6203-156">Exclusão mútua desconhecida</span><span class="sxs-lookup"><span data-stu-id="b6203-156">Unknown Mutual Exclusion</span></span>

<span data-ttu-id="b6203-157">Você pode criar uma exclusão mútua com base em qualquer critério que desejar.</span><span class="sxs-lookup"><span data-stu-id="b6203-157">You can create mutual exclusion based on any criteria you like.</span></span> <span data-ttu-id="b6203-158">Todos os tipos de exclusão mútua personalizada devem ser criados usando o tipo desconhecido.</span><span class="sxs-lookup"><span data-stu-id="b6203-158">All custom mutual exclusion types should be created using the unknown type.</span></span>

## <a name="advanced-mutual-exclusion-features"></a><span data-ttu-id="b6203-159">Recursos avançados de exclusão mútua</span><span class="sxs-lookup"><span data-stu-id="b6203-159">Advanced Mutual Exclusion Features</span></span>

<span data-ttu-id="b6203-160">Você também pode usar a exclusão mútua para atribuir fluxos a grupos que são mutuamente exclusivos uns dos outros.</span><span class="sxs-lookup"><span data-stu-id="b6203-160">You can also use mutual exclusion to assign streams to groups that are mutually exclusive of one another.</span></span> <span data-ttu-id="b6203-161">Por exemplo, talvez você queira ter fluxos de áudio em vários idiomas e atribuir um fluxo de vídeo diferente a cada um.</span><span class="sxs-lookup"><span data-stu-id="b6203-161">For example, you might want to have audio streams in multiple languages and assign a different video stream to each.</span></span> <span data-ttu-id="b6203-162">Você usa a exclusão mútua para agrupar cada fluxo de áudio com seu fluxo de vídeo correspondente e tornar todos os grupos mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="b6203-162">You use mutual exclusion to group each audio stream with its corresponding video stream and make all groups mutually exclusive.</span></span>

<span data-ttu-id="b6203-163">O leitor seleciona automaticamente fluxos para todas as exclusões mútuas.</span><span class="sxs-lookup"><span data-stu-id="b6203-163">The reader automatically selects streams for all mutual exclusions.</span></span> <span data-ttu-id="b6203-164">Para todos os tipos de exclusão mútua, exceto MBR e exclusão mútua baseada em linguagem, o leitor sempre seleciona o fluxo padrão, que é o primeiro fluxo adicionado ao objeto de exclusão mútua no perfil.</span><span class="sxs-lookup"><span data-stu-id="b6203-164">For all types of mutual exclusion except MBR and language-based mutual exclusion, the reader always selects the default stream, which is the first stream added to the mutual exclusion object in the profile.</span></span> <span data-ttu-id="b6203-165">Para MBR, o leitor seleciona o fluxo que melhor se adapta à largura de banda disponível no momento da reprodução.</span><span class="sxs-lookup"><span data-stu-id="b6203-165">For MBR, the reader selects the stream that best suits the available bandwidth at the time of playback.</span></span> <span data-ttu-id="b6203-166">Se você não quiser usar o fluxo padrão, poderá definir a seleção de fluxo como manual antes de começar a ler um arquivo.</span><span class="sxs-lookup"><span data-stu-id="b6203-166">If you do not want to use the default stream, you can set stream selection to manual before starting to read a file.</span></span>

<span data-ttu-id="b6203-167">A seleção de fluxo manual aplica-se a todo o arquivo.</span><span class="sxs-lookup"><span data-stu-id="b6203-167">Manual stream selection applies to the entire file.</span></span> <span data-ttu-id="b6203-168">Podem surgir dificuldades quando você tem exclusões mútuas de tipos diferentes no mesmo arquivo.</span><span class="sxs-lookup"><span data-stu-id="b6203-168">Difficulties can arise when you have mutual exclusions of different types in the same file.</span></span> <span data-ttu-id="b6203-169">Por exemplo, um arquivo pode conter a exclusão mútua baseada em taxa de bits e a exclusão mútua personalizada.</span><span class="sxs-lookup"><span data-stu-id="b6203-169">For example, a file can contain both bit-rate-based mutual exclusion and custom mutual exclusion.</span></span> <span data-ttu-id="b6203-170">Para selecionar um fluxo diferente do padrão na exclusão mútua personalizada, você deve usar a seleção de fluxo manual.</span><span class="sxs-lookup"><span data-stu-id="b6203-170">To select a stream other than the default in the custom mutual exclusion, you must use manual stream selection.</span></span> <span data-ttu-id="b6203-171">No entanto, se você usar a seleção de fluxo manual, o leitor não selecionará automaticamente o fluxo de taxa de bits múltiplas.</span><span class="sxs-lookup"><span data-stu-id="b6203-171">If you use manual stream selection, however, the reader will not automatically select the multiple bit rate stream.</span></span> <span data-ttu-id="b6203-172">Você deve planejar essa eventualidade em seu aplicativo se planeja dar suporte a vários tipos de exclusão mútua em um único arquivo.</span><span class="sxs-lookup"><span data-stu-id="b6203-172">You must plan for this eventuality in your application if you plan to support multiple types of mutual exclusion in a single file.</span></span> <span data-ttu-id="b6203-173">Normalmente, isso significa criar suas próprias rotinas de seleção de fluxo para tipos automáticos de exclusão mútua normalmente.</span><span class="sxs-lookup"><span data-stu-id="b6203-173">Typically this means creating your own stream selection routines for normally automatic types of mutual exclusion.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6203-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b6203-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6203-175">**Recursos de arquivo ASF**</span><span class="sxs-lookup"><span data-stu-id="b6203-175">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="b6203-176">**Usando a exclusão mútua**</span><span class="sxs-lookup"><span data-stu-id="b6203-176">**Using Mutual Exclusion**</span></span>](using-mutual-exclusion.md)
</dt> </dl>

 

 




