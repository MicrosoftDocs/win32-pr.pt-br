---
title: Arquivo SeekThumb
description: Arquivo SeekThumb
ms.assetid: 757aeb93-ebf0-4659-8cb0-686e54485ac4
keywords:
- Capas móveis do Windows Media Player, arquivos de arte
- capas, arquivos de arte
- arquivos para capas, arte
- arquivos de arte para capas, arquivos SeekThumbd
- Capas móveis do Windows Media Player, arquivos SeekThumb
- capas, arquivos SeekThumb
- Arquivos SeekThumb em capas
- Thumb, arquivos SeekThumb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc9f1e9434a614dbc02e48b63508c7c2c04f553d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916406"
---
# <a name="seekthumb-file"></a><span data-ttu-id="5447a-111">Arquivo SeekThumb</span><span class="sxs-lookup"><span data-stu-id="5447a-111">SeekThumb File</span></span>

<span data-ttu-id="5447a-112">O arquivo SeekThumb define a imagem que indica o local de reprodução dentro do item de mídia para um TrackBar de busca.</span><span class="sxs-lookup"><span data-stu-id="5447a-112">The SeekThumb file defines the image that indicates the playback location within the media item for a Seek trackbar.</span></span> <span data-ttu-id="5447a-113">Você pode usar um arquivo e defini-lo para uso por SeekThumb e VolumeThumb.</span><span class="sxs-lookup"><span data-stu-id="5447a-113">You can use one file and define it for use by both SeekThumb and VolumeThumb.</span></span> <span data-ttu-id="5447a-114">Ao contrário dos outros arquivos de arte, os arquivos Thumb são definidos na seção trackbars do arquivo de definição de capa.</span><span class="sxs-lookup"><span data-stu-id="5447a-114">Unlike the other art files, the thumb files are defined in the Trackbars section of the skin definition file.</span></span>

<span data-ttu-id="5447a-115">A imagem a seguir é um arquivo SeekThumb típico.</span><span class="sxs-lookup"><span data-stu-id="5447a-115">The following image is a typical SeekThumb file.</span></span>

![arquivo seekthumb](images/cesdksee.gif)

<span data-ttu-id="5447a-117">Esses dois arquivos de botão têm a mesma aparência, mas são tamanhos um pouco diferentes.</span><span class="sxs-lookup"><span data-stu-id="5447a-117">These two button files look the same but are slightly different sizes.</span></span> <span data-ttu-id="5447a-118">A imagem esquerda é a exibição normal que o usuário vê e a imagem correta é a imagem enviada pelo usuário quando toca no botão.</span><span class="sxs-lookup"><span data-stu-id="5447a-118">The left image is the normal view that the user sees, and the right image is the Pushed image the user sees when they tap on the button.</span></span>

> [!Note]  
> <span data-ttu-id="5447a-119">Arquivos de arte SeekThumb criados para capas usadas no Windows Media Player 10 Mobile ou posterior devem ter as três imagens a seguir (da esquerda para a direita): normal, enviada por push e desabilitado.</span><span class="sxs-lookup"><span data-stu-id="5447a-119">SeekThumb art files created for skins used in Windows Media Player 10 Mobile or later must have the following three images (from left to right): normal, pushed, and disabled.</span></span>

 

<span data-ttu-id="5447a-120">Talvez você queira tornar as áreas de imagens de polegar transparentes.</span><span class="sxs-lookup"><span data-stu-id="5447a-120">You may want to make certain areas of the thumb images transparent.</span></span> <span data-ttu-id="5447a-121">Isso permitirá que você crie imagens thumbs em formas diferentes de retangulares.</span><span class="sxs-lookup"><span data-stu-id="5447a-121">This will allow you to create thumb images in shapes other than rectangular.</span></span> <span data-ttu-id="5447a-122">Qualquer região de uma imagem Thumb que você preenche com a cor especificada pelo valor RGB 255, 0, 255 aparecerá transparente em sua capa.</span><span class="sxs-lookup"><span data-stu-id="5447a-122">Any region of a thumb image that you fill with the color specified by the RGB value 255, 0, 255 will appear transparent in your skin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5447a-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5447a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5447a-124">**Arquivos de arte**</span><span class="sxs-lookup"><span data-stu-id="5447a-124">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 




