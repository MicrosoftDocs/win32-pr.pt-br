---
title: Conversão de espaço de cor
description: Conversão de espaço de cor
ms.assetid: f5f1ec99-b3b9-4420-bf64-3872d9bbe650
keywords:
- SDK do Windows Media Format, conversão de espaço em cores
- Formato de sistema avançado (ASF), conversão de espaço de cor
- ASF (formato de sistemas avançados), conversão de espaço de cor
- conversão de espaço de cor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cbc284995cbc72aee148e12977dad9f4476b29c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159803"
---
# <a name="color-space-conversion"></a><span data-ttu-id="9d60a-107">Conversão de espaço de cor</span><span class="sxs-lookup"><span data-stu-id="9d60a-107">Color Space Conversion</span></span>

<span data-ttu-id="9d60a-108">Geralmente, há uma diferença entre a intensidade da cor do formato de vídeo compactado no perfil e o formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="9d60a-108">There is often a difference between the color depth of the compressed video format in the profile and the input format.</span></span> <span data-ttu-id="9d60a-109">Quando isso acontece, o vídeo de origem deve ser convertido para estar de acordo com o espaço de cores do destino.</span><span class="sxs-lookup"><span data-stu-id="9d60a-109">When this happens, the source video must be converted to conform to the color space of the destination.</span></span> <span data-ttu-id="9d60a-110">O gravador manipula esse processo, comunicando-se com um conversor de espaço de cor interno.</span><span class="sxs-lookup"><span data-stu-id="9d60a-110">The writer handles this process, communicating with an internal color-space converter.</span></span>

<span data-ttu-id="9d60a-111">O leitor também se comunica com o conversor de espaço de cor para reconciliar qualquer diferença entre o formato compactado e o formato de saída.</span><span class="sxs-lookup"><span data-stu-id="9d60a-111">The reader also communicates with the color-space converter to reconcile any difference between the compressed format and the output format.</span></span>

<span data-ttu-id="9d60a-112">Assim como todas as transformações executadas nos dados, a conversão entre as profundidades de cor pode reduzir a qualidade da saída.</span><span class="sxs-lookup"><span data-stu-id="9d60a-112">As with all transforms performed on data, converting between color depths can reduce the quality of the output.</span></span> <span data-ttu-id="9d60a-113">Quando possível, você deve usar formatos de entrada e saída com a mesma intensidade de cor que o formato compactado.</span><span class="sxs-lookup"><span data-stu-id="9d60a-113">When possible, you should use input and output formats with the same color depth as the compressed format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d60a-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9d60a-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d60a-115">**Recursos de gravação de arquivo**</span><span class="sxs-lookup"><span data-stu-id="9d60a-115">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="9d60a-116">**Trabalhando com entradas**</span><span class="sxs-lookup"><span data-stu-id="9d60a-116">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> <dt>

[<span data-ttu-id="9d60a-117">**Trabalhando com saídas**</span><span class="sxs-lookup"><span data-stu-id="9d60a-117">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




