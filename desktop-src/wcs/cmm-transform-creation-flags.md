---
title: Sinalizadores de criação de transformação do CMM
description: CMMs use sinalizadores de criação de transformação como dicas sobre como criar uma transformação de cor. Cabe ao CMM determinar a melhor maneira de usar esses sinalizadores.
ms.assetid: f3942929-272c-4f08-98ac-a4d14d2f6ac4
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 852ef5c080c361bfffb6915d808787d46e63ba5c
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/02/2021
ms.locfileid: "105764344"
---
# <a name="cmm-transform-creation-flags"></a><span data-ttu-id="77273-104">Sinalizadores de criação de transformação do CMM</span><span class="sxs-lookup"><span data-stu-id="77273-104">CMM Transform Creation Flags</span></span>

<span data-ttu-id="77273-105">CMMs use sinalizadores de criação de transformação como dicas sobre como criar uma transformação de cor.</span><span class="sxs-lookup"><span data-stu-id="77273-105">CMMs use transform creation flags as hints for how to create a color transform.</span></span> <span data-ttu-id="77273-106">Cabe ao CMM determinar a melhor maneira de usar esses sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="77273-106">It is up to the CMM to determine how best to use these flags.</span></span>

<span data-ttu-id="77273-107">Todas as funções que usam esses sinalizadores passam ou recebem valores de sinalizador por meio de um parâmetro chamado *dwFlags*.</span><span class="sxs-lookup"><span data-stu-id="77273-107">All of the functions that use these flags pass or receive flag values through a parameter called *dwFlags*.</span></span> <span data-ttu-id="77273-108">A **palavra** de ordem superior do *dwFlags* deve ser definida como um valor da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="77273-108">The high-order **WORD** of *dwFlags* should be set to a value from the following table.</span></span>



| <span data-ttu-id="77273-109">Constante</span><span class="sxs-lookup"><span data-stu-id="77273-109">Constant</span></span>                    | <span data-ttu-id="77273-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="77273-110">Description</span></span>                                                                                                                                  |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77273-111">Habilitar \_ verificação de gama \_</span><span class="sxs-lookup"><span data-stu-id="77273-111">ENABLE\_GAMUT\_CHECKING</span></span>     | <span data-ttu-id="77273-112">Use essa transformação para verificação de gamut.</span><span class="sxs-lookup"><span data-stu-id="77273-112">Use this transform for gamut checking.</span></span>                                                                                                       |
| <span data-ttu-id="77273-113">USAR \_ \_ colorimétrico relativo</span><span class="sxs-lookup"><span data-stu-id="77273-113">USE\_RELATIVE\_COLORIMETRIC</span></span> | <span data-ttu-id="77273-114">Não preserve o ponto branco.</span><span class="sxs-lookup"><span data-stu-id="77273-114">Do not preserve the white point.</span></span> <span data-ttu-id="77273-115">Se a gama de saída não oferecer suporte a uma determinada cor, use a cor mais próxima com suporte.</span><span class="sxs-lookup"><span data-stu-id="77273-115">If the output gamut does not support a given color, use the nearest supported color.</span></span> <span data-ttu-id="77273-116">Consulte tentativas de renderização.</span><span class="sxs-lookup"><span data-stu-id="77273-116">See Rendering Intents.</span></span> |
| <span data-ttu-id="77273-117">\_conversão rápida</span><span class="sxs-lookup"><span data-stu-id="77273-117">FAST\_TRANSLATE</span></span>             | <span data-ttu-id="77273-118">Pesquisar apenas a cor.</span><span class="sxs-lookup"><span data-stu-id="77273-118">Look up color only.</span></span> <span data-ttu-id="77273-119">Não interpolar a cor.</span><span class="sxs-lookup"><span data-stu-id="77273-119">Do not interpolate the color.</span></span>                                                                                            |
| <span data-ttu-id="77273-120">PRESERVEBLACK</span><span class="sxs-lookup"><span data-stu-id="77273-120">PRESERVEBLACK</span></span>               | <span data-ttu-id="77273-121">Insere o GMMP de geração de preto apropriado como o último GMMP na sequência de transformação</span><span class="sxs-lookup"><span data-stu-id="77273-121">Inserts the appropriate black generation GMMP as the last GMMP in the transform sequence</span></span>                                                     |
| <span data-ttu-id="77273-122">WCS \_ sempre</span><span class="sxs-lookup"><span data-stu-id="77273-122">WCS\_ALWAYS</span></span>                 | <span data-ttu-id="77273-123">Use o caminho do código WCS até mesmo para transformações ICC.</span><span class="sxs-lookup"><span data-stu-id="77273-123">Use the WCS code path even for ICC transforms.</span></span>                                                                                               |
| <span data-ttu-id="77273-124">transformação SEQUENCIAl \_</span><span class="sxs-lookup"><span data-stu-id="77273-124">SEQUENTIAL\_TRANSFORM</span></span>       | <span data-ttu-id="77273-125">Sinalizador de criação de transformação para criar uma transformação de cor sequencial (não otimizada).</span><span class="sxs-lookup"><span data-stu-id="77273-125">Transform creation flag for creating a sequential (non-optimized) color transform.</span></span>                                                           |



 

<span data-ttu-id="77273-126">A **palavra** de ordem inferior pode ter um dos valores constantes a seguir.</span><span class="sxs-lookup"><span data-stu-id="77273-126">The low-order **WORD** can have one of the following constant values.</span></span>



| <span data-ttu-id="77273-127">Constante</span><span class="sxs-lookup"><span data-stu-id="77273-127">Constant</span></span>     | <span data-ttu-id="77273-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="77273-128">Description</span></span>                                                                                        |
|--------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77273-129">modo de prova \_</span><span class="sxs-lookup"><span data-stu-id="77273-129">PROOF\_MODE</span></span>  | <span data-ttu-id="77273-130">A transformação será usada para visualizar a imagem.</span><span class="sxs-lookup"><span data-stu-id="77273-130">Transform will be used to preview the image.</span></span> <span data-ttu-id="77273-131">Baixa qualidade da imagem.</span><span class="sxs-lookup"><span data-stu-id="77273-131">Low image quality.</span></span>                                    |
| <span data-ttu-id="77273-132">\_modo normal</span><span class="sxs-lookup"><span data-stu-id="77273-132">NORMAL\_MODE</span></span> | <span data-ttu-id="77273-133">A transformação será usada para exibição de imagem normal.</span><span class="sxs-lookup"><span data-stu-id="77273-133">Transform will be used for normal image display.</span></span> <span data-ttu-id="77273-134">Qualidade média da imagem.</span><span class="sxs-lookup"><span data-stu-id="77273-134">Average image quality.</span></span>                            |
| <span data-ttu-id="77273-135">\_modo melhor</span><span class="sxs-lookup"><span data-stu-id="77273-135">BEST\_MODE</span></span>   | <span data-ttu-id="77273-136">A transformação será usada para a exibição da imagem de qualidade mais alta possível no dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="77273-136">Transform will be used for the display of the highest-quality image possible on the target device.</span></span> |



 

<span data-ttu-id="77273-137">Movendo do modo de prova \_ para o melhor \_ modo, a qualidade da saída geralmente melhora e transforma as rejeições de velocidade.</span><span class="sxs-lookup"><span data-stu-id="77273-137">Moving from PROOF\_MODE to BEST\_MODE, output quality generally improves and transform speed declines.</span></span>

## <a name="related-topics"></a><span data-ttu-id="77273-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="77273-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77273-139">Conceitos básicos de gerenciamento de cores</span><span class="sxs-lookup"><span data-stu-id="77273-139">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="77273-140">Constantes de ICM</span><span class="sxs-lookup"><span data-stu-id="77273-140">ICM Constants</span></span>](wcs-constants.md)
</dt> </dl>

 

 




