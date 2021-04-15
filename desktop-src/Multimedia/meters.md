---
title: Medidores
description: Medidores
ms.assetid: 11a98d2a-7cdd-4249-bba9-7edc51d7f8b0
keywords:
- mixers de áudio, controles
- mixers de áudio, medidores
- mixers, controles
- mixers, medidores
- controles de medidor
- Estrutura de MIXERCONTROLDETAILS_BOOLEAN
- Estrutura de MIXERCONTROLDETAILS_SIGNED
- Estrutura de MIXERCONTROLDETAILS_UNSIGNED
- Controle booliano
- controle de pico
- controle assinado
- controle não assinado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36f1bebfca22b963e5c1eb6fede3f2786b35199
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104454064"
---
# <a name="meters"></a><span data-ttu-id="a0d67-115">Medidores</span><span class="sxs-lookup"><span data-stu-id="a0d67-115">Meters</span></span>

<span data-ttu-id="a0d67-116">Os controles de medição medem os dados que passam por uma linha de áudio.</span><span class="sxs-lookup"><span data-stu-id="a0d67-116">The meter controls measure data passing through an audio line.</span></span> <span data-ttu-id="a0d67-117">Esses controles usam o [**MIXERCONTROLDETAILS \_ booliano**](/previous-versions//dd757295(v=vs.85)), o [**MIXERCONTROLDETAILS \_ assinado**](/previous-versions//dd757297(v=vs.85))e o [**MIXERCONTROLDETAILS estruturas \_ não assinadas**](/previous-versions//dd757298(v=vs.85)) para recuperar e definir propriedades de controle.</span><span class="sxs-lookup"><span data-stu-id="a0d67-117">These controls use the [**MIXERCONTROLDETAILS\_BOOLEAN**](/previous-versions//dd757295(v=vs.85)), [**MIXERCONTROLDETAILS\_SIGNED**](/previous-versions//dd757297(v=vs.85)), and [**MIXERCONTROLDETAILS\_UNSIGNED**](/previous-versions//dd757298(v=vs.85)) structures to retrieve and set control properties.</span></span> <span data-ttu-id="a0d67-118">A tabela a seguir descreve os tipos de medidores.</span><span class="sxs-lookup"><span data-stu-id="a0d67-118">The following table describes the types of meters.</span></span>



| <span data-ttu-id="a0d67-119">Control</span><span class="sxs-lookup"><span data-stu-id="a0d67-119">Control</span></span>  | <span data-ttu-id="a0d67-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="a0d67-120">Description</span></span>                                                                                                                                            |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0d67-121">Boolean</span><span class="sxs-lookup"><span data-stu-id="a0d67-121">Boolean</span></span>  | <span data-ttu-id="a0d67-122">Mede se um valor inteiro é FALSE/desligado (zero) ou TRUE/ON (diferente de zero).</span><span class="sxs-lookup"><span data-stu-id="a0d67-122">Measures whether an integer value is FALSE/OFF (zero) or TRUE/ON (nonzero).</span></span>                                                                            |
| <span data-ttu-id="a0d67-123">Peak</span><span class="sxs-lookup"><span data-stu-id="a0d67-123">Peak</span></span>     | <span data-ttu-id="a0d67-124">Mede a deflexão de 0 nas direções positiva e negativa.</span><span class="sxs-lookup"><span data-stu-id="a0d67-124">Measures the deflection from 0 in both the positive and negative directions.</span></span> <span data-ttu-id="a0d67-125">O intervalo de valores inteiros para o medidor de pico é de – 32.768 a 32.767.</span><span class="sxs-lookup"><span data-stu-id="a0d67-125">The range of integer values for the peak meter is –32,768 through 32,767.</span></span> |
| <span data-ttu-id="a0d67-126">Com sinal</span><span class="sxs-lookup"><span data-stu-id="a0d67-126">Signed</span></span>   | <span data-ttu-id="a0d67-127">Mede valores inteiros no intervalo de – 231 a (231 – 1).</span><span class="sxs-lookup"><span data-stu-id="a0d67-127">Measures integer values in the range of –231 through (231 – 1).</span></span> <span data-ttu-id="a0d67-128">O driver do mixer define os limites desse medidor.</span><span class="sxs-lookup"><span data-stu-id="a0d67-128">The mixer driver defines the limits of this meter.</span></span>                                     |
| <span data-ttu-id="a0d67-129">Não assinado</span><span class="sxs-lookup"><span data-stu-id="a0d67-129">Unsigned</span></span> | <span data-ttu-id="a0d67-130">Mede valores inteiros no intervalo de 0 a (232 – 1).</span><span class="sxs-lookup"><span data-stu-id="a0d67-130">Measures integer values in the range of 0 through (232 – 1).</span></span> <span data-ttu-id="a0d67-131">O driver do mixer define os limites desse medidor.</span><span class="sxs-lookup"><span data-stu-id="a0d67-131">The mixer driver defines the limits of this meter.</span></span>                                        |



 

 

 