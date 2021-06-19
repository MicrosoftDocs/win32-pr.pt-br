---
description: Entenda os argumentos inputlocale e keywordlocale na interface do usuário do Windows Shell, o que ajuda o mecanismo de pesquisa a usar os disjuntores de palavras corretos.
title: Argumentos de identificador de localidade (o Shell do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 881ce3a6-6cf6-45be-9a1e-148b9053d7c4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 34eab39e7ed956bf68048d9ce5861c12eedbbe7a
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403589"
---
# <a name="locale-identifier-arguments-the-windows-shell"></a><span data-ttu-id="91af4-103">Argumentos de identificador de localidade (o Shell do Windows)</span><span class="sxs-lookup"><span data-stu-id="91af4-103">Locale Identifier Arguments (The Windows Shell)</span></span>

<span data-ttu-id="91af4-104">Os identificadores e ajudam o mecanismo de pesquisa a usar os disjuntores de palavras corretos identificando o idioma das consultas inseridas pelo usuário e o idioma das palavras-chave de Sintaxe de Consulta `inputlocale` `keywordlocale` Avançada.</span><span class="sxs-lookup"><span data-stu-id="91af4-104">The `inputlocale` and `keywordlocale` identifiers help the search engine use the correct word breakers by identifying the language of user-entered queries and the language the of Advanced Query Syntax keywords.</span></span> <span data-ttu-id="91af4-105">Nem sempre são os mesmos LCIDs (identificadores de código de idioma), pois o Windows Search é oferecido em várias versões internacionais e também inclui pacotes Interface de Usuário Multilíngue (MUI) para mais idiomas.</span><span class="sxs-lookup"><span data-stu-id="91af4-105">These are not always the same language code identifiers (LCIDs) because Windows Search is offered in a number of international versions and also includes Multilingual User Interface (MUI) packs for more languages.</span></span> <span data-ttu-id="91af4-106">O identifica o LCID para a linguagem em que os usuários insejam sua consulta de pesquisa, enquanto o identifica o LCID que o mecanismo de pesquisa usa para `inputlocale` `keywordlocale` palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="91af4-106">The `inputlocale` identifies the LCID for the language users input their search query in, while the `keywordlocale` identifies the LCID the search engine uses for keywords.</span></span>

## <a name="example"></a><span data-ttu-id="91af4-107">Exemplo</span><span class="sxs-lookup"><span data-stu-id="91af4-107">Example</span></span>


```
search:query=matthew&inputlocale=2072&keywordlocale=1033
```



### <a name="argument-information"></a><span data-ttu-id="91af4-108">Informações de argumento</span><span class="sxs-lookup"><span data-stu-id="91af4-108">Argument Information</span></span>



|                              | <span data-ttu-id="91af4-109">Valor</span><span class="sxs-lookup"><span data-stu-id="91af4-109">Value</span></span>                                   |
|------------------------------|-----------------------------------------|
| <span data-ttu-id="91af4-110">**Sistema operacional mínimo**</span><span class="sxs-lookup"><span data-stu-id="91af4-110">**Minimum Operating System**</span></span> | <span data-ttu-id="91af4-111">Windows Vista com Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="91af4-111">Windows Vista with Service Pack 1 (SP1)</span></span> |



 

 

 



