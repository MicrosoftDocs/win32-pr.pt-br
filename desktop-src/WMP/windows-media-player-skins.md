---
title: Capas do Windows Media Player
description: Capas do Windows Media Player
ms.assetid: 0cd23497-9a47-4391-a2c1-0e3102dcc1d2
keywords:
- Windows Media Player, capas
- Capas do Windows Media Player, sobre
- capas, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e649a3a3708a04af5c21d059c3f06b5badc815d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822525"
---
# <a name="windows-media-player-skins"></a><span data-ttu-id="e0564-106">Capas do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="e0564-106">Windows Media Player Skins</span></span>

<span data-ttu-id="e0564-107">O Windows Media Player fornece uma plataforma de programação para criar capas personalizadas.</span><span class="sxs-lookup"><span data-stu-id="e0564-107">Windows Media Player provides a programming platform to create custom skins.</span></span> <span data-ttu-id="e0564-108">As capas são conjuntos de scripts, arte, mídia e arquivos de texto que podem ser combinados para criar uma nova aparência para o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e0564-108">Skins are sets of scripts, art, media, and text files that can be combined to create a new appearance for Windows Media Player.</span></span> <span data-ttu-id="e0564-109">Usando capas, você pode alterar não apenas a aparência do Windows Media Player, mas como ele funciona.</span><span class="sxs-lookup"><span data-stu-id="e0564-109">Using skins, you can change not only the way Windows Media Player looks, but how it functions.</span></span> <span data-ttu-id="e0564-110">Não só onde estão os botões e o que eles parecem, mas o que eles fazem, considerando os limites da tecnologia básica subjacente do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e0564-110">Not just where the knobs are and what they look like, but what they do, given the limits of the underlying Windows Media Player core technology.</span></span>

<span data-ttu-id="e0564-111">A tecnologia de capa é muito diferente de outros tipos de programação; essencialmente, você estará misturando programação e arte em partes iguais.</span><span class="sxs-lookup"><span data-stu-id="e0564-111">Skin technology is very different from other kinds of programming; essentially you will be mixing programming and art in equal parts.</span></span> <span data-ttu-id="e0564-112">Você não precisa ser um programador especialista (não muito mais do que você já sabe se criou páginas da Web e fez alguns scripts simples), nem precisa ser um artista (contanto que possa usar um aplicativo de edição de gráficos).</span><span class="sxs-lookup"><span data-stu-id="e0564-112">You do not need to be an expert programmer (not much more than you already know if you have created webpages and done some simple scripting), nor do you need to be an artist (as long as you can use a graphics editing application).</span></span> <span data-ttu-id="e0564-113">Você usará XML (semelhante ao HTML), Microsoft JScript e qualquer programa de arte que escolher.</span><span class="sxs-lookup"><span data-stu-id="e0564-113">You'll be using XML (similar to HTML), Microsoft JScript, and whatever art programs you choose.</span></span>

<span data-ttu-id="e0564-114">A documentação de capas contém as quatro seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="e0564-114">The skins documentation contains the following four sections.</span></span>



| <span data-ttu-id="e0564-115">Seção</span><span class="sxs-lookup"><span data-stu-id="e0564-115">Section</span></span>                                                                    | <span data-ttu-id="e0564-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="e0564-116">Description</span></span>                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0564-117">Sobre as capas</span><span class="sxs-lookup"><span data-stu-id="e0564-117">About Skins</span></span>](about-skins.md)                                             | <span data-ttu-id="e0564-118">Discute a teoria de capas em termos abstratos.</span><span class="sxs-lookup"><span data-stu-id="e0564-118">Discusses the theory of skins in abstract terms.</span></span> <span data-ttu-id="e0564-119">Você é aconselhado a, pelo menos, navegar nesta seção porque a tecnologia de capa é tão diferente de outros tipos de programação.</span><span class="sxs-lookup"><span data-stu-id="e0564-119">You are advised to at least browse this section because skin technology is so different from other kinds of programming.</span></span> <span data-ttu-id="e0564-120">Esta seção informa o porquê e como as coisas funcionam, mas apenas explica os detalhes.</span><span class="sxs-lookup"><span data-stu-id="e0564-120">This section tells you why and how things work, but only skims over the details.</span></span>                                             |
| [<span data-ttu-id="e0564-121">Guia de criação de capa</span><span class="sxs-lookup"><span data-stu-id="e0564-121">Skin Creation Guide</span></span>](skin-creation-guide.md)                             | <span data-ttu-id="e0564-122">Explica o que você precisa fazer para criar uma capa.</span><span class="sxs-lookup"><span data-stu-id="e0564-122">Explains what you need to do to create a skin.</span></span> <span data-ttu-id="e0564-123">Você provavelmente vai querer ler esta seção porque ela aborda os detalhes da criação de capas simples e, em seguida, capas mais complicadas que usam elementos de capa específicos.</span><span class="sxs-lookup"><span data-stu-id="e0564-123">You will probably want to read this section because it covers the details of creating simple skins, and then more complicated skins that use particular skin elements.</span></span> <span data-ttu-id="e0564-124">Esta seção também inclui tutoriais sobre a criação da arte necessária para criar capas.</span><span class="sxs-lookup"><span data-stu-id="e0564-124">This section also includes tutorials on creating the art needed to create skins.</span></span> |
| [<span data-ttu-id="e0564-125">Referência de programação de capa</span><span class="sxs-lookup"><span data-stu-id="e0564-125">Skin Programming Reference</span></span>](skin-programming-reference.md)               | <span data-ttu-id="e0564-126">Contém entradas de referência para cada elemento e atributo com suporte pelas capas.</span><span class="sxs-lookup"><span data-stu-id="e0564-126">Contains reference entries for every element and attribute supported by skins.</span></span> <span data-ttu-id="e0564-127">Leia os tópicos que explicam a funcionalidade que você deseja usar.</span><span class="sxs-lookup"><span data-stu-id="e0564-127">Read the topics that explain the functionality that you want to use.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="e0564-128">Capas móveis do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="e0564-128">Windows Media Player Mobile Skins</span></span>](windows-media-player-mobile-skins.md) | <span data-ttu-id="e0564-129">Fornece informações completas para a criação de capas para o Windows Media Player Mobile.</span><span class="sxs-lookup"><span data-stu-id="e0564-129">Provides complete information for creating skins for Windows Media Player Mobile.</span></span>                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="e0564-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e0564-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0564-131">**SDK do Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="e0564-131">**Windows Media Player SDK**</span></span>](windows-media-player-sdk.md)
</dt> </dl>

 

 




