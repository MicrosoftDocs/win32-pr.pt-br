---
title: Referência do metarquivo do Windows Media
description: Referência do metarquivo do Windows Media
ms.assetid: 03dadba3-0143-46f0-990a-108196eb58ab
keywords:
- Metaarquivos do Windows Media, referência
- metaarquivos, referência
- referência para os metaarquivos do Windows Media
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31d2c8d20d64e9a363fb37594519253206d30483
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005482"
---
# <a name="windows-media-metafile-reference"></a><span data-ttu-id="8ecb6-106">Referência do metarquivo do Windows Media</span><span class="sxs-lookup"><span data-stu-id="8ecb6-106">Windows Media Metafile Reference</span></span>

<span data-ttu-id="8ecb6-107">Esta referência documenta elementos e extensões de nome de arquivo para os metaarquivos de mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="8ecb6-107">This reference documents elements and file name extensions for Windows Media metafiles.</span></span> <span data-ttu-id="8ecb6-108">A referência é dividida nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="8ecb6-108">The reference is divided into the following sections.</span></span>



| <span data-ttu-id="8ecb6-109">Seção</span><span class="sxs-lookup"><span data-stu-id="8ecb6-109">Section</span></span>                                                                                    | <span data-ttu-id="8ecb6-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="8ecb6-110">Description</span></span>                                                                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8ecb6-111">Referência de elementos de metarquivo do Windows Media</span><span class="sxs-lookup"><span data-stu-id="8ecb6-111">Windows Media Metafile Elements Reference</span></span>](windows-media-metafile-elements-reference.md) | <span data-ttu-id="8ecb6-112">Documenta elementos de metarquivo, incluindo definições, atributos e seus valores, e condições especiais relacionadas a cada elemento.</span><span class="sxs-lookup"><span data-stu-id="8ecb6-112">Documents metafile elements, including definitions, attributes and their values, and special conditions related to each element.</span></span> |
| [<span data-ttu-id="8ecb6-113">Extensões de nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="8ecb6-113">File Name Extensions</span></span>](file-name-extensions.md)                                           | <span data-ttu-id="8ecb6-114">Documenta as extensões de nome de arquivo do metarquivo com regras e diretrizes sobre seu uso.</span><span class="sxs-lookup"><span data-stu-id="8ecb6-114">Documents metafile file name extensions with rules and guidelines on their use.</span></span>                                                  |



 

<span data-ttu-id="8ecb6-115">Os metaarquivos de mídia do Windows são arquivos de texto que fornecem informações sobre um fluxo de arquivos e sua apresentação.</span><span class="sxs-lookup"><span data-stu-id="8ecb6-115">Windows Media metafiles are text files that provide information about a file stream and its presentation.</span></span> <span data-ttu-id="8ecb6-116">Os metaarquivos são baseados na sintaxe de linguagem XML (XML) e são compostos de vários elementos do tipo XML com suas marcas e atributos.</span><span class="sxs-lookup"><span data-stu-id="8ecb6-116">The metafiles are based on the Extensible Markup Language (XML) syntax, and are made up of various XML-like elements with their tags and attributes.</span></span> <span data-ttu-id="8ecb6-117">Cada elemento define uma configuração ou ação para mídia de streaming.</span><span class="sxs-lookup"><span data-stu-id="8ecb6-117">Each element defines a setting or action for streaming media.</span></span>

<span data-ttu-id="8ecb6-118">Há dois conjuntos de marcas de elemento disponíveis para os metaarquivos.</span><span class="sxs-lookup"><span data-stu-id="8ecb6-118">There are two sets of element tags available for metafiles.</span></span> <span data-ttu-id="8ecb6-119">Os metaarquivos do lado do cliente têm um conjunto de elementos e os metaarquivos do lado do servidor têm outro conjunto de elementos.</span><span class="sxs-lookup"><span data-stu-id="8ecb6-119">Client-side metafiles have one set of elements, and server-side metafiles have another set of elements.</span></span>

<span data-ttu-id="8ecb6-120">Se uma marca de elemento não tiver elementos filho (aqueles que modificam ou estiverem contidos em outro elemento), um único caractere de barra (/) poderá ser usado no final da marca de abertura no lugar de uma marca de fechamento.</span><span class="sxs-lookup"><span data-stu-id="8ecb6-120">If an element tag does not have any child elements (those that modify or are contained within another element), a single slash character (/) can be used at the end of the opening tag in place of a closing tag.</span></span> <span data-ttu-id="8ecb6-121">Se os elementos filho não aparecerem entre a marca de abertura e de fechamento de um elemento, eles não serão elementos filho desse elemento e serão ignorados ou causarão um erro na sintaxe do metarquivo.</span><span class="sxs-lookup"><span data-stu-id="8ecb6-121">If child elements do not appear between the opening and closing tag for an element, they are not child elements for that element, and are ignored or cause an error in the syntax of the metafile.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ecb6-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8ecb6-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ecb6-123">**Sobre os metaarquivos de mídia do Windows**</span><span class="sxs-lookup"><span data-stu-id="8ecb6-123">**About Windows Media Metafiles**</span></span>](about-windows-media-metafiles.md)
</dt> <dt>

[<span data-ttu-id="8ecb6-124">**Guia de metarquivo do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="8ecb6-124">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> <dt>

[<span data-ttu-id="8ecb6-125">**Metaarquivos do Windows Media**</span><span class="sxs-lookup"><span data-stu-id="8ecb6-125">**Windows Media Metafiles**</span></span>](windows-media-metafiles.md)
</dt> </dl>

 

 




