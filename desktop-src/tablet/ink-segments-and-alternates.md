---
description: Um reconhecedor pode encontrar várias maneiras de dividir uma amostra de tinta em segmentos de reconhecimento. Por isso, o número de alternativas de reconhecimento pode ser escalonado, mesmo para uma amostra de tinta pequena.
ms.assetid: 7ecffe3f-cbe4-4e65-a1cc-9b08534b26c9
title: Segmentos de tinta e alternativas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91183f6c9628ea798b66d703a59e44b26049e692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010465"
---
# <a name="ink-segments-and-alternates"></a><span data-ttu-id="d5d78-104">Segmentos de tinta e alternativas</span><span class="sxs-lookup"><span data-stu-id="d5d78-104">Ink Segments and Alternates</span></span>

<span data-ttu-id="d5d78-105">Um reconhecedor pode encontrar várias maneiras de dividir uma amostra de tinta em segmentos de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="d5d78-105">A recognizer may find several ways to break an ink sample into recognition segments.</span></span> <span data-ttu-id="d5d78-106">Por isso, o número de alternativas de reconhecimento pode ser escalonado, mesmo para uma amostra de tinta pequena.</span><span class="sxs-lookup"><span data-stu-id="d5d78-106">Because of this, the number of recognition alternates may be staggering, even for a small ink sample.</span></span>

<span data-ttu-id="d5d78-107">Por exemplo, "t o g e t h e r" podem produzir os seguintes resultados:</span><span class="sxs-lookup"><span data-stu-id="d5d78-107">For example, "t o g e t h e r" can yield the following results:</span></span>

-   <span data-ttu-id="d5d78-108">"para obter a sua" (além de alternativas para cada palavra)</span><span class="sxs-lookup"><span data-stu-id="d5d78-108">"to get her" (plus alternates for each word)</span></span>
-   <span data-ttu-id="d5d78-109">"para reunir" (além de alternativas para cada palavra)</span><span class="sxs-lookup"><span data-stu-id="d5d78-109">"to gather" (plus alternates for each word)</span></span>
-   <span data-ttu-id="d5d78-110">"Tog ether" (mais alternativas para cada palavra)</span><span class="sxs-lookup"><span data-stu-id="d5d78-110">"tog ether" (plus alternates for each word)</span></span>
-   <span data-ttu-id="d5d78-111">"Tog" (além de alternativas para cada palavra)</span><span class="sxs-lookup"><span data-stu-id="d5d78-111">"tog at her" (plus alternates for each word)</span></span>
-   <span data-ttu-id="d5d78-112">"juntos" (além de alternativas para a palavra)</span><span class="sxs-lookup"><span data-stu-id="d5d78-112">"together" (plus alternates for the word)</span></span>

<span data-ttu-id="d5d78-113">O objeto [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) dá suporte ao armazenamento eficiente de resultados de reconhecimento completo no objeto [**Ink**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="d5d78-113">The [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) object supports efficient storage of full recognition results within the [**Ink**](inkdisp-class.md) object.</span></span> <span data-ttu-id="d5d78-114">O objeto de **tinta** mapeia as alternativas de reconhecimento para os traços no objeto de **tinta** e também pode conter outras informações, como posição da linha de base, índices de linha e intervalos de idiomas.</span><span class="sxs-lookup"><span data-stu-id="d5d78-114">The **Ink** object maps the recognition alternates to the strokes in the **Ink** object and may also contain other information such as baseline position, line indices, and language ranges.</span></span>

 

 



