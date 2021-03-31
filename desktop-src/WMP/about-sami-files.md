---
title: Sobre arquivos SAMI
description: Sobre arquivos SAMI
ms.assetid: 39b1e8a8-bbeb-4376-89d9-03a147f4c4fd
keywords:
- Windows Media Player, SAMI (intercâmbio de mídia acessível) sincronizado
- Modelo de objeto do Windows Media Player, SAMI (sincronização de mídia acessível)
- modelo de objeto, SAMI (intercâmbio de mídia acessível) sincronizado
- Windows Media Player Mobile, SAMI (sincronização de mídia acessível) sincronizado
- Controle ActiveX do Windows Media Player, SAMI (sincronização de mídia acessível)
- Controle ActiveX móvel do Windows Media Player, SAMI (sincronização de mídia acessível)
- Controle ActiveX, SAMI (sincronização de mídia acessível)
- Arquivos SAMI (intercâmbio de mídia acessível) sincronizados
- SAMI (sincronizado com o intercâmbio de mídia acessível), arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d310ab3eb3016937f148ebb26e810dd9e6e6b6b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822693"
---
# <a name="about-sami-files"></a><span data-ttu-id="25810-112">Sobre arquivos SAMI</span><span class="sxs-lookup"><span data-stu-id="25810-112">About SAMI Files</span></span>

<span data-ttu-id="25810-113">Os arquivos SAMI são arquivos de texto que têm uma extensão de nome de arquivo. SMI ou. Sami.</span><span class="sxs-lookup"><span data-stu-id="25810-113">SAMI files are text files that have an .smi or .sami file name extension.</span></span> <span data-ttu-id="25810-114">Elas contêm as cadeias de caracteres de texto usadas para legendas codificadas sincronizadas, legendas e descrições de áudio.</span><span class="sxs-lookup"><span data-stu-id="25810-114">They contain the text strings used for synchronized closed captions, subtitles, and audio descriptions.</span></span> <span data-ttu-id="25810-115">Eles também especificam os parâmetros de tempo usados pelo controle do Windows Media Player para sincronizar texto de legenda oculta com conteúdo de áudio ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="25810-115">They also specify the timing parameters used by the Windows Media Player control to synchronize closed caption text with audio or video content.</span></span> <span data-ttu-id="25810-116">Quando um arquivo de mídia digital atinge um horário designado no arquivo SAMI, o texto é alterado de acordo na área de exibição da legenda oculta da página da Web.</span><span class="sxs-lookup"><span data-stu-id="25810-116">When a digital media file reaches a time designated in the SAMI file, the text changes accordingly in the closed caption display area of the webpage.</span></span>

<span data-ttu-id="25810-117">Além de um editor de texto simples (como o Microsoft Notepad), o software especial não é necessário para criar um arquivo SAMI.</span><span class="sxs-lookup"><span data-stu-id="25810-117">Other than a simple text editor (such as Microsoft Notepad), special software is not required to create a SAMI file.</span></span> <span data-ttu-id="25810-118">SAMI e HTML compartilham elementos comuns, como as <HEAD> marcas e <BODY> .</span><span class="sxs-lookup"><span data-stu-id="25810-118">SAMI and HTML share common elements, such as the <HEAD> and <BODY> tags.</span></span> <span data-ttu-id="25810-119">Como no HTML, as marcas usadas em arquivos SAMI sempre devem ser usadas em pares.</span><span class="sxs-lookup"><span data-stu-id="25810-119">As in HTML, tags used in SAMI files must always be used in pairs.</span></span> <span data-ttu-id="25810-120">Por exemplo, um elemento BODY começa com uma <BODY> marca e sempre deve terminar com uma </BODY> marca.</span><span class="sxs-lookup"><span data-stu-id="25810-120">For example, a BODY element begins with a <BODY> tag and must always end with a </BODY> tag.</span></span>

<span data-ttu-id="25810-121">Um arquivo SAMI básico requer três marcas fundamentais: <SAMI> , <HEAD> e <BODY> .</span><span class="sxs-lookup"><span data-stu-id="25810-121">A basic SAMI file requires three fundamental tags: <SAMI>, <HEAD>, and <BODY>.</span></span>

<span data-ttu-id="25810-122">A <SAMI> marca identifica o documento como um documento Sami para que outros aplicativos possam reconhecer seu formato de arquivo.</span><span class="sxs-lookup"><span data-stu-id="25810-122">The <SAMI> tag identifies the document as a SAMI document so other applications can recognize its file format.</span></span>

<span data-ttu-id="25810-123">Entre as marcas <HEAD> e </HEAD> , você define as diretrizes básicas e outras informações de formato para o documento Sami, como o título do documento, informações gerais e propriedades de estilo para legendas ocultas.</span><span class="sxs-lookup"><span data-stu-id="25810-123">Between the <HEAD> and </HEAD> tags, you define basic guidelines and other format information for the SAMI document, such as the document title, general information, and style properties for closed captions.</span></span> <span data-ttu-id="25810-124">Como HTML, o conteúdo declarado dentro do elemento HEAD não é exibido como saída.</span><span class="sxs-lookup"><span data-stu-id="25810-124">Like HTML, content declared within the HEAD element does not display as output.</span></span>

<span data-ttu-id="25810-125">Elementos e atributos definidos entre as marcas <BODY> e </BODY> exibem o conteúdo visto pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="25810-125">Elements and attributes defined between the <BODY> and </BODY> tags display content seen by the user.</span></span> <span data-ttu-id="25810-126">No SAMI, o elemento BODY contém os parâmetros para sincronização e as cadeias de caracteres de texto usadas para legendas codificadas.</span><span class="sxs-lookup"><span data-stu-id="25810-126">In SAMI, the BODY element contains the parameters for synchronization and the text strings used for closed captions.</span></span>

<span data-ttu-id="25810-127">Definido dentro do elemento HEAD, o elemento STYLE fornece a funcionalidade adicional no SAMI.</span><span class="sxs-lookup"><span data-stu-id="25810-127">Defined within the HEAD element, the STYLE element provides for added functionality in SAMI.</span></span> <span data-ttu-id="25810-128">Entre as marcas <STYLE> e </STYLE> , você pode definir vários seletores de folha de estilo em cascata (CSS) para estilo e layout.</span><span class="sxs-lookup"><span data-stu-id="25810-128">Between the <STYLE> and </STYLE> tags, you can define several Cascading Style Sheet (CSS) selectors for style and layout.</span></span> <span data-ttu-id="25810-129">Propriedades de estilo, como fontes, tamanhos e alinhamentos, podem ser personalizadas para fornecer uma experiência de usuário avançada e também promover a acessibilidade.</span><span class="sxs-lookup"><span data-stu-id="25810-129">Style properties such as fonts, sizes, and alignments can be customized to provide a rich user experience while also promoting accessibility.</span></span> <span data-ttu-id="25810-130">Por exemplo, a definição de uma classe de estilo de fonte de texto grande pode melhorar a legibilidade para os usuários que têm dificuldade de ler texto pequeno.</span><span class="sxs-lookup"><span data-stu-id="25810-130">For example, defining a large text font style class can improve the readability for users who have difficulty reading small text.</span></span> <span data-ttu-id="25810-131">Além disso, ao definir várias classes de linguagem diferentes, você pode ajudar os usuários internacionais a entender melhor o conteúdo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="25810-131">In addition, by defining several different language classes, you can help international users better understand the digital media content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="25810-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="25810-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25810-133">**Adicionando legendas ocultas à mídia digital**</span><span class="sxs-lookup"><span data-stu-id="25810-133">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




