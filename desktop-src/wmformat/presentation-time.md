---
title: Tempo da apresentação
description: Tempo da apresentação
ms.assetid: 856e1783-85b4-4195-970f-3d7b5612672b
keywords:
- SDK do Windows Media Format, tempos de apresentação
- ASF (Advanced Systems Format), tempos de apresentação
- ASF (formato de sistemas avançados), tempos de apresentação
- tempos de apresentação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bc88dbba93d1fc68905a4bfea92328a4ef600eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292616"
---
# <a name="presentation-time"></a><span data-ttu-id="49a8d-107">Tempo da apresentação</span><span class="sxs-lookup"><span data-stu-id="49a8d-107">Presentation Time</span></span>

<span data-ttu-id="49a8d-108">Um tempo de apresentação é uma medida de tempo desde a primeira amostra do primeiro fluxo em um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="49a8d-108">A presentation time is a measurement of time from the first sample of the first stream in an ASF file.</span></span> <span data-ttu-id="49a8d-109">Essa medida, bem como a maioria das outras medições de tempo usada pelos objetos desse SDK, está em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="49a8d-109">This measurement, as well as most other measurements of time used by the objects of this SDK, is in 100-nanosecond units.</span></span> <span data-ttu-id="49a8d-110">Os tempos de apresentação são importantes porque permitem que os vários fluxos em um arquivo sejam sincronizados.</span><span class="sxs-lookup"><span data-stu-id="49a8d-110">Presentation times are important because they enable the various streams in a file to be synchronized.</span></span> <span data-ttu-id="49a8d-111">Você deve fornecer um tempo de apresentação para cada exemplo de entrada que passa para o gravador.</span><span class="sxs-lookup"><span data-stu-id="49a8d-111">You must supply a presentation time for each input sample you pass to the writer.</span></span> <span data-ttu-id="49a8d-112">Cada objeto de dados na seção de dados de um arquivo ASF tem um tempo de apresentação associado a ele.</span><span class="sxs-lookup"><span data-stu-id="49a8d-112">Every data object in the data section of an ASF file has a presentation time associated with it.</span></span> <span data-ttu-id="49a8d-113">Cada exemplo de saída recuperada pelo leitor também tem um tempo de apresentação.</span><span class="sxs-lookup"><span data-stu-id="49a8d-113">Every output sample retrieved by the reader also has a presentation time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49a8d-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="49a8d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49a8d-115">**Conceitos**</span><span class="sxs-lookup"><span data-stu-id="49a8d-115">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="49a8d-116">**Entradas, fluxos e saídas**</span><span class="sxs-lookup"><span data-stu-id="49a8d-116">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="49a8d-117">**Amostras de mídia**</span><span class="sxs-lookup"><span data-stu-id="49a8d-117">**Media Samples**</span></span>](media-samples.md)
</dt> </dl>

 

 




