---
title: Funções e estruturas do Gerenciador de compactação de áudio
description: Funções e estruturas do Gerenciador de compactação de áudio
ms.assetid: eb00ec23-ecae-4a6c-a767-fa27513c168d
keywords:
- áudio de multimídia, funções do ACM
- áudio, funções do ACM
- Gerenciador de compactação de áudio (ACM), funções
- ACM (Gerenciador de compactação de áudio), funções
- áudio multimídia, estruturas ACM
- áudio, estruturas ACM
- Gerenciador de compactação de áudio (ACM), estruturas
- ACM (Gerenciador de compactação de áudio), estruturas
- Estruturas do ACM
- Funções do ACM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b2c261e0a3de7409fc79ec43eb5046f084ee11d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "105751624"
---
# <a name="audio-compression-manager-functions-and-structures"></a><span data-ttu-id="3d04e-113">Funções e estruturas do Gerenciador de compactação de áudio</span><span class="sxs-lookup"><span data-stu-id="3d04e-113">Audio Compression Manager Functions and Structures</span></span>

<span data-ttu-id="3d04e-114">As funções do ACM se enquadram em várias categorias.</span><span class="sxs-lookup"><span data-stu-id="3d04e-114">The ACM functions fall into several categories.</span></span> <span data-ttu-id="3d04e-115">As convenções de nomenclatura para as funções facilitam a identificação dessas categorias.</span><span class="sxs-lookup"><span data-stu-id="3d04e-115">Naming conventions for the functions make it easy to identify these categories.</span></span> <span data-ttu-id="3d04e-116">Os nomes de função (com duas exceções) são do formato *acmGroupFunction*, em que *Group* designa a categoria ACM (como "driver", "Format", "" FormatTag "," "Filter", "FilterTag" ou "Stream") e a *função* descreve a ação executada pela função.</span><span class="sxs-lookup"><span data-stu-id="3d04e-116">Function names (with two exceptions) are of the form *acmGroupFunction*, where *Group* designates the ACM category (such as "Driver," "Format," "FormatTag," "Filter," "FilterTag," or "Stream"), and *Function* describes the action performed by the function.</span></span>

<span data-ttu-id="3d04e-117">As funções nos grupos de filtro e formato são muito semelhantes.</span><span class="sxs-lookup"><span data-stu-id="3d04e-117">The functions in the filter and format groups are very similar.</span></span> <span data-ttu-id="3d04e-118">Quase todas as funções que atuam em filtros têm uma função paralela que atua em formatos.</span><span class="sxs-lookup"><span data-stu-id="3d04e-118">Almost every function that acts on filters has a parallel function that acts on formats.</span></span>

<span data-ttu-id="3d04e-119">No grupo de formato, algumas funções usam marcas de formato Wave-Audio (o membro **wFormatTag** de uma estrutura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) ) enquanto outras exigem formatos Full Wave-Audio (a estrutura **WAVEFORMATEX** completa).</span><span class="sxs-lookup"><span data-stu-id="3d04e-119">In the format group, some functions use waveform-audio format tags (the **wFormatTag** member of a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure) while others require full waveform-audio formats (the full **WAVEFORMATEX** structure).</span></span> <span data-ttu-id="3d04e-120">(Para obter informações de referência sobre a estrutura **WAVEFORMATEX** , consulte [Error](error.md).)</span><span class="sxs-lookup"><span data-stu-id="3d04e-120">(For reference information about the **WAVEFORMATEX** structure, see [Error](error.md).)</span></span>

<span data-ttu-id="3d04e-121">No grupo de filtros, algumas funções usam marcas de filtro de onda-áudio (o membro **dwFilterTag** de uma estrutura [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) ), enquanto outras exigem filtros Full Wave-Audio (a estrutura **WAVEFILTER** completa).</span><span class="sxs-lookup"><span data-stu-id="3d04e-121">In the filter group, some functions use waveform-audio filter tags (the **dwFilterTag** member of a [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) structure), while others require full waveform-audio filters (the full **WAVEFILTER** structure).</span></span>

<span data-ttu-id="3d04e-122">As funções no grupo de fluxos representam as várias etapas envolvidas em uma conversão: abrir uma instância de conversão, preparar a conversão, executar a conversão, limpar após a conclusão da conversão e fechar a instância de conversão.</span><span class="sxs-lookup"><span data-stu-id="3d04e-122">The functions in the stream group represent the many steps involved in a conversion: opening a conversion instance, preparing for the conversion, performing the conversion, cleaning up after the conversion is complete, and closing the conversion instance.</span></span>

 

 