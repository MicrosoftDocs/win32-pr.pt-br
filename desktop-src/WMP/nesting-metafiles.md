---
title: Aninhando metaarquivos
description: Aninhando metaarquivos
ms.assetid: fa355c98-31e2-4bb9-ad67-fd9a727300c3
keywords:
- Metaarquivos do Windows Media, aninhamento
- Metaarquivos do Windows Media, fazendo referência a outros metaarquivos
- aninhando metaarquivos
- metaarquivos, aninhamento
- metaarquivos, fazendo referência a outros metaarquivos
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3cd5743424858c4bbcd6f66952f4275ea82d947e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291833"
---
# <a name="nesting-metafiles"></a><span data-ttu-id="f86de-108">Aninhando metaarquivos</span><span class="sxs-lookup"><span data-stu-id="f86de-108">Nesting Metafiles</span></span>

<span data-ttu-id="f86de-109">Um metarquivo pode fazer referência A outro metarquivo.</span><span class="sxs-lookup"><span data-stu-id="f86de-109">A metafile can reference another metafile.</span></span> <span data-ttu-id="f86de-110">Para fazer referência a outro metarquivo, use o elemento **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="f86de-110">To reference another metafile, use the **ENTRYREF** element.</span></span> <span data-ttu-id="f86de-111">Um elemento **ENTRYREF** no metarquivo primário aponta para um metarquivo externo.</span><span class="sxs-lookup"><span data-stu-id="f86de-111">An **ENTRYREF** element in the primary metafile points to an external metafile.</span></span>

<span data-ttu-id="f86de-112">O controle do Windows Media Player processa os elementos de **entrada** do metarquivo referenciado como se eles estivessem incluídos no metarquivo primário na posição do elemento **ENTRYREF** .</span><span class="sxs-lookup"><span data-stu-id="f86de-112">The Windows Media Player control processes the **ENTRY** elements of the referenced metafile as if they were included in the primary metafile at the position of the **ENTRYREF** element.</span></span> <span data-ttu-id="f86de-113">No entanto, ele ignora todos os elementos de **entrada** no metarquivo referenciado que têm o atributo **SKIPIFREF** definido como Sim.</span><span class="sxs-lookup"><span data-stu-id="f86de-113">However, it skips any **ENTRY** elements in the referenced metafile that have the **SKIPIFREF** attribute set to YES.</span></span>

<span data-ttu-id="f86de-114">Os controles do Windows Media Player 7,0, 7,1 e Windows Media Player para Windows XP ignoram todos os elementos **ENTRYREF** no metarquivo referenciado.</span><span class="sxs-lookup"><span data-stu-id="f86de-114">The Windows Media Player 7.0, 7.1, and Windows Media Player for Windows XP controls ignore any **ENTRYREF** elements in the referenced metafile.</span></span> <span data-ttu-id="f86de-115">Portanto, os metaarquivos só podem ser aninhados em um nível profundo usando essas versões.</span><span class="sxs-lookup"><span data-stu-id="f86de-115">Thus, metafiles can only be nested one level deep using these versions.</span></span> <span data-ttu-id="f86de-116">Essas versões também ignoram o elemento **ASX** e seus atributos no arquivo referenciado.</span><span class="sxs-lookup"><span data-stu-id="f86de-116">These versions also ignore the **ASX** element and its attributes in the referenced file.</span></span> <span data-ttu-id="f86de-117">O Windows Media Player 9 Series ou posterior dá suporte ao aninhamento de metaarquivos de até 5 níveis.</span><span class="sxs-lookup"><span data-stu-id="f86de-117">Windows Media Player 9 Series or later supports nesting metafiles up to 5 deep.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f86de-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f86de-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f86de-119">**Criando listas de reprodução de metarquivo**</span><span class="sxs-lookup"><span data-stu-id="f86de-119">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> </dl>

 

 




