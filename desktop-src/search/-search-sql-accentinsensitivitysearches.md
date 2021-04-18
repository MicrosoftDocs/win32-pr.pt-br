---
description: Por padrão, o mecanismo de pesquisa do Windows e o catálogo não diferenciam sinais diacríticos, que são adicionados às letras para alterar o significado ou a pronúncia de uma palavra.
ms.assetid: 71007bd4-5232-469c-982b-ff0d24bd0c1f
title: Sensibilidade de diacríticos em pesquisas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46fb68676418fc109fa24ed2d55fb9602b7ad41d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105787725"
---
# <a name="diacritic-sensitivity-in-searches"></a><span data-ttu-id="baa83-103">Sensibilidade de diacríticos em pesquisas</span><span class="sxs-lookup"><span data-stu-id="baa83-103">Diacritic Sensitivity in Searches</span></span>

<span data-ttu-id="baa83-104">Por padrão, o mecanismo de pesquisa do Windows e o catálogo não diferenciam sinais diacríticos, que são adicionados às letras para alterar o significado ou a pronúncia de uma palavra.</span><span class="sxs-lookup"><span data-stu-id="baa83-104">By default, the Windows Search engine and catalog are insensitive to diacritics, which are accent marks added to letters to alter a word's meaning or pronunciation.</span></span> <span data-ttu-id="baa83-105">No entanto, o Windows Search permite que você altere isso para o catálogo usando o [Gerenciador de catálogo](-search-3x-wds-mngidx-catalog-manager.md) para definir a sensibilidade de diacríticos.</span><span class="sxs-lookup"><span data-stu-id="baa83-105">However, Windows Search enables you to change this for your catalog using the [Catalog Manager](-search-3x-wds-mngidx-catalog-manager.md) to set diacritic sensitivity.</span></span> <span data-ttu-id="baa83-106">Por exemplo, com a sensibilidade de diacríticos definida como **false**, o catálogo trataria "resume" e "resumé" como se fossem a mesma palavra.</span><span class="sxs-lookup"><span data-stu-id="baa83-106">For example, with diacritic sensitivity set to **FALSE**, the catalog would treat "resume" and "resumé" as if they were the same word.</span></span>

<span data-ttu-id="baa83-107">Na camada de consulta, os termos de consulta com sinais diacríticos nas cláusulas FREETEXT e CONTAINS são passados para o mecanismo e, em seguida, são normalizados (como seriam no momento do índice) para correspondência.</span><span class="sxs-lookup"><span data-stu-id="baa83-107">At the query layer, query terms with diacritics in FREETEXT and CONTAINS clauses are passed through to the engine and are then normalized (as they would be at index time) for matching.</span></span> <span data-ttu-id="baa83-108">A correspondência com relação ao catálogo sempre é sensível ao diacrítico.</span><span class="sxs-lookup"><span data-stu-id="baa83-108">Matching against the catalog is always diacritic sensitive.</span></span>

> [!Note]  
> <span data-ttu-id="baa83-109">Esse não é o caso para os intervalos de caracteres 0x2e81-F8FF e 0x1100-0x11ff.</span><span class="sxs-lookup"><span data-stu-id="baa83-109">This is not the case for the character ranges 0x2e81-f8ff and 0x1100-0x11ff.</span></span>

 

 

 



