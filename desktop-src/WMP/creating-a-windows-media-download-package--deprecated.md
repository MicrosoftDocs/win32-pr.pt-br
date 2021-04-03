---
title: Criando um pacote de download do Windows Media (preterido)
description: Criando um pacote de download do Windows Media (preterido)
ms.assetid: 95d6a214-9da6-496d-ba40-4476814b1d5a
keywords:
- Metaarquivos do Windows Media, pacotes de download do Windows Media
- Windows Media Player, pacotes de download do Windows Media
- metaarquivos, pacotes de download do Windows Media
- Windows Media, pacotes de download do Windows Media
- Pacotes de download do Windows Media, criando
- Criando pacotes de download do Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a8716e1783f0e00cb561c3aba1d15a2c3e5b147
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005724"
---
# <a name="creating-a-windows-media-download-package-deprecated"></a><span data-ttu-id="e63db-109">Criando um pacote de download do Windows Media (preterido)</span><span class="sxs-lookup"><span data-stu-id="e63db-109">Creating a Windows Media Download Package (deprecated)</span></span>

<span data-ttu-id="e63db-110">Esta página documenta um recurso que pode não estar disponível em versões futuras do Windows Media Player e no SDK do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e63db-110">This page documents a feature that may be unavailable in future versions of Windows Media Player and the Windows Media Player SDK.</span></span>

<span data-ttu-id="e63db-111">Siga estas etapas para criar um pacote de download do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e63db-111">Follow these steps to create a Windows Media Download package.</span></span>

1.  <span data-ttu-id="e63db-112">**Criar uma borda.**</span><span class="sxs-lookup"><span data-stu-id="e63db-112">**Create a border.**</span></span> <span data-ttu-id="e63db-113">Use as mesmas técnicas que você usaria para criar uma capa para o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e63db-113">Use the same techniques you would use to build a skin for Windows Media Player.</span></span> <span data-ttu-id="e63db-114">Projete a borda para que o redimensionamento do Windows Media Player não arruinar a composição dos elementos de borda.</span><span class="sxs-lookup"><span data-stu-id="e63db-114">Design the border so that resizing Windows Media Player will not ruin the composition of the border elements.</span></span> <span data-ttu-id="e63db-115">Por exemplo, use uma cor sólida ou uma visualização como um plano de fundo, pois elas serão dimensionadas corretamente à medida que o Windows Media Player for redimensionado.</span><span class="sxs-lookup"><span data-stu-id="e63db-115">For instance, use a solid color or visualization as a background because these will scale well as Windows Media Player is resized.</span></span>
2.  <span data-ttu-id="e63db-116">**Compactar o conteúdo da borda.**</span><span class="sxs-lookup"><span data-stu-id="e63db-116">**Compress the border contents.**</span></span> <span data-ttu-id="e63db-117">Crie uma pasta compactada (com uma extensão de nome de arquivo. zip) que contenha os arquivos de borda: imagens, arquivos JScript e o arquivo de definição de capa com uma extensão de nome de arquivo. WMS.</span><span class="sxs-lookup"><span data-stu-id="e63db-117">Create a compressed folder (with a .zip file name extension) that contains the border files: images, JScript files, and the skin definition file with a .wms file name extension.</span></span> <span data-ttu-id="e63db-118">Renomeie o arquivo compactado para que ele tenha uma extensão de nome de arquivo. wmz.</span><span class="sxs-lookup"><span data-stu-id="e63db-118">Rename the compressed file so that it has a .wmz file name extension.</span></span>
3.  <span data-ttu-id="e63db-119">**Escreva um metarquivo do Windows Media.**</span><span class="sxs-lookup"><span data-stu-id="e63db-119">**Write a Windows Media metafile.**</span></span> <span data-ttu-id="e63db-120">O Windows Media Player não carregará a borda, a menos que você crie um metarquivo do Windows Media com uma extensão de nome de arquivo. asx que implemente o elemento **Skin** .</span><span class="sxs-lookup"><span data-stu-id="e63db-120">Windows Media Player will not load the border unless you create a Windows Media metafile with an .asx file name extension that implements the **SKIN** element.</span></span> <span data-ttu-id="e63db-121">O metarquivo também pode ser usado para criar uma lista de reprodução que descreve o conteúdo incluído no pacote.</span><span class="sxs-lookup"><span data-stu-id="e63db-121">The metafile can also be used to create a playlist that describes the content included in the package.</span></span>
4.  <span data-ttu-id="e63db-122">**Monte seu conteúdo.**</span><span class="sxs-lookup"><span data-stu-id="e63db-122">**Assemble your content.**</span></span> <span data-ttu-id="e63db-123">Coloque todos os arquivos que você deseja usar em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="e63db-123">Put all the files that you want to use into a folder.</span></span> <span data-ttu-id="e63db-124">Isso inclui arquivos de áudio, arquivos de vídeo, metaarquivos e arquivos de definição de borda.</span><span class="sxs-lookup"><span data-stu-id="e63db-124">This includes audio files, video files, metafiles, and border definition files.</span></span>
5.  <span data-ttu-id="e63db-125">**Crie o pacote.**</span><span class="sxs-lookup"><span data-stu-id="e63db-125">**Create the package.**</span></span> <span data-ttu-id="e63db-126">Crie uma pasta compactada (com uma extensão de nome de arquivo. zip) que contenha o arquivo de borda, arquivos de conteúdo e o metarquivo.</span><span class="sxs-lookup"><span data-stu-id="e63db-126">Create a compressed folder (with a .zip file name extension) that contains the border file, content files, and the metafile.</span></span> <span data-ttu-id="e63db-127">Altere a extensão de nome de arquivo desse arquivo. zip para uma extensão de nome de arquivo. WMD.</span><span class="sxs-lookup"><span data-stu-id="e63db-127">Change the file name extension of this .zip file to a .wmd file name extension.</span></span>
6.  <span data-ttu-id="e63db-128">**Poste o pacote em um site.**</span><span class="sxs-lookup"><span data-stu-id="e63db-128">**Post the package to a website.**</span></span> <span data-ttu-id="e63db-129">O pacote concluído está pronto para ser Postado em um site e baixado pelos usuários.</span><span class="sxs-lookup"><span data-stu-id="e63db-129">The completed package is ready to be posted to a website and downloaded by users.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e63db-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e63db-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e63db-131">**Pacotes de download do Windows Media (preterido)**</span><span class="sxs-lookup"><span data-stu-id="e63db-131">**Windows Media Download Packages (deprecated)**</span></span>](windows-media-download-packages--deprecated.md)
</dt> </dl>

 

 




