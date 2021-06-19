---
description: Entenda os argumentos InputLocale e keywordlocale no Windows Search, que ajuda o mecanismo de pesquisa a usar os separadores de palavras corretos.
ms.assetid: dc610f49-5106-47f9-b29b-84949dd2c42b
title: Argumentos de identificador de localidade (pesquisa do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe4c56e9c3fb5a84938d4779c7a3ebeb849b0787
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403749"
---
# <a name="locale-identifier-arguments-windows-search"></a><span data-ttu-id="7ae78-103">Argumentos de identificador de localidade (pesquisa do Windows)</span><span class="sxs-lookup"><span data-stu-id="7ae78-103">Locale Identifier Arguments (Windows Search)</span></span>

<span data-ttu-id="7ae78-104">Os `inputlocale` `keywordlocale` identificadores e ajudam o mecanismo de pesquisa a usar os separadores de palavras corretos identificando o idioma das consultas inseridas pelo usuário e o idioma o das palavras-chave da sintaxe de consulta avançada.</span><span class="sxs-lookup"><span data-stu-id="7ae78-104">The `inputlocale` and `keywordlocale` identifiers help the search engine use the correct word breakers by identifying the language of user-entered queries and the language the of Advanced Query Syntax keywords.</span></span> <span data-ttu-id="7ae78-105">Esses nem sempre são os mesmos identificadores de código de linguagem (LCIDs) porque o Windows Search é oferecido em várias versões internacionais e também inclui MUI Packs para mais idiomas.</span><span class="sxs-lookup"><span data-stu-id="7ae78-105">These are not always the same language code identifiers (LCIDs) because Windows Search is offered in a number of international versions and also includes MUI packs for more languages.</span></span> <span data-ttu-id="7ae78-106">O InputLocale identifica o LCID para a linguagem na qual os usuários inserim sua consulta de pesquisa, enquanto o keywordlocale identifica o LCID que o mecanismo de pesquisa usa para palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="7ae78-106">The inputlocale identifies the LCID for the language users input their search query in, while the keywordlocale identifies the LCID the search engine uses for keywords.</span></span>

<span data-ttu-id="7ae78-107">Este tópico é organizado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7ae78-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="7ae78-108">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7ae78-108">Example</span></span>](#example)
-   [<span data-ttu-id="7ae78-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7ae78-109">Related topics</span></span>](#related-topics)

## <a name="example"></a><span data-ttu-id="7ae78-110">Exemplo</span><span class="sxs-lookup"><span data-stu-id="7ae78-110">Example</span></span>


```
 search-ms:query=matthew&inputlocale=2072&keywordlocale=1033
```



## <a name="related-topics"></a><span data-ttu-id="7ae78-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7ae78-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ae78-112">Introdução com argumentos de Parameter-Value</span><span class="sxs-lookup"><span data-stu-id="7ae78-112">Getting Started with Parameter-Value Arguments</span></span>](getting-started-with-parameter-value-arguments.md)
</dt> <dt>

[<span data-ttu-id="7ae78-113">Argumento de trilha</span><span class="sxs-lookup"><span data-stu-id="7ae78-113">CRUMB Argument</span></span>](-search-3x-wds-qryidx-crumb.md)
</dt> <dt>

[<span data-ttu-id="7ae78-114">Argumento de sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ae78-114">SYNTAX Argument</span></span>](-search-3x-wds-qryidx-syntaxargument.md)
</dt> <dt>

[<span data-ttu-id="7ae78-115">Argumento STACKEDBY</span><span class="sxs-lookup"><span data-stu-id="7ae78-115">STACKEDBY Argument</span></span>](-search-3x-wds-qryidx-stackedby.md)
</dt> <dt>

[<span data-ttu-id="7ae78-116">Argumento de subconsulta</span><span class="sxs-lookup"><span data-stu-id="7ae78-116">SUBQUERY Argument</span></span>](-search-3x-wds-qryidx-subquery.md)
</dt> </dl>

 

 



