---
description: 'Considere o seguinte ao decidir quando e como usar o objeto divisória em um aplicativo:'
ms.assetid: 17404789-7f08-4cf1-88f8-e1f70296c163
title: Outras considerações sobre divisor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6e00ebc926dd51efb592304f6015351bdc2790b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170462"
---
# <a name="other-divider-considerations"></a><span data-ttu-id="c5446-103">Outras considerações sobre divisor</span><span class="sxs-lookup"><span data-stu-id="c5446-103">Other Divider Considerations</span></span>

<span data-ttu-id="c5446-104">Considere o seguinte ao decidir quando e como usar o objeto [**divisória**](inkdivider-class.md) em um aplicativo:</span><span class="sxs-lookup"><span data-stu-id="c5446-104">Consider the following when deciding when and how to use the [**Divider**](inkdivider-class.md) object in an application:</span></span>

-   <span data-ttu-id="c5446-105">O objeto [**divisória**](inkdivider-class.md) é projetado para separar desenhos e blocos de manuscrito, mas não para reconhecer níveis mais altos de estrutura, como tabelas ou colunas.</span><span class="sxs-lookup"><span data-stu-id="c5446-105">The [**Divider**](inkdivider-class.md) object is designed to separate drawings and blocks of handwriting, but not to recognize higher levels of structure, such as tables or columns.</span></span>
-   <span data-ttu-id="c5446-106">O objeto [**divisória**](inkdivider-class.md) não fornece interfaces especificamente para a correção de resultados da análise de layout.</span><span class="sxs-lookup"><span data-stu-id="c5446-106">The [**Divider**](inkdivider-class.md) object does not provide interfaces specifically for correction of results of layout analysis.</span></span>
-   <span data-ttu-id="c5446-107">O uso do tempo limite e do número de heurística de traço para adicionar ou remover vários traços por vez dos traços no objeto de [**divisória**](inkdivider-class.md) pode melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="c5446-107">The use of timeout and number of stroke heuristics to add or remove multiple strokes at a time from the strokes in the [**Divider**](inkdivider-class.md) object may improve performance.</span></span>

## <a name="reanalysis-considerations"></a><span data-ttu-id="c5446-108">Considerações de reanálise</span><span class="sxs-lookup"><span data-stu-id="c5446-108">Reanalysis Considerations</span></span>

<span data-ttu-id="c5446-109">Se você estiver considerando o uso do objeto [**divisor**](inkdivider-class.md) em um aplicativo em que o objeto **divisor** pode ter que reanalisar grandes quantidades de tinta, tenha em mente o seguinte.</span><span class="sxs-lookup"><span data-stu-id="c5446-109">If you are considering using the [**Divider**](inkdivider-class.md) object in an application where the **Divider** object may have to reanalyze large amounts of ink, keep the following in mind.</span></span>

### <a name="retaining-copies-of-ink-and-strokes"></a><span data-ttu-id="c5446-110">Retenção de cópias de tinta e traços</span><span class="sxs-lookup"><span data-stu-id="c5446-110">Retaining Copies of Ink and Strokes</span></span>

<span data-ttu-id="c5446-111">Um aplicativo pode manter cópias de objetos [**Ink**](inkdisp-class.md) e [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) para elementos de aplicativo que podem ser revisitados posteriormente na sessão do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c5446-111">An application can keep copies of [**Ink**](inkdisp-class.md) and [**DivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) objects for application elements that may be revisited later in the application session.</span></span> <span data-ttu-id="c5446-112">Isso elimina a necessidade de reanalisar o objeto de **tinta** se o usuário retornar ao elemento.</span><span class="sxs-lookup"><span data-stu-id="c5446-112">This eliminates the need to reanalyze the **Ink** object if the user returns to the element.</span></span> <span data-ttu-id="c5446-113">Essa abordagem compensa a memória para melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="c5446-113">This approach trades off memory for better performance.</span></span>

### <a name="data-reduction-heuristics"></a><span data-ttu-id="c5446-114">Heurística de redução de dados</span><span class="sxs-lookup"><span data-stu-id="c5446-114">Data Reduction Heuristics</span></span>

<span data-ttu-id="c5446-115">Você pode registrar os resultados da análise como dados do aplicativo e implementar a heurística para determinar quando reanalisar um conjunto de traços.</span><span class="sxs-lookup"><span data-stu-id="c5446-115">You may be able to record the analysis results as application data, and implement heuristics to determine when to reanalyze a set of strokes.</span></span> <span data-ttu-id="c5446-116">Essa prática reduziria a necessidade de analisar novamente toda a tinta no aplicativo entre as sessões do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c5446-116">This practice would reduce the need to reanalyze all the ink in the application between application sessions.</span></span> <span data-ttu-id="c5446-117">No entanto, deve-se ter cuidado para preservar os limites de elementos estruturais ou para reanalisar todos os traços dos elementos afetados.</span><span class="sxs-lookup"><span data-stu-id="c5446-117">However, care must be taken to preserve structural element boundaries or to reanalyze all the strokes for affected elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c5446-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c5446-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5446-119">**Classe InkDivider**</span><span class="sxs-lookup"><span data-stu-id="c5446-119">**InkDivider Class**</span></span>](inkdivider-class.md)
</dt> <dt>

<span data-ttu-id="c5446-120">[Classe Microsoft. Ink. divisor](/previous-versions/ms583616(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="c5446-120">[Microsoft.Ink.Divider Class](/previous-versions/ms583616(v=vs.100))</span></span>
</dt> </dl>

 

 
