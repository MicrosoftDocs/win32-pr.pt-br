---
description: Um &\# 0034; conjunto de caracteres&\# 0034; é um mapeamento de caracteres para seus valores de código de identificação.
ms.assetid: 0a055c02-c5ed-4790-83e4-183bc3cc6b51
title: Conjuntos de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8e62a0afbe9e5b2b3ab596a8129db833477e53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759395"
---
# <a name="character-sets"></a><span data-ttu-id="9253c-103">Conjuntos de caracteres</span><span class="sxs-lookup"><span data-stu-id="9253c-103">Character Sets</span></span>

<span data-ttu-id="9253c-104">Um "conjunto de caracteres" é um mapeamento de caracteres para seus valores de código de identificação.</span><span class="sxs-lookup"><span data-stu-id="9253c-104">A "character set" is a mapping of characters to their identifying code values.</span></span> <span data-ttu-id="9253c-105">O conjunto de caracteres mais comumente usado em computadores hoje é [Unicode](unicode.md), um padrão global para codificação de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9253c-105">The character set most commonly used in computers today is [Unicode](unicode.md), a global standard for character encoding.</span></span> <span data-ttu-id="9253c-106">Internamente, os aplicativos do Windows usam a implementação UTF-16 do Unicode.</span><span class="sxs-lookup"><span data-stu-id="9253c-106">Internally, Windows applications use the UTF-16 implementation of Unicode.</span></span> <span data-ttu-id="9253c-107">Em UTF-16, a maioria dos caracteres é identificada por códigos de dois bytes.</span><span class="sxs-lookup"><span data-stu-id="9253c-107">In UTF-16, most characters are identified by two-byte codes.</span></span> <span data-ttu-id="9253c-108">Os caracteres suplementares usados com menos frequência são representados por um par alternativo, que é um par de códigos de dois bytes.</span><span class="sxs-lookup"><span data-stu-id="9253c-108">The less commonly used supplementary characters are each represented by a surrogate pair, which is a pair of two-byte codes.</span></span> <span data-ttu-id="9253c-109">Para obter mais informações, consulte [substitutos e caracteres suplementares](surrogates-and-supplementary-characters.md).</span><span class="sxs-lookup"><span data-stu-id="9253c-109">For more information, see [Surrogates and Supplementary Characters](surrogates-and-supplementary-characters.md).</span></span>

<span data-ttu-id="9253c-110">Alguns aplicativos do Windows devem funcionar com os conjuntos de caracteres mais antigos que são nativos do Windows me/98/95.</span><span class="sxs-lookup"><span data-stu-id="9253c-110">Some Windows applications must work with the older character sets that are native to Windows Me/98/95.</span></span> <span data-ttu-id="9253c-111">As [páginas de código do Windows](code-pages.md) permitem que seu aplicativo funcione com esses conjuntos de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9253c-111">[Windows code pages](code-pages.md) allow your application to work with these character sets.</span></span> <span data-ttu-id="9253c-112">Esses conjuntos de caracteres podem ser divididos em:</span><span class="sxs-lookup"><span data-stu-id="9253c-112">These character sets can be divided into:</span></span>

-   <span data-ttu-id="9253c-113">SBCS ( [conjuntos de caracteres de byte único](single-byte-character-sets.md) ).</span><span class="sxs-lookup"><span data-stu-id="9253c-113">[Single-byte character sets](single-byte-character-sets.md) (SBCS).</span></span> <span data-ttu-id="9253c-114">Em um SBCS, cada caractere é identificado por um valor de um byte de largura.</span><span class="sxs-lookup"><span data-stu-id="9253c-114">In an SBCS, each character is identified by a value one byte wide.</span></span>
-   <span data-ttu-id="9253c-115">Conjuntos de caracteres multibyte, em particular os [conjuntos de caracteres de dois bytes](double-byte-character-sets.md) (DBCS).</span><span class="sxs-lookup"><span data-stu-id="9253c-115">Multibyte character sets, in particular the [double-byte character sets](double-byte-character-sets.md) (DBCS).</span></span> <span data-ttu-id="9253c-116">Conjuntos de caracteres multibyte fornecem um meio para representar o grande número de caracteres em muitos idiomas asiáticos.</span><span class="sxs-lookup"><span data-stu-id="9253c-116">Multibyte character sets provide a means to represent the large number of characters in many Asian languages.</span></span>

<span data-ttu-id="9253c-117">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="9253c-117">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="9253c-118">Páginas de código</span><span class="sxs-lookup"><span data-stu-id="9253c-118">Code Pages</span></span>](code-pages.md)
-   [<span data-ttu-id="9253c-119">Conjuntos de caracteres de byte duplo</span><span class="sxs-lookup"><span data-stu-id="9253c-119">Double-byte Character Sets</span></span>](double-byte-character-sets.md)
-   [<span data-ttu-id="9253c-120">Conjuntos de caracteres de byte único</span><span class="sxs-lookup"><span data-stu-id="9253c-120">Single-byte Character Sets</span></span>](single-byte-character-sets.md)
-   [<span data-ttu-id="9253c-121">Caracteres substitutos e suplementares</span><span class="sxs-lookup"><span data-stu-id="9253c-121">Surrogates and Supplementary Characters</span></span>](surrogates-and-supplementary-characters.md)
-   [<span data-ttu-id="9253c-122">Unicode</span><span class="sxs-lookup"><span data-stu-id="9253c-122">Unicode</span></span>](unicode.md)

## <a name="related-topics"></a><span data-ttu-id="9253c-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9253c-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9253c-124">Sobre Unicode e conjuntos de caracteres</span><span class="sxs-lookup"><span data-stu-id="9253c-124">About Unicode and Character Sets</span></span>](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



