---
title: Como os pacotes de download do Windows Media funcionam (preteridos)
description: Como os pacotes de download do Windows Media funcionam (preteridos)
ms.assetid: 8bab1764-93da-4abc-a8b7-17bc44b381ce
keywords:
- Metaarquivos do Windows Media, pacotes de download do Windows Media
- Windows Media Player, pacotes de download do Windows Media
- metaarquivos, pacotes de download do Windows Media
- Windows Media, pacotes de download do Windows Media
- Pacotes de download do Windows Media, sobre
- Pacotes de download do Windows Media, como os pacotes funcionam
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1db477791bb93cd599dcef38a90b230c6cd7ddde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084062"
---
# <a name="how-windows-media-download-packages-work-deprecated"></a><span data-ttu-id="f938a-109">Como os pacotes de download do Windows Media funcionam (preteridos)</span><span class="sxs-lookup"><span data-stu-id="f938a-109">How Windows Media Download Packages Work (deprecated)</span></span>

<span data-ttu-id="f938a-110">Esta página documenta um recurso que pode não estar disponível em versões futuras do Windows Media Player e no SDK do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f938a-110">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="f938a-111">Um pacote de download do Windows Media é iniciado em um site quando um usuário clica em um link em um navegador da Web, como o Microsoft Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="f938a-111">A Windows Media Download package is launched from a website when a user clicks a link in a Web browser, such as Microsoft Internet Explorer.</span></span> <span data-ttu-id="f938a-112">Essa ação abre o Windows Media Player e, em seguida, baixa e cancela pacotes do pacote de download do Windows Media no disco rígido do usuário em uma pasta padrão.</span><span class="sxs-lookup"><span data-stu-id="f938a-112">This action opens Windows Media Player and then downloads and un-packages the Windows Media Download package on the user's hard disk in a default folder.</span></span>

<span data-ttu-id="f938a-113">Depois que os arquivos tiverem sido extraídos do pacote de download do Windows Media, o Windows Media Player localizará uma lista de reprodução do metarquivo do Windows Media com uma extensão de nome de arquivo. asx entre os arquivos empacotados.</span><span class="sxs-lookup"><span data-stu-id="f938a-113">Once the files have been extracted from the Windows Media Download package, Windows Media Player locates a Windows Media metafile playlist with an .asx file name extension among the packaged files.</span></span> <span data-ttu-id="f938a-114">Se encontrar uma, o Player criará uma lista de reprodução com base no metarquivo incluído.</span><span class="sxs-lookup"><span data-stu-id="f938a-114">If it finds one, the Player creates a playlist based on the included metafile.</span></span> <span data-ttu-id="f938a-115">Os arquivos que contêm conteúdo multimídia são então adicionados à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="f938a-115">Files that contain multimedia content are then added to the library.</span></span>

<span data-ttu-id="f938a-116">O Windows Media Player também procura um elemento **Skin** no metarquivo.</span><span class="sxs-lookup"><span data-stu-id="f938a-116">Windows Media Player also looks for a **SKIN** element in the metafile.</span></span> <span data-ttu-id="f938a-117">Se o elemento **Skin** contiver uma referência a um arquivo de borda com uma extensão de nome de arquivo. WMZ, o Player carregará a borda no painel **agora em execução** .</span><span class="sxs-lookup"><span data-stu-id="f938a-117">If the **SKIN** element contains a reference to a border file with a .wmz file name extension, the Player loads the border into the **Now Playing** pane.</span></span> <span data-ttu-id="f938a-118">Em seguida, o Player começa a reproduzir o conteúdo fornecido no pacote.</span><span class="sxs-lookup"><span data-stu-id="f938a-118">The Player then starts to play the content provided in the package.</span></span>

<span data-ttu-id="f938a-119">O diagrama a seguir mostra como o conteúdo é empacotado em um arquivo de download do Windows Media, Postado em um site, baixado e reproduzido em um computador cliente usando o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f938a-119">The following diagram shows how content is packaged in a Windows Media Download file, posted to a website, downloaded, and played on a client computer using Windows Media Player.</span></span>

![como um arquivo de download do Windows Media é obtido e reproduzido.](images/wmd-image.png) <span data-ttu-id="f938a-121">Download do Windows Media</span><span class="sxs-lookup"><span data-stu-id="f938a-121">Windows Media Download</span></span>

<span data-ttu-id="f938a-122">A tabela a seguir descreve os três elementos que compõem um pacote de download do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f938a-122">The following table describes the three elements that make up a Windows Media Download package.</span></span>



| <span data-ttu-id="f938a-123">Elemento Package</span><span class="sxs-lookup"><span data-stu-id="f938a-123">Package element</span></span>    | <span data-ttu-id="f938a-124">Função</span><span class="sxs-lookup"><span data-stu-id="f938a-124">Function</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="f938a-125">Extensões de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="f938a-125">File name extensions</span></span>                     |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="f938a-126">Borda</span><span class="sxs-lookup"><span data-stu-id="f938a-126">Border</span></span>             | <span data-ttu-id="f938a-127">Uma interface de usuário fixa e personalizada criada pelo proprietário do conteúdo para exibir, vincular e reproduzir todas as mídias empacotadas no pacote de download do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f938a-127">A fixed, customized user interface created by the content owner for displaying, linking, and playing all media packaged in the Windows Media Download package.</span></span> <span data-ttu-id="f938a-128">As técnicas usadas para criar bordas são semelhantes às usadas para criar capas.</span><span class="sxs-lookup"><span data-stu-id="f938a-128">The techniques used to create borders are similar to those used to create skins.</span></span> | <span data-ttu-id="f938a-129">.wmz</span><span class="sxs-lookup"><span data-stu-id="f938a-129">.wmz</span></span>                                     |
| <span data-ttu-id="f938a-130">Playlist de metarquivo</span><span class="sxs-lookup"><span data-stu-id="f938a-130">Metafile Playlist</span></span>  | <span data-ttu-id="f938a-131">Um metarquivo do Windows Media que contém elementos de **entrada** , informações de playlist e uma identidade de elemento de **capa** para arquivos de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="f938a-131">A Windows Media metafile that contains **ENTRY** elements, playlist information, and a **SKIN** element identity for content files.</span></span>                                                                                                             | <span data-ttu-id="f938a-132">.asx</span><span class="sxs-lookup"><span data-stu-id="f938a-132">.asx</span></span>                                     |
| <span data-ttu-id="f938a-133">Conteúdo multimídia</span><span class="sxs-lookup"><span data-stu-id="f938a-133">Multimedia Content</span></span> | <span data-ttu-id="f938a-134">Um arquivo que contém qualquer formato de áudio ou vídeo com suporte no Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f938a-134">A file containing any audio or video format that is supported by Windows Media Player.</span></span>                                                                                                                                                          | <span data-ttu-id="f938a-135">. WMA,. wmv,. ASF,. wav,. avi,. mpg,. mp3</span><span class="sxs-lookup"><span data-stu-id="f938a-135">.wma, .wmv, .asf, .wav, .avi, .mpg, .mp3</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f938a-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f938a-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f938a-137">**Pacotes de download do Windows Media (preterido)**</span><span class="sxs-lookup"><span data-stu-id="f938a-137">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




