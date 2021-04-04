---
title: Esmaecimentos
description: Esmaecimentos
ms.assetid: 2ca6be9f-9825-44d9-99c1-abcf6f0b42f7
keywords:
- mixers de áudio, controles
- mixers de áudio, esmaecimentos
- mixers, controles
- mixers, esmaecimentos
- esmaecimentos
- Estrutura de MIXERCONTROLDETAILS_UNSIGNED
- controle de esmaecimento de volume
- controle de esmaecimento de volume baixo
- controle de esmaecimento de volume de agudos
- controle de equalizador gráfico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2b560b61a694089b947b0cfda7a54b486f1e3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917200"
---
# <a name="faders"></a><span data-ttu-id="6caf0-113">Esmaecimentos</span><span class="sxs-lookup"><span data-stu-id="6caf0-113">Faders</span></span>

<span data-ttu-id="6caf0-114">Os controles Fader geralmente são controles verticais que podem ser ajustados ou reduzidos.</span><span class="sxs-lookup"><span data-stu-id="6caf0-114">The fader controls are typically vertical controls that can be adjusted up or down.</span></span> <span data-ttu-id="6caf0-115">Esses controles têm uma escala linear e usam a estrutura não [**\_ assinada MIXERCONTROLDETAILS**](/previous-versions//dd757298(v=vs.85)) para recuperar e definir detalhes de controle.</span><span class="sxs-lookup"><span data-stu-id="6caf0-115">These controls have a linear scale and use the [**MIXERCONTROLDETAILS\_UNSIGNED**](/previous-versions//dd757298(v=vs.85)) structure to retrieve and set control details.</span></span> <span data-ttu-id="6caf0-116">A tabela a seguir descreve os tipos de esmaecimentos.</span><span class="sxs-lookup"><span data-stu-id="6caf0-116">The following table describes the types of faders.</span></span>



| <span data-ttu-id="6caf0-117">Control</span><span class="sxs-lookup"><span data-stu-id="6caf0-117">Control</span></span>   | <span data-ttu-id="6caf0-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="6caf0-118">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6caf0-119">Fader</span><span class="sxs-lookup"><span data-stu-id="6caf0-119">Fader</span></span>     | <span data-ttu-id="6caf0-120">Controle de esmaecimento geral.</span><span class="sxs-lookup"><span data-stu-id="6caf0-120">General fade control.</span></span> <span data-ttu-id="6caf0-121">O intervalo de valores aceitáveis é de 0 a 65.535.</span><span class="sxs-lookup"><span data-stu-id="6caf0-121">The range of acceptable values is 0 through 65,535.</span></span>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="6caf0-122">Volume</span><span class="sxs-lookup"><span data-stu-id="6caf0-122">Volume</span></span>    | <span data-ttu-id="6caf0-123">Controle de esmaecimento de volume geral.</span><span class="sxs-lookup"><span data-stu-id="6caf0-123">General volume fade control.</span></span> <span data-ttu-id="6caf0-124">O intervalo de valores aceitáveis é de 0 a 65.535.</span><span class="sxs-lookup"><span data-stu-id="6caf0-124">The range of acceptable values is 0 through 65,535.</span></span> <span data-ttu-id="6caf0-125">Para obter informações sobre como alterar esse intervalo, consulte a documentação do seu dispositivo MIXER.</span><span class="sxs-lookup"><span data-stu-id="6caf0-125">For information about changing this range, see the documentation for your mixer device.</span></span>                                                                                                                                                                                                                                        |
| <span data-ttu-id="6caf0-126">Graves</span><span class="sxs-lookup"><span data-stu-id="6caf0-126">Bass</span></span>      | <span data-ttu-id="6caf0-127">Controle de esmaecimento de volume baixo.</span><span class="sxs-lookup"><span data-stu-id="6caf0-127">Bass volume fade control.</span></span> <span data-ttu-id="6caf0-128">O intervalo de valores aceitáveis é de 0 a 65.535.</span><span class="sxs-lookup"><span data-stu-id="6caf0-128">The range of acceptable values is 0 through 65,535.</span></span> <span data-ttu-id="6caf0-129">Os limites da banda de frequência de baixo são específicos de hardware.</span><span class="sxs-lookup"><span data-stu-id="6caf0-129">The limits of the bass frequency band are hardware specific.</span></span> <span data-ttu-id="6caf0-130">Para obter informações sobre limites de banda, consulte a documentação do seu dispositivo de mixer.</span><span class="sxs-lookup"><span data-stu-id="6caf0-130">For information about band limits, see the documentation for your mixer device.</span></span>                                                                                                                                                                                      |
| <span data-ttu-id="6caf0-131">Agudo</span><span class="sxs-lookup"><span data-stu-id="6caf0-131">Treble</span></span>    | <span data-ttu-id="6caf0-132">Controle de esmaecimento de volume de agudos.</span><span class="sxs-lookup"><span data-stu-id="6caf0-132">Treble volume fade control.</span></span> <span data-ttu-id="6caf0-133">O intervalo de valores aceitáveis é de 0 a 65.535.</span><span class="sxs-lookup"><span data-stu-id="6caf0-133">The range of acceptable values is 0 through 65,535.</span></span> <span data-ttu-id="6caf0-134">Os limites da banda de frequência de agudo são específicos de hardware.</span><span class="sxs-lookup"><span data-stu-id="6caf0-134">The limits of the treble frequency band are hardware specific.</span></span> <span data-ttu-id="6caf0-135">Para obter informações sobre os limites de banda, consulte a documentação do seu dispositivo de mixer.</span><span class="sxs-lookup"><span data-stu-id="6caf0-135">For information about the band limits, see the documentation for your mixer device.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="6caf0-136">Equalizer</span><span class="sxs-lookup"><span data-stu-id="6caf0-136">Equalizer</span></span> | <span data-ttu-id="6caf0-137">Controle de equalizador gráfico.</span><span class="sxs-lookup"><span data-stu-id="6caf0-137">Graphic equalizer control.</span></span> <span data-ttu-id="6caf0-138">O intervalo de valores aceitáveis para uma banda do equalizador é de 0 a 65.535.</span><span class="sxs-lookup"><span data-stu-id="6caf0-138">The range of acceptable values for one band of the equalizer is 0 through 65,535.</span></span> <span data-ttu-id="6caf0-139">O número de bandas do equalizador e seus limites são específicos de hardware.</span><span class="sxs-lookup"><span data-stu-id="6caf0-139">The number of equalizer bands and their limits are hardware specific.</span></span> <span data-ttu-id="6caf0-140">Para obter informações sobre o equalizador, consulte a documentação do seu dispositivo de mixer.</span><span class="sxs-lookup"><span data-stu-id="6caf0-140">For information about the equalizer, see the documentation for your mixer device.</span></span> <span data-ttu-id="6caf0-141">Você pode usar a estrutura [**MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85)) para recuperar rótulos de texto para o equalizador.</span><span class="sxs-lookup"><span data-stu-id="6caf0-141">You can use the [**MIXERCONTROLDETAILS\_LISTTEXT**](/previous-versions//dd757296(v=vs.85)) structure to retrieve text labels for the equalizer.</span></span> |



 

 

 