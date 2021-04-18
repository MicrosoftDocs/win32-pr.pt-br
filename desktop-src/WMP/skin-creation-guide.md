---
title: Guia de criação de capa
description: Guia de criação de capa
ms.assetid: 86c77764-5c8c-4493-ac2d-15268c1ba564
keywords:
- Windows Media Player, capas
- Capas do Windows Media Player, guia de criação
- capas, guia de criação
- Criando capas, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7214accedf24bd80449bf8952bc9268f9b9bf49d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105764364"
---
# <a name="skin-creation-guide"></a><span data-ttu-id="9db5b-107">Guia de criação de capa</span><span class="sxs-lookup"><span data-stu-id="9db5b-107">Skin Creation Guide</span></span>

<span data-ttu-id="9db5b-108">Este guia é uma série de explicações detalhadas de como criar diferentes tipos de capas.</span><span class="sxs-lookup"><span data-stu-id="9db5b-108">This guide is a series of detailed explanations of how to create different kinds of skins.</span></span> <span data-ttu-id="9db5b-109">Para obter mais informações gerais sobre capas, consulte [about skins](about-skins.md).</span><span class="sxs-lookup"><span data-stu-id="9db5b-109">For more general information on skins, see [About Skins](about-skins.md).</span></span> <span data-ttu-id="9db5b-110">Para obter detalhes específicos sobre cada atributo, método e evento usado em capas, consulte a [referência de programação de capa](skin-programming-reference.md).</span><span class="sxs-lookup"><span data-stu-id="9db5b-110">For specific details about every attribute, method, and event used in skins, see the [Skin Programming Reference](skin-programming-reference.md).</span></span> <span data-ttu-id="9db5b-111">À medida que você se tornar mais envolvido na programação de sua capa, convém ler a parte desse SDK que abrange o [modelo de objeto do Windows Media Player](windows-media-player-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="9db5b-111">As you get more involved in the programming of your skin, you may want to read the part of this SDK covering the [Windows Media Player Object Model](windows-media-player-object-model.md).</span></span>

<span data-ttu-id="9db5b-112">Neste guia, as instruções para criar a arte serão fornecidas para o Adobe Photoshop 5,5, um programa de manipulação de arte popular.</span><span class="sxs-lookup"><span data-stu-id="9db5b-112">In this guide, instructions for creating the art will be given for Adobe Photoshop 5.5, a popular art manipulation program.</span></span> <span data-ttu-id="9db5b-113">As instruções específicas podem ser diferentes se você tiver um programa de arte semelhante, como o Jasc Paint Shop Pro ou o Sonic viscosity, mas os conceitos serão os mesmos.</span><span class="sxs-lookup"><span data-stu-id="9db5b-113">The specific instructions may be different if you have a similar art program such as Jasc Paint Shop Pro or Sonic Foundry Viscosity, but the concepts will be the same.</span></span> <span data-ttu-id="9db5b-114">O Photoshop foi escolhido por dois motivos: é um programa de arte popular para artistas comerciais e funciona com camadas.</span><span class="sxs-lookup"><span data-stu-id="9db5b-114">Photoshop was chosen for two reasons: it is a popular art program for commercial artists, and it works with layers.</span></span> <span data-ttu-id="9db5b-115">Como você verá nos tutoriais, as camadas são muito úteis para a criação de capa.</span><span class="sxs-lookup"><span data-stu-id="9db5b-115">As you will see in the tutorials, layers are very useful for skin creation.</span></span>

<span data-ttu-id="9db5b-116">Este guia abordará as seguintes tarefas.</span><span class="sxs-lookup"><span data-stu-id="9db5b-116">This guide will cover the following tasks.</span></span>



| <span data-ttu-id="9db5b-117">Tarefa</span><span class="sxs-lookup"><span data-stu-id="9db5b-117">Task</span></span>                                                     | <span data-ttu-id="9db5b-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="9db5b-118">Description</span></span>                                                                                     |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9db5b-119">Criando sua primeira capa</span><span class="sxs-lookup"><span data-stu-id="9db5b-119">Building Your First Skin</span></span>](building-your-first-skin.md) | <span data-ttu-id="9db5b-120">Um passo a passo de uma capa simples que inicia e para o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="9db5b-120">A walk-through of a simple skin that starts and stops Windows Media Player.</span></span>                     |
| [<span data-ttu-id="9db5b-121">Adicionando uma lista de reprodução</span><span class="sxs-lookup"><span data-stu-id="9db5b-121">Adding a Playlist</span></span>](adding-a-playlist.md)               | <span data-ttu-id="9db5b-122">Como usar uma lista de reprodução simples.</span><span class="sxs-lookup"><span data-stu-id="9db5b-122">How to use a simple playlist.</span></span>                                                                   |
| [<span data-ttu-id="9db5b-123">Escolhendo arquivos</span><span class="sxs-lookup"><span data-stu-id="9db5b-123">Choosing Files</span></span>](choosing-files.md)                     | <span data-ttu-id="9db5b-124">Como escolher arquivos com uma caixa de diálogo de arquivo aberto.</span><span class="sxs-lookup"><span data-stu-id="9db5b-124">How to pick files with an open file dialog box.</span></span>                                                 |
| [<span data-ttu-id="9db5b-125">Adicionando vídeo</span><span class="sxs-lookup"><span data-stu-id="9db5b-125">Adding Video</span></span>](adding-video.md)                         | <span data-ttu-id="9db5b-126">Como colocar uma janela de vídeo em sua capa.</span><span class="sxs-lookup"><span data-stu-id="9db5b-126">How to put a video window into your skin.</span></span>                                                       |
| [<span data-ttu-id="9db5b-127">Adicionando visualizações</span><span class="sxs-lookup"><span data-stu-id="9db5b-127">Adding Visualizations</span></span>](adding-visualizations.md)       | <span data-ttu-id="9db5b-128">Como adicionar visualizações.</span><span class="sxs-lookup"><span data-stu-id="9db5b-128">How to add visualizations.</span></span>                                                                      |
| [<span data-ttu-id="9db5b-129">Adicionando um controle deslizante</span><span class="sxs-lookup"><span data-stu-id="9db5b-129">Adding a Slider</span></span>](adding-a-slider.md)                   | <span data-ttu-id="9db5b-130">Como usar um controle deslizante para acompanhar o progresso do conteúdo de mídia... e permitir que o usuário mude!</span><span class="sxs-lookup"><span data-stu-id="9db5b-130">How to use a slider to track the progress of your media content ... and let the user change it!</span></span> |
| [<span data-ttu-id="9db5b-131">Criando controles deslizantes personalizados</span><span class="sxs-lookup"><span data-stu-id="9db5b-131">Creating Custom Sliders</span></span>](creating-custom-sliders.md)   | <span data-ttu-id="9db5b-132">Como controlar o volume com um controle deslizante personalizado.</span><span class="sxs-lookup"><span data-stu-id="9db5b-132">How to control the volume with a custom slider.</span></span>                                                 |
| [<span data-ttu-id="9db5b-133">Outros exemplos de pele</span><span class="sxs-lookup"><span data-stu-id="9db5b-133">Other Skin Samples</span></span>](other-skin-samples.md)             | <span data-ttu-id="9db5b-134">Consulte a seção de exemplos do SDK.</span><span class="sxs-lookup"><span data-stu-id="9db5b-134">See the samples section of the SDK.</span></span>                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="9db5b-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9db5b-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9db5b-136">**Capas do Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="9db5b-136">**Windows Media Player Skins**</span></span>](windows-media-player-skins.md)
</dt> </dl>

 

 




