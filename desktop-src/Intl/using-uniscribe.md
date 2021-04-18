---
description: O Uniscribe fornece APIs para dar suporte à tipografia e dar suporte à exibição e edição de texto internacional, incluindo as complexas regras de scripts do Oriente Médio e asiático.
ms.assetid: d27e82df-ee97-4f55-bfab-0d1e10eaa1b7
title: Usando o Uniscribe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dcfcd602940c04aa8615d141dd9a83db1fa2e55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810163"
---
# <a name="using-uniscribe"></a><span data-ttu-id="71ea6-103">Usando o Uniscribe</span><span class="sxs-lookup"><span data-stu-id="71ea6-103">Using Uniscribe</span></span>

<span data-ttu-id="71ea6-104">O Uniscribe fornece APIs para dar suporte à tipografia e dar suporte à exibição e edição de texto internacional, incluindo as complexas regras de scripts do Oriente Médio e asiático.</span><span class="sxs-lookup"><span data-stu-id="71ea6-104">Uniscribe provides APIs to support typography and to support the display and editing of international text, including the complex rules of Middle Eastern and Asian scripts.</span></span> <span data-ttu-id="71ea6-105">O Uniscribe fornece rotinas de baixo nível para lidar com texto totalmente formatado e uma API ScriptString simples definida para texto não formatado.</span><span class="sxs-lookup"><span data-stu-id="71ea6-105">Uniscribe provides low-level routines for handling fully formatted text, and a simple ScriptString API set for unformatted text.</span></span>

<span data-ttu-id="71ea6-106">Usando o Uniscribe, os aplicativos precisam apenas gerenciar um repositório de backup de códigos de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="71ea6-106">Using Uniscribe, applications only have to manage a backing store of Unicode character codes.</span></span> <span data-ttu-id="71ea6-107">Os aplicativos de layout de texto não precisam manter nenhum outro buffer ou tabela de mapeamento para rastrear a ordem dos caracteres.</span><span class="sxs-lookup"><span data-stu-id="71ea6-107">Text layout applications do not have to maintain any other buffer or mapping table to track character order.</span></span> <span data-ttu-id="71ea6-108">Cada aplicativo só precisa armazenar e gerenciar a ordem na qual os caracteres são inseridos pelo usuário, que é a mesma ordem lógica definida por Unicode.</span><span class="sxs-lookup"><span data-stu-id="71ea6-108">Each application only has to store and manage the order in which the characters are entered by the user, which is the same logical order as defined by Unicode.</span></span> <span data-ttu-id="71ea6-109">O armazenamento de backup nunca muda como resultado de operações de layout.</span><span class="sxs-lookup"><span data-stu-id="71ea6-109">The backing store never changes as a result of layout operations.</span></span> <span data-ttu-id="71ea6-110">O Uniscribe mantém um índice dos clusters reordenados para os limites de caracteres originais passados pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="71ea6-110">Uniscribe maintains an index from the reordered clusters to the original character boundaries passed by the application.</span></span>

<span data-ttu-id="71ea6-111">Os tópicos a seguir são abordados nesta seção.</span><span class="sxs-lookup"><span data-stu-id="71ea6-111">The following topics are covered in this section.</span></span>

<span data-ttu-id="71ea6-112">**Formatação**</span><span class="sxs-lookup"><span data-stu-id="71ea6-112">**Shaping**</span></span>

-   [<span data-ttu-id="71ea6-113">Determinando se um script requer formatação de glifos</span><span class="sxs-lookup"><span data-stu-id="71ea6-113">Determining If a Script Requires Glyph Shaping</span></span>](determining-if-a-script-requires-glyph-shaping.md)
-   [<span data-ttu-id="71ea6-114">Usando mecanismos de shaping</span><span class="sxs-lookup"><span data-stu-id="71ea6-114">Using Shaping Engines</span></span>](using-shaping-engines.md)

<span data-ttu-id="71ea6-115">**Outro processamento**</span><span class="sxs-lookup"><span data-stu-id="71ea6-115">**Other Processing**</span></span>

-   [<span data-ttu-id="71ea6-116">Cache</span><span class="sxs-lookup"><span data-stu-id="71ea6-116">Caching</span></span>](caching.md)
-   [<span data-ttu-id="71ea6-117">Exibindo texto com o Uniscribe</span><span class="sxs-lookup"><span data-stu-id="71ea6-117">Displaying Text with Uniscribe</span></span>](displaying-text-with-uniscribe.md)
-   [<span data-ttu-id="71ea6-118">Processando scripts complexos</span><span class="sxs-lookup"><span data-stu-id="71ea6-118">Processing Complex Scripts</span></span>](processing-complex-scripts.md)
-   [<span data-ttu-id="71ea6-119">Usando fallback de fonte</span><span class="sxs-lookup"><span data-stu-id="71ea6-119">Using Font Fallback</span></span>](using-font-fallback.md)
-   [<span data-ttu-id="71ea6-120">Usando as funções ScriptString</span><span class="sxs-lookup"><span data-stu-id="71ea6-120">Using the ScriptString Functions</span></span>](using-the-scriptstring-functions.md)

<span data-ttu-id="71ea6-121">**Acento**</span><span class="sxs-lookup"><span data-stu-id="71ea6-121">**Caret**</span></span>

-   [<span data-ttu-id="71ea6-122">Exibindo o cursor em cadeias bidirecionais</span><span class="sxs-lookup"><span data-stu-id="71ea6-122">Displaying the Caret in Bidirectional Strings</span></span>](displaying-the-caret-in-bidirectional-strings.md)
-   [<span data-ttu-id="71ea6-123">Gerenciando posicionamento de cursor e teste de clique</span><span class="sxs-lookup"><span data-stu-id="71ea6-123">Managing Caret Placement and Hit Testing</span></span>](managing-caret-placement-and-hit-testing.md)
-   [<span data-ttu-id="71ea6-124">Convertendo o deslocamento de clique do mouse X na posição do cursor</span><span class="sxs-lookup"><span data-stu-id="71ea6-124">Translating Mouse Hit X Offset to Caret Position</span></span>](translating-mouse-hit-x-offset-to-caret-position.md)

<span data-ttu-id="71ea6-125">**Palavras e clusters de caracteres**</span><span class="sxs-lookup"><span data-stu-id="71ea6-125">**Words and Character Clusters**</span></span>

-   [<span data-ttu-id="71ea6-126">Usando clusters de caracteres</span><span class="sxs-lookup"><span data-stu-id="71ea6-126">Using Character Clusters</span></span>](using-character-clusters.md)
-   [<span data-ttu-id="71ea6-127">Usando pontos de quebra de palavras</span><span class="sxs-lookup"><span data-stu-id="71ea6-127">Using Word Break Points</span></span>](using-word-break-points.md)
-   [<span data-ttu-id="71ea6-128">Trabalhando com relações entre posições de cursor, pontos de justificações e clusters</span><span class="sxs-lookup"><span data-stu-id="71ea6-128">Working with Relationships Among Caret Positions, Justification Points, and Clusters</span></span>](working-with-relationships-among-caret-positions--justification-points--and-clusters.md)

 

 



