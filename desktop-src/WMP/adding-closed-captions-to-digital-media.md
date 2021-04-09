---
title: Adicionando legendas ocultas à mídia digital
description: Adicionando legendas ocultas à mídia digital
ms.assetid: 0fdd2cdc-32d4-4fda-9596-b050107abd5f
keywords:
- Windows Media Player, SAMI (intercâmbio de mídia acessível) sincronizado
- Modelo de objeto do Windows Media Player, SAMI (sincronização de mídia acessível)
- modelo de objeto, SAMI (intercâmbio de mídia acessível) sincronizado
- Windows Media Player Mobile, SAMI (sincronização de mídia acessível) sincronizado
- Controle ActiveX do Windows Media Player, SAMI (sincronização de mídia acessível)
- Controle ActiveX móvel do Windows Media Player, SAMI (sincronização de mídia acessível)
- Controle ActiveX, SAMI (sincronização de mídia acessível)
- SAMI (sincronização de mídia acessível), sobre
- SAMI (sincronizado com o intercâmbio de mídia acessível), sobre
- Windows Media Player, adicionando legendas ocultas
- Modelo de objeto do Windows Media Player, adicionando legendas ocultas
- modelo de objeto, adicionando legendas ocultas
- Windows Media Player Mobile, adicionando legendas ocultas
- Controle ActiveX do Windows Media Player, adicionando legendas ocultas
- Controle ActiveX móvel do Windows Media Player, adicionando legendas ocultas
- Controle ActiveX, adicionando legendas ocultas
- SAMI (intercâmbio de mídia acessível), adicionando legendas ocultas
- SAMI (sincronizado com o intercâmbio de mídia acessível), adicionando legendas ocultas
- adicionando legendas ocultas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc464fb879df1c7642cd0a04b319383654bae4aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005190"
---
# <a name="adding-closed-captions-to-digital-media"></a><span data-ttu-id="5e402-122">Adicionando legendas ocultas à mídia digital</span><span class="sxs-lookup"><span data-stu-id="5e402-122">Adding Closed Captions to Digital Media</span></span>

<span data-ttu-id="5e402-123">O SAMI (Synchronized Media Interchange) é um formato de arquivo projetado para fornecer texto sincronizado, como legendas, legendas ou descrições de áudio com conteúdo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="5e402-123">Synchronized Accessible Media Interchange (SAMI) is a file format designed to deliver synchronized text such as captions, subtitles, or audio descriptions with digital media content.</span></span> <span data-ttu-id="5e402-124">Integrado em um navegador da Web usando o modelo de objeto do Windows Media Player, o SAMI promove a acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="5e402-124">Integrated in a Web browser using the Windows Media Player object model, SAMI promotes accessibility.</span></span> <span data-ttu-id="5e402-125">Usando SAMI, você pode criar conteúdo de mídia avançado que atinja um público maior e mais diversificado.</span><span class="sxs-lookup"><span data-stu-id="5e402-125">By using SAMI, you can create rich media content that reaches a larger, more diverse audience.</span></span>

<span data-ttu-id="5e402-126">Além das fontes padrão, o SAMI pode dar suporte a outros estilos de texto, como diferentes cores, tamanhos ou linguagens para auxiliar uma variedade de usuários.</span><span class="sxs-lookup"><span data-stu-id="5e402-126">In addition to standard fonts, SAMI can support other text styles, such as different colors, sizes, or languages to aid a variety of users.</span></span> <span data-ttu-id="5e402-127">O SAMI pode ser particularmente útil para indivíduos com deficiência visual ou aqueles surdos ou com deficiência auditiva.</span><span class="sxs-lookup"><span data-stu-id="5e402-127">SAMI can be particularly useful for individuals who have low vision or those who are deaf or hard-of-hearing.</span></span> <span data-ttu-id="5e402-128">O formato SAMI também pode ajudar em propósitos educacionais, como ensinar alunos a uma segunda linguagem.</span><span class="sxs-lookup"><span data-stu-id="5e402-128">The SAMI format can also assist in educational purposes, such as teaching students a second language.</span></span>

<span data-ttu-id="5e402-129">Este tópico se concentra na incorporação do SAMI com o modelo de objeto de controle ActiveX do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="5e402-129">This topic focuses on the incorporation of SAMI with the Windows Media Player ActiveX control object model.</span></span> <span data-ttu-id="5e402-130">Os arquivos SAMI existem independentemente dos arquivos de mídia digital e não dependem de um formato de áudio ou vídeo específico para funcionar.</span><span class="sxs-lookup"><span data-stu-id="5e402-130">SAMI files exist independently from digital media files and do not rely on a specific video or audio format to function.</span></span> <span data-ttu-id="5e402-131">Como os arquivos são separados, o controle do Windows Media Player irá localizar, analisar, sincronizar e renderizar cada arquivo no computador do cliente.</span><span class="sxs-lookup"><span data-stu-id="5e402-131">Since the files are separate, the Windows Media Player control will locate, parse, synchronize, and render each file on the client's computer.</span></span> <span data-ttu-id="5e402-132">Isso proporciona flexibilidade e funcionalidade adicionais porque permite a edição de arquivos SAMI individuais, a incorporação do arquivo SAMI com formatos de mídia digital diferentes e o armazenamento de arquivos SAMI em diferentes locais de servidor.</span><span class="sxs-lookup"><span data-stu-id="5e402-132">This provides for added flexibility and functionality because it allows for the editing of individual SAMI files, the incorporation of the SAMI file with different digital media formats, and the storage of SAMI files on different server locations.</span></span>

<span data-ttu-id="5e402-133">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="5e402-133">This topic contains the following sections.</span></span>



| <span data-ttu-id="5e402-134">Seção</span><span class="sxs-lookup"><span data-stu-id="5e402-134">Section</span></span>                                                                                                                            | <span data-ttu-id="5e402-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="5e402-135">Description</span></span>                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e402-136">Sobre arquivos SAMI</span><span class="sxs-lookup"><span data-stu-id="5e402-136">About SAMI Files</span></span>](about-sami-files.md)                                                                                           | <span data-ttu-id="5e402-137">Descreve a estrutura básica de arquivos SAMI.</span><span class="sxs-lookup"><span data-stu-id="5e402-137">Describes the basic structure of SAMI files.</span></span>                                               |
| [<span data-ttu-id="5e402-138">Exemplo de arquivo SAMI</span><span class="sxs-lookup"><span data-stu-id="5e402-138">SAMI File Example</span></span>](sami-file-example.md)                                                                                         | <span data-ttu-id="5e402-139">Descreve a estrutura de um exemplo de arquivo SAMI.</span><span class="sxs-lookup"><span data-stu-id="5e402-139">Describes the structure of an example SAMI file.</span></span>                                           |
| [<span data-ttu-id="5e402-140">Usando SAMI com o controle do Windows Media Player em um navegador</span><span class="sxs-lookup"><span data-stu-id="5e402-140">Using SAMI with the Windows Media Player Control in a Browser</span></span>](using-sami-with-the-windows-media-player-control-in-a-browser.md) | <span data-ttu-id="5e402-141">Descreve como usar o SAMI em uma página da Web com o controle do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="5e402-141">Describes how to use SAMI in a webpage with the Windows Media Player control.</span></span>              |
| [<span data-ttu-id="5e402-142">Sobre URLs SAMI</span><span class="sxs-lookup"><span data-stu-id="5e402-142">About SAMI URLs</span></span>](about-sami-urls.md)                                                                                             | <span data-ttu-id="5e402-143">Descreve como os arquivos de mídia digital podem ser associados a arquivos SAMI usando uma única URL.</span><span class="sxs-lookup"><span data-stu-id="5e402-143">Describes how digital media files can be associated with SAMI files by using a single URL.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="5e402-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5e402-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e402-145">**Guia de controle do Player**</span><span class="sxs-lookup"><span data-stu-id="5e402-145">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




