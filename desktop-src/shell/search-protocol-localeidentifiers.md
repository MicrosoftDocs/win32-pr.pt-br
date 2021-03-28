---
description: Os identificadores InputLocale e keywordlocale ajudam o mecanismo de pesquisa a usar os separadores de palavras corretos identificando o idioma das consultas inseridas pelo usuário e o idioma do das palavras-chave da sintaxe de consulta avançada.
title: Argumentos de identificador de localidade (o Shell do Windows)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 881ce3a6-6cf6-45be-9a1e-148b9053d7c4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 403e0338b61a4dedba37a620000e3fd82c91f383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171549"
---
# <a name="locale-identifier-arguments-the-windows-shell"></a><span data-ttu-id="eb3fe-103">Argumentos de identificador de localidade (o Shell do Windows)</span><span class="sxs-lookup"><span data-stu-id="eb3fe-103">Locale Identifier Arguments (The Windows Shell)</span></span>

<span data-ttu-id="eb3fe-104">Os `inputlocale` `keywordlocale` identificadores e ajudam o mecanismo de pesquisa a usar os separadores de palavras corretos identificando o idioma das consultas inseridas pelo usuário e o idioma o das palavras-chave da sintaxe de consulta avançada.</span><span class="sxs-lookup"><span data-stu-id="eb3fe-104">The `inputlocale` and `keywordlocale` identifiers help the search engine use the correct word breakers by identifying the language of user-entered queries and the language the of Advanced Query Syntax keywords.</span></span> <span data-ttu-id="eb3fe-105">Esses nem sempre são os mesmos identificadores de código de linguagem (LCIDs) porque o Windows Search é oferecido em várias versões internacionais e também inclui pacotes MUI (Multilingual User interface) para mais idiomas.</span><span class="sxs-lookup"><span data-stu-id="eb3fe-105">These are not always the same language code identifiers (LCIDs) because Windows Search is offered in a number of international versions and also includes Multilingual User Interface (MUI) packs for more languages.</span></span> <span data-ttu-id="eb3fe-106">O `inputlocale` identifica o LCID para os usuários de idioma que inserim sua consulta de pesquisa no, enquanto o `keywordlocale` identifica o LCID que o mecanismo de pesquisa usa para palavras-chave.</span><span class="sxs-lookup"><span data-stu-id="eb3fe-106">The `inputlocale` identifies the LCID for the language users input their search query in, while the `keywordlocale` identifies the LCID the search engine uses for keywords.</span></span>

## <a name="example"></a><span data-ttu-id="eb3fe-107">Exemplo</span><span class="sxs-lookup"><span data-stu-id="eb3fe-107">Example</span></span>


```
search:query=matthew&inputlocale=2072&keywordlocale=1033
```



### <a name="argument-information"></a><span data-ttu-id="eb3fe-108">Informações do argumento</span><span class="sxs-lookup"><span data-stu-id="eb3fe-108">Argument Information</span></span>



|                          |                                         |
|--------------------------|-----------------------------------------|
| <span data-ttu-id="eb3fe-109">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="eb3fe-109">Minimum Operating System</span></span> | <span data-ttu-id="eb3fe-110">Windows Vista com Service Pack 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="eb3fe-110">Windows Vista with Service Pack 1 (SP1)</span></span> |



 

 

 



