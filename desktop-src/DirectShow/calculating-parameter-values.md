---
description: Calculando valores de parâmetro
ms.assetid: cc3c26ed-a007-4350-99be-0ebd94953689
title: Calculando valores de parâmetro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89dac0767d7d19bc4331e1a9ee032ec5b3eaae2e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105748237"
---
# <a name="calculating-parameter-values"></a><span data-ttu-id="3db56-103">Calculando valores de parâmetro</span><span class="sxs-lookup"><span data-stu-id="3db56-103">Calculating Parameter Values</span></span>

<span data-ttu-id="3db56-104">Potencialmente, um buffer de entrada poderia ser muito grande.</span><span class="sxs-lookup"><span data-stu-id="3db56-104">Potentially, an input buffer could be very large.</span></span> <span data-ttu-id="3db56-105">O ideal é que, quando o DMO processa o buffer, os parâmetros sigam exatamente suas curvas em todo o lote de dados.</span><span class="sxs-lookup"><span data-stu-id="3db56-105">Ideally, when the DMO processes the buffer, the parameters will exactly follow their curves throughout the entire batch of data.</span></span> <span data-ttu-id="3db56-106">No entanto, um DMO tem algumas reserva em como calcula esses valores.</span><span class="sxs-lookup"><span data-stu-id="3db56-106">However, a DMO has some leeway in how it calculates those values.</span></span>

-   <span data-ttu-id="3db56-107">A abordagem mais precisa é calcular o valor exato de cada unidade atômica de dados; por exemplo, cada amostra de áudio.</span><span class="sxs-lookup"><span data-stu-id="3db56-107">The most accurate approach is to calculate the exact value for every atomic unit of data; for example, each audio sample.</span></span> <span data-ttu-id="3db56-108">Essa abordagem é a mais cara em termos computacionais.</span><span class="sxs-lookup"><span data-stu-id="3db56-108">This approach is the most computationally expensive.</span></span>
-   <span data-ttu-id="3db56-109">Outra abordagem é dividir os dados em unidades menores de algum tamanho fixo, como exemplos de 100.</span><span class="sxs-lookup"><span data-stu-id="3db56-109">Another approach is to slice the data into smaller units of some fixed size, such as 100 samples.</span></span> <span data-ttu-id="3db56-110">Essa abordagem cria um efeito de "etapa de escada".</span><span class="sxs-lookup"><span data-stu-id="3db56-110">This approach creates a "stair-stepping" effect.</span></span> <span data-ttu-id="3db56-111">Para alguns parâmetros, isso pode ser aceitável.</span><span class="sxs-lookup"><span data-stu-id="3db56-111">For some parameters, that might be acceptable.</span></span> <span data-ttu-id="3db56-112">Em efeitos de áudio, ele pode criar artefatos audíveis.</span><span class="sxs-lookup"><span data-stu-id="3db56-112">In audio effects, it might create audible artifacts.</span></span>
-   <span data-ttu-id="3db56-113">Um comprometimento é usar a técnica anterior, mas em cada lote, executar uma interpolação linear do valor do parâmetro para cada amostra.</span><span class="sxs-lookup"><span data-stu-id="3db56-113">A compromise is to use the previous technique, but within each batch, perform a linear interpolation of the parameter value for each sample.</span></span>

<span data-ttu-id="3db56-114">Esses problemas são especialmente importantes para o processamento de áudio.</span><span class="sxs-lookup"><span data-stu-id="3db56-114">These issues are especially important for audio processing.</span></span> <span data-ttu-id="3db56-115">Um segundo de áudio pode conter 48.000 amostras de áudio por canal, que são muitos cálculos a serem executados, mas o Ear é sensível a artefatos como alias.</span><span class="sxs-lookup"><span data-stu-id="3db56-115">One second of audio might contain 48,000 audio samples per channel, which is a lot of calculations to perform, yet the ear is sensitive to artifacts such as aliasing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3db56-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3db56-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3db56-117">Parâmetros de mídia</span><span class="sxs-lookup"><span data-stu-id="3db56-117">Media Parameters</span></span>](media-parameters.md)
</dt> </dl>

 

 



