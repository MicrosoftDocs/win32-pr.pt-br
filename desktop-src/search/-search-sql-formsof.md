---
description: O termo FORMSOF executa correspondências usando outras formas linguísticas da palavra.
ms.assetid: b705b8bc-dc2c-4cee-8306-f494b0f96cbf
title: FORMSOF termo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20504a7a36c7f0cb9c69b9513f33446501641bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105762403"
---
# <a name="formsof-term"></a><span data-ttu-id="78c9d-103">FORMSOF termo</span><span class="sxs-lookup"><span data-stu-id="78c9d-103">FORMSOF Term</span></span>

<span data-ttu-id="78c9d-104">O termo FORMSOF executa correspondências usando outras formas linguísticas da palavra.</span><span class="sxs-lookup"><span data-stu-id="78c9d-104">The FORMSOF term performs matches using other linguistic forms of the word.</span></span> <span data-ttu-id="78c9d-105">A seguir está a sintaxe do termo FORMSOF:</span><span class="sxs-lookup"><span data-stu-id="78c9d-105">The following is the FORMSOF term syntax:</span></span>


```
FORMSOF (<generation_type>,<match_words>)
```



<span data-ttu-id="78c9d-106">O tipo de geração especifica como o Microsoft Windows Search escolhe as formas de palavra alternativas.</span><span class="sxs-lookup"><span data-stu-id="78c9d-106">The generation type specifies how Microsoft Windows Search chooses the alternative word forms.</span></span> <span data-ttu-id="78c9d-107">O valor de **Inflexde** escolhe formulários de inflexão alternativos para as palavras de correspondência.</span><span class="sxs-lookup"><span data-stu-id="78c9d-107">The **INFLECTIONAL** value chooses alternative inflection forms for the match words.</span></span> <span data-ttu-id="78c9d-108">Se a palavra for um verbo, as dezenases alternativas serão usadas.</span><span class="sxs-lookup"><span data-stu-id="78c9d-108">If the word is a verb, alternative tenses are used.</span></span> <span data-ttu-id="78c9d-109">Se a palavra for um substantivo, os formulários singular, plural e Possessive serão usados para detectar correspondências.</span><span class="sxs-lookup"><span data-stu-id="78c9d-109">If the word is a noun, the singular, plural, and possessive forms are used to detect matches.</span></span>

<span data-ttu-id="78c9d-110">O valor de corresponder \_ palavras é uma ou mais palavras, separadas por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="78c9d-110">The match\_words value is one or more words, separated by commas.</span></span>

## <a name="examples"></a><span data-ttu-id="78c9d-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="78c9d-111">Examples</span></span>

<span data-ttu-id="78c9d-112">O exemplo a seguir pesquisa correspondências de inflexões para a palavra "Run".</span><span class="sxs-lookup"><span data-stu-id="78c9d-112">The following example searches for inflectional matches for the word "run".</span></span> <span data-ttu-id="78c9d-113">Este exemplo corresponde a documentos que contêm "Run", "Running" ou "Execute".</span><span class="sxs-lookup"><span data-stu-id="78c9d-113">This example matches documents containing "run", "running", or "ran".</span></span>


```
...CONTAINS('FORMSOF(INFLECTIONAL,"run")')
```



## <a name="related-topics"></a><span data-ttu-id="78c9d-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="78c9d-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="78c9d-115">**Referência**</span><span class="sxs-lookup"><span data-stu-id="78c9d-115">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="78c9d-116">Predicado FREETEXT</span><span class="sxs-lookup"><span data-stu-id="78c9d-116">FREETEXT Predicate</span></span>](-search-sql-freetext.md)
</dt> <dt>

[<span data-ttu-id="78c9d-117">Cláusula WHERE</span><span class="sxs-lookup"><span data-stu-id="78c9d-117">WHERE Clause</span></span>](-search-sql-where.md)
</dt> </dl>

 

 



