---
title: Números (multimídia do Windows)
description: Números
ms.assetid: d416c4c2-a3e1-45a2-9ae1-82050a5e471b
keywords:
- mixers de áudio, controles
- mixers de áudio, números
- mixers, controles
- mixers, números
- controles de número
- Estrutura de MIXERCONTROLDETAILS_SIGNED
- Estrutura de MIXERCONTROLDETAILS_UNSIGNED
- controle decibéi
- controle de porcentagem
- controle assinado
- controle não assinado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f02c4ffd40f1058fae51af3798135840394be918
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104085059"
---
# <a name="numbers-windows-multimedia"></a><span data-ttu-id="c9fc0-114">Números (multimídia do Windows)</span><span class="sxs-lookup"><span data-stu-id="c9fc0-114">Numbers (Windows Multimedia)</span></span>

<span data-ttu-id="c9fc0-115">O número de controles permite que o usuário insira dados numéricos associados a uma linha.</span><span class="sxs-lookup"><span data-stu-id="c9fc0-115">The number controls allow the user to enter numerical data associated with a line.</span></span> <span data-ttu-id="c9fc0-116">Os dados numéricos são expressos como inteiros assinados, inteiros não assinados ou valores de número inteiro de decibéis.</span><span class="sxs-lookup"><span data-stu-id="c9fc0-116">The numerical data is expressed as signed integers, unsigned integers, or integer decibel values.</span></span> <span data-ttu-id="c9fc0-117">Esses controles usam as estruturas [**\_ não**](/previous-versions//dd757298(v=vs.85)) [**\_ assinadas MIXERCONTROLDETAILS**](/previous-versions//dd757297(v=vs.85)) e MIXERCONTROLDETAILS para recuperar e definir propriedades de controle.</span><span class="sxs-lookup"><span data-stu-id="c9fc0-117">These controls use the [**MIXERCONTROLDETAILS\_SIGNED**](/previous-versions//dd757297(v=vs.85)) and [**MIXERCONTROLDETAILS\_UNSIGNED**](/previous-versions//dd757298(v=vs.85)) structures to retrieve and set control properties.</span></span> <span data-ttu-id="c9fc0-118">A tabela a seguir descreve os tipos de controles de número.</span><span class="sxs-lookup"><span data-stu-id="c9fc0-118">The following table describes the types of number controls.</span></span>



| <span data-ttu-id="c9fc0-119">Control</span><span class="sxs-lookup"><span data-stu-id="c9fc0-119">Control</span></span>  | <span data-ttu-id="c9fc0-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="c9fc0-120">Description</span></span>                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9fc0-121">Com sinal</span><span class="sxs-lookup"><span data-stu-id="c9fc0-121">Signed</span></span>   | <span data-ttu-id="c9fc0-122">Permite valores inteiros inseridos no intervalo de – 231 a (231 – 1).</span><span class="sxs-lookup"><span data-stu-id="c9fc0-122">Allows integer values entered in the range of – 231 through (231 –1).</span></span>                                                               |
| <span data-ttu-id="c9fc0-123">Não assinado</span><span class="sxs-lookup"><span data-stu-id="c9fc0-123">Unsigned</span></span> | <span data-ttu-id="c9fc0-124">Permite valores inteiros inseridos no intervalo de 0 a (232 – 1).</span><span class="sxs-lookup"><span data-stu-id="c9fc0-124">Allows integer values entered in the range of 0 through (232 –1).</span></span>                                                                   |
| <span data-ttu-id="c9fc0-125">Decibéi</span><span class="sxs-lookup"><span data-stu-id="c9fc0-125">Decibel</span></span>  | <span data-ttu-id="c9fc0-126">Permite que valores de um inteiro decibéi sejam inseridos, em décimos de decibéis.</span><span class="sxs-lookup"><span data-stu-id="c9fc0-126">Allows integer decibel values to be entered, in tenths of decibels.</span></span> <span data-ttu-id="c9fc0-127">O intervalo de valores para esse controle é de – 32.768 a 32.767.</span><span class="sxs-lookup"><span data-stu-id="c9fc0-127">The range of values for this control is –32,768 through 32,767.</span></span> |
| <span data-ttu-id="c9fc0-128">Porcentagem</span><span class="sxs-lookup"><span data-stu-id="c9fc0-128">Percent</span></span>  | <span data-ttu-id="c9fc0-129">Permite que os valores sejam inseridos como porcentagens.</span><span class="sxs-lookup"><span data-stu-id="c9fc0-129">Allows values to be entered as percentages.</span></span>                                                                                         |



 

 

 
