---
title: Bordas do Windows Media Player (preterido)
description: Bordas do Windows Media Player (preterido)
ms.assetid: defa461b-ffa5-4fee-bed4-aba3e733b8c4
keywords:
- Windows Media Player, bordas
- Capas do Windows Media Player, bordas
- capas, bordas
- bordas, em comparação com as capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a48ff3ec17230002e9c6b4a1eb17e3024375a58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292160"
---
# <a name="borders-for-windows-media-player-deprecated"></a><span data-ttu-id="82156-107">Bordas do Windows Media Player (preterido)</span><span class="sxs-lookup"><span data-stu-id="82156-107">Borders for Windows Media Player (deprecated)</span></span>

<span data-ttu-id="82156-108">Esta página documenta um recurso que pode não estar disponível em versões futuras do Windows Media Player e no SDK do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="82156-108">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="82156-109">Uma borda é semelhante a uma capa, mas em vez de substituir a interface do usuário pelo modo compacto do Windows Media Player, uma borda é inserida no painel em execução do modo completo do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="82156-109">A border is similar to a skin, but instead of replacing the user interface for the compact mode of Windows Media Player, a border is embedded in the Now Playing pane of the full mode Windows Media Player.</span></span>

<span data-ttu-id="82156-110">Usando um pacote de download do Windows Media, você pode incluir conteúdo com uma borda, abrindondo a maneira de aplicativos multimídia.</span><span class="sxs-lookup"><span data-stu-id="82156-110">By using a Windows Media Download package, you can include content with a border, paving the way to multimedia applications.</span></span>

<span data-ttu-id="82156-111">Um exemplo de pacote de download do Windows Media que inclui uma borda e conteúdo inserido está incluído no diretório de exemplos deste SDK.</span><span class="sxs-lookup"><span data-stu-id="82156-111">A sample Windows Media Download package that includes a border and embedded content is included in the samples directory of this SDK.</span></span>

## <a name="creating-a-border"></a><span data-ttu-id="82156-112">Criando uma borda</span><span class="sxs-lookup"><span data-stu-id="82156-112">Creating a Border</span></span>

<span data-ttu-id="82156-113">Uma borda é criada da mesma maneira que uma capa.</span><span class="sxs-lookup"><span data-stu-id="82156-113">A border is created the same way as a skin.</span></span> <span data-ttu-id="82156-114">A única diferença é que a capa é inserida dentro do painel **agora em execução** .</span><span class="sxs-lookup"><span data-stu-id="82156-114">The only difference is that the skin is embedded inside the **Now Playing** pane.</span></span> <span data-ttu-id="82156-115">Isso significa que o tamanho da capa não pode ser calculado e que todos os elementos de capa devem ser relativos.</span><span class="sxs-lookup"><span data-stu-id="82156-115">This means that the skin size cannot be calculated and that all skin elements must be relative.</span></span> <span data-ttu-id="82156-116">Se o usuário redimensionar o Windows Media Player, partes da borda poderão ser recortadas e não vistas.</span><span class="sxs-lookup"><span data-stu-id="82156-116">If the user resizes Windows Media Player, portions of the border may be clipped off and not seen.</span></span>

## <a name="loading-a-border"></a><span data-ttu-id="82156-117">Carregando uma borda</span><span class="sxs-lookup"><span data-stu-id="82156-117">Loading a Border</span></span>

<span data-ttu-id="82156-118">Uma borda é carregada quando um metarquivo do Windows Media que usa o elemento **Skin** é carregado.</span><span class="sxs-lookup"><span data-stu-id="82156-118">A border is loaded when a Windows Media metafile that uses the **SKIN** element is loaded.</span></span> <span data-ttu-id="82156-119">O atributo **href** do elemento **Skin** deve fazer referência a uma capa.</span><span class="sxs-lookup"><span data-stu-id="82156-119">The **HREF** attribute of the **SKIN** element must reference a skin.</span></span> <span data-ttu-id="82156-120">Um elemento típico de **Skin** ficaria assim:</span><span class="sxs-lookup"><span data-stu-id="82156-120">A typical **SKIN** element would look like this:</span></span>


```C++
<SKIN HREF="myborder.wmz">

```



<span data-ttu-id="82156-121">Para obter mais informações, consulte [elemento Skin (preterido)](skin-element--deprecated.md).</span><span class="sxs-lookup"><span data-stu-id="82156-121">For more information, see [SKIN Element (deprecated)](skin-element--deprecated.md).</span></span>

## <a name="including-content-with-a-border"></a><span data-ttu-id="82156-122">Incluindo conteúdo com uma borda</span><span class="sxs-lookup"><span data-stu-id="82156-122">Including Content with a Border</span></span>

<span data-ttu-id="82156-123">Você pode incluir conteúdo com uma borda usando um arquivo de download do Windows Media (com uma extensão de nome de arquivo. WMD).</span><span class="sxs-lookup"><span data-stu-id="82156-123">You can include content with a border by using a Windows Media Download file (with a .wmd file name extension).</span></span> <span data-ttu-id="82156-124">Siga estas etapas:</span><span class="sxs-lookup"><span data-stu-id="82156-124">Follow these steps:</span></span>

1.  <span data-ttu-id="82156-125">Crie a borda.</span><span class="sxs-lookup"><span data-stu-id="82156-125">Create the border.</span></span> <span data-ttu-id="82156-126">Tome cuidado para criá-lo de tal forma que o redimensionamento não arruinará a composição da borda.</span><span class="sxs-lookup"><span data-stu-id="82156-126">Take care to create it in such a way that resizing will not ruin the composition of the border.</span></span> <span data-ttu-id="82156-127">Por exemplo, não inclua um arquivo de plano de fundo; tornar o plano de fundo transparente para que uma visualização possa ser executada por trás dela.</span><span class="sxs-lookup"><span data-stu-id="82156-127">For example, do not include a background file; make the background transparent so that a visualization could run behind it.</span></span>
2.  <span data-ttu-id="82156-128">Compacte o conteúdo da capa (arte, arquivos JScript e arquivo de definição de capa) em um arquivo com uma extensão de nome de arquivo. wmz.</span><span class="sxs-lookup"><span data-stu-id="82156-128">Compress the skin contents (art, JScript files, and skin definition file) into a file with a .wmz file name extension.</span></span>
3.  <span data-ttu-id="82156-129">Crie um metarquivo do Windows Media (com uma extensão de nome de arquivo. asx) que referencie o arquivo de borda compactado (com uma extensão de nome de arquivo. wmz).</span><span class="sxs-lookup"><span data-stu-id="82156-129">Create a Windows Media metafile (with an .asx file name extension) that references the compressed border file (with a .wmz file name extension).</span></span> <span data-ttu-id="82156-130">O metarquivo pode incluir informações de playlist com metadados para arte e URLs para conteúdo específico.</span><span class="sxs-lookup"><span data-stu-id="82156-130">The metafile can include playlist information with metadata for art and URLs for specific content.</span></span>
4.  <span data-ttu-id="82156-131">Monte o conteúdo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="82156-131">Assemble the digital media content.</span></span>
5.  <span data-ttu-id="82156-132">Compacte a borda, o metarquivo e o conteúdo em um arquivo e dê a ele uma extensão de nome de arquivo. WMD.</span><span class="sxs-lookup"><span data-stu-id="82156-132">Compress the border, metafile, and content into one file and give it a .wmd file name extension.</span></span>

## <a name="using-a-border"></a><span data-ttu-id="82156-133">Usando uma borda</span><span class="sxs-lookup"><span data-stu-id="82156-133">Using a Border</span></span>

<span data-ttu-id="82156-134">Depois de criar o arquivo de download do Windows Media, tudo o que o usuário precisa fazer é clicar duas vezes nele.</span><span class="sxs-lookup"><span data-stu-id="82156-134">After you have created the Windows Media Download file, all that the user has to do is double-click on it.</span></span> <span data-ttu-id="82156-135">O arquivo será baixado para o computador do usuário.</span><span class="sxs-lookup"><span data-stu-id="82156-135">The file will be downloaded to the user's computer.</span></span> <span data-ttu-id="82156-136">Os arquivos dentro do pacote serão desempacotados, a lista de reprodução será adicionada às listas de reprodução, a borda aparecerá no painel em **execução** do modo completo do Windows Media Player e o primeiro item na nova lista de reprodução começará a ser reproduzido.</span><span class="sxs-lookup"><span data-stu-id="82156-136">The files inside the package will be unpacked, the playlist will be added to the playlists, the border will appear in the **Now Playing** pane of the full mode Windows Media Player, and the first item on the new playlist will begin playing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82156-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="82156-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82156-138">**Sobre as capas**</span><span class="sxs-lookup"><span data-stu-id="82156-138">**About Skins**</span></span>](about-skins.md)
</dt> <dt>

[<span data-ttu-id="82156-139">**Exemplos**</span><span class="sxs-lookup"><span data-stu-id="82156-139">**Samples**</span></span>](samples.md)
</dt> <dt>

[<span data-ttu-id="82156-140">**Pacotes de download do Windows Media (preterido)**</span><span class="sxs-lookup"><span data-stu-id="82156-140">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




