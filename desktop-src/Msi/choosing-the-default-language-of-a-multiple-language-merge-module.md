---
description: O idioma padrão para um módulo de mesclagem é o idioma listado na tabela ModuleSignature do módulo antes que as transformações de idioma sejam aplicadas. Esse também é o primeiro idioma listado na propriedade de resumo do modelo.
ms.assetid: 4d795727-684c-4dc1-8b46-d72b69c455c3
title: Escolhendo o idioma padrão de um módulo de mesclagem de vários idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758a3b47b7a41777652a11a1cdc1b7f380055cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828038"
---
# <a name="choosing-the-default-language-of-a-multiple-language-merge-module"></a><span data-ttu-id="3612c-104">Escolhendo o idioma padrão de um módulo de mesclagem de vários idiomas</span><span class="sxs-lookup"><span data-stu-id="3612c-104">Choosing the Default Language of a Multiple Language Merge Module</span></span>

<span data-ttu-id="3612c-105">O idioma padrão para um módulo de mesclagem é o idioma listado na [tabela ModuleSignature](modulesignature-table.md) do módulo antes que as transformações de idioma sejam aplicadas.</span><span class="sxs-lookup"><span data-stu-id="3612c-105">The default language for a merge module is the language that is listed in the [ModuleSignature Table](modulesignature-table.md) of the module before language transforms are applied.</span></span> <span data-ttu-id="3612c-106">Esse também é o primeiro idioma listado na propriedade de [**Resumo do modelo**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="3612c-106">This is also the first language that is listed in the [**Template Summary**](template-summary.md) Property.</span></span>

<span data-ttu-id="3612c-107">O idioma padrão do módulo deve ser uma das linguagens mais específicas às quais você dá suporte, pois o idioma padrão sempre é verificado primeiro e, se ele satisfizer o idioma solicitado, ele será usado mesmo se outra linguagem for uma correspondência melhor.</span><span class="sxs-lookup"><span data-stu-id="3612c-107">The default language for the module should be one of the most specific languages that you support, because the default language is always checked first, and if it satisfies the requested language, it is used even if another language is a better match.</span></span> <span data-ttu-id="3612c-108">Por exemplo, se um módulo der suporte a 1033 e a 0, 1033 deverá ser o idioma padrão.</span><span class="sxs-lookup"><span data-stu-id="3612c-108">For example, if a module supports 1033 and 0, 1033 should be the default language.</span></span> <span data-ttu-id="3612c-109">Se 0 fosse o idioma padrão, ele sempre atenderia a qualquer solicitação, e a transformação 1033 nunca seria usada, mesmo se 1033 for o idioma exato solicitado.</span><span class="sxs-lookup"><span data-stu-id="3612c-109">If 0 were the default language, it would always satisfy any request, and the 1033 transform would never be used, even if 1033 is the exact language requested.</span></span>

 

 



